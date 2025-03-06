# Despesas Residenciais

Sistema de controle de gastos residencial

## Funções

- Criar, visualizar e deletar pessoas.
- Criar e visualizar transações.
- Visualizar saldo individual e familiar.

## Instalação

### Pré-requisitos

Garanta que você tenha o seguinte instalado:

- Maven
- npm

### Passos
Compile a classe "DespesasResidenciaisApplication" pela sua IDE ou:
```bash
mvn spring-boot:run
```
Vá para o diretório do código onde está o front-end:
```bash
  cd app
  npm run dev
```
Abra o link que a ferramente Vite disponibilizou no terminal: "http://localhost:5173/"

## Estrutura da pasta 

- app/ - Contém  o código do front-end, escrito em Typescript, React, HTML e CSS.

- src/ - Contém o código do back-end, escrito em Java e Spring Boot

- src/test - Contém os testes unitários e de integração do back-end, escritos em JUnit.

- target/reports/apidocs - Contém a documentação (javadoc) do projeto.

- pom.xml - Contém todas as dependências usadas no projeto e os porquês.

## API Endpoints

- /pessoas: Endpoint usado para criar, listar e deletar pessoas.

- /totais: Endpoint para consultar receita, despesa e saldo das pessoas.

- /transacoes: Endpoint para criar e listar transações.

Mais detalhes sobre os endpoints podem ser encontrados na documentação.

## Documentação 

Todas as classes e metódos que considerei relevantes estão com comentários as descrevendo.
Você pode encontrar a documentação abrindo diretamente o index.html que se encontra no 
diretório target/reports/apidoc/ ou então:
No macOS/Linux:
```bash
xdg-open target/reports/apidocs/index.html
```
No Windows:
```bash
start target/reports/apidocs/index.html
```

## Decisões de Arquitetura

### Contexto
Este projeto foi desenvolvido visando agilidade e simplicidade, utilizando tecnologias com as quais já 
tinha experiência, atendendo aos requisitos do desafio sem adicionar complexidade desnecessária.

### Front-end
- React: Utilizado para a criação dos quatro componentes principais da interface.
- TypeScript: Empregado para evitar a tipagem dinâmica do JavaScript.
- Vite: Escolhido como alternativa ao create-react-app, pois o mesmo está sendo abandonado.

### Back-end
- Spring Boot: Utilizado para gerar o boilerplate do projeto, permitindo que eu focasse na lógica 
do desafio sem me preocupar com a configuração inicial.

### Banco de Dados
- Armazenamento em Memória: Optei por não utilizar um banco de dados para reduzir a complexidade 
(evitando lidar com JDBC/Hibernate/JPA). Dessa forma, todas as informações são mantidas em memória 
e são perdidas quando o servidor é desligado. Essa escolha também facilita a execução do projeto em 
diferentes máquinas, visto que não há necessidade de instalar ou configurar nada.

## Testes

Você pode rodar os testes do projeto através da sua IDE ou pelo terminal:
```bash
mvn test
```
