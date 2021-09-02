# Conheça o Entity Framework e crie aplicações ASP.NET
## Pré-requisitos
- Lógica de programação
- Introdução ao .NET

## Guia
Abra o Visual Studio > Ferramentas > Gerenciador de Pacotes do NuGet > Console do Gerenciador de Pacotes e digite:
>update-database

- Execute o projeto
- Dica extra: Caso queira ver o banco de dados e tabelas criados instale o `SQL Server Management Studio (SSMS)`, no arquivo `` adicione o nome do servidor.

## Criando o projeto
- Visual Studio
- Aplicativo Web ASP.NET (Core) 
- ASP.NET Core 3.0
- Aplicativo Web (Modelo-Exibição-Controlador)
- Sem autenticação
- Configurar para HTTPS (Sim)
- Habilitar suporte ao Docker (Não)

## Criar um Controller
- Visual Studio
- Clique com o botão direito na pasta Controller > Adicionar > Novo item com scaffold > Controlador MVC com exibições, usando o Entity Framework.
- Selecione `classe de modelo` e a `classe de contexto de dados`
- Gerar modos de exibição (Sim)
- Bibliotecas de scripts de referência (Sim)
- Use uma página de layout (Sim)
- Dê o nome da Controller

## Entendendo o código
`Context.cs`: configura o Entity Framework. <br> 
`Startup.cs`: adicione o código `services.AddDbContext<Context>(options => options.UseSqlServer(connection));` que disponibiliza o uso o context. <br>
`Migrations`: são as migrations criadas com o comando de criá-la. <br>
`ProdutosController.cs`: na linha 50 adicionou a `Descricao` que por default vem como `Id` <br>
`Produtos`: nos arquivos dessa pasta, substituiu o `Id` por `Descricao` <br>
`Produto.cs`: apresenta displays para mostrar o nome `Descrição` ao mostrar esse dado e validações <br>

## Pacotes e comandos executados durante o projeto via terminal
Primeiro pacote:
>Install-Package Microsoft.EntityFrameworkCore.SqlServer 

Segundo pacote:
>Install-Package Microsoft.EntityFrameworkCore.Tools

Cria uma Migration:
>Add-Migration NomeDaTabela

Logo após criar uma Migration, crie um Database:
>Update-Database

## Dica 
- Ao digital `prop` em um arquivo Model, as propriedades são criadas e com o `tab` do seu teclado, é possível preencher os dados dos atributos

## Entity Framework
É um ORM (Mapeador Relacional de Objeto) que permite os desenvolvedores de .NET trabalharem com um banco de dados usando objetos .NET. Elimina a necessidade da maioria do código de acesso a dados que os desenvolvedores geralmente precisam gravar.

## Linhas de utilização
O Entity Framework possui três linhas principais de utilização:
- Database First
- Model First
- Code First

## Database First
Em diversos casos nos deparamos com situações em que o banco de dados foi criado antes de iniciar aplicação, isso é muito comum em equipes mais acostumadas com modelo relacional do que com o modelo orientado a objetos. Diante desse cenário é normal optar pela utilização Database First  que tem como objetivo ler o banco de dados e aplicar uma engenharia reversa carregando as classes que representarão as tabelas do banco.

## Model First
O Model First nos permite gerar primeiro modelo e a partir dele gerar nossa base de dados, essa montagem de modelo é feita através do EDM Designer,utilizando os componentes que ele nos disponibiliza sendo as mais comuns “Entity” e “Association”.

## Code First
Primeiro cria as classes de entidade e deixa para o Entity Framework a responsabilidade de criar o banco de dados. Essas classes são conhecidas como classes POCO (Plan Old CLR Objects) que são classes que utilizam apenas os tipos do .NET Framework sendo independentes de qualquer outro framework inclusive do "Entity", essas classes podem ser utilizadas por outros projetos que utilizem ou não o Entity Framework.

## Data Annotations
É um recurso que permite adicionar atributos e métodos nas classes para alterar convenções padrão e personalizar alguns comportamentos.

## Principais atributos
- Required: Significa campo obrigatório
- RegularExpression: Valida o campo por expressão regular
- Display: Nome a ser mostrado em todas as interfaces do usuário
- StringLength: Determina a quantidade máxima de caracteres que poderá ser informada
- MinLength: Determina a quantidade mínima de caracteres que poderá ser informada
- DisplayFormat: Formato a ser exibido nas interfaces do usuário
- Range: Define a faixa de dados aceita pela propriedade

## Migrations
É um recurso que oferece uma maneira de atualizar de forma incremental o esquema de banco de dados para manter a sincronia com o modelo de classe do seu projeto preservando os dados existentes no banco de dados. Também é possível realizar o downgrade caso você deseje voltar o seu banco de dados para a versão anterior em que se encontrava, além de manter um histórico de alterações. Antes do Entity Framework contar com suporte ao Migrations existia apenas três estratégias para criação de banco de dados, quais sejam:
- CreateDatabaseIfNotExists
- DropCreateDatabaseAlways
- DropCreateDatabaseIfModelChanges

## CreateDatabaseIfNotExists
O Entity Framework cria o banco de dados se ele não existir, ou seja, se você estiver utilizando essa estratégia e realizar uma alteração no seu modelo de classes você teria que remover o seu banco de dados e criá-lo novamente, perdendo todos os dados.

## Razor
É uma View Engine utilizada no ASP.NET MVC. O seu principal objetivo é simplificar o desenvolvimento de aplicações ASP.NET, pois ele deixa o código mais simples, fácil e legível.

## ConfigureServices
É responsável por registrar as classes ao container de injeção de dependência, após isso a classe poderá ser usada em qualquer lugar da aplicação desde que seja incluída no construtor da classe em que deseja usar.

## Sobre a Autora
Oi, eu sou a Fernanda! Estou aqui para contribuir com meu conhecimento e espero poder ajudar no desenvolvimento profissional de cada um de vocês.

[![Linkedin Badge](https://img.shields.io/badge/-Fernanda_Maki_Hirose-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/fernanda-maki-hirose-801117208/)](https://www.linkedin.com/in/fernanda-maki-hirose-801117208/)  [![Gmail Badge](https://img.shields.io/badge/-femahi2020@gmail.com-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:femahi2020@gmail.com)](mailto:femahi2020@gmail.com)
