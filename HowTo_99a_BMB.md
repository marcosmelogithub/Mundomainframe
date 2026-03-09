# Banco Mercantil do Brasil
---
##### Contexto Geral do Sistema Mainframe Atual
---

>O Banco Mercantil do Brasil utiliza atualmente o mainframe IBM z17, tendo sido uma das primeiras instituições financeiras do país a adotar essa tecnologia de última geração.

---
##### Infraestrutura de Mainframe
---

- **Hardware:** IBM z17. O banco atualizou seu parque tecnológico em 2025 para este modelo, que é equipado com o processador Telum II. Essa máquina permite ao banco processar bilhões de operações de inferência por dia com latência mínima (cerca de 1 milissegundo), integrando Inteligência Artificial (IA) diretamente no "core" bancário.

- **Destaque Tecnológico:** O uso do z17 foca em segurança quântica (preparação para futuras ameaças de computação quântica) e detecção de fraudes em tempo real, o que é crucial para o público-alvo do banco (aposentados e pensionistas).

---
##### Sistema Operacional e Software
---

- **Sistema Operacional:** O banco opera sobre o z/OS, o sistema operacional padrão da IBM para mainframes, que oferece a robustez necessária para transações críticas de alta disponibilidade.

- **Banco de Dados:** Utiliza o IBM Db2 for z/OS, otimizado para lidar com volumes massivos de dados transacionais.

- **IBM z/OS Connect:** O Mercantil também utiliza soluções como o IBM z/OS Connect para integrar o legado do mainframe com APIs modernas e serviços em nuvem (estratégia de nuvem híbrida com Google Cloud).

>**Curiosidade:** Essa atualização para o z17 permitiu que o banco reduzisse drasticamente o tempo de resposta em análises de crédito e prevenção à lavagem de dinheiro, realizando esses processos durante a própria transação, sem que o cliente perceba o atraso.

---
##### Integração mainframe e nuvem do Google
---
A integração entre o mainframe IBM z17 do Banco Mercantil do Brasil e a nuvem do Google (Google Cloud) é um exemplo de arquitetura de ***nuvem híbrida***, desenhada para unir o máximo de segurança e desempenho do ambiente local com a agilidade e inovação da nuvem pública.

**1. Conectividade e Exposição de APIs**

- **IBM z/OS Connect:** Esta ferramenta é a "ponte" principal. Ela permite que as aplicações e dados que residem no mainframe (escritos em linguagens como COBOL ou armazenados no Db2) sejam expostos como APIs RESTful modernas.

- **Consumo pelo Google Cloud:** As aplicações hospedadas no Google Cloud (como o aplicativo móvel ou novos serviços de front-end) consomem essas APIs de forma transparente, como se estivessem acessando qualquer outro microserviço, sem precisar entender a complexidade interna do mainframe.

**2. Estratégia de Nuvem Híbrida**

- **Onde fica cada coisa:** O Mercantil mantém o "Core Banking" (processamento de saldo, extrato e liquidações críticas) no IBM z17 devido à altíssima disponibilidade e segurança. Já as camadas de engajamento com o cliente (experiência do usuário, canais digitais e processamento de dados em escala) rodam no Google Cloud.

- **Baixa Latência:** A comunicação entre o z17 e o Google Cloud é otimizada para ser extremamente rápida, permitindo que uma consulta feita no celular do cliente chegue ao mainframe e retorne em milissegundos.

**3. Inteligência Artificial e Dados**

- **Processador Telum II:** Como o z17 possui o processador Telum II, ele consegue executar modelos de IA para detecção de fraude no momento exato da transação (on-chip AI).

- **Big Data no Google:** Os dados gerados pelo mainframe são enviados para o ambiente de dados do Google Cloud (como o BigQuery) para análises de longo prazo, marketing personalizado e modelos de aprendizado de máquina que não exigem resposta em tempo real.

**4. Segurança e Resiliência**

- **Segurança Quântica:** O z17 traz criptografia pronta para a era quântica, garantindo que os dados que trafegam entre o banco e a nuvem permaneçam protegidos mesmo contra futuras tecnologias de quebra de códigos.

