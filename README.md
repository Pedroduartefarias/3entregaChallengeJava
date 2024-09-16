# JavaAdvancedChallenge

## Nomes dos integrantes
#### Pedro Duarte Farias: Responsavel pela criação do projeto java
#### henrique Baptista: Responsavel pela criação do projeto IOT
#### Leonardo Dourado: Responsavel por criar o projeto de QA
#### Gabriel Caverzan: Responsavel por criar o projeto de Mobile e Banco de dados
#### Felipe: Responsavel por criar o projeto de C# e Cloud
<br>

</head>
<body>
  <h1>Projeto de Gestão de Clientes</h1>
  <p>Este projeto é um sistema de gestão de clientes e compras, que permite criar, visualizar, editar e excluir dados de clientes, assim como suas compras.</p>

  <h2>🚀 Tecnologias Utilizadas</h2>
  <ul>
    <li>Java 17</li>
    <li>Spring Boot 3.3.2</li>
    <li>Spring Security</li>
    <li>JPA com Hibernate</li>
    <li>Banco de Dados Oracle (com SQL Developer)</li>
  </ul>

  <h2>🛠️ Funcionalidades</h2>
  <ul>
    <li>Autenticação e Autorização de Usuário com Spring Security</li>
    <li>CRUD de Clientes</li>
    <li>CRUD de Compras</li>
    <li>Persistência com Banco de Dados Oracle</li>
  </ul>

  <h2>🗃️ Estrutura de Pastas</h2>
  <ul>
    <li><code>src/main/java</code>: Código-fonte Java</li>
    <li><code>src/main/resources</code>: Configurações e arquivos estáticos</li>
    <li><code>src/test/java</code>: Testes unitários e de integração</li>
  </ul>


  <h2>🔐 Configuração de Segurança</h2>
  <p>O projeto utiliza autenticação baseada em JWT. Para acessar as rotas protegidas, é necessário obter um token JWT.</p>

  <h3>Obtendo o Token JWT</h3>
  <p>Para obter um token JWT, faça uma requisição POST para <code>/login</code> com um JSON contendo o <code>email</code> e <code>password</code>:</p>
  <pre><code>
POST /login
{
  "email": "user@example.com",
  "password": "sua-senha"
}
  </code></pre>
  <p>O retorno será o token JWT, que deve ser utilizado no cabeçalho das requisições às rotas protegidas:</p>
  <pre><code>Authorization: Bearer seu-token-jwt</code></pre>

  <h2>📄 JSON para Testes</h2>
  <p>Exemplo de JSON para cadastrar um cliente:</p>
  <pre><code>
POST /clientes
{
  "name": "João da Silva",
  "genero": "Masculino",
  "email": "joao.silva@example.com",
  "password": "senha123",
  "idade": "30"
}
  </code></pre>

  <p>Exemplo de JSON para cadastrar uma compra:</p>
  <pre><code>
POST /compras
{
  "clienteId": 1,
  "produto": "Notebook",
  "valor": 3500.00,
  "quantidade": 1
}
  </code></pre>

  <h2>📋 Requisições</h2>
  <ul>
    <li>GET /clientes: Retorna a lista de clientes</li>
    <li>POST /clientes: Cadastra um novo cliente</li>
    <li>GET /clientes/{id}: Retorna os dados de um cliente</li>
    <li>PUT /clientes/{id}: Atualiza os dados de um cliente</li>
    <li>DELETE /clientes/{id}: Remove um cliente</li>
  </ul>




