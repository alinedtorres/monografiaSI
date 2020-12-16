# CODE REVIEW
## UM GUIA SOBRE REVISÃO DE CÓDIGO COM EXEMPLOS REAIS

O objetivo desse artigo é oferecer dicas de como realizar um code review, demonstrando exemplos práticos reais retirados de projetos do github. Todos os comentários citados neste artigo são exemplos reais retirados de projetos do github

## Introdução

A revisão de código é um estudo cuidadoso e sistemático do código-fonte por alguém que não é o autor original do código. O processo visa a criação de softwares confiáveis, corretos e com valor de negócio. É possível realizar code review através de programação de pares ou de análise dos pull requests. O code review tem outros aspectos importantes, como informar outras pessoas sobre as alterações, transferência de conhecimento, processo de feedback, entre outros. Além disso, auxilia na qualidade do software, melhora a confiabilidade, corretude, eficiência, manutenibilidade e valor de negócio. 

Encontrar defeitos continua sendo a principal motivação para a revisão. Porém, o resultado de algumas pesquisas mostra que as revisões são menos sobre defeitos do que o esperado e, em vez disso fornecem benefícios adicionais, como aumento da conscientização da equipe e criação de soluções alternativas para os problemas.

A revisão de código possui dois propósitos. Melhorar o código, ou seja, encontrar bugs, antecipar possíveis bugs, verificar a clareza do código e verificar a consistência com os padrões de estilo do projeto. Melhorar o programador, pois a revisão de código é uma maneira importante de os programadores aprenderem e ensinarem uns aos outros, sobre novos recursos de linguagem, mudanças no design do projeto ou seus padrões de codificação e novas técnicas.

## Trabalhos Relacionados

Em 2013, Alberto Bacchelli e  Christian Bird realizaram um estudo de Code Review através de uma pesquisa com desenvolvedores, testadores e gerentes da Microsoft [1]. O objetivo foi descobrir o que os desenvolvedores e gerentes esperam da revisão de código, como as revisões são realizadas na prática e quais os resultados reais e desafios.

Existem várias motivações para revisão de código. No geral, as entrevistas revelaram que encontrar defeitos, embora proeminentes, é apenas uma das muitas motivações que levam os desenvolvedores a executar o code review. Especialmente quando reforçado por uma forte cultura de equipe em torno das revisões, os desenvolvedores percebem as revisões de código como uma atividade que tem múltiplas influências benéficas não apenas no código, mas também para a equipe e todo o processo de desenvolvimento. 

!Comentários em cada categoria - Aqui  vem uma imagem

Conforme gráfico acima, extraído do estudo de Alberto Bacchelli e  Christian Bird, analisando os resultados dos comentários avaliados, melhoria de código é a categoria mais frequente, com maior quantidade de comentários. Embora a descoberta de defeitos seja a principal motivação, é apenas a quarta categoria mais frequente nos resultados. 


## Recomendações

Baseado no trabalho produzido por Doctor McKayla, 10 Tips for Respectful and Constructive Code Review Feedback [2] e após um estudo de 624 comentários de 120 pull requests, sendo 259 comentários de code review, foram criadas as recomendações abaixo para um Code Review com respeito e que agrega valor.

### 1 - Fornecer Orientação

Ao realizar uma revisão de código, é extremamente importante explicar e dar orientações de como o programador pode melhorar o código de acordo com as sugestões.


### 2 - Agregar valor para o autor do código

Pensar no autor do código e identificar como agregar valor na revisão baseado no autor.


### 3 - Mostrar Evidências

Se possível, mostrar evidências de que sua sugestão está correta, exibindo documentações ou testes.

>_"to specify volume id instead of volume name, because the id is UUID and safe to be specified. cinder delete allows id as https://docs.openstack.org/python-cinderclient/latest/cli/details.html#cinder-delete"_

No comentário acima o revisor colocou o link da documentação justificando sua sugestão.

