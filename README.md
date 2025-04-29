# 📡 Infra Web Monitor

**Infra Web Monitor** é um projeto prático de infraestrutura que configura um servidor web Apache dentro do WSL (Windows Subsystem for Linux) e implementa um sistema de **monitoramento de acessos em tempo real** com **Python** e **SQLite**.

> Ideal para quem deseja entender fundamentos de servidores web, segurança da informação, automação com scripts e análise de logs.

---

## 🚀 Funcionalidades

- 🧰 Instalação automatizada do Apache, SQLite e dependências via script Bash.
- 🛡️ Ativação de autenticação básica com `.htpasswd` e `.htaccess`.
- 📑 Monitoramento de logs de acesso em tempo real com Python.
- 🗃️ Registro de IPs, horários e URLs acessadas no banco de dados SQLite.
- 📊 Geração de estatísticas básicas para análise de tráfego web.

---

## 🎯 Objetivos de Aprendizado

- Configurar e administrar um servidor web Linux (Apache).
- Automatizar tarefas com scripts em Bash e Python.
- Aplicar práticas de segurança básicas com autenticação HTTP.
- Gerenciar dados com SQLite e executar comandos SQL.
- Ler e manipular arquivos de log (`access.log`) com Python.

---

## 📦 Tecnologias Utilizadas

| Ferramenta      | Função                                               |
|-----------------|------------------------------------------------------|
| **Ubuntu (WSL)* | Backend Linux rodando dentro do Windows              |
| **Apache2**     | Servidor web para gerar os logs                      |
| **SQLite3**     | Banco local para registrar acessos                   |
| **Python 3**    | Script para capturar e inserir os logs               |
| **Bash**        | Automatização da instalação e configuração           |
| **VS Code**     | Editor principal, acessando o WSL via extensão       |

---

## 📋 Pré-requisitos

Antes de rodar o projeto, certifique-se de ter:

- ✅ WSL com Ubuntu instalado
- ✅ Acesso root/sudo no Ubuntu (para instalar pacotes)
- ✅ Git instalado (Windows ou WSL)
- ✅ Python 3 instalado no WSL
- ✅ Permissão de execução nos scripts (`chmod +x setup.sh`)

---

## ⚙️ Instalação e Execução

```bash
# Clone o repositório
git clone https://github.com/ThiagoAlmeidaTI/infra-web-monitor.git

# Acesse o diretório do projeto
cd infra-web-monitor

# Execute o script de instalação
./setup.sh

# Inicie o monitoramento de logs
python3 monitor.py 
```

📈 Exemplo de Consulta SQL

SELECT ip_address, access_time, requested_url 
FROM access_logs 
ORDER BY access_time DESC 
LIMIT 10;

🔒 Segurança Implementada

Autenticação básica via .htpasswd e .htaccess
Monitoramento constante dos logs de acesso
Registro de IPs e tentativas de acesso
Código Python legível e modular para análise de segurança

👨‍💻 Autor
Thiago Almeida dos Santos
📍 Duque de Caxias, RJ
📧 thiagoalmeida.work7@gmail.com
🔗 LinkedIn | GitHub

