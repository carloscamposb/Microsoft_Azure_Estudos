## Microsoft Azure - Criando máquinas Virtuais na Azure ☁️
---
### Benefícios da Nuvem 

Quando você está implantando um aplicativo, um serviço ou qualquer recurso de TI, é importante que os recursos estejam disponíveis quando necessário. A alta disponibilidade se concentra em garantir a disponibilidade máxima, independentemente de interrupções ou eventos que possam ocorrer.

Ao arquitetar sua solução, você precisará considerar as garantias de disponibilidade do serviço. O Azure é um ambiente de nuvem altamente disponível com garantias de tempo de atividade, dependendo do serviço. Essas garantias fazem parte dos **SLAs (Contratos de Nível de Serviço)**.

---
### Benefícios da Nuvem 

#### 1) Alta disponibilidade

SLAs representam para a Azure a porcentagem relacioonada a disponibilidade de serviços ou aplicativos. Essa disponibilidade é conhecida como uptime. Se o programa esta sempre disponivel para uso, podemos dizer que é 100%. Serviços indisponiveis -down time . seriviços com 99% de disponibilidade pode apresentar uma indisponibilidade de até 1.6horas por semana ou 7.2 h por mês e ainda sim, ser um serviço disponível.e 99.9% disponivel - pode ficar indisponivel apenas 10 min por semana ou 43.2 minutos por mês. Quanto mais 9 após o ponto, menor o tempo de inatividade. Se não houver retorno dos serviços dentro do prazo estabelecido, a Microsoft entrega a seu cliente créditos extras (nunca dinheiro).

<div align=center>
  <img src="https://github.com/user-attachments/assets/04cc8126-6657-4dd7-aba8-ba0a854719cd" width=400 />
</div>
<div align=center>
  <img src="https://github.com/user-attachments/assets/52589952-885a-45e8-b15f-ecc3bcda9286" width=400 />
</div>
<div align=center>
  <img src="https://github.com/user-attachments/assets/db12bea1-f7f3-4326-ab33-6ff671fa27a9" width=600 />
</div>

#### 2) Escalabilidade

Refere-se a capacidade de ajustar os recursos para atender à demandas. Ou seja você pode escalar adicionando mais recursos para lidae melhor com o aumento da demanda. Além disso você só paga pelo necessário por aquele serviço.Como nuvem é um modelo baseado em consumo, você só paga o que usa. Se a demanda cair você poderá reduzir seus recursos e, assim, reduzir os custos. A escala aqui é **vertical** , você pode escalar verticalmente adicionando mais CPUs ou RAM à sua máquina virtual caso precise de mais processamento 

Existe uma diferença entre escalar vertical e escalar horizontal:
<div align=center>
  <img src="https://github.com/user-attachments/assets/7fad19e9-7b51-4e66-bfea-680c07f26d25" width=600 />
</div>
<div align=center>
  <img src="https://github.com/user-attachments/assets/73cf3055-6710-4b0a-9292-7a7a6fc57f01" width=600 />
</div>



#### 3) Elasticidade

Com Elasticidade, se você experimentasse um salto repentino e acentuado na demanda, seus recursos implementados poderiam ser expandidos (automaticamente ou manualmente)
Por exemplo adição de máquinas virtuais ou contêiners por meio da expansão. Da mesma forma , se houver uma queda significativa na demanda, os recursos implementados podem ser reduzidos horizontalemnte(automaticamente ou manualmente).Eu posso redimencionar meu ambiente por base em requisições. A informática elástica é a capacidade de expandir ou diminuir rapidamente recursos informáticos de processamento, memória e armazenamento, para dar resposta às mudanças de necessidades sem que se tenha de preocupar com o planeamento da capacidade e a engenharia para picos de utilização. Geralmente controlada com ferramentas de monitorização de sistemas, a informática elástica disponibiliza a quantidade de recursos alocados em conformidade com a quantidade de recursos efetivamente necessários, sem afetar as operações. Com a elasticidade na nuvem, as empresas evitam pagar por capacidade não utilizada ou por recursos inativos e não têm de se preocupar em investir na compra nem na manutenção de recursos e equipamentos adicionais. Embora seja necessário ter em conta preocupações ao nível da segurança e do controlo limitado ao considerar a utilização da informática em nuvem elástica, esta tem muitas vantagens. A informática elástica é mais eficiente do que a infraestrutura de TI típica, é normalmente automatizada, para que não tenha de depender de administradores humanos permanentemente, e oferece disponibilidade contínua de serviços ao evitar atrasos desnecessários ou interrupções do serviço.

#### 4) Confiabilidade

Devido ao design decentralizado, a nuvem naturalmente dá suporte a uma infraestrutura confiável e resiliente.Assim a nuvem permite que você tenha recursos implementados em várias regiões do mundo. Com essa escala global , mesmo que ocorra uma situação catastrófica em uma região, as outras regiões ainda estarão em funcionamento. 


#### 5) Previsibilidade

A previsibilidade na nuvem permite que você avance com confiança, seja no desempenho ou no custo. Ambas são influenciadas pelo *Microsoft Azure Well-Architected Framework*. 

O Microsoft Azure Well-Architected Framework é um conjunto de diretrizes e melhores práticas que visa garantir soluções na nuvem Azure eficientes, seguras e econômicas. Baseado em cinco pilares principais—Excelência Operacional, Segurança, Confiabilidade, Desempenho e Eficiência, e Custo—o framework ajuda a assegurar que as soluções sejam bem gerenciadas, protegidas, resilientes, escaláveis e financeiramente otimizadas, promovendo previsibilidade tanto no desempenho quanto nos custos.


#### 6) Segurança

A nuvem oferece ferramentas de segurança que atendem às necessidade dos clientes, mas é importante lembrar que a implementação de muitas delas devem ser realizadas pelos clientes "Como se fosse um casamento uma parte de cada". Se você quiser controle máximo de segurança , a infraestrutura como serviço fornecerá recursos físicos, mas permitirá que você gerencie os sistemas operacionais e o software instalado, incluindo aplicação de patches e manutenção.  

#### 7) Governança

A *auditoria* baseada em nuvem ajuda a sizalizar qualquer recurso que esteja fora de conformidade com seus padrões corporativos e fornece estratégia de mitigação.Dependendo do seu modelo operacional, patches de software e atualizações também podem ser aplicados automaticamente, o que ajuda na governaça e na segurança.Ao estabelecer uma presença de governança o mais cedo possível, você poderá manter sua presença de nuvem atualizada, protegida e bem gerenciada. 

#### 8) Gerenciabilidade

Um dos principais benefícios da computação em nuvem são as opções de capacidade de gerenciamento.
> Gerenciamento na nuvem diz respeito a gerenciar seus recursos de nuvem: Ex:
* Escalar automaticamente a implemnetação de recursos com base na necessidade
* Implantar recursos com base em um modelo pré-configurado, removendo a necessidade de configuração manual.
> O gerenciamento na nuvem diz respeito à maneira de gerenciar seu ambiente de nuvem e seus recursos. 
* Por meio de um portal Web
* Usando uma interface de linha de comando
* Usando APIs
* Usando PowerShell