- **Disponibilidade:** A infraestrutura é montada para que, caso haja instabilidade em um dos ambientes, o outro continue operando funções essenciais, garantindo que o banco nunca fique "fora do ar" para o cliente final.

>**Resumo Estratégico**
>>Essa modernização permitiu ao Banco Mercantil manter sua tradição e robustez, ao mesmo tempo em que oferece uma experiência digital rápida e segura, focada especialmente na eficiência para o seu público-alvo.
>>
>>O Telum II permite que o banco ofereça o nível mais alto de segurança do mundo (Nível 4 do padrão FIPS 140-2) sem que o cliente sinta qualquer lentidão ao usar o aplicativo. É a união de força bruta com inteligência microscópica.
>>
>>Enquanto o z/OS Connect dá ao Banco Mercantil a agilidade para competir com as fintechs e se integrar ao Google Cloud, a Segurança Quântica dá a imunidade necessária para proteger o patrimônio dos clientes contra as ameaças tecnológicas mais avançadas do século XXI.
>>
>>Enquanto o Google Cloud oferece a flexibilidade e as ferramentas de análise de dados para o Banco Mercantil, o z/OS no z17 fornece a âncora de confiança: a garantia de que cada centavo será processado com precisão matemática, segurança absoluta e velocidade recorde.
>>
>>A grande vantagem para o Banco Mercantil é o "In-Transaction AI": Enquanto um servidor comum analisa a fraude depois que o dinheiro saiu (e tenta estornar), o Telum II do z17 permite analisar a fraude durante o processamento, autorizando ou bloqueando o PIX em milissegundos.

---
##### A modernização tecnológica e ESG
---
>A estratégia de ESG (Environmental, Social, and Governance) do Banco Mercantil do Brasil está profundamente conectada ao seu processo de modernização tecnológica. O banco utiliza a eficiência do mainframe e a inovação digital para cumprir metas de sustentabilidade e inclusão.

**1. Ambiental (Environmental): Eficiência e TI Verde**
O banco utiliza a infraestrutura do IBM z17 como uma ferramenta central de descarbonização.
- **Consolidação de Servidores:** Um único IBM z17 pode substituir milhares de servidores x86 comuns. Isso reduz o consumo de energia em até 65% e a pegada de carbono em mais de 100 toneladas de $CO_2$ anuais.
- **Projeto Paperless:** O Mercantil eliminou quase totalmente o uso de papel em suas agências. As transações são feitas em tablets e plataformas digitais, o que já poupou mais de 120 toneladas de papel.
- **Energia Renovável:** O banco estabeleceu a meta de utilizar a maior parte de sua energia (cerca de 80%) vinda de fontes renováveis, como usinas solares e pequenas centrais hidrelétricas (CGHs).

**2. Social: O Público 50+ e Inclusão Financeira**

Este é o diferencial estratégico do Mercantil. Como o banco foca em aposentados e pensionistas, o pilar social é voltado para a longevidade.

- **Educação Financeira:** O banco possui políticas rigorosas para evitar o superendividamento desse público sensível, oferecendo conteúdos adaptados via WhatsApp (pela assistente virtual Mel) e redes sociais.

- **Acessibilidade Digital:** A integração do mainframe com o Google Cloud permitiu criar um aplicativo com interface simplificada, focado em quem tem dificuldades com tecnologia, mas precisa de segurança absoluta (garantida pela IA do z17).

- **Investimento Social:** O banco mantém editais anuais de projetos sociais (destinando centenas de milhares de reais) para instituições que cuidam de idosos e promovem o desenvolvimento comunitário nas regiões onde o banco atua.

**3. Governança (Governance): Transparência e Segurança**

A governança no Mercantil é pautada pela solidez bancária e pelo cumprimento estrito das normas do Banco Central (BC).

- **Segurança de Dados:** O uso de criptografia quântica e o processador Telum II não são apenas decisões técnicas, mas de governança. Eles garantem que o banco proteja o patrimônio do cliente contra ataques cibernéticos sofisticados.

