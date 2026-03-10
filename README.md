# Agendador de Horários API

API REST desenvolvida em Java com Spring Boot para gerenciamento de agendamentos de serviços.

A aplicação permite:

* Criar agendamentos
* Consultar agendamentos por dia
* Atualizar agendamentos
* Remover agendamentos
* Evitar conflitos de horários

O sistema possui validação para evitar conflito de horários.

Caso já exista um agendamento para o mesmo serviço dentro do mesmo intervalo de tempo, o sistema impede a criação e retorna erro:

``` Horário já está preenchido. Tente outro! ```

Tecnologias Utilizadas: 

* Java
* Spring Boot
* Spring Data JPA
* Lombok
* H2 Database
* Maven
* Postman (testes da API)

Como executar o projeto

1️⃣ Clonar o repositório

```git clone https://github.com/evellyncsl/agendador-horarios.git```

2️⃣ Entrar na pasta do projeto

```cd agendador-horarios```

3️⃣ Executar o projeto

```mvn spring-boot:run```

A aplicação estará disponível em:

```http://localhost:8080```

Testando com Postman

1. Execute a aplicação

2. Abra o Postman

3. Utilize a URL:

```http://localhost:8080/agendamentos```

📡 Endpoints da API

Criar Agendamento

Body:

```
{
  "servico": "Unhas",
  "profissional": "Manicure",
  "dataHoraAgendamento": "2026-03-09T10:00",
  "cliente": "Evellyn",
  "telefoneCliente": "994008675"
}
```

Buscar Agendamentos por Dia

GET:

```/agendamentos?data=2026-03-09```

Retorna todos os agendamentos do dia informado.

Alterar Agendamento

PUT

```/agendamentos?cliente=Evellyn&dataHoraAgendamento=2026-03-09T10:00```

Remover Agendamento

DELETE

```/agendamentos?cliente=Evellyn&dataHoraAgendamento=2026-03-09T10:00```

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

💻 Projeto desenvolvido para fins de aprendizado em Java e Spring Boot.


