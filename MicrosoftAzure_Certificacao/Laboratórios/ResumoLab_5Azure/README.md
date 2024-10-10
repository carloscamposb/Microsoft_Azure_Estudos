## Microsoft Azure - Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure ☁️
---
A **computação do Azure** é um serviço sob demanda que fornece recursos de computação, como discos , processadores, memórias, redes e sistemas operacionais.

<!-- IMAGEM SLIDE 1 -->

### Máquinas virtuais do Azure
* As máquinas virtuais do Azure(VMs)são emulações de software de computadores físicos 
* Inclui processador virtual, memória, armazenamento e rede
* Oferta de IaaS que oferece personalização e controle total 

### Conjuntos de dimensionamento de VMs
Os conjuntos de dimensionamento oferecem uma oportunidade de balanceamento de carga para dimensionar os recursos automaticamente.
<!-- IMAGEM SLIDE -->

### Área de trabalho virtual da Azure
É uma virtualização de área de trabalho e aplicativo executada na nuvem. Desktop personalizado
* Dá para criar um ambiente completo de virtualização da área de trabalho sem precisar executar outros servidores de gateway
* Reduz o risco de que o recurso seja deixado para trás
* Implantações reais de várias sessões

### Serviços de contêineres do Azure
Os contêineres do Azure fornecem um ambiente leve e virtualizado que não exige o gerenciamento do sistema operacional e pode responder a alteração sob demanda. 

* **Instâncias de Contêiner do Azure:** uma oferta de PaaS que executa um contêiner ou pod de contêineres no Azure
* **Aplicativos de Contêiner do Azure:** uma oferta de PaaS, como instâncias de contêineres, que pode balancear a carga e escalar (Balanceamento é a palavra chave)
* **Serviço de Kubernetes do Azure:** um serviço de orquestração para contêineres com arquiteturas destribuídas e grandes volumes de contêineres (Orquestração é a palavra chave)

### Azure Functions
Uma oferta de PaaS que dá suporte a operações de computação sem servidor
O código baseado em eventos é executado quando chamado, sem exigir uma infraestrutura de servidor durante períodos inativos.

### Comparar opções de computação do Azure
Máquinas virtuais
* Servidor beseado em nuvem que dá suporte a ambientes Windows ou Linux
* Útil para migração de lift-and-shift (levar e buscar) para a nuvem 
* Pacote do sistema operacional completo, incluindo o sistema operacional do host
* Fornece uma experiência de área de trabalho do Windows baseada em nuvem 
* Aplicativos dedicados para conexão e uso ou acessíveis de qualquer navegador moderno

Área de trabalho virtual 
* Fornece uma experiência de área de trabalho do Windows baseada em nuvem 
* Aplicativos dedicados para conexão e uso ou acessíveis de qualquer navegador moderno 

Contêineres
* Ambiente leve e em miniatura adequado para a execução de microsserviços
* Projetado para escabilidade e reseliência por meio da orquestração
* Os aplicativos e serviços são empacotados em um contêiner que fica na parte superior do sistema operacional do host. Vários contêineres podem ficar em um sistema operacional do host.

### Serviços de Aplicativo do Azure 
Consistem em uma plataforma totalmente gerenciada para criar, implantar e dimensionar aplicativos Web e APIs rapidamente
* Trabalha com .NET, .NET Core, Node.js, Java , Python ou php 
* Oferta de PaaS com requisitos de nível corporativo de desempenho , segurança e conformidade 
* A **Rede Virtual do Azure(VNet)** permite que os recursos do Azure se comuniquem uns com os outros, com a internet e com as redes locais
* Pontos de extremidade públicos , acessíveis de qualquer lugar na internet
* Pontos de extremidade privados, acessíveis somente de dentro da sua reede
* As sub-redes vuirtuais segmentam sua rede para atender às suas necessidades
* O emparelhamento de rede conecta suas redes privadas diretamente

### Serviços de rede do Azure Gateway de VPN 
É usado para enviar tráfego criptografando entre uma rede virtual do Azure e uma no local pela internet pública
 <!--imagemmm  -->

### Serviços de rede do Azure: ExpressRoute 
 <!--imagamem´  -->
O **ExpressRoute** estende as redes locais para o Azure por meio de uma conexão privada facilitada por um provedor de conectividade

### DNS do Azure
* Confiabilidade e desempenho aproveitando uma rede global de servidores de nome DNS usando a rede Anycast
* A segurança do DNS do Azure baseia-se no gerenciador de recursos do Azure, habilitando o controle de acesso baseado em função e o monitoramento e o registro em log. 
* Facilidade de uso para gerenciar seus recursos externos e do Azure com um único serviço DNS 
* As redes virtuais personalizáveis permitem que você use nomes de domínio privados e totalmente personalizados em suas redes virtuais privadas
* Os registros de alias dão suporte a conjutos de registros de alias para apontar diretamente para um recurso do Azure 







