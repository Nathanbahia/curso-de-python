# Aula 3 - Estruturas de Dados - Parte I

Como temos visto, em programação em Python podemos usar variáveis para poder armazenar valores como números e textos. 

### Os números se dividem em dois grupos:
- Inteiros (int): Números inteiros
- Fracionados (float): Números com casas decimais

### Os textos:
- String (str): Textos, números, espaços, etc... Sempre declarados dentro de aspas, simples (') ou duplas (").

Essas estruturas de dados já vimos e usamos bastante nas últimas aulas. Agora, vamos conhecer algumas outras que são extremamente úteis no desenvolvimento de sistemas.

### Booleanos
Os boleanos podem conter apenas dois valores: True (verdadeiro) ou False (falso), ambos com iniciais maiúsculas. Quando realizamos uma comparação, em um bloco ```if```, por exemplo, obtemos um resultado boleano mesmo sem porceber. Por exemplo:

{% highlight python %}
if idade == 18:
  # se esta comparação for verdadeira...
  print("Maior de idade")
else:
  # se esta comparação for falsa...
  print("Menor de idade")
{% endhighlight %}


Outro exemplo:
```console
motor_ligado = False
combustivel = 100

if motor_ligado == True:
  combustivel = combustivel - 10
  print(f"O nível de combustível está em {combustivel}")

if motor_ligado == False:
  print(f"O nível de combustível está em {combustivel}")
```

### Listas
As listas (list) são estruturas de dados muito utilizadas em conjunto de estruturas de repetição (estudaremos sobre o assunto mais adiante). Sua função é armazenar diversos valores dentro de uma única variável.

#### Criação de uma lista
```console
minha_lista = []
```
No exemplo acima, criamos uma lista vazia, com o uso de colchetes. Também podemos criar listas com valores pré-definidos.

```console
minha_lista = [1, 2, 3]
```
Criamos uma lista com 3 valores, separados por vírgula. 

#### Listas armazenam diversos tipos de valores, às vezes simultâneamente
```console
minha_lista = ['Brasil', 10, 3.14]
```
Podemos armazenar diversos tipode de dados em uma única lista.

#### Podemos inserir novos elementos em uma lista
```console
minha_lista = []
minha_lista.append(3)
print(minha_lista)
>>> [3]
```
Podemos inserir novos dados dentro de uma lista usando a função append, que insere o valor ao final da lista.


#### Consultando o tamanho de uma lista
```console
minha_lista = [1, 2, 3]
tamanho_da_lista = len(minha_lista)
print(tamanho_da_lista)
>>> 3
```
Podemos armazenar o valor da quantidade de elementos de uma lista usando a função len()

#### Soma dos elementos de uma lista
```console
minha_lista = [1, 2, 3]
soma_dos_elementos = sum(minha_lista)
print(soma_dos_elementos)
>>> 6
```
Quando todos os elementos de uma lista forem numéricos, é possível obter a soma dos valores de seus elementos usando a função sum()


#### Consultado valores por indices
```console
minha_lista = [1, 2, 3, 4, 5]

primeiro_elemento = minha_lista[0]
print(primeiro_elemento)
>>> 1
```
Podemos recuperar um único valor de uma lista e usá-lo ou guardá-lo em outra variável usando o conceito de slice. Ao usar o nome da lista e ao lado um par de conchetes com um número, acessamos o elemento da lista que corresponde a esse índice. No exemplo acima, acessamos o elemento 0, cujo valor é 1. As listas iniciam a contagem dos elementos sempre no indice 0. Por tanto, os elementos da lista acima são os seguintes:

```console
minha_lista[0] == 1
minha_lista[1] == 2
minha_lista[2] == 3
minha_lista[3] == 4
minha_lista[4] == 5
```

Caso tentemos acessar um valor com um índice que não existe, obtermos um erro do Python:
```console
minha_lista[5]
>>> IndexError: list index out of range
Significado do erro: Não existe nenhum elemento dentro da lista que corresponda a esse indice.
```

#### Sobrescrevendo valores de uma lista
```console
minha_lista = [1, 2, 3]
print(minha_lista)
>>> [1, 2, 3]
minha_lista[0] = 10
print(minha_lista)
>>> [10, 2, 3]
```
Também podemos sobreescrever valores de uma lista. Usando o índice do elemento que se deseja sobrescrever, podemos atribuir um novo valor da mesma forma que faríamos com qualquer tipo de variável.

#### Removendo elementos de uma lista

```console
minha_lista = [5, 9, 6, 8, 10]
del minha_lista[4]
print(minha_lista)
>>> [5, 9, 6, 8]
```
No exemplo acima, deletamos o elemento de índice 4, cujo valor era 10.
