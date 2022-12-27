# O que é um Pod?
O contexto compartilhado de um Pod é um conjunto de namespaces, cgroups e potencialmente outras facetas do isolamento - as mesmas coisas que isolam um recipiente. Dentro do contexto de um Pod, os aplicativos individuais podem ter outras sub-isolações aplicadas.


# O que é um ReplicaSet?
O objetivo de um ReplicaSet é manter um conjunto estável de Pods de réplica em execução a qualquer momento. Como tal, é frequentemente usado para garantir a disponibilidade de um número especificado de Pods idênticos.

# O que é um Deployment?
A Implantação fornece atualizações declarativas para Pods e ReplicaSets.

# O que é um Service?
Uma maneira abstrata de expor um aplicativo em execução em um conjunto de Pods como um serviço de rede.

 - Cluster IP, Expõe o serviço em um IP interno do cluster. A escolha desse valor torna o serviço acessível apenas de dentro do cluster. Este é o tipo padrão

 - NodePort, Expõe o serviço no IP de cada Node em uma porta estática (o NodePort). Um serviço ClusterIP, para o qual o serviço NodePort irá rotear, é criado automaticamente. Você poderá entrar em contato com o serviço NodePort, de fora do cluster, solicitando <NodeIP>:<NodePort>.

 - Load Balancer, Expõe o serviço externamente usando o balanceador de carga de um provedor de nuvem. Os serviços NodePort e ClusterIP, para os quais o balanceador de carga    externo fará o roteamento, são criados automaticamente.
