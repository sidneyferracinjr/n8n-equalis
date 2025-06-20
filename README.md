# n8n-equalis

Este repositório contém a infraestrutura e configurações necessárias para executar o [n8n](https://n8n.io/), uma plataforma de automação de workflows, utilizando Docker e Caddy como proxy reverso.

## Estrutura do Projeto

- `n8n-docker-caddy/`
  - `compose.yaml`: Arquivo de configuração do Docker Compose para orquestrar os containers do n8n e do Caddy.
  - `caddy_config/Caddyfile`: Arquivo de configuração do Caddy para gerenciamento de proxy reverso, HTTPS e domínios personalizados.
  - `local_files/`: Diretório para arquivos locais e persistência de dados.

## Como usar

1. **Pré-requisitos**
   - [Docker](https://www.docker.com/get-started) e [Docker Compose](https://docs.docker.com/compose/) instalados.
   - (Opcional) Domínio configurado para uso com Caddy.

2. **Configuração**
   - Edite o arquivo `n8n-docker-caddy/caddy_config/Caddyfile` conforme necessário para seu domínio e ambiente.
   - Adapte variáveis de ambiente no `compose.yaml` se necessário.

3. **Subindo os containers**
   ```powershell
   cd n8n-docker-caddy
   docker compose up -d
   ```

4. **Acessando o n8n**
   - O serviço estará disponível no domínio configurado ou em `localhost` na porta definida.

## Personalização

- Adicione arquivos personalizados em `n8n-docker-caddy/local_files/` para persistência ou customização.
- Modifique o `Caddyfile` para ajustar regras de proxy, HTTPS, redirecionamentos, etc.

## Licença

Este projeto está licenciado sob os termos do arquivo [LICENSE](LICENSE).

---

> Projeto mantido por [Equalis](https://equalis.com.br)