# Projeto: Infra Web Server no WSL

## Pré-requisitos

Antes de começar, você precisa ter os seguintes softwares instalados:

- **Windows Subsystem for Linux (WSL)** configurado com a distribuição **Ubuntu**.
- **Apache**: Para instalar o Apache, siga as instruções abaixo.

Este repositório tem como objetivo configurar um servidor web básico utilizando o Apache no WSL (Windows Subsystem for Linux), criando um ambiente de desenvolvimento para testar a configuração de servidores web.

## Tecnologias Utilizadas

- **Apache**: Servidor web de código aberto.
- **Ubuntu (WSL)**: Sistema operacional baseado em Linux no Windows Subsystem for Linux.
- **Bash Scripting**: Usado para automatizar a instalação e a configuração do Apache.
- **UFW (Firewall)**: Ferramenta de firewall para gerenciar a segurança do servidor.

## Passos para Configuração

1. **Instalação do Apache no Ubuntu (WSL)**:
    - Atualize o repositório de pacotes:
      ```bash
      sudo apt update
      ```
    - Instale o Apache:
      ```bash
      sudo apt install apache2
      ```
### Por que Apache?

O Apache é um dos servidores web mais utilizados no mundo. Ele é fácil de configurar, flexível e possui uma grande comunidade de suporte. Além disso, a sua compatibilidade com ambientes Linux e Windows (via WSL) torna-o uma excelente escolha para um ambiente de desenvolvimento local.

2. **Criação de um Arquivo HTML Simples**:
    - Crie um arquivo `index.html` na pasta `/var/www/html/`:
      ```bash
      echo "<html><body><h1>Servidor Web funcionando!</h1></body></html>" > /var/www/html/index.html
      ```

3. **Automatizando o Processo com `setup.sh`**:
    - Faça o download do arquivo `setup.sh` e execute-o:
      ```bash
      bash setup.sh
      ```

4. **Configuração de Virtual Host (Opcional)**:
    - Configure o Apache para rodar múltiplos sites locais com um Virtual Host. Exemplo:
      ```bash
      sudo nano /etc/apache2/sites-available/meu_site.conf
      ```

5. **Testar o Servidor Localmente**:
    - Acesse o servidor no seu navegador:
      ```
      http://localhost
      ```

6. **Segurança**:
    - Adicione uma camada de segurança configurando o **firewall UFW**:
      ```bash
      sudo ufw allow 'Apache'
      sudo ufw enable
      ```

## Conclusão

Este projeto serve como base para entender a configuração e manutenção de servidores web utilizando o Apache no WSL. Ele pode ser expandido para incluir integração com bancos de dados, automação de deploy e outras ferramentas de segurança.
