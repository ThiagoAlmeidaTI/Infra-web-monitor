📡 Infra Web Monitor
Infra Web Monitor é um projeto prático de infraestrutura que tem como objetivo configurar um servidor web utilizando Apache dentro do Windows Subsystem for Linux (WSL) e implementar um sistema de monitoramento de acessos em tempo real com Python e SQLite. Ideal para quem busca automatizar a gestão de logs e entender os fundamentos de servidores web, segurança e análise de acessos.

🚀 Funcionalidades
🧰 Instalação automatizada do Apache, SQLite e dependências via script Bash.

🛡️ Ativação de autenticação básica no servidor Apache para proteção de acesso.

📑 Monitoramento de logs em tempo real usando Python.

🗃️ Registro dos acessos em um banco de dados SQLite, pronto para consultas SQL.

📊 Geração de estatísticas simples para análise de tráfego.

🧠 Objetivos de Aprendizado
Configurar e administrar um servidor web Linux/Apache.

Automatizar tarefas com Bash e Python.

Aplicar conceitos de Segurança da Informação com autenticação básica.

Gerenciar dados com SQLite e executar comandos SQL.

Ler e manipular arquivos de log (access.log) com Python.

📦 Tecnologias Utilizadas

Tecnologia	Descrição
Apache HTTP Server	Servidor web de código aberto (porta 80/443).
Ubuntu (WSL)	Subsistema Linux para Windows 10/11.
Python 3	Script para leitura e inserção dos logs no banco.
SQLite	Banco de dados local para registro de acessos.
Bash Script	Instalação e configuração automatizadas.
.htpasswd/.htaccess	Proteção por autenticação no Apache.

📋 Pré-requisitos
Antes de rodar o projeto, você precisa garantir:

✅ WSL com a distribuição Ubuntu instalada.

✅ Acesso root/sudo no Ubuntu (para instalar pacotes).

✅ Git instalado no Windows ou no WSL.

✅ Python 3 instalado no WSL.

✅ Permissão de execução (chmod +x) nos scripts do projeto.

⚙️ Instalação e Uso
git clone https://github.com/ThiagoAlmeidaTI/infra-web-monitor.git
cd infra-web-monitor
./setup.sh        # Instala Apache, SQLite e configura o ambiente
python3 monitor.py  # Inicia o monitoramento de logs e grava no banco

📈 Exemplo de Consulta SQL
SELECT ip_address, access_time, requested_url 
FROM access_logs 
ORDER BY access_time DESC 
LIMIT 10;

🔒 Segurança Implementada
Autenticação básica com .htpasswd e .htaccess

Monitoramento constante dos logs de acesso

Registro detalhado de IPs e tentativas de acesso

👨‍💻 Autor
Thiago Almeida dos Santos
📍 Duque de Caxias, RJ
📧 thiagoalmeida.work7@gmail.com
🔗 LinkedIn | GitHub




