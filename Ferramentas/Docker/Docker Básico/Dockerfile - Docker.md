---
tags:
  - Docker
---
---
#### O que é um Dockerfile?

- É um arquivo de texto que informa ao Docker como construir sua imagem. Ele lista todos os comandos Docker necessários para montar uma imagem de container. Usar um Dockerfile garante que suas imagens sejam construídas da mesma maneira todas as vezes, tornando seu trabalho mais consistente e fácil de gerenciar.

- Exemplo de um modelo simples de Dockerfile:

```
FROM ubuntu:latest  
WORKDIR /app  
COPY . .  
RUN apt-get update && apt-get install -y curl  
CMD ["curl", "https://www.exemplo.com"]
```

- **FROM ubuntu:latest** ‒ este comando puxa a imagem Ubuntu mais recente e a define como a camada base. As seguintes camadas serão construídas em cima disso.
- **WORKDIR /app** ‒ define o diretório de trabalho do container, criando uma nova camada que serve como contexto para os comandos subsequentes.
- **COPY . .** ‒ copia arquivos locais para a mesma pasta do container, criando uma camada adicional contendo os arquivos do seu projeto.
- **RUN apt-get update && apt-get install -y curl** ‒ o comando Docker **run** instala o [**cURL**](https://www.hostinger.com.br/tutoriais/comando-curl-linux) no container, adicionando uma nova camada para a lista de pacotes atualizada e o pacote cURL instalado.
- **CMD [“curl”, “https://www.exemplo.com”]** ‒ define o comando padrão para executar o aplicativo quando o container iniciar.