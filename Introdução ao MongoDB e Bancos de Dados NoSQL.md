# Introdução ao MongoDB e Bancos de Dados NoSQL

## Apresentação do curso

apresentar os bancos não relacionais. Introdução ao NoSQL (Not Only SQL), os tipos de bancos NoSQL assim como realizar pequenas operações em alguns deles com ênfase  no MongoDB no qual iremos desde sua instalação, opções de uso na nuvem e operações de manipulação de dados, além de mostrar os fatores que o mostraram únicos no mercado.

- AULA 1: Verificar fatores históricos que marcaram o NoSQL no mercado de dados não relacionais e mostrar os tipos e usos diferentes
- AULA 2: 4 banco de dados não relacionais e diferentes entre si para praticar e ver como funcionam e qual melhor utilizar
- AULA 3: Introdução ao MongoDB, que é o banco não relacional Mais utilizado atualmente, fará introdução e instalação. Caso não seja possível instalar, teremos o MongoCloud para utilizar na nuvem o Mongo
- AULA 4: SCHEMA e design
- AULA 5: aprendendo mais sobre JSON e BSON
- AULA 6: Operações de manipulação de dados
- AULA 7: Performance e índices (importante, pois grandes volumes de dados significa buscas de alta performance)
- AULA 8: agregações (facilita a vida do dev e tem ferramentas boas nas agregações)

## Objetivos

- Entender os fatores que levaram a criação dos bancos NoSQL
- Conhecer as principais diferenças entre os Banco de Dados SQL e NoSQL
- Conhecer características e vantagens de usar banco de dados não relacionais 

## História

1970 - os banco de dados relacionais são amplamente utilizados

1998 - 1° introdução do NoSQL, criado por Carlos Strozzi

1. 2009 - reaparição do NoSQL, amplamente discutido por entusiastas em uma conferência, mas por que surgiu em 2009?Bem, o contexto: A cada ano, dobramos a quantidade de dados produzidos e armazenados; temos várias aplicações não convencionais; a necessidade de suprir a demanda por aplicativos escaláveis; flexibilização dos dados e armazenamentos.

NoSQL engloba uma série de tecnologias que não necessariamente tem semelhanças entre elas. A única semelhança entre elas é que são não relacionais

Os NoSQL não substituíram os SQL, pois cada um tem suas forças e fraquezas, suas habilidades e oportunidades

## Diferença: BD relacional x BD NoSQL

1. Escalabilidade: banco de dados **Relacional** é Vertical (aumento de capacidade para um único recurso; Processador, memória e disco rígido) ou Horizontal (replicas de dados **APENAS PARA LEITURA**). Já no caso **NoSQL**, nativamente é Horizontal (particionando os dados entre os nós é o mais conhecido, através do sharding)
2. Schemas ou Estruturas: os relacionais precisão de uma estrutura rígida e bem estruturada (com tuplas, colunas, PK e FK); já os não relacionais... não tem regras, é schemaless/Schema-free, não precisa pré-deifnir os tipos de dados que ele vai receber MAS **TENHA BOAS PRÁTICAS DE NÃO COLOCAR QUALQUER TIPO DE DADO LÁ** 
3. Performance: os relacionais necessitam do sistema de Disco para um melhor funcionamento (quanto mais espaço no disco é dedicado ao banco de dados, melhor será o processamento, ao custo de todas as outras funções do teu pc); Já no **NoSQL**, dependerá do tamanho do seu Cluster e a potência da sua rede
4. Transações: os BD relacionais são ***ACID (Atomicidade, Consistência, Isolamento e Durabilidade)*** - Que ou uma transação é executada por completo ou nada será feito; Quando for concluída a transação, o BD estará em conforme com o que foi realizado; Uma transação nunca interfere em outra diretamente; Uma vez que uma transação for concluída, o seu dado jamais será perdido. Os BD NoSQL são ***BaSE (Basically Available, Soft-State, Eventually Consistent)*** 

Assim posto, é possível perceber que as qualidades de um banco de dados não relacional recai em Flexibilidade, Escalabilidade e Alta Performance