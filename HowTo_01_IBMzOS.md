# 01. zOS do IBM z17
---

>O ***z/OS rodando no IBM z17*** representa o ápice da computação de missão crítica, combinando décadas de estabilidade com inovações disruptivas em Inteligência Artificial e segurança. Esse sistema operacional é o "cérebro" que orquestra o hardware de última geração.

#### 1. Visão Estratégica (O Valor para o Negócio)

- **Disponibilidade "Seven-Nines" (99,99999%):** O z/OS é projetado para que o banco nunca pare. Ele permite atualizações de hardware e software sem interromper as transações, algo vital para qualquer missão crítica.

- **Time-to-Market com APIs:** Através do z/OS Connect, o sistema transforma processos legados complexos em APIs REST modernas. Isso permite que se lance novos produtos em aplicativo móvel (front-end no Google Cloud, por exemplo) consumindo dados do mainframe de forma instantânea.

- **Consolidação e Eficiência de Custo:** O z/OS no z17 permite rodar milhares de cargas de trabalho simultâneas (transações bancárias, PIX, folha de pagamento) em uma pegada de datacenter reduzida, otimizando o consumo de energia e licenciamento.

- **Prontidão Quântica:** Estrategicamente, o z/OS já protege os dados contra "ataques futuros" de computadores quânticos, garantindo a longevidade e a conformidade regulatória do banco.

#### 2. Visão Técnica (As Engrenagens do Sistema)

- **Aceleração de IA Nativa (Telum II):** O z/OS no z17 é otimizado para explorar o acelerador de IA integrado ao processador Telum II. Tecnicamente, isso permite que o sistema execute modelos de Deep Learning (inferência) dentro do ciclo da transação, com latência inferior a 1ms, sem precisar enviar dados para um servidor externo.

- **Criptografia Onipresente (Pervasive Encryption):** O sistema operacional gerencia a criptografia de 100% dos dados em repouso e em trânsito, sem impacto na performance, utilizando coprocessadores criptográficos dedicados.

- **Gerenciamento de Workload (WLM):** O Workload Manager do z/OS é um dos componentes mais sofisticados. Ele prioriza automaticamente os recursos (CPU, Memória) para as transações mais importantes. Se uma transação importante estiver com volume alto, o WLM garante que ele tenha prioridade sobre um relatório interno, por exemplo.

- **Arquitetura de Memória e I/O:** O z/OS utiliza uma arquitetura de entrada e saída (I/O) massivamente paralela, permitindo que se processe bilhões de registros no banco de dados Db2 com uma velocidade que servidores convencionais (x86) não conseguem atingir.

- **Segurança Multinível (RACF):** O software de segurança nativo (Resource Access Control Facility) oferece um controle granular extremo sobre quem pode acessar cada bit de informação, sendo virtualmente imune a ransomwares tradicionais.