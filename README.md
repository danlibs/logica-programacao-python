# Resumo - print(), input(), if e variáveis

Em programação, utilizamos diversos comandos para indicar para o computador o que nós queremos que ele faça. Damos o nome de **algoritmo** ao conjunto das instruções que damos ao computador.

Utilizando a linguagem de programação Python, estudamos até os seguintes comandos: print(), input() e if, que podem ser utilizados para gerar uma grande variedade de algoritmos. Além disso, estudamos também as **variáveis**, que nos permitem armazenar temporariamente dados para que possamos utilizá-los em nossos programas. A seguir, veremos cada um desses comandos.

## O comando print()

O print() é usado para fazer o computador escrever algo na tela. Por exemplo, quando queremos mostrar um texto, um número ou uma informação qualquer, usamos o print(). É o comando mais básico do Python. Utilizamos da seguinte maneira:

```python
print("Olá, mundo!")
```

O programa acima é, sim, um programa de computador, apesar de super simples, e tem como único objetivo exibir na tela o texto “Olá, mundo!”. Podemos utilizar o print() de diversas formas para exibir quaisquer informações que queiramos, como nos exemplos a seguir (obs.: tudo o que vem após o sinal # são comentários, não são interpretados como comandos de programação):

```python
# Escreve na tela o resultado de uma conta:
print(4 + 9) # Aparece o número 13 na tela

# Escreve na tela a junção (concatenação) de duas palavras:
print("Olá," + "amigo") # Aparece o texto "Olá, amigo" na tela
```

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

Podemos ainda utilizar uma variável e inseri-la no meio de um texto para exibi-la de uma forma mais útil, e isso pode ser feito de três formas diferentes em Python. Utilizando o exemplo anterior, veja a seguir as três maneiras para inserir a idade da pessoa no meio de um texto utilizando o comando print():

```python
idade = 16

# Maneira 1 (difícil leitura, não é tão utilizada):
print("Ele tem", idade, "anos.")

# Maneira 2 (melhor opção até há algum tempo atrás):
print("Ele tem {} anos.".format(idade)) # As chaves {} são substituídas 
																				# pelo valor da idade

# Maneira 3 (mais atual e atualmente a melhor forma):
print(f"Ele tem {idade} anos.")
```

Se executássemos o programa acima, teríamos o seguinte resultado:

```python
Ele tem 16 anos.
Ele tem 16 anos.
Ele tem 16 anos.
```

Ou seja, as três maneiras fizeram exatamente a mesma coisa, porém a maneira 3 (que utiliza o que chamamos de *fstring* por causa do f antes do texto) é claramente a mais eficiente em termos de leitura de código. 

Voltando às variáveis, é importante lembrar que elas possuem tipos. Existem, tanto em Python quanto em outras linguagens, diversos tipos diferentes de variáveis, usados com propósitos também diferentes, porém inicialmente utilizaremos apenas quatro:

- string: são conjuntos de caracteres, texto. Uma string é facilmente reconhecida por estar sempre entre aspas “ ”. Assim, perceba que os textos que exibimos dentro do comando print() são, na maior parte dos exemplos vistos anteriormente, strings. Lembre-se que uma string pode ser tanto formada a partir do uso de letras quanto de números, o único requisito é que estejam entre “ ”. Importante também lembrar que NÃO é possível fazer cálculos usando strings. Exemplos de variáveis do tipo string:

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

## O comando input()
