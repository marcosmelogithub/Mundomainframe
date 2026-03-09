# 05. IA/Criptografia
### Telum II versus processadores de servidores x86
---

#### 1. Latência de Inferência de IA e Criptografia
Em servidores comuns, quando o sistema precisa realizar uma análise de fraude ou uma criptografia pesada, o dado precisa viajar do processador para uma placa externa (GPU ou HSM). No Telum II, isso acontece "dentro de casa".

| Característica | Telum II (IBM z17) | Servidor x86 + GPU/HSM |
| :-- | :-- | :-- |
| Localização da IA | Integrada no núcleo (On-chip) | Placa Externa (PCIe) |
| Latência de Resposta | ~1 milissegundo | 10 a 100+ milissegundos |
| Capacidade diária | +450 bilhões de inferência | Limitada pelo gargalo do barramento |
| Criptografia | Nativa e sem perda de performance | Consome CPU ou exige hardware extra |

#### 2. O Triunfo do Cache (Memória Interna)

O Telum II possui uma arquitetura de cache revolucionária. Enquanto um processador Intel topo de linha pode ter cerca de 60 MB a 100 MB de cache, o design do z17 permite um Cache Virtual L3 e L4 massivo.

>- **Telum II:** 360 MB de L2 (baixíssima latência) e até 2.88 GB de cache L4 por gaveta de processadores.
>- **x86:** Geralmente limitado a algumas centenas de MB de L3, com latência muito superior.

Significa que o banco de dados (Db2) consegue manter muito mais informações "pertinho" do processador, evitando buscas lentas na memória RAM principal.

#### 3. Confiabilidade e "Redundância Ativa"

>**Em processadores Intel:**
>>Se um núcleo de um processador Intel falha em um servidor comum, o servidor geralmente trava ou precisa ser reiniciado.

>**No z17**
>>- **Núcleos Reservados:** O mainframe possui núcleos "sobressalentes" que assumem o trabalho instantaneamente se um núcleo principal falhar.
>>- **RAIM (Redundant Array of Independent Memory):** Assim como em discos (RAID), a memória RAM do z17 é redundante. Se um pente de memória queimar, o sistema continua rodando sem perder um único bit de dados.

#### 4. Eficiência Energética e Espaço

>O Telum II é produzido com tecnologia de 5nm. Ele consegue entregar o desempenho de centenas de servidores x86 ocupando uma fração do espaço físico e consumindo muito menos energia por transação realizada.