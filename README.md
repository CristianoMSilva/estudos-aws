<br>
<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/9/93/Amazon_Web_Services_Logo.svg" alt="AWS Logo" width="300"/>
</p>
<br>

# AWS Cloud Practitioner Essentials

### Repositório dedicado a documentação de conceitos, anotações de módulos para a certificação AWS Cloud Practitioner.


## Módulo 1: Conceitos de Nuvem e Infraestrutura Global

### O que é Computação em Nuvem?

É a entrega sob demanda de recursos de TI por meio da internet, com um modelo de precificação de pagamento conforme o uso. Em vez de comprar e manter data centers físicos, você acessa serviços de tecnologia conforme a necessidade.

### Tipos de Implantação (Modelos de Nuvem)

* **Nuvem (Cloud-based):** Migração total da infraestrutura para a nuvem, permitindo utilizar os recursos de maneira estendida e escalável.

* **On-premises (Local/Privada):** Utilizada para fornecer recursos dedicados dentro do próprio data center físico da empresa, focando em baixa latência ou restrições locais.

* **Híbrida:** Modelo que conecta a infraestrutura local (geralmente softwares legados) à nuvem, visando a manutenção de sistemas antigos e o crescimento escalável em novos módulos.

### As 6 Vantagens da Computação em Nuvem (AWS)

1. **Troca de despesas fixas por despesas variáveis:** Pague apenas pelo que consumir, em vez de investir pesado em infraestrutura antes de usá-la.

2. **Parar de tentar adivinhar a capacidade:** Elimina o desperdício por superdimensionamento ou a falta de recursos por subdimensionamento.

3. **Economia massiva em escala:** Devido ao volume de clientes, os provedores conseguem repassar reduções de custos em forma de preços mais baixos.

4. **Aumento da velocidade e agilidade:** Recursos de TI ficam disponíveis para os desenvolvedores em minutos, reduzindo o tempo de inovação.

5. **Parar de gastar dinheiro com execução e manutenção de data centers:** Foco no negócio, deixando a segurança física, energia e resfriamento do hardware por conta da AWS.

6. **Alcance global em segundos:** Capacidade de implantar aplicações em múltiplas Regiões ao redor do mundo com poucos cliques.

### Infraestrutura Global: Regiões e Zonas de Disponibilidade (AZs)

* **Região:** Uma localização geográfica isolada no mundo que contém múltiplos data centers.

* **Zonas de Disponibilidade (AZs):** Data centers isolados e independentes dentro de uma Região, conectados por redes de alta velocidade e baixa latência. Uma Região é composta por um agrupamento de AZs, garantindo alta disponibilidade e tolerância a falhas.

### Modelo de Responsabilidade Compartilhada

Determina exatamente as fronteiras de segurança entre o provedor e o usuário:

* **Cliente:** Responsável pela **Segurança NA Nuvem** (dados do cliente, gerenciamento de acessos/IAM, criptografia e configurações de rede).

* **AWS:** Responsável pela **Segurança DA Nuvem** (infraestrutura global, hardware, softwares de virtualização e segurança física dos data centers).

* *Nota:* A linha de divisão pode variar dependendo do tipo de serviço utilizado (IaaS, PaaS ou SaaS).

## Módulo 2: Computação na Nuvem

### Introdução ao Amazon EC2 (Elastic Compute Cloud)

O Amazon EC2 fornece capacidade de computação escalável e segura na nuvem AWS. Ele foi projetado para tornar a computação em nuvem em escala web mais fácil para os desenvolvedores.

* **Características:** Altamente flexível, econômico e rápido para implantar.

* **Modelo de Cobrança:** Paga-se apenas pelo tempo em que as instâncias (Máquinas Virtuais) estiverem em execução.

* **Infraestrutura Multilocatária (Multi-tenant):** As instâncias compartilham os mesmos recursos físicos de hardware (servidores) de forma isolada e segura.

* **Comparativo de Gerenciamento:**
  
  * **On-premises:** Exige o gerenciamento e manutenção física e local de toda a infraestrutura.
  
  * **Baseada em Nuvem (AWS):** Elimina a necessidade de gerenciar hardware físico, focando apenas no provisionamento lógico.

