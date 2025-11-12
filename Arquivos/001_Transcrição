Laboratório AWS – Instância EC2 com Proteção contra Encerramento
📘 Descrição Geral

Neste laboratório, foi criada e configurada uma instância do Amazon EC2 com proteção contra encerramento habilitada. O objetivo principal foi compreender o ciclo de vida de uma instância EC2, incluindo implantação, monitoramento, configuração de rede, ajuste de tipo e volume, além do uso de grupos de segurança e scripts de inicialização (User Data) para automatizar a instalação de um servidor web.

🧩 Tarefa 1: Iniciar a Instância EC2
Objetivo

Implantar uma instância EC2 protegida contra encerramento acidental e configurada com um servidor web Apache via script de inicialização.

Etapas Realizadas

Nomeação da instância como Web Server (chave Name).

Utilização da AMI Amazon Linux 2023.

Seleção do tipo de instância t3.micro.

Definição da VPC Lab VPC.

Criação de um Security Group personalizado (“Web Server security group”) sem acesso SSH.

Habilitação da proteção contra encerramento.

Inclusão de um User Data Script para instalação automática do Apache:

#!/bin/bash
yum -y install httpd
systemctl enable httpd
systemctl start httpd
echo '<html><h1>Hello From Your Web Server!</h1></html>' > /var/www/html/index.html


O script instalou o servidor Apache, o habilitou na inicialização e criou uma página HTML simples com a mensagem “Hello From Your Web Server!”.

📊 Tarefa 2: Monitorar a Instância
Objetivo

Compreender o funcionamento das verificações automáticas e do monitoramento via CloudWatch.

Ações Realizadas

Acompanhamento das verificações de status: System reachability e Instance reachability.

Acesso à aba Monitoring, observando métricas básicas enviadas ao Amazon CloudWatch.

Utilização do recurso Get Instance Screenshot para visualizar o console virtual da instância.

🌐 Tarefa 3: Atualizar o Grupo de Segurança e Acessar o Servidor Web
Situação Inicial

O acesso HTTP à página não era possível, pois o Security Group bloqueava tráfego na porta 80.

Solução Aplicada

Adicionada regra de entrada para permitir:

Tipo: HTTP

Origem: IPv4 Anywhere (0.0.0.0/0)

Após atualização, o servidor web respondeu com sucesso à requisição exibindo a página:
“Hello From Your Web Server!”

⚙️ Tarefa 4: Redimensionar a Instância e o Volume EBS
Etapas

Parada da instância (estado “Stopped”).

Alteração do tipo de instância de t3.micro → t3.small, dobrando a memória.

Modificação do volume EBS de 8 GiB → 10 GiB.

Reinicialização da instância para aplicar as mudanças.

Resultado

A instância foi redimensionada com sucesso, garantindo maior capacidade de processamento e armazenamento.

🔒 Tarefa 5: Testar a Proteção contra Encerramento
Objetivo

Verificar o comportamento da instância ao tentar encerrá-la com a proteção ativada.

Resultado

Primeira tentativa de encerramento falhou (proteção ativa).

Após desativar a opção Termination Protection, foi possível encerrar a instância normalmente.

Confirmação de encerramento exibida no painel: “Ended AWS Lab Successfully”

🧠 Conceitos Aprendidos

Diferença entre AMIs, tipos de instância e volumes EBS.

Importância dos Security Groups como firewall virtual.

Uso de User Data para automação de configuração.

Monitoramento básico via CloudWatch.

Função da proteção contra encerramento para evitar exclusões acidentais.

Procedimentos para redimensionar instâncias e volumes conforme a demanda.

🧾 Resumo Técnico
Recurso	Configuração
AMI	Amazon Linux 2023
Tipo de Instância	t3.micro → t3.small
Volume EBS	8 GiB → 10 GiB
Security Group	HTTP (porta 80) liberado
Proteção contra Encerramento	Ativada (testada e desativada)
Script User Data	Instalação do Apache + página HTML
Monitoramento	CloudWatch básico (5 minutos)
🚀 Conclusão

O laboratório demonstrou de forma prática os principais fundamentos do Amazon EC2, desde a criação até o encerramento controlado de uma instância. Essa experiência reforça os conceitos de infraestrutura como serviço (IaaS), segurança e automação na nuvem AWS.
