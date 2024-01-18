1. Os discos de tecnoloxía "SCSI".
//equipos/máquina[hardware/disco[@tecnoloxía='SCSI']]

2. O nome do sistema operativo da máquina con IP "192.168.10.45".
//equipos/máquina[config/IP='192.168.10.45']

3. Os atributos que figuran nos procesadores da marca "AMD".
//equipos/máquina/hardware/procesador[@marca='AMD']/@*

4. Os textos (soamente) que figuran na configuración (elemento "config") do equipo de nome "COPERNICO".
//equipos/máquina[@nome='COPERNICO']/config

5. As máquinas de tipo "Semitorre" con sistema operativo "Windows XP".
//máquina[hardware[tipo='Semitorre']and(config[OS='Windows XP'])]

6. Os fabricantes das máquinas que teñan 4GB de memoria "DDR2".
//hardware[memoria[@tecnoloxía='DDR2'][text()='4']]/fabricante

7. O sistema operativo das máquinas nas que figure o número de núcleos do procesador.
//máquina[hardware/procesador[@num_nucleos>'0']]/config/OS

8. Os nomes das máquinas que empreguen memoria con tecnoloxía "DDR2".
//máquina[hardware/memoria[@tecnoloxía='DDR2']]/@nome

9. As máquinas con procesador da marca "Intel" e gravadora de DVD.
//máquina[hardware/procesador[@marca='Intel']and(hardware/gravadora[@tipo='DVD'])]

10. A configuración daquelas máquinas nas que figura un gateway
//máquina[config/gateway]/config

11. As máquinas con nome comezando por "PC".
//máquina[starts-with(@nome,'PC')]

12. O nome das máquinas con máis de un disco duro.
//máquina[hardware[count(disco)>1]]/@nome

13. A suma dos GB de memoria RAM de todas as máquinas.
sum(//máquina/hardware/memoria)

14. A suma das capacidades dos discos duros de tipo "SCSI".
sum(//máquina/hardware/disco[@tecnoloxía='SCSI']/@capacidade)

15. Os nomes das máquinas das que se coñeza a súa cantidade de memoria, pero non a tecno-loxía desta.
//máquina[hardware/memoria>0 and not(hardware/memoria/@tecnoloxía) ]/@nome

16. As máquinas con sistema operativo da familia Windows e gravadora de DVD.
//máquina[config[contains(OS,'Windows')]and hardware/gravadora[@tipo='DVD']]

17. As máquinas nas que non figure o sistema operativo.
//máquina[config[not(OS)]]

18. O nome da máquina e do SO daquelas máquinas con máis de un disco duro.
//máquina/@nome | //máquina[hardware[count(disco)>1]]/config/OS

19. A configuración daquelas máquinas nas que figura unha dirección IP pero non o gateway.
//máquina[config[starts-with(IP,'1') and not(gateway)]]/config

20. Os elementos baleiros (non conteñen texto).
//*[not(node())]

21. As direccións IP dentro da rede 192.168.10.0/24.
//máquina/config[contains(IP,'192.168.10')]/IP

22. Os nomes das máquinas con procesador multinúcleo e 2GB ou menos de memoria.
//máquina[hardware[procesador[@num_nucleos>1]][memoria/text()<='2']]/@nome

23. As máquinas que teñan disco duro (un ou varios) con capacidade total maior de 1000GB.
//máquina[hardware[count(disco)>=1]][sum(hardware/disco/@capacidade)>1000]

24. As máquinas que teñan disco duro (un ou varios) con capacidade total menor de 80GB.
//máquina[hardware[count(disco)>=1]][sum(hardware/disco/@capacidade)<80]