#### Ciclo de Inicialização de uma Instância EC2

1. **Escolha da AMI (Amazon Machine Image):** Seleção do modelo básico que inclui o sistema operacional, servidor de aplicação e aplicações iniciais.

2. **Escolha do Tipo de Instância:** Seleção da combinação ideal de recursos (CPU, memória, armazenamento e capacidade de rede).

3. **Iniciar (Launch):** Execução da instância na nuvem.

4. **Gerenciamento de Acesso:** Definição de acessos e redes (Público ou Privado) para permitir ou restringir conexões.

5. **Conectar e Usar:** Acesso à máquina virtual para utilização e deploy de aplicações.

---

### Tipos de Instâncias EC2

A AWS oferece famílias de instâncias otimizadas para diferentes casos de uso:

* **Uso Geral (General Purpose):** Equilíbrio entre recursos de processamento, memória e rede. Ideal para aplicações diversas, repositórios e servidores web básicos.

* **Otimizada para Computação (Compute Optimized):** Focada em processamento massivo e de alto desempenho. Ideal para servidores de jogos, codificação de vídeo e modelagem científica.

* **Otimizada para Memória (Memory Optimized):** Projetada para entregar desempenho rápido para cargas de trabalho que processam grandes volumes de dados na memória RAM (como bancos de dados relacionais e não-relacionais).

* **Computação Acelerada (Accelerated Computing):** Utiliza co-processadores de hardware (GPUs ou FPGAs) para acelerar o processamento de dados e gráficos. Ideal para Machine Learning e renderização 3D.

* **Otimizada para Armazenamento (Storage Optimized):** Projetada para aplicações que exigem acesso sequencial rápido de leitura e gravação em grandes conjuntos de dados locais (I/O intensivo).

---

### Provisionamento de Recursos e Formas de Interação

O provisionamento e o gerenciamento dos serviços na AWS ocorrem por meio de chamadas de API. Existem três métodos principais para interagir com essas APIs:

1. **Console de Gerenciamento AWS:** Interface web (gráfica) simples e intuitiva para gerenciar os recursos.

2. **AWS CLI (Command Line Interface):** Ferramenta de linha de comando que permite controlar os serviços por meio de scripts e comandos diretos, automatizando processos.

3. **AWS SDK (Software Development Kit):** Conjunto de ferramentas que possibilita a integração e o gerenciamento dos serviços AWS diretamente através de linguagens de programação (como Python, Java, JavaScript, etc.).

---

### Modelos de Precificação do EC2

* **Sob Demanda (On-Demand):** Pagamento por segundo ou hora de uso, sem compromisso de longo prazo ou pagamento adiantado. Ideal para cargas de trabalho de curto prazo e imprevisíveis.

* **Savings Plans:** Modelo de preço flexível que oferece economias significativas em troca de um compromisso de uso consistente (mensurado em $/hora) por um período de 1 ou 3 anos.

* **Instâncias Reservadas (Reserved Instances):** Proporcionam um desconto significativo em comparação às instâncias Sob Demanda, baseado em um compromisso estático de configuração e uso por 1 ou 3 anos. *(Nota: A AWS pode gerenciar a capacidade emprestando instâncias ociosas).*

* **Instâncias Spot (Spot Instances):** Permitem aproveitar a capacidade ociosa do EC2 com descontos massivos (de até 90%). Contudo, a AWS pode interromper a instância com um aviso prévio de 2 minutos caso precise da capacidade de volta.

* **Hosts Dedicados (Dedicated Hosts):** Servidores físicos totalmente dedicados ao uso exclusivo do cliente, permitindo utilizar licenças de software existentes (BYOL) e atender a requisitos estritos de conformidade corporativa.

* **Instâncias Dedicadas (Dedicated Instances):** Instâncias executadas em um hardware fisicamente isolado e de uso exclusivo, mas sem o controle total do servidor físico que o Host Dedicado oferece.

---

### Escalabilidade e Elasticidade

