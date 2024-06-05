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

Para executar a aplicação no Visual Studio Code, você precisa instalar a extensão "Debugger for Java"

## Configuração do Banco de Dados
Obs : O banco está hospedado temporariamente , se a hospegagem terminar ou se optar usar seu propio banco de dados , utilize esses passo a passo :

Crie um banco de dados MySQL e configure as credenciais no arquivo application.propeties , localizado no diretorio resources:

spring.datasource.url=jdbc:mysql://localhost:3306/nome_do_seu_banco_de_dados

spring.datasource.username=seu_usuario

spring.datasource.password=sua_senha

spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.show-sql=true

spring.jpa.properties.hibernate.format_sql=true

spring.jpa.open-in-view=true

spring.jpa.hibernate.ddl-auto=update

## Hospedagem 
A aplicação está hospedada temporariamente no seguinte link:

https://cocacola-api-production.up.railway.app

Caso a hospedagem tenha terminado, utilize http://localhost:8080 para as requisições.


## Executando a Aplicação

Clone o repositório:


git clone https://github.com/HirokiAsano1/CocaCola-api.git


Navegue até o diretório do projeto:


cd price-management-api


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
*  Corpo:"produtoId" e "quantidade"

*Obter produtos cadastrados aos clientes*

* URL: /clients/{clienteId}/produtos
* Método: GET

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
