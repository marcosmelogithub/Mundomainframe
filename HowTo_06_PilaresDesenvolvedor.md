# 06. Pilares de um desenvolvedor Mainframe
---

| Pilar | Infra e S.O. | Linguagem | Dados e Arquivos | Processamento | Apoio |
| :-- | :--: | :--: | :--: | :--: | :--: |
| z/OS | x |  |  |  |  |
| TSO/ISPF | x |  |  |  |  |
| COBOL |  | x |  |  |  |
| JCL |  | x  |  |  |  |
| Assembler (HLASM) |  | x |  |  |  |
| VSAM |  |  | x |  |  |
| DB2 |  |  | x |  |  |
| Datasets |  |  | x |  |  |
| CICS |  |  |  | x |  |
| Batch |  |  |  | x |  |
| Endevor ou Changeman |  |  |  |  | x |
| IBM Debug Tool ou Intertest |  |  |  |  | x |
| IDCAMS |  |  |  | | x |
| IEBGENER |  |  |  | | x |
| SyncSort DFSORT |  |  |  |  | x |
| Zowe |  |  |  |  | x |

---
#### Dicionário
---

>**z/OS:** O sistema operacional dominante. É preciso entender conceitos de endereçamento, subsistemas e como o hardware se comunica com o software.

>**TSO/ISPF:** A interface de "linha de comando" e menus. É por onde o desenvolvedor navega em arquivos, edita código e submete tarefas.

O TSO (Time Sharing Option) é, em termos simples, o ambiente que permite que múltiplos usuários acessem e interajam com o sistema operacional z/OS simultaneamente de forma interativa.

Se fizermos uma analogia com sistemas modernos, o TSO funciona como o Terminal do Linux ou o Prompt de Comando do Windows, mas otimizado para a arquitetura de mainframe.
**Principais caracterísitcas**
|Interatividade|Comandos|Hospedeiro|Sessão|
|:--|:--|:--|:--|
|Antes do TSO, o mainframe era puramente batch (você mandava um cartão e esperava o resultado). O TSO permitiu que o desenvolvedor digitasse comandos e recebesse respostas imediatas.|Através do "Ready mode", você executa comandos para gerenciar arquivos (datasets), submeter jobs ou verificar o status de tarefas.|Quase todo desenvolvedor usa o TSO apenas como a "porta de entrada" para carregar o ISPF (a interface de menus e painéis), mas o TSO continua rodando por trás de tudo.|Cada desenvolvedor possui sua própria sessão TSO, com limites de memória e recursos definidos pelo administrador do sistema.|

**Comandos Principais**

**1. Manipulação de Datasets (Arquivos)**

|Comando|Definição|
|:--|:--|
|ALLOCATE (ou ALLOC)|Cria um novo dataset ou associa um arquivo existente a um nome lógico (ddname) para uso imediato|
|DELETE|Exclui um dataset do sistema|
|RENAME|Altera o nome de um dataset|
|LISTDS (List Dataset Attributes)|Exibe as características técnicas do arquivo (formato de registro, tamanho do bloco, volume, etc.)|
|LISTCAT (Lista Catalog)|Lista os arquivos que seguem um determinado padrão de nome (ex: LISTCAT LEVEL(USUARIO.PROJETO))|

**2. Gerenciamento de Jobs (Execuções)**

|Comando|Definição|
|:--|:--|
|SUBMIT (ou SUB)|Envia um arquivo JCL para a fila de execução do sistema (JES)|
|STATUS (ou ST)|Verifica se o seu job está na fila, em execução ou se já terminou|
OUTPUT|Permite visualizar o log e o resultado de um job diretamente na tela, sem precisar de um visualizador externo como o SDSF|
|CANCEL|Interrompe a execução de um job que foi submetido por você|

**3. Utilidades de Sessão**

|Comando|Definição|
|:--|:--|
|SEND|Envia uma mensagem curta para outro usuário que esteja logado no sistema (ex: SEND 'Cuidado com o CICS' USER(DBA01))|
|LISTBC (List Broadcast)|Exibe mensagens do sistema ou de outros usuários enviadas para você|
|HELP|O socorro imediato. Digite HELP seguido do comando para ver a sintaxe e os parâmetros disponíveis|
|LOGOFF|Encerra sua sessão TSO com segurança|