* **Escalabilidade:** A capacidade de um sistema de expandir sua estrutura para suportar o crescimento da demanda.
  
  * **Escala Vertical (Scale-up / Scale-down):** Adicionar ou remover recursos (como CPU ou RAM) em uma máquina existente.
  
  * **Escala Horizontal (Scale-out / Scale-in):** Adicionar novas máquinas (Scale-out) ou remover máquinas existentes (Scale-in) para distribuir o peso do sistema.

* **Elasticidade:** O ajuste dinâmico e automático do provisionamento de recursos, liberando-os ou contratando-os em tempo real para atender exatamente à demanda do momento.

#### Amazon EC2 Auto Scaling
Serviço que ajuda a garantir que você tenha o número correto de instâncias EC2 disponíveis para lidar com a carga da aplicação de forma elástica:

* **Escalonamento Dinâmico:** Ajusta a quantidade de instâncias em tempo real, reagindo imediatamente às mudanças na demanda (ex: pico de acessos).

* **Escalonamento Preditivo:** Utiliza algoritmos para prever e agendar o dimensionamento com base em padrões e demandas passadas.

---

### ELB (Elastic Load Balancing)

O ELB distribui automaticamente o tráfego de entrada de aplicações entre vários destinos, como instâncias EC2, contêineres e endereços IP.

* Atua como um **ponto centralizado de entrada** para todo o tráfego de rede da aplicação.

* Garante alta disponibilidade ao trabalhar em conjunto com o Auto Scaling para direcionar o tráfego apenas para instâncias saudáveis.

#### Métodos de Roteamento de Tráfego do ELB:

* **Round Robin:** Distribuição uniforme e circular das requisições entre as instâncias disponíveis.

* **Menor número de conexões:** Direciona o tráfego prioritariamente para a instância que estiver lidando com menos requisições no momento.

* **Hash de IP:** Utiliza o endereço IP do cliente para determinar qual instância receberá a requisição, garantindo que o usuário mantenha persistência de sessão no mesmo servidor.

* **Menor tempo de resposta:** Direciona a requisição para o servidor que apresentar a menor latência ou tempo de resposta mais rápido.

---

### Arquiteturas de Integração e Desacoplamento

A forma como os componentes de uma aplicação se comunicam dita a resiliência do sistema:

* **Aplicação Monolítica:** Arquitetura tradicional onde todos os componentes estão fortemente acoplados e interligados de forma unificada. Se um componente falha, todo o sistema pode cair.

* **Microsserviços:** Abordagem de arquitetura onde a aplicação é dividida em pequenos serviços independentes que se comunicam entre si. Permite o desacoplamento do sistema, onde a falha de um módulo não interrompe o funcionamento dos demais.

#### Serviços AWS para Desacoplamento e Eventos:

* **Amazon EventBridge:** Um barramento de eventos sem servidor (serverless) que conecta diferentes partes de uma aplicação utilizando eventos gerados por suas próprias aplicações, aplicações SaaS integradas ou serviços AWS.

* **Amazon SQS (Simple Queue Service):** Serviço de enfileiramento de mensagens gerenciado. Permite enviar, armazenar e receber mensagens entre componentes de software em qualquer volume, sem perder mensagens ou depender da disponibilidade imediata de outros serviços.

* **Amazon SNS (Simple Notification Service):** Opera com base no modelo de **Publicação/Assinatura (Pub/Sub)**. Permite que publicadores enviem mensagens e notificações para múltiplos assinantes ou endpoints (como e-mail, SMS, funções Lambda, ou filas SQS) por meio de canais centralizados (tópicos).

## Módulo 3: Compreensão dos Serviços Computacionais (AWS)

### Classificação dos Serviços de Nuvem

Antes de entender cada serviço, é crucial entender que na AWS os recursos computacionais são classificados de acordo com o nível de gerenciamento e controle da infraestrutura:

* **Serviços Não Gerenciados (Ex: Amazon EC2):** O cliente é o total responsável por configurar a infraestrutura lógica, aplicar patches de segurança, gerenciar atualizações do Sistema Operacional e cuidar do escalonamento manual.

* **Serviços Gerenciados:** A AWS reduz consideravelmente a carga de administração física e de infraestrutura.