- **Ética e Compliance:** O banco divulga anualmente seu Relatório de Sustentabilidade (seguindo padrões globais como o GRI) e possui comitês específicos para monitorar riscos sociais, ambientais e climáticos.

- **Acordos Tributários:** Recentemente, em 2025, o banco demonstrou transparência ao resolver 96% de seus passivos tributários em acordos com o governo, fortalecendo sua imagem perante investidores e o mercado.

**4. Resumo do Impacto ESG (2025/2026)**

| Pilar | Principal Iniciativa | Resultado/Meta |
| :-- | :-- | :-- |
| **E** | Migração para IBM z17 | Redução de 65% no consumo de energia de TI.|
| **S** | Foco no Público 50+ | 10 milhões de clientes com acesso a crédito e educação. |
| **G** | Criptografia Quântica	Proteção | contra fraudes em tempo real (< 1ms). |

---
##### Desempenho financeiro recorde do BMB e investimento nas metas de sustentabilidade**
---

>O desempenho financeiro recorde do Banco Mercantil — que ultrapassou a marca de R$ 1 bilhão em lucro líquido anual em 2025 — não é um evento isolado, mas o combustível para acelerar sua agenda ESG e sua transformação digital.

>O banco reinveste esse capital seguindo um ciclo estratégico onde a eficiência tecnológica gera lucro, que por sua vez financia mais sustentabilidade e inclusão.

**1. Reinvestimento em TI Verde e Eficiência (E)**
>O lucro recorde permitiu ao banco acelerar a substituição de infraestruturas antigas pelo IBM z17.

- **Capex em Sustentabilidade:** Parte do lucro foi direcionada para a modernização do datacenter, que agora consome menos energia por transação.

- **Nuvem Híbrida:** O investimento na parceria com o Google Cloud permite que o banco escale seus serviços sem precisar construir novos datacenters físicos, reduzindo o impacto ambiental direto.

**2. Expansão do Ecossistema para o Público 50+ (S)**

>O Mercantil reinveste seus ganhos para ser mais do que um banco para o aposentado; ele quer ser um "ecossistema de longevidade".

- **Novos Canais Digitais:** O lucro financia a melhoria constante da Mel (inteligência artificial do banco), tornando-a mais humana e capaz de resolver problemas complexos por voz, facilitando a vida de quem tem dificuldades motoras ou visuais.

- **Crédito Consciente:** Com maior solidez financeira, o banco consegue oferecer taxas de juros mais competitivas no crédito consignado, garantindo que o público sênior tenha acesso a capital sem cair em armadilhas de endividamento.

**3. Blindagem e Governança de Dados (G)**
>O lucro robusto permite que o banco esteja sempre à frente nas exigências do Banco Central (BC) e na segurança dos dados.

- **Cibersegurança de Ponta:** O investimento no processador Telum II e em criptografia quântica é caro, mas o lucro recorde permite que o Mercantil adote essas tecnologias antes mesmo de muitos bancos globais.

- **Transparência:** O banco utiliza seus recursos para aprimorar auditorias internas e sistemas de compliance, garantindo que o crescimento acelerado (o banco ganha milhares de novos clientes por mês) não comprometa a ética ou a segurança.

**4. O "Círculo Virtuoso" do Mercantil (2025/2026)**

| Ação Financeira | Impacto Estratégico | Resultado ESG |
| :-- | :-- | :-- |
| Lucro de R$ 1 bi+ | Reinvestimento no IBM z17 | Menor pegada de carbono (TI Verde) |
| Baixa Inadimplência | Melhores taxas para o público 50+ | Inclusão financeira e social |
| Eficiência Operacional | Digitalização total de processos | Redução drástica no uso de papel e resíduos |

>**Conclusão**
>>O Banco Mercantil provou que focar em um nicho específico (público 50+) com tecnologia de mainframe de última geração é altamente lucrativo. O diferencial é que esse lucro está sendo usado para "blindar" o futuro do Banco Mercantil contra ameaças cibernéticas e climáticas, mantendo o foco no seu impacto social.