## Microsoft Azure - Construindo Arquiteturas no Azure ☁️
---
### Compreendendo as Regiões

Regiões com pontos brancos são regiões anunciadas que estão quase prontas para se tornar uma região disponível.
<div align=center>
<img src="https://github.com/user-attachments/assets/8a0aa5f7-7d9f-4761-86b3-0311423546f3" width=600/>
</div>

 Os recursos criados podem ser de acordo com o acesso. Quanto mais longe maior o delay. Valores dos serviços variam de acordo com as regiões, impostos etc... nem todos os recursos estão disponíveis para todas as regiões.

* O Azure oferece mais regiões globais do que qualquer outro provedor de nuvem, com mais de 60 regiões representando mais de 140 países

* As regiões são compostas de um ou mais datacenters (por regra no mínimo é 3) muito próximos.

* Eles fornecem flexibilidade e escala para reduzir a latência do cliente

* As regiões preservam a residência dos dados com uma oferta abrangente de conformidade (A questão da LGPD - nem tudo pode sair do país, Microsoft disponibliza os recursos mas não é dona da informação)

>Região formada por datacenters - 3 datacenters, se um cair tem o outro, a comunicação entre eles é de baixa latência e alta performance. A redução de latência é responsabilidade da Microsoft.  
<div align=center>
<img src="https://github.com/user-attachments/assets/47d46553-1d75-491c-9351-9a14f6f6f96a" width=600/>
</div>

----

### Zonas de disponibilidade
<div align=center>
<img src="https://github.com/user-attachments/assets/dfbaa915-262d-4d61-ab9a-313b962ada51" width=600/>
</div>

* Fornece proteção contra tempo de inatividade devido a falha do datacenter
* Separa fisicamente os datacenters dentro da mesma região
* Cada datacenter é equipado com alimentação, resfriamento e redes independentes
* Conectadas por meio de redes privadas de fibras ópticas

### Pares de Região
* No mínimo 300 milhas de separação entre pares de região
* Replicação automática para alguns serviços
* Recuperação de região priorizada em caso de interrupção
* As atualizações são distribuídas sequencialmente para minimizar o tempo de inatividade
<div align=center>
<img src="https://github.com/user-attachments/assets/d375762a-6fe5-4deb-a94d-43ededac6af3" width=600/>
</div>

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
<div align=center>
<img src="https://github.com/user-attachments/assets/8426d7ba-43eb-4a3e-b949-4cdf9a7ecf0a" width=600/>
</div>

Grupo de recursos é um contêiner que você usa para gerenciar e agregar recursos em uma única unidade
<div align=center>
<img src="https://github.com/user-attachments/assets/43ae0d15-3750-4adf-86ad-fefa3321244e" width=600/>
</div>



* Os recursos podem existir em apenas um grupo de recursos
* Os recursos podem existir em diferentes regiões

### Grupo de recursos

* Os recursos podem ser movidos para diferentes grupos de recursos
* Os aplicativos podem utilizar vários grupos de recursos


----

### Assinatura da Azure
<div align=center>
<img src="https://github.com/user-attachments/assets/ff398e7c-9fa8-44ee-844c-72cca52018d8" width=600/>
</div>


Uma conta pode ter diversas assinaturas mas uma assinatura esta associada apenas a uma conta. Para cada assinatura tem uma fatura. é bom porque cada grupo vai usar um conjunto de recursos diferentes  

* Uma assinatura do Azure fornece acesso atenticado e autorizado às contas Azure

Limite de cobrança:
* Gera relatórios de cobranças e faturas separados para cada assinatura
Limite de controle de acesso:
* Gerenciar e controlar o acesso aos recursos que os usuários podem provisionar com assinaturas específicas

### Grupos de gerenciamento
<div align=center>
<img src="https://github.com/user-attachments/assets/01952ebb-f732-4081-9c65-f1e98486f806" width=600/>
</div>

* Os grupos de gerenciamento podem incluir várias assinaturas Azure
* As assinaturas herdam as condições aplicadas ao grupo de gerenciamento

----

### Criando recurso 
<div align=center>
<img src="https://github.com/user-attachments/assets/b46d4f50-5a0e-4c84-8f4a-6f7a373988fa" width=600/>
</div>
<div align=center>
<img src="https://github.com/user-attachments/assets/0544a990-5cbc-4096-8f71-fd5ccb7bfef0" width=600/>
</div>

O recurso foi criado usando a região (US) East US
<div align=center>
<img src="https://github.com/user-attachments/assets/3eae1fe1-a6b4-4d00-8f2e-55462a48e1ca" width=600/>
</div>

#### Log de atividades (ainda vazio)
<div align=center>
<img src="https://github.com/user-attachments/assets/54e0e803-2e64-4235-a8fd-d108580a2647" width=600/>
</div>


#### Controle de acesso (onde é definido as permissões)
<div align=center>
<img src="https://github.com/user-attachments/assets/288f2ef3-3235-4bf1-876a-52bb0ac717e4" width=600/>
</div>

----

### Criando uma rede virtual para testar o recurso
<div align=center>
<img src="https://github.com/user-attachments/assets/ba940881-9563-4899-924e-b2215a559be6" width=600/>
</div>
Aqui vamos colocar a região no Brasil para mostrar que os recursos podem estar em regiões diferentes
<div align=center>
<img src="https://github.com/user-attachments/assets/b12271bc-4e9e-4dd8-a0fa-1665a4a07b9c" width=600/>
</div>
<div align=center>
<img src="https://github.com/user-attachments/assets/d7d16d2f-c53c-4870-aa4a-d6d1daf1aaf9" width=600/>
</div>