* **Serviços Totalmente Gerenciados / Serverless (Ex: AWS Lambda):** O cliente não enxerga ou gerencia servidores. O foco passa a ser 100% voltado para a aplicação e o código, deixando o provisionamento, escalonamento e resiliência por conta da AWS.

---

### AWS Lambda (Computação Serverless)

O **AWS Lambda** é um serviço de computação orientado a eventos que executa códigos sem que você precise provisionar ou gerenciar servidores físicos ou virtuais.

* **Ciclo de Funcionamento:**
  
  1. O desenvolvedor faz o upload do código (Função Lambda).
  
  2. Define-se um gatilho (*trigger*) baseado em eventos (ex: um arquivo sendo enviado ao Amazon S3 ou uma alteração em banco de dados).
  
  3. O código roda exclusivamente em resposta ao evento acionado.

* **Runtime:** Define as configurações do ambiente de execução nativo fornecido para o código rodar com estabilidade.

* **Modelo de Cobrança:** Paga-se estritamente pelo tempo computacional consumido enquanto o código estiver rodando (medido em milissegundos). Se a função não for chamada, o custo é zero.

---

### Contêineres e Orquestração na AWS

Diferente das Máquinas Virtuais tradicionais (VMs), que necessitam de um hipervisor para rodar Sistemas Operacionais completos e isolados, os **Contêineres** compartilham o mesmo Kernel do S.O. do host hospedeiro. 
* *Vantagem:* Eles empacotam a aplicação com todas as dependências necessárias, sendo muito mais leves, portáveis e rápidos para iniciar do que instâncias EC2 tradicionais.

Para gerenciar o ciclo de vida de contêineres em larga escala, a AWS oferece os seguintes serviços:

| Serviço AWS | Função Principal | Objetivo de Exame |
| :--- | :--- | :--- |
| **Amazon ECS (Elastic Container Service)** | Orquestrador de Contêineres próprio da AWS | Rodar e escalar contêineres Docker de alta performance de forma integrada ao ecossistema AWS. |
| **Amazon EKS (Elastic Kubernetes Service)** | Orquestrador baseado em Kubernetes | Gerenciar e rodar contêineres na AWS utilizando a ferramenta open-source Kubernetes padrão de mercado. |
| **Amazon ECR (Elastic Container Registry)** | Registro de Imagens de Contêiner | Repositório totalmente gerenciado e seguro para armazenar e puxar imagens de contêineres. |
| **AWS Fargate** | Computação Serverless para Contêineres | Mecanismo que executa contêineres (tanto no ECS quanto no EKS) sem que você precise gerenciar ou provisionar instâncias EC2 por baixo. |

---

### Outros Serviços Computacionais Essenciais

* **AWS Elastic Beanstalk:** O serviço perfeito para desenvolvedores. Você faz o upload do seu código (Java, .NET, PHP, Node.js, Python, etc.) e o Beanstalk cuida automaticamente do provisionamento de infraestrutura, balanceamento de carga (ELB), Auto Scaling e monitoramento de saúde da aplicação.

* **AWS Batch:** Planejado para planejar e executar cargas de trabalho computacionais em lote (*batch computing*) de qualquer escala com eficiência.

* **Amazon Lightsail:** Oferece servidores virtuais privados (VPS), armazenamento e bancos de dados em pacotes simplificados de baixo custo mensal fixo. Ideal para sites simples ou ambientes de teste rápidos.

* **AWS Outposts:** Solução de nuvem **híbrida**. Permite que o cliente execute serviços nativos da AWS dentro do seu próprio data center local (on-premises).

---

## AWS Módulo 4: Alcance Global e Automação

### 1. Infraestrutura Global e Rede de Borda

A AWS distribui seus recursos globalmente para garantir baixa latência e alta resiliência para os usuários finais.

* **Locais de Borda (Edge Locations):** São pontos de presença que armazenam itens em **cache**, permitindo que os usuários passem a acessar o conteúdo de que precisam com a menor latência possível.

* **Rede Global de Borda (Amazon CloudFront):** Funciona como uma CDN (Content Delivery Network / Rede de Entrega de Conteúdo), oferecendo serviços e dados (cache) mais próximos dos clientes.

---

### 2. Considerações Cruciais ao Escolher Regiões AWS

