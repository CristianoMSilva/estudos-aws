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