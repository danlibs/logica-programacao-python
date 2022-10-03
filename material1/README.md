# Resumo - print(), input(), if e variáveis

Em programação, utilizamos diversos comandos para indicar para o computador o que nós queremos que ele faça. Damos o nome de **algoritmo** ao conjunto das instruções que damos ao computador.

Ao estudar a linguagem de programação Python, é comum iniciarmos com os seguintes comandos: ```print()```, ```input()``` e ```if```, que podem ser utilizados para gerar uma grande variedade de algoritmos. Além disso, estudamos também as **variáveis**, que nos permitem armazenar temporariamente dados para que possamos utilizá-los em nossos programas. A seguir, veremos cada um desses comandos. 

**IMPORTANTE:** ao longo deste material serão mostrados diversos códigos. É fundamental que você FAÇA OS TESTES você mesmo, seja no computador ou em um interpretador Python para celular. Além disso, tome um tempo para analisar cada código até ter certeza de que você entende o que ele está fazendo. Os primeiros códigos serão bem simples, porém ao fim do material alguns ficarão um pouquinho mais complexos.

## O comando print()

O ```print()``` é usado para fazer o computador escrever algo na tela. Por exemplo, quando queremos mostrar um texto, um número ou uma informação qualquer, usamos o ```print()```. É o comando mais básico do Python. Utilizamos da seguinte maneira:

```python
print("Olá, mundo!")
```

Ao executar, temos o seguinte resultado:

---

Olá, mundo!

---