A escolha de uma Região geográfica para implantar sua infraestrutura deve ser baseada em 4 fatores fundamentais:

1. **Conformidade:** Atendimento a requisitos regulatórios e leis de proteção de dados específicas de cada Região.

2. **Proximidade:** Escolha de Regiões próximas dos clientes para **minimizar o tempo** (latência) de resposta.

3. **Disponibilidade de Recursos:** Nem todas as Regiões têm exatamente os mesmos serviços disponíveis; eles variam para atender a requisitos regulamentares governamentais.

4. **Preço:** A localização geográfica e as regulamentações locais afetam diretamente os custos dos serviços.

---

### 3. Pilares de uma Arquitetura Altamente Disponível

Para construir sistemas robustos na nuvem, deve-se focar em três características essenciais:

* **Alta Disponibilidade:** Garantir que o sistema opere continuamente **sem falhar**.

* **Agilidade:** Capacidade de adaptação rápida às mudanças e demandas do mercado.

* **Elasticidade:** Habilidade de aumentar ou diminuir a infraestrutura conforme a flutuação da demanda.

---

### 4. Automação e Infraestrutura como Código (IaC)

Gerenciar servidores e redes manualmente não escala. A nuvem permite tratar infraestrutura como se fosse software.

* **AWS CloudFormation:** É um serviço que ajuda a modelar e configurar os recursos na AWS de forma automatizada. Ele permite definir toda a infraestrutura como código, garantindo uma configuração consistente para expansão.

* **IaC (Infrastructure as Code):** Funciona como um "banco de comandos" estruturado para automação e configuração de ambientes.

## AWS Módulo 5: Redes e Segurança de Tráfego

### 1. Amazon VPC (Virtual Private Cloud) e Componentes de Conectividade

A VPC funciona como uma rede virtual definida por você para executar seus recursos AWS de forma isolada e segura.

* **Sub-rede (Subnet):** Organiza os recursos dentro da VPC através de intervalos de endereços IP. Podem ser configuradas como:
  
  * **Públicas:** Acessíveis diretamente pela internet.
  
  * **Privadas:** Isoladas do acesso direto externo.

* **Benefícios Core:** Aumenta a segurança, economiza tempo e controla rigorosamente o acesso.

* **Gateways de Acesso:**
  
  * **Internet Gateway:** Fornece o ponto de acesso público para a internet.
  
  * **Gateway Privado (Virtual Private Gateway):** Cria um "funil" criptografado (**VPN**) para proteger o tráfego de dados corporativos.
  
  * **NAT Gateway (Conversão de Endereços de Rede):** Permite que instâncias em uma sub-rede privada se conectem a serviços fora da VPC (como atualizações de software), mas impede que a internet inicie conexões com elas.

---

### 2. Modelos de Conectividade Híbrida e Integração

A AWS oferece diferentes abordagens para integrar sua infraestrutura local (*on-premises*) ou conectar serviços de forma isolada:

| Serviço | Função Principal | Diferencial Técnico |
| :--- | :--- | :--- |
| **AWS Client VPN** | Conecta profissionais remotos e redes locais à nuvem. | Solução elástica e totalmente gerenciada. |
| **AWS Site-to-Site VPN** | Conecta filiais ou data centers locais à VPC. | Utiliza túneis criptografados via internet. |
| **AWS PrivateLink** | Conecta a VPC a serviços e recursos de forma estritamente privada. | O tráfego não expõe os dados à internet pública; age como se o serviço estivesse dentro da sua VPC. |
| **AWS Direct Connect** | Estabelece uma conexão física e privada dedicada entre a empresa e a AWS. | Ideal para **aplicações em tempo real** e **transferência de grandes volumes de dados** (evita a internet pública). |
| **AWS Transit Gateway** | Atua como um *hub* central de roteamento. | Conecta de forma simplificada múltiplas VPCs e redes *on-premises*. |

---

### 3. Segurança de Rede: ACLs vs. Grupos de Segurança (Security Groups)

Esta distinção é cobrada em praticamente todas as versões do exame. Ambos atuam como firewalls virtuais, mas em níveis e lógicas diferentes:

#### Network ACLs (NACLs)

