# CODE REVIEW
## UM GUIA SOBRE REVISÃO DE CÓDIGO COM EXEMPLOS REAIS

O objetivo desse artigo é oferecer dicas de como realizar um code review, demonstrando exemplos práticos reais retirados de projetos do github. Todos os comentários citados neste artigo são exemplos reais retirados de projetos do github

## Introdução

A revisão de código é um estudo cuidadoso e sistemático do código-fonte por alguém que não é o autor original do código. O processo visa a criação de softwares confiáveis, corretos e com valor de negócio. É possível realizar code review através de programação de pares ou de análise dos pull requests. O code review tem outros aspectos importantes, como informar outras pessoas sobre as alterações, transferência de conhecimento, processo de feedback, entre outros. Além disso, auxilia na qualidade do software, melhora a confiabilidade, corretude, eficiência, manutenibilidade e valor de negócio. 

Encontrar defeitos continua sendo a principal motivação para a revisão. Porém, o resultado de algumas pesquisas mostra que as revisões são menos sobre defeitos do que o esperado e, em vez disso fornecem benefícios adicionais, como aumento da conscientização da equipe e criação de soluções alternativas para os problemas.

A revisão de código possui dois propósitos. Melhorar o código, ou seja, encontrar bugs, antecipar possíveis bugs, verificar a clareza do código e verificar a consistência com os padrões de estilo do projeto. Melhorar o programador, pois a revisão de código é uma maneira importante de os programadores aprenderem e ensinarem uns aos outros, sobre novos recursos de linguagem, mudanças no design do projeto ou seus padrões de codificação e novas técnicas.

## Trabalhos Relacionados

