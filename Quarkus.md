
## Quarkus Reactive

**Definição**  
É o suporte reativo do framework Quarkus, voltado a aplicações Java nativas para nuvem (GraalVM), com APIs não bloqueantes e alto desempenho.

**Principais tecnologias e bibliotecas**

- **Mutiny**: API reativa do Quarkus, simples e _type-safe_.
    
- **Vert.x**: infraestrutura de I/O não bloqueante por baixo do capô.
    
- **Reactive SQL Client**: `PgClient`, `MySQLPool` reativos.
    
- **RESTEasy Reactive**: extensões para criar endpoints REST reativos.
    
- **Reactive Messaging**: integração com Kafka, AMQP, usando _channels_ baseados em Mutiny.