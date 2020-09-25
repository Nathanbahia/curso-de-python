# AULA 2 - CONDIÇÕES

Nem sempre todas as linhas dos programas serão executadas. Muitas vezes, será mais interessante decidir que partes do programa devem ser executadas com base no resultado de uma condição. A base dessas decisões consistirá em expressões lógicas que permitam representar escolhas em programas.

### Exemplos de expressões lógicas: 
 - Valor da fatura menor que 500 reais = SIM OU NÃO
 - Idade é maior que 18 anos = SIM OU NÃO
 - Usuário e senha cadastrados = SIM OU NÃO

As condições servem para selecionar uma parte do programa que deve ser ativada e quando deve ser ignorada.

#### OBERVAÇÃO IMPORTANTE!
Os operadores relacionais (usados para avaliações de expressões lógicos) são os seguintes:
```
== Igualdade
!= Diferente
> Maior
>= Maior ou igual
< Menor
<= Menor ou igual
```

É comum confundir os sinais == e =. O sinal de = é usado apenas para atribuição de valores, e nunca para comparação de dois valores. Então:

```
a = 5 (Lê-se, a recebe 5)
a == 5 (Lê-se, a é igual a 5???)

```
Exemplo: ```idade == 18``` tem apenas duas respostas: é igual ou não


## CLÁUSULA IF

Em Python, a estrutura de decisão é o if, que nada mais é que nosso "se". 

**Vejamos um exemplo em português:**
```
numero_1 = 4
numero_2 = 9

se o numero_1 for maior que o numero_2:
	exiba("O primeiro número é maior que o segundo")

se o numero_2 for maior que o numero_1:
	exiba("O segundo número é maior que o primeiro")
```

**Em Python:**
```
numero_1 = 4
numero_2 = 9

if numero_1 > numero_2:
	print("O primeiro número é maior que o segundo")

if numero_2 > numero_1:
	print("O segundo número é maior que o primero")
```

Observe que as linhas onde o if aparece terminam em " : ". Quando isso acontece, temos o anúncio de um bloco de linhas a seguir. Em Python, um bloco é representado deslocando-se o início da linha para a direita. O bloco continua até a primeira linha com deslocamento diferente. Para deslocar o texto à direita, utilize espaços, normalmente 4, ou pressione a tecla TAB para cada nível de indentação. É importante adotar uma única metodologia, para que o projeto seja desenvolvido de maneira padronizada. Eu recomendo apenas o uso do TAB, por ser mais prático e mais utilizado. Caso o recuo no início de um bloco não seja realizado, o Python gerará um erro (SyntaxError: expected an indented block).


# ------------------------------------------
#### (EXERCÍCIOS DE 1 A 3)
# ------------------------------------------



## CLÁUSULA ELSE

Quando a segunda condição for simplesmente o inverso da primeira, podemos usar outra forma de if para simplificar os programas. Essa forma é a cláusula else (senão) para especificar o que fazer caso o resultado da avaliação da condição seja falso, sem precisarmos de um novo if. 

Vejamos novamente o exemplo do carro velho:

```
idade = int(input("Digite a idade de seu carro: "))
if idade < 5:
	print("O carro é novo.")
else:
	print("O carro é velho.")
```

Veja que também utilizamos os " : " após o else, porque ele inicia um novo bloco, da mesma forma que o if, ou seja, com o mesmo recuo.

# ------------------------------------------
#### (EXERCÍCIO 4)
# ------------------------------------------


## BLOCOS ANINHADOS

Nem sempre nossos programas serão tão simples. Muitas vezes, precisamos aninhar vários if para obter o comportamento desejado. Aninhar, nesse caso, significa colocar um if dentro de outro.

Exemplo:
```
#Programa que define preço de produto por categoria
# Categoria 1 = R$ 10, 00
# Categoria 2 = R$ 20, 00
# Categoria 3 = R$ 30, 00

categoria = int(input("Digite a categoria do produto: "))

if categoria == 1:
	preco = 10
else:
	if categoria == 2:
		preco = 20
	else:
		if categoria == 3:
			preco = 30
```

Veja que para cada bloco de else, um novo if foi criado, aumentando o nível de recuo do código cada vez mais, prejudicando a legibilidade do programa.

### CLÁUSULA ELIF

O Python apresenta uma solução muito interessante ao problema de múltiplos if aninhados. A cláusula elif, (senão se) substitui um par de else if, mas sem ser necessário criar um novo nível de recuo no código. Veja o código acima refatorado.

```
categoria = int(input("Digite a categoria do produto: "))

if categoria == 1:
	preco = 10

elif categoria == 2:
	preco = 20

elif categoria == 3:
	preco = 30

else:
  print("Opção inválida")
  preco = "inválido"

print(f"Preço: R$ {preco}")
```

Essa estrutura é indicada para situações nas quais as condições não são apenas duas, como no caso do exemplo do carro, onde era apenas analisado um limite de idade (5), sendo considerado novo ou velho. Com o elif, seria fácil desenvolver um programa que considerasse classificações como novo, semi-usado e velho, com limites de idades distintos por exemplo.

# ------------------------------------------
#### (EXERCÍCIO 5 E DESAFIO)
# ------------------------------------------