Em 2013, Alberto Bacchelli e  Christian Bird realizaram um estudo de Code Review através de uma pesquisa com desenvolvedores, testadores e gerentes da Microsoft [[1]](https://dl.acm.org/doi/10.5555/2486788.2486882). O objetivo foi descobrir o que os desenvolvedores e gerentes esperam da revisão de código, como as revisões são realizadas na prática e quais os resultados reais e desafios.

Existem várias motivações para revisão de código. No geral, as entrevistas revelaram que encontrar defeitos, embora proeminentes, é apenas uma das muitas motivações que levam os desenvolvedores a executar o code review. Especialmente quando reforçado por uma forte cultura de equipe em torno das revisões, os desenvolvedores percebem as revisões de código como uma atividade que tem múltiplas influências benéficas não apenas no código, mas também para a equipe e todo o processo de desenvolvimento. 

[![comentarios-Em-Categoria.png](https://i.postimg.cc/h4LbRFfM/comentarios-Em-Categoria.png)](https://postimg.cc/HjL7bh07)

Conforme gráfico acima, extraído do estudo de Alberto Bacchelli e  Christian Bird, analisando os resultados dos comentários avaliados, melhoria de código é a categoria mais frequente, com maior quantidade de comentários. Embora a descoberta de defeitos seja a principal motivação, é apenas a quarta categoria mais frequente nos resultados. 


## Recomendações

Após um estudo de 624 comentários de 120 pull requests do GitHub, sendo 259 comentários de code review, foram criadas as recomendações abaixo para um Code Review com respeito e que agrega valor. As recomendações de 1 a 10 foram inspiradas no artigo How to Give Respectful and Constructive Code Review Feedback, de autoria de Michaela Greiler [[2]](https://www.michaelagreiler.com/respectful-constructive-code-review-feedback/).


### 1 - Fornecer Orientação

Ao realizar uma revisão de código, é extremamente importante explicar e dar orientações de como o programador pode melhorar o código de acordo com as sugestões. Disponibilizar documentações ou até mesmo trechos de códigos para auxiliar o programador pode fazer a diferença em um comentário.


### 2 - Realizar perguntas e não fazer exigências

As perguntas abrem a mente do programador. Com perguntas, você está abrindo um diálogo.

![Recomendacao14](https://github.com/alinedtorres/monografiaSI/blob/main/Recomenda%C3%A7%C3%A3o%2012.png)

O exemplo acima mostra um comentário em que o revisor não faz uma exigência, ele realiza uma pergunta para iniciar um diálogo e abrir a mente do programador.


### 3 - Agregar valor para o autor do código

Pensar no autor do código e identificar como agregar valor na revisão baseado no autor.


### 4 - Não assumir que o autor fez algo intencionalmente errado

Tenha cuidado para que o comentário não seja uma acusação ao autor do código, supondo que o erro foi intencional.

![Recomendacao4](https://github.com/alinedtorres/monografiaSI/blob/main/Recomenda%C3%A7%C3%A3o%207.png)

Realizar perguntas é uma boa forma de não aparentar que a pessoa fez algo intencionalmente errado. No exemplo acima o revisor questiona por qual motivo foi incluída essa parte no código.


### 5 - O feedback deve ser sobre o código

O feedback deve ser sobre o código, e não refletir sobre o autor do código.


### 6 - O seu ponto de vista também pode estar errado

O feedback não é uma declaração universal da verdade, e sim uma observação da sua perspectiva.

![Recomendacao8](https://github.com/alinedtorres/monografiaSI/blob/main/Recomenda%C3%A7%C3%A3o%2011.png)

Neste exemplo o programador explicou seu ponto de vista, fazendo com que o revisor conseguisse compreender o que foi feito, mudando de ideia.


### 7 - Não utilizar ironia ou sarcasmo

Sarcasmo ou ironia são difíceis de identificar na linguagem escrita.


### 8 - Usar emoji

Os emojis auxiliam a entender o sentido da frase que foi colocada.

![Recomendacao9a](https://github.com/alinedtorres/monografiaSI/blob/main/Recomenda%C3%A7%C3%A3o%20emoticon1.png)


### 9 - Não utilizar palavras ofensivas

Evite palavras que possam ofender o autor.


### 10 - Explicar seu ponto de vista

Explicar a sua sugestão e o porque você pensa dessa forma.

![Recomendacao10a](https://github.com/alinedtorres/monografiaSI/blob/main/Recomenda%C3%A7%C3%A3o%2014a.png)
![Recomendacao10b](https://github.com/alinedtorres/monografiaSI/blob/main/Recomenda%C3%A7%C3%A3o%2014b.png)

Neste exemplo o revisor explica seu ponto de vista com evidências. Logo em seguida o autor também explica seu pensamento demonstrando partes do código, facilitando o entendimento.


### 11 - Mostrar Evidências

Se possível, mostrar evidências de que sua sugestão está correta, exibindo documentações ou testes.

![Recomenda-o-3-red.png](https://i.postimg.cc/nr8wRVxL/Recomenda-o-3-red.png)

No comentário acima o revisor colocou o link da documentação justificando sua sugestão.


### 12 - Volte a ler os comentários

Se necessário, releia os argumentos do autor, você pode ter uma nova visão sobre seu ponto de vista, como no exemplo abaixo.

![Recomenda-o-4-red.png](https://i.postimg.cc/Mpr53Zb8/Recomenda-o-4-red.png)


### 13 - Os comentários também podem ser positivos

Faça comentários positivos sobre as alterações, esses comentários também agregam valor e motivam o autor.

![Recomendacao13](https://github.com/alinedtorres/monografiaSI/blob/main/Recomenda%C3%A7%C3%A3o%206.png)

No exemplo acima o revisor envia um feedback positivo sobre a alteração e comenta sobre as instruções de testes criadas.


### 14 - Questionar suas dúvidas sobre a alteração revisada

Caso tenha dúvidas sobre alguma alteração, faça perguntas  e questione o autor. Muitas vezes uma simples pergunta pode mudar o pensamento do programador, evitando alguns erros no código.


### 15 - Deixar claro seus questionamentos sobre a revisão sugerida

Caso tenha dúvida em uma sugestão, deixe claro sua dúvida, para que outros revisores possam opinar e iniciar um diálogo sobre o assunto.

![Recomendacao15](https://github.com/alinedtorres/monografiaSI/blob/main/Recomenda%C3%A7%C3%A3o%2015.png)


## Conclusão

Concluindo, revisões de código modernas fornecem benefícios além de encontrar defeitos. A revisão do código pode ser usada para melhorar o estilo de código, encontrar soluções alternativas, aumentar o aprendizado, compartilhar propriedade do código, etc. Isso deve orientar as políticas de revisão de código.

60% dos defeitos podem ser encontrados na revisão de código. Revisão de código é uma boa ferramenta para identificar defeitos relacionados à evolutibilidade do código que não são identificáveis na fase de testes.

A revisão do código tem sido uma parte necessária do desenvolvimento de software, tornando-se cada vez mais importante o aprendizado sobre o assunto.




