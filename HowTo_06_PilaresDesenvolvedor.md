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

- **z/OS:** O sistema operacional dominante. É preciso entender conceitos de endereçamento, subsistemas e como o hardware se comunica com o software.

- **TSO/ISPF:** A interface de "linha de comando" e menus. É por onde o desenvolvedor navega em arquivos, edita código e submete tarefas.

- **COBOL:** A espinha dorsal das aplicações transacionais e batch.

- **JCL (Job Control Language):** Linguagem de script essencial para dizer ao sistema como executar um programa (alocação de arquivos, memória e logs).

- **Assembler (HLASM):** Para tarefas de baixo nível e performance extrema (menos comum no dia a dia, mas um diferencial enorme).

- **VSAM:** O método de acesso a arquivos indexados e sequenciais nativo.

- **DB2:** O banco de dados relacional padrão da plataforma. Exige conhecimento de SQL otimizado para alto volume.

- **Datasets:** Entender a diferença entre arquivos sequenciais (PS) e particionados (PDS/PDSE).

- **CICS:** O monitor transacional para telas "online" e APIs. É o que permite que milhares de usuários acessem o sistema simultaneamente.

- **Batch Processing:** O processamento em massa de dados, geralmente executado durante a noite (o famoso "fechamento").

- **Endevor ou Changeman:** Gerenciadores de Versão

- **IBM Debug Tool ou Intertest:** Depuradores (Debuggers)

- **IDCAMS, IEBGENER e ferramentas de SORT (SyncSort/DFSORT):** Utilitários de Sistema

- **Zowe:** permite interagir com o mainframe de uma forma moderna.
>O Zowe é um projeto de código aberto (governado pela Open Mainframe Project) que funciona como uma ponte de modernização para o ecossistema z/OS.
>
>Em termos simples: ele permite que você interaja com o mainframe utilizando ferramentas modernas que os desenvolvedores já amam (como o VS Code, terminais Linux/Mac ou navegadores web), em vez de ficar limitado exclusivamente à interface clássica de "tela verde" (3270).
>
>**Pilares do Zowe**
>| Zowe CLI | Zowe Desktop | API Mediation Layer |
>| :-- | :-- | :-- |
>|Interface de linha de comando que permite comandar o mainframe (submeter JCLs, baixar datasets, verificar logs) diretamente do terminal do seu computador. Isso possibilita incluir o mainframe em esteiras de CI/CD (DevOps). | Interface gráfica via navegador que simula uma área de trabalho moderna, facilitando a gestão de arquivos e sistemas sem precisar decorar comandos complexos do ISPF. | Gateway que organiza e expõe as funcionalidades do mainframe como APIs REST, permitindo que outras aplicações se conectem a ele de forma padronizada e segura.|