---
tags:
  - Docker
---

### Conceito de Docker Compose

- Docker Compose é o orquestrador de containers do Docker.
- O comportamento do Docker será regido através do docker-compose, semelhante ao [[Dockerfile - Docker|dockerfile]], escrito em YAML.
- Executar funções no Docker também podem exigir que as aplicações utilizem mais de um container, então às vezes é necessário criar banco de dados, com cache, Redis, etc. E para lidar com isso, o Docker Compose é uma solução multi-container que utiliza um arquivo declarativo para definir os serviços que você quer rodar, sendo que cada serviço é basicamente um container que você pode executar.

#### docker-compose

- Nesse arquivo, descreve-se a infraestrutura como código e diz como ela deverá se comportar ao ser iniciado.