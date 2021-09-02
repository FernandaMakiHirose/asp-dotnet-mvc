# Criando e testando uma aplicação ASP.NET API e publicando na Cloud
## Pré-requisitos
- Lógica de programação
- Introdução ao .NET
- Visual Studio

## Rodar o projeto
- Visual Studio
- Clique duas vezes no arquivo `CursoMVC.sln`
- Clique com o botão direito da solução do projeto > Propriedades > Projeto de inicialização > Vários projetos de inicialização (✅) > Adicione a opção `Iniciar` para ambos > Aplicar > Ok
- Por fim, clique em `Iniciar`
- Execute o projeto na IDE

## Como criei o projeto?
- Visual Studio
- API
- ASP.NET Core 3.0
- Aplicativo Web (Modelo-Exibição-Controlador)
- Sem autenticação
- Configurar para HTTPS (Sim)
- Habilitar suporte ao Docker (Não)

## Quais pacotes usei?
- Clique com o botão direito na aplicação > Gerenciar Pacotes do NuGet
- Pacotes adicionados: Swashbuckle.AspNetCore

## Como configurei o Swagger?
- Clique com o botão direito no projeto > Propriedades > Compilar > Arquivo de documentação XML (✅) 
- Clique com o botão direito no projeto > Propriedades > Depurar > Iniciar navegador > Digite: swagger

## Entendendo o código 
`Startup.cs`: habilita o Swagger, adiciona os Middlewares. Após adicioná-los fiz o build.

## O que é API?
A sigla API em português significa "interface de programação de aplicações". As APIs sãouma forma de realizar a integração entre sistemas mesmo que esses possuam linguagens de programação diferente. Um exemplo de API é o Google Maps que é utilizado por empresas de Hotel em que é disponibilizada dentro do site da empresa a localização em que ele fica. 

## O que é REST?
É um conjunto de princípios que quando aplicados de maneira correta em uma aplicação, a beneficia como a arquitetura e padrões da própria web. Uma aplicação que é capaz de aplicar tais princípios é chamada de RESTful.

## Swagger
Quando é preciso consumir uma API existente é necessário conhecer as funcionalidades disponíveis e detalhes de como consumir tal funcionalidade. Diante dessa necessidade existe o Swagger que é um projeto composto por algumas ferramentas para auxiliar o desenvolvedor de API em algumas tarefas como por exemplo a documentação da API.
