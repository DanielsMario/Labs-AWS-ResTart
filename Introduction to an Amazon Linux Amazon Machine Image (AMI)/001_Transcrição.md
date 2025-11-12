Este laboratório introduz os primeiros passos na administração de sistemas Linux em instâncias EC2, destacando a importância da documentação embutida (man pages) e do acesso seguro via SSH.

Esses conceitos são a base para o trabalho futuro com EC2, AMI, CLI da AWS e automação de servidores

# 🐧 AWS Lab – Introdução a uma Imagem de Máquina da Amazon (AMI) no Amazon Linux

## 📘 Visão Geral
Este laboratório teve como objetivo apresentar a **utilização prática de uma AMI (Amazon Machine Image)** no **Amazon Linux**, reforçando o uso da **interface de linha de comando (CLI)** e introduzindo conceitos fundamentais de administração em sistemas Linux via **SSH**.

Durante o processo, foi realizado o acesso remoto a uma instância EC2 por meio do **Secure Shell (SSH)**, a exploração do sistema de ajuda do Linux (as **man pages**) e a análise das principais seções que compõem a documentação dos comandos.

---

## 🧠 Cenário
O laboratório simulou o acesso a uma instância **Amazon Linux** em execução dentro da infraestrutura da AWS (Vocareum Labs).  
A conexão foi feita via **SSH**, e o ambiente foi usado para explorar os **comandos man** e entender como consultar a documentação interna do Linux.

### Componentes do ambiente
- **Amazon EC2 (Host de comando)** — instância Linux na sub-rede pública.  
- **Amazon VPC** — rede virtual utilizada para hospedagem da instância.  
- **Sub-rede pública** — camada de rede onde a instância pôde ser acessada via SSH.

---

## 🚀 Tarefa 1 – Acessar a Instância Amazon Linux via SSH

### 🎯 Objetivo
Conectar-se à instância EC2 do Amazon Linux utilizando um **par de chaves** e o protocolo **SSH**, simulando o processo real de administração remota em nuvem.

---

### 💻 Usuários Windows
1. Baixar o arquivo de chave privada `labsuser.ppk`.  
2. Anotar o **endereço IP público (PublicIP)** da instância.  
3. Utilizar o **PuTTY** para configurar e realizar a conexão SSH.  
4. Autenticação via chave privada (sem necessidade de senha).

