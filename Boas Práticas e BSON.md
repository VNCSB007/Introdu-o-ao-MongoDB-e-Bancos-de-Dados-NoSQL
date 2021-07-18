# Boas Práticas e BSON

 

- Evite documentos muito grandes (pois quanto maior o documento, maior o _overhead_ que é o processamento de documentos grandes, o que diminui o desempenho do aparelho que sofreu _overhead_)
- use nomes em campos curtos, com objetivos claros (quanto maior o nome, maior o espaço ocupado, por menor que seja; além disso, poder passar de forma rápida e clara para outros desenvolvedores os seus schemas é fundamental no ramo)
- Analise as suas queries complexas utilizando "explain()" (dará o tempo de execução, quantos arquivos foram escaneados, quais índices utlizados, entre outros)
- Atualize apenas os campos alterados (É a questão do WHERE em relação ao UPDATE: sem ele, toda a tabela será atualizada. Prefira sempre especificar os campos que foram pretendidos para a alteração desejada)
- Evite fazer queries com negação "NE" (o Mongo não consegue indexar valores e condições negativas)
- Lista/Arrays dentro dos documentos não podem crescer sem limite (defini um limite sempre, tendo em mente uma noção de que tipo de dado será inserido na sua Array)

## Armazenamento de dados BSON

É uma serialização codificada em binário de documentos semelhantes a JSON. 

Contém extensões que permitem  representação de tipos de dados que não fazem parte da especificação JSON (Por exemplo, BSON tem um tipo "Date", "ObjectID", diferente do JSON)

O JSON  lida apenas com dados primitivos como String ou número, e caso quiséssemos a mesma funcionalidade do BSON, seriamos obrigados a manualmente criar uma String que gravasse a mesma informação (ou seja, entre criar manualmente e usar uma linguagem com codificação nativa, qual você escolheria?:sunglasses:)  

