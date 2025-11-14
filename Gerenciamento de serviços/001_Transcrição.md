# 🧩 AWS Lab – Gerenciamento de Serviços e Monitoramento

## 📘 Visão Geral
Este laboratório teve como objetivo compreender e aplicar técnicas de **monitoramento de serviços e instâncias Linux** no ambiente **Amazon EC2**, utilizando tanto **ferramentas do sistema operacional (CLI)** quanto **serviços de observabilidade da AWS (CloudWatch)**.

Durante as etapas, foi monitorado o **serviço httpd (Apache Web Server)**, simulada uma carga de trabalho no sistema com o **script stress.sh**, e analisadas as métricas resultantes através do **AWS CloudWatch Dashboard**.

---

## 🎯 Objetivos do Laboratório
- Verificar o status do serviço **httpd** (Apache) e garantir seu funcionamento.  
- Monitorar o desempenho da instância EC2 usando o comando **top**.  
- Utilizar o **AWS CloudWatch** para observar métricas do sistema (CPU, disco, rede).  

---

## ⚙️ Tarefa 1 – Verificar o Status do Serviço httpd

### 🧩 Comandos Utilizados

```bash
sudo systemctl status httpd.service