* **Nível de Atuação:** Atua no nível da **sub-rede**.

* **Comportamento Padrão:** Libera tudo por padrão (entra e sai). Se personalizada, nada entra ou sai sem autorização explícita.

* **Mecânica (Stateless):** É **Sem Estado**. Ela não lembra das requisições; verifica o tráfego rigidamente tanto na entrada quanto na saída de forma independente.

#### Grupos de Segurança (Security Groups)

* **Nível de Atuação:** Atua no nível da **instância** (ex: EC2).

* **Comportamento Padrão:** Nega todo o tráfego de entrada e permite todo o tráfego de saída. Você define regras personalizadas para determinar quem pode entrar.

* **Mecânica (Stateful):** É **Com Estado**. Ele lembra as decisões anteriores tomadas para cada pacote recebido; se uma conexão de entrada for permitida, o tráfego de retorno correspondente sai automaticamente, ignorando regras de saída.

---

### 4. Roteamento Global, Performance e APIs

* **Amazon API Gateway:** Ferramenta desenvolvida para monitorar e proteger APIs em qualquer escala de acesso.

* **Amazon Route 53:** Serviço de DNS altamente confiável e econômico, projetado para rotear usuários finais para aplicações web globais.

* **Amazon CloudFront:** Serviço de rede de entrega de conteúdo (CDN) que otimiza a entrega armazenando cópias em cache nos Locais de Borda.

* **AWS Global Accelerator:** Otimiza a performance global usando roteamento inteligente de tráfego sobre a infraestrutura de rede da AWS, contando com **failover rápido** caso ocorra qualquer instabilidade.

---

### 🧠 Gatilhos de Prova para Fixação Rápida

* Falou em **"Firewall Stateless que atua na sub-rede"** $\rightarrow$ **Network ACL**.

* Falou em **"Firewall Stateful que protege a instância"** $\rightarrow$ **Security Group**.

* Pediu conexão dedicada de **alta velocidade, sem passar pela internet**, para **tempo real ou massa de dados** $\rightarrow$ **AWS Direct Connect**.

* Centralizar conexões de **centenas de VPCs e redes locais** em um único ponto $\rightarrow$ **AWS Transit Gateway**.

## AWS Módulo 6: Introdução ao Armazenamento

### 1. Tipos de Armazenamento de Dados

A AWS classifica seus serviços de armazenamento com base na estrutura de acesso e na persistência dos dados:

* **Armazenamento em Bloco:** Os dados são divididos em blocos puros. Podem ser criptografados, copiados por meio de *snapshots* e modificados dinamicamente durante o uso.
  
  * **Armazenamento de Instância EC2 (Instance Store):** Armazenamento temporário (efêmero) e **não gerenciado**, ideal para dados temporários, pois está fisicamente conectado ao host da instância.
  
  * **Amazon EBS (Elastic Block Store):** Armazenamento **gerenciado e persistente** em blocos. Funciona como discos rígidos externos, oferecendo desempenho consistente e baixa latência para workloads como bancos de dados (BD) e sistemas de arquivos na mesma AZ.

* **Armazenamento de Objeto (Amazon S3):** Altamente dimensionável e totalmente gerenciado. Trata os dados como objetos isolados dentro de contêineres conhecidos como **Buckets**. Permite armazenar e recuperar qualquer quantidade de dados de qualquer lugar.

* **Armazenamento de Arquivos:** Projetado para arquivos compartilhados que necessitam de **acesso simultâneo** por múltiplos clientes/instâncias.

---

### 2. Classes de Armazenamento do Amazon S3 e Ciclo de Vida

Para otimizar custos, o S3 oferece diferentes classes baseadas na frequência de acesso. O **Ciclo de Vida do S3** permite automatizar ações de transição entre essas classes ou a expiração (deleção) dos objetos.

