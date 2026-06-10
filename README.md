# Estudos AWS Cloud Practitioner Essentials

Repositório dedicado a documentação de conceitos, anotações de módulos e laboratórios práticos para a certificação AWS Cloud Practitioner.

---

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

### Arquiteturas de Integração e Desacoplamento (Mensageria)

A forma como os componentes de uma aplicação se comunicam dita a resiliência do sistema:

* **Aplicação Monolítica:** Arquitetura tradicional onde todos os componentes estão fortemente acoplados e interligados de forma unificada. Se um componente falha, todo o sistema pode cair.

* **Microsserviços:** Abordagem de arquitetura onde a aplicação é dividida em pequenos serviços independentes que se comunicam entre si. Permite o desacoplamento do sistema, onde a falha de um módulo não interrompe o funcionamento dos demais.

#### Serviços AWS para Desacoplamento e Eventos:

* **Amazon EventBridge:** Um barramento de eventos sem servidor (serverless) que conecta diferentes partes de uma aplicação utilizando eventos gerados por suas próprias aplicações, aplicações SaaS integradas ou serviços AWS.

* **Amazon SQS (Simple Queue Service):** Serviço de enfileiramento de mensagens gerenciado. Permite enviar, armazenar e receber mensagens entre componentes de software em qualquer volume, sem perder mensagens ou depender da disponibilidade imediata de outros serviços.

* **Amazon SNS (Simple Notification Service):** Opera com base no modelo de **Publicação/Assinatura (Pub/Sub)**. Permite que publicadores enviem mensagens e notificações para múltiplos assinantes ou endpoints (como e-mail, SMS, funções Lambda, ou filas SQS) por meio de canais centralizados (tópicos).