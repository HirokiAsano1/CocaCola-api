# PROJETO SolarCocaCola

Este projeto é uma aplicação Spring Boot que inclui funcionalidades de CRUD para clientes, CRUD Para Produtos , CRUD Para Promoções e relacionamento das entidades Clientes e Produtos.

## Funcionalidades

Adicionar, atualizar, deletar, listar clientes , adicionar produtos , visuazliar produtos e remover produdos de  clientes.
Adicionar, atualizar, deletar, listar clientes de  Produtos.
Adicionar, atualizar, deletar, listar clientes de  Promoções.

## Requisitos

Java 17 ou superior

Maven

MySQL

## Configuração do Banco de Dados

Crie um banco de dados MySQL e configure as credenciais no arquivo application.propeties , localizado no diretorio resources:

spring.datasource.url=jdbc:mysql://localhost:3306/nome_do_seu_banco_de_dados
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

# Configuração para mostrar o SQL no console
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
spring.jpa.open-in-view=true
spring.jpa.hibernate.ddl-auto=update


## Executando a Aplicação

Clone o repositório:


git clone https://github.com/HirokiAsano1/CocaCola-api.git


Navegue até o diretório do projeto:


cd seu-repositorio


Compile e execute a aplicação


## Endpoints

### Clientes

*Adicionar Cliente*

* URL: /clients/add
* Método: POST
* Corpo: JSON com os detalhes do cliente

*Listar Clientes*

* URL: /clients
* Método: GET

*Obter Cliente por ID*

* URL: /clients/{id}
* Método: GET
* Parâmetro: id

*Atualizar Cliente*

* URL: /clients/update/{id}
* Método: PUT
* Corpo: JSON com os novos detalhes do cliente

*Deletar Cliente*

* URL: /clients/delete/{id}
* Método: DELETE

*Add produtos aos clientes* 

* URL: /clients/{clienteId}/add/produtos
* Método: Post
*  Corpo:

*Obter produtos cadastrados aos clientes*

* URL: /clients/{clienteId}/produtos
* Método: GET
* Corpo:

*Deletar produtos cadastrados a Clientes*

* URL: /clients/{clienteId}/DeleteProduct/{produtoId}
* Método: DELETE


### Produtos

*Adicionar Produtos*

* URL: /products/add
* Método: POST
* Corpo: JSON com os detalhes do produto

*Listar Produtos*

* URL: /products
* Método: GET

*Obter Produtos por ID*

* URL: /products/{id}
* Método: GET
* Parâmetro: id

*Atualizar Produto*

* URL: /products/update/{id}
* Método: PUT
* Corpo: JSON com os novos detalhes do Produto

*Deletar Produto*

* URL: /products/delete/{id}
* Método: DELETE

### Promoções

*Adicionar Promoção*

* URL: /promotions/add
* Método: POST
* Corpo: JSON com os detalhes da promoção

*Listar Promoções*

* URL: /promotions
* Método: GET

*Atualizar Promoções*

* URL: /promotions/update/{id}
* Método: PUT
* Corpo: JSON com os novos detalhes da promoção

*Deletar Promoção*

* URL: /promotions/delete/{id}
* Método: DELETE