| Classe de Armazenamento | Cenário de Uso Principal | Características Técnicas |
| :--- | :--- | :--- |
| **S3 Standard** | Uso geral (Padrão/Default). | Acesso frequente e imediato. |
| **S3 Intelligent-Tiering** | Dados com padrões de acesso desconhecidos. | Move os dados automaticamente entre 3 camadas (Frequente, Pouco Frequente e Instantâneo) para adequar os gastos. |
| **S3 Standard-IA** | Acesso menos frequente. | Exige acesso rápido quando necessário, mas com menor custo de armazenamento. |
| **S3 One Zone-IA** | Dados replicáveis de baixa frequência. | Armazena em uma **única AZ** para reduzir custos. |
| **S3 Express One Zone** | Workloads de altíssima performance. | Armazenado em uma única AZ com a maior velocidade de acesso a dados. |
| **S3 Glacier Instant Retrieval** | Arquivos de longa retenção raramente acessados. | Mesma velocidade do Standard-IA, mas com menor custo de armazenamento. |
| **S3 Glacier Flexible Retrieval** | Backups tradicionais de baixo custo. | Tempo de recuperação flexível. |
| **S3 Glacier Deep Archive** | Arquivamento de conformidade/regulamentação. | A classe mais barata de todas; para dados que você quase nunca usa, mas precisa manter. |
| **S3 Outposts** | Ambientes locais (*on-premises*). | Armazenamento de objetos nativo do S3 executado localmente. |

> 🔒 **Segurança no S3:** O controle de acesso é gerenciado pelas **Bucket Policies** (que especificam quais ações são permitidas ou negadas no Bucket e em seus objetos). A segurança também se apoia em **Identidade** (quem está autorizado) e **Criptografia** (em repouso, dentro do bucket, ou em trânsito, na comunicação fora do S3).

---

### 3. Armazenamento de Arquivos Avançado: EFS vs. FSx

* **Amazon EFS (Elastic File System):** Sistema de arquivos NFS totalmente gerenciado, projetado para suportar uma grande variedade de workloads. Pode ser acessado por **várias instâncias EC2 simultaneamente** em diferentes AZs e serviços de nuvem/on-premises. Você paga apenas pelo armazenamento utilizado.

* **Amazon FSx:** Reduz a complexidade de gerenciamento fornecendo os atributos e capacidades de sistemas de arquivos tradicionais e populares, eliminando planejamentos complexos. Suporta:
  
  * Windows File Server
  
  * NetApp ONTAP
  
  * OpenZFS
  
  * Lustre

---

### 4. Armazenamento Híbrido e Resiliência

* **AWS Storage Gateway:** Serviço que possibilita a **integração perfeita de ambientes locais (on-premises)** com o armazenamento em nuvem da AWS. É dividido em:
  
  * **Amazon S3 File Gateway:** Conecta diretamente o ambiente local ao Amazon S3.
  
  * **Volume Gateway:** Cria volumes de armazenamento virtual locais enquanto mantém o acesso e backup na nuvem.
  
  * **Tape Gateway:** Substitui fitas físicas por **fitas virtuais**, excelente para manter sistemas de backup em fita existentes.

* **AWS Elastic Disaster Recovery:** Simplifica e automatiza a réplica de workloads críticos (servidores físicos, virtuais ou em nuvem) para a AWS com o mínimo de tempo de inatividade, proporcionando:
  
  * Resiliência empresarial.
  
  * Recuperação de desastres eficiente.
  
  * Otimização de custos.


## AWS Módulo 7: Banco de Dados

### 1. Visão Geral e Bancos de Dados Relacionais (SQL)

Os bancos de dados relacionais organizam os dados em tabelas com linhas e colunas, utilizando a linguagem SQL (Structured Query Language). A AWS oferece suporte a mecanismos de BD populares para facilitar a migração e o gerenciamento.

* **Amazon RDS (Relational Database Service):** Serviço de banco de dados relacional totalmente gerenciado. Ele lida com tarefas rotineiras e complexas, otimizando custos, implantação, alta disponibilidade (Multi-AZ) e segurança.
  
  * **Facilidades:** Automatiza patches de segurança, backups e monitoramento de desempenho.
  
  * **Mecanismos suportados:** MySQL, PostgreSQL, MariaDB, Oracle e Microsoft SQL Server.

