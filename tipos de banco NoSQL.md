# tipos de banco NoSQL

DBengines: rank dos bacnos de dados relacionais e não relacionais 

bd para **document store** (Json), **chave-valor  store** (redis), **wide-column store** (o que menos apresenta diferença aos tradicionais) e **Graph Store** (bem usado)

## Tipo Grafos

estruturas matemáticas entre nós e vértices. Nós são os dados, vértices são os relacionamentos. grafso comuns para detectar fraude, recomendações (Neo4j; ArangoDB)

**criando uma estrutura de registros que compõem os dados de uma rede social utilizando um sandbox do Neo4j**

sandbox.neo4j.com

CREATE (:Client {name: "bob", age: 28, hobbies: ['caça agua viva, come hamburg']});

MATCH (bob) RETURN bob;

CREATE (:Client {name: "Lula", age: 33, hobbies: ['Tocar clarinete']}) -[:Bloqueado]-> (:Client {name:"Patrick", hobbie:'Caça agua viva'});

MATCH (todos) RETURN todos;

CREATE (:Object);

MATCH (todos) RETURN todos;

MATCH (Lula:Client {name:"Lula"}), (patrick:Client {name:"Patrick"}) CREATE (lula)-[:Bloqueado] -> (Patrick)

MATCH (todos) RETURN todos;

## Coluna/família de colunas

armazenam exatamente em suas colunas de forma independente entre elas. Primeira diferença: hierarquia - Qui space que dentro dele há uma família de colunas, que seriam como tabelas nas db relacionais tradicionais, e  dentro dessa família de colunas há as colunas que armazenam os dados (Cassandra; Microsoft Azure; Google Cloud Bigtable; ScyllaDB; Elassandra)

Keyspace: agrupamento de famílias de colunas => **DB**

Column Family/Table: agrupamento de colunas => **Table**

Row Key: chave que representa uma linha de coluna => **PK**

Column: representa um valor contendo: Name, Value, Timestamp

Registro de transações: compras, resultados de teste, filmes assitidos e localização mais recente do filme 

Rasreando praticamente qualquer coisa, incluindo status do pedido

**Utilizando o Cassandra iremos criar uma estrutura de banco e realizar operações**

## Chave-valor

constituído por chave unica e a valor, e ambos podem ser simples ou complexos

Bom desempenho em aplicações na nuvem; menor capacidade de busca (bom de escrever, ruim de ler)

uso: cache, sessão de usuário, carrinho de compra 

Rank: Redis; Amazon DynamoDB; Microsoft Azure

**Iremos utilizar o Redis um banco de dados, cache, messageria e fila**

**Alto desempenho**

**Estrutura de dados na memória**

**Versatilidade de uso**

**Replicação e persistência** 

**Usado: Twitter, Github, StackOverflow**

tempo de expiração da chave: para poder ficar repetindo o código, enquanto ele estiver ativo (utilizado mais em cache, hence why o ggogle roda mesmo sem internet - digo - a página inicial do google)

## Documento

documento é dado autocontido (dentro dele mesmo) e auto descritivo

permite redundância e inconsistência

Schemaless podendo utilizar JSON, XML entre outros

**MongoDB, Firebase realtime Database, Firestore, DynamoDB**

