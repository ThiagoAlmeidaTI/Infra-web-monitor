# Projeto: Infra Web Server no WSL

Este repositório tem como objetivo configurar um servidor web básico utilizando o Apache no WSL (Windows Subsystem for Linux), criando um ambiente de desenvolvimento para testar a configuração de servidores web.

## Passos para Configuração:

1. **Instalação do Apache no Ubuntu (WSL)**:
    - Atualize o repositório de pacotes:
      ```bash
      sudo apt update
      ```
    - Instale o Apache:
      ```bash
      sudo apt install apache2
      ```

2. **Criação de um Arquivo HTML Simples**:
    - Crie um arquivo `index.html` na pasta `/var/www/html/`:
      ```bash
      echo "<html><body><h1>Servidor Web funcionando!</h1></body></html>" > /var/www/html/index.html
      ```

3. **Testar o Servidor Localmente**:
    - Acesse o servidor no seu navegador:
      ```
      http://localhost
      ```

4. **Configuração Adicional (Opcional)**:
    - Se desejar configurar o Apache para iniciar automaticamente ao iniciar o WSL, você pode adicionar comandos personalizados de inicialização.

## Tecnologias Utilizadas

- **Apache** como servidor web
- **Ubuntu** no WSL
