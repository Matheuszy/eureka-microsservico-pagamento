# Server

Serviço **Eureka Server** do projeto `codex.food`, responsável pelo registro e descoberta de serviços em uma arquitetura de microserviços.

## Tecnologias utilizadas

- Java 17
- Spring Boot 4.0.6
- Spring Cloud
- Spring Cloud Netflix Eureka Server
- Maven

## Funcionalidades

- Servidor de descoberta Eureka
- Registro centralizado de serviços
- Dashboard web do Eureka para visualização dos serviços conectados

## Estrutura do projeto

- `src/main/java/codex/food/server/ServerApplication.java`  
  Classe principal da aplicação.

- `src/main/resources/application.properties`  
  Configurações da aplicação, incluindo porta e parâmetros do Eureka.

## Pré-requisitos

Antes de executar o projeto, você precisa ter instalado:

- Java 17
- Maven 3.9+  
  ou usar o Maven Wrapper incluído no projeto (`mvnw` / `mvnw.cmd`)

## Configuração atual

A aplicação está configurada para subir na porta:

- `8081`

### Propriedades principais

```properties
server.port=8081
spring.application.name=server-historico
eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false
eureka.client.service-url.defaultZone=http://localhost:8081/eureka
```

Como executar
Windows PowerShell
```powershell
./mvnw spring-boot:run
```

Observações
Esta aplicação funciona como Eureka Server, portanto normalmente ela é usada como base para outros microserviços se registrarem

👨‍💻 Autor Desenvolvido por Matheus
