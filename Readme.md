Infraestrutura

A Oracle é uma empresa de Tecnologia que possui como um de seus produtos, oferecer infraestrutura de qualidade em serviços de 'nuvem'.
Como medida preventiva a OCI (Oracle Cloud Infrastructure), foi idealizada de forma provisionada para garantir que as aplicações de seus clientes sempre fiquem disponíveis. A seguir, explicarei passo a passo como a arquitetura física da OCI é estruturada:

1º Region (Regiões)
A OCI está presente fisicamente em todos os 5 continentes. A Oracle utiliza dessa medida a fim estabelecer aos seus usuários baixa latencia e alta performance. A recomendação da Oracle é que as aplicações estejam rodando na mesma região em que o usuário está localizado para poder utilizar de todos os recursos disponíveis com o máximo de desempenho.

2º Availability Domain (Dominios de disponibilidade)
Cada região possui até 3 domínios de disponibilidade (são os datacenters). Cada domínio de disponibilidade possui infraestrutura própria e não compartilha seu hardware com outro. Assim, caso algum domínio de disponibilidade esteja indisponível, é possível manter as aplicaçoes dos usuários funcionando em outro domínio que esteja disponível no momento.

3ºFault Domains (Domínios de falha)
Em cada domínio de disponibilidade, existem 3 domínios de falha, que nada mais são que data centers lógicos que assim como os domínios de disponibilidade, onde cada um possui sua própria infraestrutura, os domínios de falha também foram arquitetados do mesmo modo, com finalidade de ter um plano de contingencia caso ocorra algum problema. Assim, caso o domínio de falha onde a aplicação do usuário esteja rodando precise ser desligado para alguma manutenção preventiva por exemplo, a aplicação continua funcionando em outro dominio de falha enquanto o domínio inicial é averiguado.

Recapitulando, a OCI está presente nos 5 continentes cada um com sua propria infraestrutura nomeada de 'regiões'. Cada região possui até 3 dominios de disponibilidade (datacenter), que são isolados um do outro não compartilhanhando do mesmo hardware. Cada um desses dominios possuem 3 dominios de falha que são datacenters lógicos que também não compartilham da mesma infraestrutura. Essa arquitetura foi desenvolvida afim de entregar um serviço com alta disponibilidade e qualidade ao usuário final.

Região
|
|--->Dominio(s) de disponibilidade
|
|
|--->Dominio de falha
|--->Dominio de falha
|--->Dominio de falha
