# Segurança Quantica (Quantum-Safe)
---
>A computação quântica, embora ainda em evolução, representa uma ameaça teórica: no futuro, um computador quântico potente poderá quebrar quase toda a criptografia usada hoje na internet (como o RSA). O IBM z17 foi projetado para que o ambiente computacional esteja protegido hoje contra esse cenário.

**Criptografia de Próxima Geração:** O z17 utiliza algoritmos de Criptografia Pós-Quântica (PQC). São fórmulas matemáticas tão complexas que nem mesmo um computador quântico conseguiria resolver em tempo hábil.

**Proteção "Harvest Now, Decrypt Later":** Um dos maiores riscos atuais é hackers roubarem dados criptografados hoje para guardá-los e descriptografá-los daqui a 10 anos, quando a computação quântica for comum. O z17 permite que o ambiente computacional já use chaves quânticas para proteger esses dados agora, invalidando essa estratégia de ataque.

**Hardware Dedicado (HSM):** O z17 possui placas de segurança (Crypto Express 8S) que geram e armazenam essas chaves quânticas em um ambiente físico inviolável. Se alguém tentar abrir a placa fisicamente, ela "se apaga" para proteger o segredo.

**Assinaturas Digitais Seguras:** Além de proteger os dados guardados, a segurança quântica no z17 garante que as transações e contratos assinados digitalmente pelo banco hoje permaneçam válidos e autênticos por décadas, sem risco de falsificação futura.