* **Amazon Aurora:** Banco de dados relacional da própria AWS, totalmente compatível com MySQL e PostgreSQL. É projetado para oferecer o desempenho e a disponibilidade de bancos comerciais de ponta com o custo de softwares de código aberto.
  
  * **Características Técnicas:** Oferece alto desempenho, tolerância a falhas e armazenamento auto-executável (redimensiona automaticamente conforme o uso). É altamente resiliente e consegue gerenciar o backup de forma automatizada e contínua.

---

### 2. Gerenciamento de Infraestrutura: Gerenciado (RDS) vs. Não Gerenciado (EC2)

Uma decisão arquitetural crítica na AWS é escolher o nível de controle sobre o banco de dados:

* **Solução Não Gerenciada (Banco no Amazon EC2):** Consiste em instalar o motor do banco de dados diretamente em uma instância virtual do EC2.
  
  * **Cenário de Uso Ideal:** Quando a empresa necessita de **controle total sobre o sistema operacional (acesso root)**, precisa aplicar configurações/plugins customizados e profundos, ou necessita rodar versões de software legadas/específicas que não são suportadas pelos serviços gerenciados da AWS.
  
  * **Responsabilidade:** Toda a manutenção (backups, patches, alta disponibilidade) fica a cargo do usuário.

* **Solução Gerenciada (Amazon RDS / Aurora):** A AWS assume a responsabilidade pela infraestrutura subjacente, atualizações do SO e rotinas de backup.
  
  * **Cenário de Uso Ideal:** Workloads padrão onde o foco principal é o desenvolvimento do negócio e a redução do overhead operacional.

---

### 3. Bancos de Dados Não Relacionais (NoSQL) e Especializados

Bancos de dados NoSQL são projetados para modelos de dados específicos e possuem esquemas flexíveis para construir aplicações modernas de alta performance.

* **Amazon DynamoDB:** Serviço de banco de dados NoSQL (Chave-Valor e Documental) totalmente gerenciado e *serverless*.
  
  * **Características Técnicas:** Oferece latência de milissegundo de dígito único em qualquer escala, replicação global automatizada e alta performance constante, tornando-o ideal para aplicações que exigem escalabilidade extrema.

* **Amazon DocumentDB:** Serviço de banco de dados documental rápido, escalável e totalmente gerenciado, projetado para lidar com dados semiestruturados.
  
  * **Características Técnicas:** Oferece compatibilidade com cargas de trabalho do **MongoDB**, permitindo iterar de forma rápida sem a necessidade de gerenciar esquemas predefinidos.

* **Amazon Neptune:** Banco de dados de **grafos** totalmente gerenciado e otimizado para armazenar e navegar por conjuntos de dados altamente conectados.
  
  * **Cenário de Uso Principal:** Redes sociais, motores de recomendação, deteção de fraudes e gráficos de conhecimento.

---

### 4. Serviços de Cache, Migração e Governaça de Dados

* **Serviços de Armazenamento em Cache (In-Memory Data Store):**
  
  * **Cache:** Reduz drasticamente a carga nos bancos de dados relacionais/não relacionais tradicionais ao armazenar dados frequentemente acessados na memória RAM.
  
  * **Amazon ElastiCache:** Serviço gerenciado compatível com Redis e Memcached. Deteta e substitui nós com falha de forma automática, garantindo alta velocidade de resposta para a aplicação.

* **AWS Database Migration Service (AWS DMS):** Serviço focado em resolver o problema de movimentação de dados para a nuvem de forma rápida e segura.
  
  * **Cenário de Uso Principal:** Permite migrar bancos de dados comerciais e de código aberto para a AWS com o **mínimo de tempo de inatividade (downtime)**, mantendo o banco de origem totalmente operacional durante o processo.
  
  * **Versatilidade:** Suporta migrações homogêneas (ex: Oracle para Oracle) e heterogêneas (ex: Oracle para Amazon Aurora ou DynamoDB), cobrindo estruturas relacionais, não relacionais e documentais.

* **AWS Backup:** Serviço centralizado e gerenciado para automatizar e consolidar a proteção de dados.
  
  * **Características Técnicas:** Torna o gerenciamento de cópias de segurança menos complexo ao oferecer suporte a vários tipos de armazenamento e serviços da AWS, permitindo configurar estratégias de backup globais e em total conformidade regulatória.
  
