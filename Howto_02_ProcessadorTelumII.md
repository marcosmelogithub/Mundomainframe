# 02. Processador Telum II
---
>O processador Telum II, que equipa o mainframe IBM z17  é o grande "músculo" por trás da agilidade e da segurança da instituição. Ele não é apenas uma CPU convencional; ele possui aceleradores dedicados que mudam o jogo na proteção de dados.

Como o Telum II atua especificamente no processamento das chaves de segurança e na criptografia:

**1. Aceleradores Integrados (On-Chip)**
>Diferente de servidores comuns, onde a criptografia muitas vezes é feita pelo software (consumindo muita CPU) ou por placas externas (gerando latência), o Telum II possui aceleradores criptográficos integrados diretamente no silício de cada núcleo.

- **Velocidade de Execução:** Quando o z/OS precisa assinar uma transação ou criptografar um lote de dados com chaves quânticas, o Telum II processa isso instantaneamente dentro do chip.

- **Baixíssima Latência:** Como o dado não precisa sair do processador para uma placa externa, a resposta é quase imediata. Isso é o que permite ao banco manter a Criptografia Onipresente (Pervasive Encryption) sem degradar a performance do sistema.

**2. Suporte Nativo a Algoritmos Pós-Quânticos (PQC)**
>O Telum II foi desenhado para lidar com a carga matemática pesada dos novos algoritmos de segurança quântica (como o Dilithium e o Kyber).

- **Eficiência Matemática:** Algoritmos quânticos exigem cálculos muito mais complexos que o RSA tradicional. O Telum II possui instruções de hardware específicas para acelerar esses cálculos de matrizes e polinômios.

- **Assinaturas Digitais em Larga Escala:** Isso significa que milhares de contratos e transações podem ser assinados digitalmente com proteção quântica simultaneamente, sem criar "filas" de processamento.

**3. O Coprocessador Crypto Express 8S**
>Embora o Telum II faça o "trabalho pesado" de processamento, ele trabalha em conjunto com o módulo Crypto Express 8S.

- **Gerenciamento de Chaves:** O Telum II processa a criptografia, mas as chaves mestras ficam guardadas dentro deste módulo físico inviolável (HSM - Hardware Security Module).

- **Isolamento Total:** Mesmo que um hacker conseguisse acesso ao sistema operacional, ele não conseguiria "ler" as chaves de segurança, pois elas nunca saem do hardware protegido. O Telum II apenas solicita ao módulo que execute a operação usando a chave protegida.

**4. Proteção contra Ataques de Canal Lateral**
>O design do Telum II inclui proteções físicas contra ataques que tentam "adivinhar" chaves de segurança medindo variações no consumo de energia ou nas radiações eletromagnéticas do chip enquanto ele processa dados sensíveis. Ele mascara esses sinais, tornando o processamento das chaves "invisível" para observadores externos.