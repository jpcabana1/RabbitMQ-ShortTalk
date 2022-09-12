# RabbitMQ 

## Info:
- **Docker Run:** docker run -d -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.10-management
- **RabbitMQ Management:** http://localhost:15672

## **Hello World**

### Setup
- dotnet new console --name Send
- mv Send/Program.cs Send/Send.cs
- dotnet new console --name Receive
- mv Receive/Program.cs Receive/Receive.cs
- cd Send
- dotnet add package RabbitMQ.Client
- cd ../Receive
- dotnet add package RabbitMQ.Client

### Start Send

- cd Send
- dotnet run

### Start Receive
- cd Receive
- dotnet run

## **Work Queues**

### Setup
- dotnet new console --name NewTask
- mv NewTask/Program.cs NewTask/NewTask.cs
- dotnet new console --name Worker
- mv Worker/Program.cs Worker/Worker.cs
- cd NewTask
- dotnet add package RabbitMQ.Client
- cd ../Worker
- dotnet add package RabbitMQ.Client