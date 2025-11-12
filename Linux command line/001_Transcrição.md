# 🧮 AWS Lab – Linha de Comando do Linux

Este laboratório consolidou as noções fundamentais do ambiente de linha de comando Linux, explorando comandos essenciais e práticas que aumentam a eficiência operacional e familiaridade com o terminal.

O domínio desses comandos é o primeiro passo para administrar servidores EC2, automatizar tarefas e compreender o comportamento interno do Linux.


## 📘 Visão Geral
Este laboratório teve como objetivo introduzir o uso prático de **comandos básicos do Linux** em uma instância **Amazon Linux EC2**, reforçando a familiaridade com o **terminal bash**, o **histórico de comandos** e as **ferramentas nativas de sistema**.

Ao longo das atividades, foram explorados comandos essenciais para identificar o usuário, hostname, tempo de atividade do sistema, fuso horário, exibição de calendários e manipulação de histórico — consolidando a base para a administração de sistemas Linux em ambiente de nuvem.

---

## 🎯 Objetivos do Laboratório

Após a conclusão deste laboratório, você foi capaz de:

- Executar comandos para obter informações do sistema e da sessão atual.  
- Pesquisar e reutilizar comandos executados anteriormente.  
- Manipular o histórico de comandos (`history`, `!!`, `Ctrl + R`).  
- Explorar opções de data, hora e calendário.  
- Reforçar a prática de navegação e automação em shell bash.

---

## ⚙️ Tarefa 1 – Executar Comandos para Obter Informações do Sistema

### 🧩 Comandos Utilizados

| Comando | Função |
|----------|--------|
| `whoami` | Exibe o nome do usuário atual. |
| `hostname -s` | Mostra o nome abreviado do host (máquina). |
| `uptime -p` | Mostra há quanto tempo o sistema está ativo. |
| `who -H -a` | Lista usuários conectados e informações adicionais (linha, PID, hora, etc.). |
| `TZ=America/New_York date` / `TZ=America/Los_Angeles date` | Mostra a data e hora para diferentes fusos horários. |
| `cal -j` | Exibe o calendário do mês atual com datas no formato juliano. |
| `cal -s` / `cal -m` | Mostra o calendário com diferentes layouts (domingo ou segunda como primeiro dia). |
| `id ec2-user` | Exibe IDs de usuário, grupos e permissões do usuário atual. |

---

## 📅 Exemplos de Saída

```bash
whoami
# Saída: ec2-user

hostname -s
# Saída: ip-10-0-0-123

uptime -p
# Saída: up 2 hours, 14 minutes

TZ=America/New_York date
# Saída: Wed Sep 1 21:27:35 EDT 2021


