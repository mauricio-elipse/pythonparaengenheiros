# O que são os "módulos Python"

Quando lemos: “módulos Python” podemos interpretar quase que diretamente como sendo bibliotecas; o *“quase que diretamente”* deve-se ao fato de que alguns trazem outros recursos e facilidades adicionais que transcendem o simples conceito de biblioteca (são verdadeiros *frameworks*!).

Então, para utilizarmos estes módulos, a primeira coisa a fazer é “carrega-los” no ambiente ou script que pretendemos executar. Esta é uma operação que se tornará recorrente na utilização de scripts Python: a importação de módulos ao ambiente para utilização/chamadas de seus recursos/funções.

Existem diversas formas de carregar, ou melhor, importar uma biblioteca (ou melhor, módulo), mas todas utilizam a palavra reservada **import**. Sem mais delongas, vamos apresentar quatro formas de importar o módulo *numpy* para utilizar suas "funcionalidades":

**Formato 1**
```py
# carregando o módulo numpy para o ambiente de trabalho (ou script)
import numpy
# criando um vetor de valores inteiros e atribuindo à variável v
v = numpy.array([1, 2, 3, 4, 5])
```
Neste primeiro caso o módulo é carregado, e para utilizar suas funcionalidades (classes, funções, etc.) é preciso sempre escrever **numpy.** seguido da "funcionalidade" desejada, no exemplo acima é a construção de um objeto do tipo **array** do *numpy*.

**Formato 2**
```py
import numpy as np
# criando um vetor de valores inteiros e atribuindo à variável v
v = np.array([1, 2, 3, 4, 5])
```
Neste segundo caso optou-se por criar um "apelido" para o módulo *numpy*, desta forma, para chamar as "funcionalidades", basta usar o "apelido" **np.**.

>**Nota**
>
>Esta é a forma mais usada e recomendada. Para quem for realmente curioso e ousado sugiro uma rápida pesquisa na *WWW* sobre este tema!

**Formato 3**
```py
from numpy import array
# criando um vetor de valores inteiros e atribuindo à variável v
v = array([1, 2, 3, 4, 5])
```
Nesta terceira forma o que está sendo efetivamente importado é a "funcionalidade" (classe) que possibilita criar um objeto **array** do *numpy*. Notar que neste caso não é necessário usar o nome do módulo antes da chamada da "funcionalidade", muito menos seu apelido (até porque o mesmo nem foi dado)!

>**Nota**
>
>O "apelido" **np** ja está consolidado na comunidade Python para o módulo *numpy*, assim como **sp** para o *scipy*, dentre outros que veremos mais adiante. Agora, se fores realmente criativo e ousado, podes inventar o apelido que achares mais conveniente - só não diz que eu não avisei quando chegarem as queixas de amigos que eventualmente venham a ver teu código, ou mesmo quando pedires por auxílio nos fóruns!!!

**Formato 4**
```py
from numpy import *
# criando um vetor de valores inteiros e atribuindo à variável v
v = array([1, 2, 3, 4, 5])
```
Aparentemente este formato parece com o anterior no que diz respeito à utilização da "funcionalidade", mas não se engane! Neste caso, absolutamente TODAS as funcionalidades que se "localizam no nível logo abaixo do *numpy*" foram importadas! Desta forma, não apenas a "funcionalidade" **array** pode ser chamada sem a necessidade do **numpy.**, mas também todas as demais!!
Isso se deve ao caractere asterisco $$*$$, que funciona como um coringa!

Para os mais atentos, provavelmente surgiu a dúvida:
>.. o que ele quis dizer com: "localizam no nivel logo abaixo do *numpy*..." *??!*

Bem... este assunto diz respeito a como os módulos Python são organizados e, a princípio, não pretendo abordar neste material; mas para os mais ousados recomendo fortemente pesquisar na *WWW* por: *"how to create python modules"*!!!

>**Nota**
>
>Esta última forma de importação de módulos do Python NÃO é a mais recomendada - motivo: pode acabar gerando "conflitos" de nomes de "funcionalidades", na verdade o conflito estará apenas na cabeça de quem está digitando/brincando, pois para o Python é fácil, ele vai "escolher" apenas um deles!!! Imaginem a situação de não saber se a palavra **array** refere-se à classe do *numpy*, ou de qualquer outro módulo ou variável!!!
>
>Aos ousados, recomendo pesquisar na *WWW* por:*"python namespace"* !!!
>
>Aos demais, deixa assim... o que foi dito já é muito mais que suficiente - MAS... só pra garantir: **usar o formato 2 !!!**.
