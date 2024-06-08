+++
title = 'Primeiro Freela'
subtitle = 'Aprendizados'
date = 2024-06-05T23:05:53-03:00
+++

Esse é meu primeiro blog post, então se você está lendo isso, obrigado! A ideia
é fazer posts assim regularmente, documentando um pouco a minha experiência como
estudante de Ciência da Computação entrando no mercado de trabalho. Mas vamos
ao que interessa: como foi meu primeiro _'freela'_ e as lições que tive com ele.

## Definição de Freela

> "Freela é todo trabalho remunerado, de escopo fechado, que quem paga e quem faz o serviço não possuem vínculo trabalhista"
                                                    -- Eu

## Contexto

Comecei a estudar web dev a aproximadamente 1 ano, fiz o caminho default: HTML, CSS,
pulei o JS vanilla pra ir direto pro React (depois me arrependi e aprendi os addEventListener
da vida), Nodejs, SQL, desenvolver APIs REST, um cadinho de docker e mais recentemente Java.
Cada projeto nesse meio tempo me ajudou a melhorar algum ponto em específico, alguns o requerimento
era velocidade - de entrega não performance bruta - outros era a mantenabilidade, alguns eu nem sabia
a stack antes de começar, aprendi o que precisava sob demanda e toquei o barco. Em um desses projetos
conheci um brother muito gente fina que me guiou sobre as famosas questões de boas práticas, o ~~famigerado~~
clean code e refatoração; esse projeto em específico era o back-end da V2 de outro projeto que ele tinha feito antes. 
Como o front-end desta V2 está em desenvolvimento, a V1 ainda está sendo utilizada, e é sobre ela que falaremos mais hoje.  

## Mais Contexto

Este projeto é uma plataforma de estudos para concurso, na versão mais recente utilizamos Next.js no front-end e 
microsserviços com Nestjs, Postgres e mais recentemente Kafka no back-end. A versão antiga foi desenvolvida
com Vue.js, PHP/Laravel (nada contra, tenho até parentes que são) e MySql. Isso é importante por que quero que você
entenda a situação que me encontrei, as lições vão fazer mais sentido.

A V1 estava com 2 problemas: um campo que deveria dar highlight em uma determinada data não estava, e opções que deveriam
aparecer depois de uma data não estavam aparecendo. Simples não? Foram esses _bugs_ que me pediram pra consertar.

## Soluções

Evidentemente não vou entrar nos detalhes que eu gostaria por que o código não é meu, mas basicamente
o primeiro problema estava relacionado com a construção de um objeto de data, quebrei um pouco a cabeça mas foi relativamente
tranquilo. O segundo foi _trickyer_, estava relacionada com a query que o back-end estava fazendo pra uma determinada rota. Agora
como cheguei neles? Onde acertei? E principalmente, onde errei?

## Aprendizados

## 1. Se Atente ao problema

Meu maior erro foi sem dúvidas tentar entender o sistema inteiro de uma vez, ao invés de focar única e exclusivamente nos problemas.
Trabalhar com o código feito por outra pessoa é uma coisa engraçada, e sem dúvidas o cenário mais comum; você precisa entender os "comos" e 
"porquês", explorar os componentes, módulos e classes de forma a tentar criar um modelo mental do sistema o mais próximo possível do
outro dev. Fazer isso não é fácil - na verdade a dificuldade depende de vários fatores, mas isso é tema pra outro dia -, e pode demorar
de alguns dias até meses, eu não tinha esse tempo todo. Quando percebi que estava tentando entender o código de cada página ao invés de
focar na página que apresentava o problema, tive que pivotar a abordagem. 

Situações como essa, onde se tem uma task muito específica, requerem uma abordagem muito específica. O que na realidade é muito mais simples
do que parece; você não precisa desenvolver algo novo ou refazer todo o código, só resolver aquele pequeno problema. O que nos leva ao próximo 
aprendizado.

## 2. Não tenha medo de novas stacks

Como você pôde ver pelo meu background, nunca tinha trabalhado com nenhuma dessas tecnologias, mas independente delas: o protocolo HTTP é o mesmo,
o modelo de _front-end -> back-end -> banco de dados_ é o mesmo, o modelo do Laravel de controllers, services, repositórios, interfaces não é 
muito diferente do Nestjs ou do Spring boot. Enfim, tecnologias mainstream são bem mais parecidas do que se imagina.

Dessa forma, se você aprendeu bem o problema que determinada ferramenta se propôs a resolver, você consegue entender as variações dessa ferramenta
e as diferentes formas que elas resolvem o mesmo problema.

## 3. Crie e teste hipóteses

Uma lição mais prática. O método científico[1] se aplica excepcionalmente bem em sessões de debug; por exemplo, o sistema apresenta um comportamento
inesperado, após vasculhar logs, requisições, ou qualquer rastro que te dê algum indício deste comportamento, você:

1. Cria um hipótese da razão deste comportamento;
2. Encontre um caso de teste que faça sua hipótese falhar;
3. Reavalie;

Eu acho particularmente divertido fazer este tipo de coisa, me sinto um detetive vasculhando a cena do crime - ou mais precisamente um mecânico 
consertando um carro já consertado por outro mecânico, que o pegou montado por um primo -. Crie hipóteses, teste, revise, e vasculhe. No mínimo
você vai aprender algo novo, e não se esqueça:

> "Eliminando o impossível, o que sobra, por mais improvável que seja, é a verdade."
                                                    -- Mr. Spock

## 4. Assuma riscos!

Por fim, assuma riscos! Estou dizendo pra apostar no macaco no próximo jogo do bixo? Não! Ou pra emprestar dinheiro pro teu parente finalmente abrir
sua loja de sal do himalaia? Muito menos. Estou dizendo que se colocar em situações em que não se tem muito a perder, mas muito a ganhar, sempre é
vantajoso[2], mesmo que você pense que não está 100% preparado (só não me vá chamar o popó no ringue). Cada oportunidade que te tira da zona de conforto
é uma oportunidade de ser melhor.

# Conclusão

Obrigado por ler até aqui. Espero que esta minha experiência tenha te ajudado de alguma forma. Se sim, sinta-se livre para compartilhar esse post :)
Estou sempre a disposição pra trocar ideia. Até mais e obrigado pelos peixes.



#### Notas

1. Um conceito bem poderoso, e até rotineiro na programação, é a navalha de Ockham, que postula: "[...] de múltiplas explicações 
adequadas e possíveis para o mesmo conjunto de fatos, deve-se optar pela mais simples daquelas". Antes de caçar races conditions ou deadlocks, verifique
aquela vírgula no final da linha :)

2. Para quem leu os livros do Taleb isso é o arroz com feijão da "antifragilidade", recomendo qualquer livro do Nassim.







