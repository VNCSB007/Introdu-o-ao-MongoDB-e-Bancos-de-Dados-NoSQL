# Schema Design 

Apresentar o conceito | Aprender Boa Práticas 

## Embedding x Referência

No caso do embedding, os Documentos são autocontido (atualmente devido a complexidade de dados que são analisados, é difícil você ter um um documento que não faça referência com outro); no caso da Referência, os documentos tem depência de outros documentos ou collections.

No caso embedding, o código se parece com uma função ou uma transação, em que todo o conteúdo necessário para sua execução está contido num único valor; já as referências trazem valores de  outros códigos que são essenciais para o seu funcionamento

(Pensa assim: as informações que você irá escrever, quando elas são necessárias? **SEMPRE:** Embedding; **c.c. :** Referência)

**Embedding:**

- Pros:

Consulta informações em uma única Query

Atualiza o regsitro em uma única operação

- Contra:

Limite de 16 MB (grande, mas é um limitador ainda assim)

**Referência:**

- Pros:

Documentos pequenos

Não duplica informações

usado quando os dados não são requeridos em todas as runs ou consultas

- Contras:

Duas ou mais queries ou utilização do $lookup para requisitar os dados

## De acordo com o relacionamento

One-to-one: prefira atributos chave-valor no documento (a pessoa tem só um nome, só uma idade, só uma condição de Ativa no mercado de trabalho)

One-to-few: prefira Embedding (uma pessoa que vive em vários logradouros)

One-to-many e many-to-many: prefira Referência

link para maiores conhecimentos sobre Schema Design: https://www.mongodb.com/blog/post/building-with-patterns-a-summary

