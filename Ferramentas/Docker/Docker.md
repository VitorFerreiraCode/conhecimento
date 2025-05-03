---
tags:
  - Docker
---

#### Conceito de Docker

- É um [[Software]] de código aberto open-source utilizado para implantar aplicativos dentro de containers virtuais. A conteinerização permite que vários aplicativos funcionem em diferentes ambientes complexos.

#### Conceitos Importantes de Docker

1. [[Container - Docker]]
2. [[Imagem - Docker]]
#### Docker vs Máquina Virtual

- Em resumo, os containers do Docker compartilham o mesmo sistema operacional do host, enquanto as máquinas virtuais têm um sistema operacional convidado sendo executado no sistema host.

|                              |                               Docker                                |              Máquina Virtual               |
| :--------------------------: | :-----------------------------------------------------------------: | :----------------------------------------: |
|              SO              |   [[Sistemas Operacionais \| SO]] compartilhado entre containers.   | Novo SO para cada [[Máquina Virtual\|MV]]. |
|          Segurança           | Menos seguro porque o SO e o [[Kernel\|kernel]] são compartilhados. |  Mais seguro, pois não compartilham o SO.  |
|          Desempenho          |           Desempenho rápido mesmo com vários containers.            |          Exige muito [[Hardware]]          |
|    Tempo de Inicialização    |                         Rápido (segundos).                          |              Lento (minutos).              |
|    Necessidade de memória    |                                Leve.                                |           Requer muita memória.            |
| Necessidade de armazenamento |                        Geralmente megabytes.                        |         Geralmente gigabytes.<br>          |
|        Portabilidade         |             Fácil de implantar em diferentes ambientes.             | Difícil portar uma MV para outro sistema.  |

#### Docker Swarm vs Kubernetes

- Em resumo, Docker é responsável pela criação de containers e o Kubernetes os gerencia em grande escala.
- Entretanto o Docker possui seu próprio sistema de orquestração chamado Docker Swarm.

|                        |                       Docker Swarm                        |                Kubernetes                |
| :--------------------: | :-------------------------------------------------------: | :--------------------------------------: |
|       Instalação       |                      Fácil e rápida.                      |             Difícil e longa.             |
|     Escalabilidade     |                    Não oferece escala.                    |        Escalonamento automático.         |
|   Criação de cluster   |                         Díficil.                          |                  Fácil.                  |
| Balanceamento de carga |                        Automático.                        |                 Manual.                  |
|     Monitoramento      | Suporta apenas ferramentas de monitoramento de terceiros. | Ferramentas de monitoramento integradas. |
