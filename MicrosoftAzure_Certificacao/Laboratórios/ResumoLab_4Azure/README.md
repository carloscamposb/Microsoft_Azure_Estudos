## Microsoft Azure - Construindo Arquiteturas no Azure ☁️
---
### Compreendendo as Regiões

Regiões com pontos brancos são regiões anunciadas que estão quase prontas para se tornar uma região disponível.

<!-- imagem -->

 Os recursos criados podem ser de acordo com o acesso. Quanto mais longe maior o delay. Valores dos serviços variam de acordo com as regiões, impostos etc... nem todos os recursos estão disponíveis para todas as regiões.

* O Azure oferece mais regiões globais do que qualquer outro provedor de nuvem, com mais de 60 regiões representando mais de 140 países

* As regiões são compostas de um ou mais datacenters (por regra no mínimo é 3) muito próximos.

* Eles fornecem flexibilidade e escala para reduzir a latência do cliente

* As regiões preservam a residência dos dados com uma oferta abrangente de conformidade (A questão da LGPD - nem tudo pode sair do país, Microsoft disponibliza os recursos mas não é dona da informação)

>Região formada por datacenters - 3 datacenters, se um cair tem o outro, a comunicação entre eles é de baixa latência e alta performance. A redução de latência é responsabilidade da Microsoft.  

<!-- imagem 1-->

----
### Zonas de disponibilidade
<!-- imagem 2 -->

* Fornece proteção contra tempo de inatividade devido a falha do datacenter
* Separa fisicamente os datacenters dentro da mesma região
* Cada datacenter é equipado com alimentação, resfriamento e redes independentes
* Conectadas por meio de redes privadas de fibras ópticas

### Pares de Região
* No mínimo 300 milhas de separação entre pares de região
* Replicação automática para alguns serviços
* Recuperação de região priorizada em caso de interrupção
* As atualizações são distribuídas sequencialmente para minimizar o tempo de inatividade

<!-- imagem -->

> É importante notar que o Brasil ainda esta ligado ao Estados Unidos como par de região. Mas já tem um datacenter no Rio De Janeiro que possivelmente futuramente será o par. 
----
### Regiões soberanas da Azure

Azure Governamental:
* Instancia separada da Azure
* Fisicamente isolada de implantações que não sejam do governo dos EUA.
* Acessível apenas as pessoas verificadas e autorizadas

Serviços governamentais dos EUA:
* Atende às necessidades de segurança e conformidade das agências federais, governos e estaduais e locais dos EUA e seus provedores de soluções.


Azure China:
A microsoft é o primeiro provedor estrangeiro de serviços de nuvem pública da China, em conformidade com as regulamentações governamentais

* Instância fisicamente separada dos serviços de nuvem da Azure, operados pela 21Vianet
* Todos os dados permanecem dentro da China para garantir a conformidade

-----

### Recursos da Azure
Os recursos da Azure sãoc componentes como armazenamento, máquinas virtuais e redes que estão disponíveis para criar soluções de nuvem.
 <!--imagem  -->


Grupo de recursos é um contêiner que você usa para gerenciar e agregar recursos em uma única unidade

 <!-- imagem -->

* Os recursos podem existir em apenas um grupo de recursos
* Os recursos podem existir em diferentes regiões

### Grupo de recursos

* Os recursos podem ser movidos para diferentes grupos de recursos
* Os aplicativos podem utilizar vários grupos de recursos


----

### Assinatura da Azure
<!-- imagem -->
Uma conta pode ter diversas assinaturas mas uma assinatura esta associada apenas a uma conta. Para cada assinatura tem uma fatura. é bom porque cada grupo vai usar um conjunto de recursos diferentes  

* Uma assinatura do Azure fornece acesso atenticado e autorizado às contas Azure

Limite de cobrança:
* Gera relatórios de cobranças e faturas separados para cada assinatura
Limite de controle de acesso:
* Gerenciar e controlar o acesso aos recursos que os usuários podem provisionar com assinaturas específicas

### Grupos de gerenciamento
<!-- imagem -->
* Os grupos de gerenciamento podem incluir várias assinaturas Azure
* As assinaturas herdam as condições aplicadas ao grupo de gerenciamento

----
### Criando recurso 
<!-- imagens -->

O recurso foi criado usando a região (US) East US

#### Log de atividades (ainda vazio)
<!-- imagem -->

#### Controle de acesso (onde é definido as permissões)
<!-- imagem -->
----
### Criando uma rede virtual para testar o recurso
<!-- imagem -->

Aqui vamos colocar a região no Brasil para mostrar que os recursos podem estar em regiões diferentes
<!-- imagens -->