O programa acima é, sim, um programa de computador, apesar de super simples, e tem como único objetivo exibir na tela o texto “Olá, mundo!”. Podemos utilizar o ```print()``` de diversas formas para exibir quaisquer informações que queiramos, como nos exemplos a seguir (obs.: tudo o que vem após o sinal # na mesma linha são comentários, ou seja, não são códigos de programação, servem apenas para nós, programadores, entendermos melhor o código):

```python
# Escreve na tela o resultado de uma conta:
print(4 + 9) # Aparece o número 13 na tela

# Escreve na tela a junção (concatenação) de duas palavras:
print("Olá," + "amigo") # Aparece o texto "Olá, amigo" na tela
```

Executando:

---

13 <br>
Olá, amigo

--- 

## Variáveis

Uma das ferramentas mais importantes na programação são as variáveis. Variáveis são espaços na memória do computador ao qual atribuímos um nome, que nos permite acessar os dados que lá estão armazenados. Por exemplo, se criamos uma variável chamada “numero”, podemos armazenar algo nela e, sempre que precisarmos da informação que ela armazena, basta chamarmos por seu nome, “numero”. Para criarmos uma variável, usamos o sinal =, que deve ser entendido como um sinal de atribuição, não de igualdade. Ex.:

```python
numero = 5
```

Ao escrevermos essa linha de código, solicitamos ao computador que guarde um dado (que, nesse caso, é o número 5) em sua memória, para que possamos usá-lo quando precisarmos. Por exemplo, digamos que queremos guardar o valor da idade de alguém e mostrar na tela esse número, daí basta fazer o seguinte:

```python
idade = 16
print(idade) # Exibe o número 16 na tela do computador
```

Ao executar, temos:

---

16

---

Podemos ainda utilizar uma variável e inseri-la no meio de um texto para exibi-la de uma forma mais útil, e isso pode ser feito de três formas diferentes em Python. Utilizando o exemplo anterior, veja a seguir as três maneiras para inserir a idade da pessoa no meio de um texto utilizando o comando ```print()```:

```python
idade = 16

# Maneira 1 (difícil leitura, não é tão utilizada):
print("Ele tem", idade, "anos.")

# Maneira 2 (melhor opção até há algum tempo atrás):
print("Ele tem {} anos.".format(idade)) # As chaves {} são substituídas pelo valor da idade

# Maneira 3 (mais atual e atualmente a melhor forma):
print(f"Ele tem {idade} anos.")
```

Se executássemos o programa acima, teríamos o seguinte resultado:

---

Ele tem 16 anos. <br>
Ele tem 16 anos. <br>
Ele tem 16 anos.

---

Ou seja, as três maneiras fizeram exatamente a mesma coisa, porém a maneira 3 (que utiliza o que chamamos de *fstring* por causa do f antes do texto) é claramente a mais eficiente em termos de leitura de código. 

### Tipos de variáveis

Um dos pontos mais importantes no uso de variáveis é o fato de que elas possuem tipos. Existem, tanto em Python quanto em outras linguagens, diversos tipos diferentes de variáveis, usados com propósitos também diferentes, porém inicialmente utilizaremos apenas quatro:

- string: são conjuntos de caracteres, texto. Uma string é facilmente reconhecida por estar sempre entre aspas “ ”. Assim, perceba que os textos que exibimos dentro do comando ```print()``` são, na maior parte dos exemplos vistos anteriormente, strings. Lembre-se que uma string pode ser tanto formada a partir do uso de letras quanto de números, o único requisito é que estejam entre “ ”. Importante também lembrar que NÃO é possível fazer cálculos usando strings. Exemplos de variáveis do tipo string:

```python
palavra = "casa" 
n = "48"
frase = "E aí, tudo bem?"
```

- int: são números inteiros, a partir dos quais podemos fazer cálculos. Exemplos de int:

```python
n = 48
numero = 3
a = n + numero # A variável a recebe o valor 51
```

- float: são números reais, que possuem o chamado ponto flutuante (no Brasil, utilizamos uma vírgula para expressá-los), como, por exemplo, 3.6, 8.44444, 9.0 etc. Exemplos de float:

```python
numero = 8.0
a = 9.56
b = 7.1
```

- bool: são valores booleanos, ou seja, verdadeiro e falso. Em Python, os booleanos são True (verdadeiro) e False (falso), com letra maiúscula mesmo. Geralmente são usados para determinar resultados de condições, como veremos mais à frente. Exemplos de bool:

```python
a = True
b = False
```

Outro detalhe importante é que **Python é uma linguagem dinamicamente tipada**, isto é, a variável adquire um tipo de acordo com o dado que inserimos nela. Para verificarmos isso, podemos utilizar uma função chamada ```type()```, conforme o exemplo:

```python
var = 3
print(type(var))
var = 'virei uma string'
print(type(var))
```

O código acima gera o seguinte resultado:

---

``<class 'int'>`` <br>
``<class 'str'>``

---

Assim, fica claro que inicialmente a variavel ```var```, a qual atribuímos o valor 3, é um int, já quando a modificamos e inserimos o valor "virei uma string", ela passa a ser uma string. Enfim, saber os tipos das variáveis que criamos é muito importante, especialmente porque os tipos estão atrelados a determinados comportamentos. Por exemplo, não é possível somar ou subtrair strings, mas é possível fazer isso com ints e floats. Podemos ver um exemplo de como as variáveis podem ser comportar de formas diferentes a partir do código a seguir:

```python
valor1 = 2
valor2 = 3
print(valor1 + valor2)
valor3 = "2"
valor4 = "3"
print(valor3 + valor4)
```

Nesse código temos quatro variáveis, sendo duas (```valor1``` e ```valor2```) do tipo int e duas (```valor3``` e ```valor4```) do tipo string. Perceba que, por mais que os valores inseridos em cada uma sejam os mesmos (2 e 3), o fato de colocarmos as duas últimas entre aspas "" faz toda a diferença, pois é o que torna ```valor3``` e ```valor4``` strings. Sabendo disso, o mais interessante é o resultado desse código:

---

5 <br>
23

---

Por que aconteceu isso? Como ```valor1``` e ```valor2``` são int, o Python faz sua soma normalmente, de modo que 2 + 3 = 5. No entanto, como ```valor3``` e ```valor4``` são strings, o uso do sinal + não faz a soma realmente, mas sim faz a concatenação (união) das strings, fazendo "2" + "3" = "23"! Esse é apenas um exemplo de diferenças comportamentais entre tipos de variáveis, porém há ainda muitas outras, que serão vistas ao longo de nossos estudos. 

**OBS.:** Ao tratarmos aqui sobre tipos de variáveis em Python, estamos ignorando alguns aspectos técnicos sobre essa linguagem por questão de simplificação (este material é para iniciantes!). Na realidade, Python não implementa os tipos primitivos de variáveis (alguns dos vistos acima, com exceção da string) da mesma forma que outras linguagens. Para entender melhor sobre os tipos de variáveis, vale a pena estudar linguagens como C ou Java. No entanto, para este material, basta saber o que são variáveis e os tipos apresentados. 

## O comando input()

O comando ```input()``` é responsável por permitir que o usuário de nosso software dê entrada em alguma informação solicitada. Por exemplo, imagine que você quer perguntar o nome de seu usuário a fim de exibir uma mensagem de boas-vindas ou de sempre explicar algo chamando-o por seu nome. Ou ainda, podemos pensar em uma situação mais complexa, em que você está construindo uma ferramenta para validar um CPF, aí você precisa que seu usuário proveja essa informação. É aí que entra a importância do ```input()```!

No entanto, é importante lembrar que o ```input()``` praticamente sempre será associado ao uso de uma variável. Afinal de contas, se o usuário vai prover algum dado, é necessário que o armazenemos em algum lugar. Por exemplo:

```python
frase = input()
print(frase)
```

Se executado, esse código esperaria o usuário digitar algo e depois escreveria na tela exatamente o que foi informado. Contudo, da forma como está o código, ao ser executado esse programa simplesmente espera que o usuário digite alguma coisa, mas ele não informa o que digitar! Talvez a leitura do resultado da execução dos códigos a seguir não faça sentido para você, então TESTE o código você mesmo, na ferramenta que estiver a sua disposição. 

Para melhorar nosso código, precisamos dizer para o usuário o que ele deve digitar. Para isso, basta colocarmos o comando para o usuário dentro dos parênteses de ```input()```:

```python
frase = input('Diga alguma coisa: ')
print(frase)
```

Dessa forma, o programa iniciará com a frase "Diga alguma coisa: " na tela. Ao digitar algo e apertar a tecla *enter* no teclado, a frase digitada aparece impressa na linha seguinte. Um exemplo da execução completa desse programa pode ser visto a seguir:

---

Diga alguma coisa: Sabe qual o nome do chefe que dá comandos simples? É o "pythrão"! <br>
Sabe qual o nome do chefe que dá comandos simples? É o "pytrão"!

---

Evidentemente não colocamos nada nesse programa que limitasse aquilo que o usuário poderia escrever, o que quase sempre é um problema. O ideal é sempre criarmos formas de nosso programa não quebrar por conta de um ```input()``` errado de nosso usuário, porém isso é assunto para outro momento. 

Outro ponto muito imporante que precisamos levar em consideração ao usar o ```input()``` é o fato de que essa função retorna sempre uma string, ou seja, não importa se seu usuário digitar uma palavra ou um número, a variável em que o ```input()``` foi armazenado será do tipo string. No entanto, podemos convertê-la facilmente para outros tipos de acordo com a nossa necessidade. Veja o exemplo abaixo:

```python
var1 = input('Digite algo que será uma string: ')
var2 = int(input('Digite algo que será um int: '))
var3 = float(input('Digite algo que será um float: '))

print(f'Sua string: {var1}')
print(f'Seu int: {var2}')
print(f'Seu float: {var3}')
```

Perceba que para ```var2``` e ```var3```, colocamos a função ```input()``` dentro de uma função chamada ```int()``` e de outra chamada ```float()```, responsáveis por converter a string gerada pelo ```input()``` em um int e um float, respectivamente. Ao fazer isso, também limitamos o que nosso usuário pode escrever: se ele escrever uma palavra em vez de um número (nas situações em que um número é solicitado), ocorrerá um erro no programa, informando que não é possível converter uma palavra para um int ou um float. A seguir, veja primeiro uma execução normal desse programa e depois uma em que um erro acontece:

---

Digite algo que será uma string: casa <br>
Digite algo que será um int: 3 <br>
Digite algo que será um float: 54 <br>
Sua string: casa <br>
Seu int: 3 <br>
Seu float: 54.0 <br>

---

Agora, veja o que ocorre quando inserimos um valor que não pode ser convertido:

---

Digite algo que será uma string: olá <br>
Digite algo que será um int: tudo bem? <br>
Traceback (most recent call last): <br>
  File "/home/danlibs/Documentos/Repositórios/Programming-Exercises/Scripts Python/Tests.py", line 2, in <module> <br>
    var2 = int(input('Digite algo que será um int: ')) <br>
ValueError: invalid literal for int() with base 10: 'tudo bem?' <br>

---

Vá desde já se familiarizando com os erros de execução! No caso acima, é informado que na linha ```var2 = int(input('Digite algo que será um int: '))``` ocorreu um ValueError (erro de valor), e que o dado 'tudo bem?' não é válido para a função ```int()``` funcionar. Erros como esse serão tratados em um outro momento.

De posse dessas informações, você já tem um grande aparato para criar diversos algoritmos! Podemos, por fim, visualizar um exemplo simples de um programa que solicita dois números para o usuário e retorna a operação de soma montada, além de seu resultado:

```python
primeiro_numero = int(input('Informe um valor: '))
segundo_numero = int(input('Informe outro valor: '))
print(f'{primeiro_valor} + {segundo_valor} = {primeiro_valor + segundo_valor}')
```

Ao executar, podemos ter o seguinte cenário:

---

Informe um valor: 4 <br>
Informe outro valor: 6 <br>
4 + 6 = 10

---

## O comando if

O comando ```if``` (que significa, literalmente, *se* em português) é o mais básico para criar o que chamamos na programação de **estrutura condicional**. Como o próprio nome já deixa claro, trata-se de uma forma de criarmos condições que, se forem verdadeiras, darão início à execução de um determinado bloco de código e, se forem falsas, podem ou não também dar execução a um bloco de código diferente. Há outras formas de criarmos condições, seja em Python ou outras linguagens, porém aqui nos ateremos apenas ao ```if```.

A sintaxe básica do if é:

```python
if condicao:
    # insira seu código aqui
```

Em outras palavras, chamamos a palavra-chave ```if```, indicamos a condição que deve ser atendida e, se esta for verdadeira, o código seguinte é executado. Num exemplo bem simplificado:

```python
x = 5
if x < 10:
    print(f'{x} é menor que 10!')
```

Ao executarmos:

---

5 é menor que 10!

---