**Dica de Produtividade: Comandos TSO dentro do ISPF**
No dia a dia, você estará quase sempre dentro dos painéis do ISPF. Para executar qualquer comando TSO listado acima sem sair da tela onde você está, basta prefixá-lo com a letra TSO:
Exemplo: TSO LISTCAT LEVEL(MEU.NOME) na linha de comando de qualquer painel.

**DataSet:** O TSO se baseia em datasets e para entender melhor seguem abaixo os tipos de datasets
|Característica|Physical Sequential (PS)|Partitioned Dataset (PDS ou PDSE)|
|:--|:--|:--|
|**Definição**|Arquivo de dados simples e linear. Imagine-o como um documento de texto único ou uma fita de dados|Biblioteca ou uma pasta. Ele contém vários "arquivos menores" dentro de um único grande arquivo|
|**Estrutura**|Os registros são gravados um após o outro, do início ao fim|É dividido em Directory (um índice no início) e Members (os arquivos individuais)|
|**Uso Comum**|Grandes volumes de dados, arquivos de log, arquivos de entrada/saída de programas COBOL (movimentações bancárias, cadastros de clientes)|Armazenar código-fonte (COBOL), scripts JCL, bibliotecas de carga (Load Modules) e procedimentos (PROCs)|
|**Acesso**|Para ler o último registro, o sistema geralmente precisa percorrer os anteriores (ou saltar para uma posição específica se o tamanho for fixo)|O sistema olha o diretório, encontra o nome do member e vai direto para onde ele começa|
|**Componentes**|Apenas os dados|Diretório + Membros|
|**Como Referenciar**|USUARIO.DADOS.ARQUIVO|USUARIO.COBOL.LOAD(PROGRAMA1)|
|**Curiosidade**||- No **PDS "*clássico*"** quando você deleta ou altera um membro, o espaço antigo não é liberado automaticamente; ele vira um "buraco" (espaço morto). Por isso, desenvolvedores mainframe precisam executar periodicamente um utilitário chamado COMPRESS para reorganizar o arquivo.<br>- O **PDSE (versão moderna)** resolve isso gerenciando o espaço automaticamente.


>**COBOL:** A espinha dorsal das aplicações transacionais e batch.

>**JCL (Job Control Language):** Linguagem de script essencial para dizer ao sistema como executar um programa (alocação de arquivos, memória e logs).

>**Assembler (HLASM):** Para tarefas de baixo nível e performance extrema (menos comum no dia a dia, mas um diferencial enorme).

>**VSAM:** O método de acesso a arquivos indexados e sequenciais nativo.

>**DB2:** O banco de dados relacional padrão da plataforma. Exige conhecimento de SQL otimizado para alto volume.

>**Datasets:** Entender a diferença entre arquivos sequenciais (PS) e particionados (PDS/PDSE).

>**CICS:** O monitor transacional para telas "online" e APIs. É o que permite que milhares de usuários acessem o sistema simultaneamente.

>**Batch Processing:** O processamento em massa de dados, geralmente executado durante a noite (o famoso "fechamento").

>**Endevor ou Changeman:** Gerenciadores de Versão

> **IBM Debug Tool ou Intertest:** Depuradores (Debuggers)

>**IDCAMS, IEBGENER e ferramentas de SORT (SyncSort/DFSORT):** Utilitários de Sistema

>**Zowe:** permite interagir com o mainframe de uma forma moderna.
O Zowe é um projeto de código aberto (governado pela Open Mainframe Project) que funciona como uma ponte de modernização para o ecossistema z/OS.

Em termos simples: ele permite que você interaja com o mainframe utilizando ferramentas modernas que os desenvolvedores já amam (como o VS Code, terminais Linux/Mac ou navegadores web), em vez de ficar limitado exclusivamente à interface clássica de "tela verde" (3270).

**Pilares do Zowe**
| Zowe CLI | Zowe Desktop | API Mediation Layer |
| :-- | :-- | :-- |
|Interface de linha de comando que permite comandar o mainframe (submeter JCLs, baixar datasets, verificar logs) diretamente do terminal do seu computador. Isso possibilita incluir o mainframe em esteiras de CI/CD (DevOps). | Interface gráfica via navegador que simula uma área de trabalho moderna, facilitando a gestão de arquivos e sistemas sem precisar decorar comandos complexos do ISPF. | Gateway que organiza e expõe as funcionalidades do mainframe como APIs REST, permitindo que outras aplicações se conectem a ele de forma padronizada e segura.|