# Desenvolvimento de aplicações com .NET
## Requisitos
- Visual Studio
- Cada pasta apresenta uma documentação, clique em uma delas para ver 
- C#

## Publicação na nuvem
Caso esteja usando uma versão acima do .NET Core 3.0.0:
>dotnet tool install --global dotnet-ef --version 3.0.0

Clique com o botão direito no projeto `CursoMVC` > Publicar > Criar Novo > Você pode dar um nome para o `Nome` e `Grupo de recursos` > Criar um Banco de Dados SQL (Preencha os dados) > Criar > Editar > Use essa cadeia de conexão no tempo de execução ✅ > Aplicar essa migração ao publicar ✅ > Salvar > Publicar 

Fiz o mesmo processo para `CursoAPI`, porém não criei um banco de dados, apenas clique em `Adicionar`, a qual fez a conexão do projeto com o banco de dados já existente

## Quiz
### Quais são as vantagens da Cloud?
É a entrega da computação como serviço ao invés de um produto, permitindo que o serviço seja acessado através de qualquer dispositivo com internet.

### O que é Mock?
São objetos que imitam o comportamento de objetos reais.

### Quais são as várias abordagens para modelagem de domínio no Entity Framework?
Database First, Model First e Code First.

### Qual é a diferença entre MVC e Web Forms?
No MVC as requisições do navegador são enviados a ações da controller enquanto no Web Forms cada requisição é enviada para uma página que deve existir fisicamente.

### Quais são as vantagens da Web API?
Criar serviços usando recursos HTTP.

### O que é o Entity Framework?
ORM que permite que os desenvolvedores de .NET trabalhem com um banco de dados usando objetos .NET.

### O que é o arquivo Startup.cs?
É o responsável por ser o ponto inicial do projeto.

### Quais são as vantagens de utilizar Unit Tests?
Encontrar problemas nos estágios iniciais do desenvolvimento e aumentar a confiança na manutenção do código.

### O que é Azure?
É um conjunto de serviços de nuvem da Microsoft.

### Quais são os principais HTTP Verbs?
GET, POST, PUT, PATCH E DELETE
