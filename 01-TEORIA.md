# AULA 1 - VARIÁVEIS

### O que é uma variável?
Variável é um nome que armazena um valor, que pode ser um número, texto, uma expressão matemática, etc. Uma variável pode ser declarada (criada) em qualquer lugar do código e deve seguir algumas regras e recomendações de boas práticas para serem criadas.

#### Regras para nomes de variáveis:
1. Não podem começar com números:
- 👎 ```1var```
- 👍 ```var1```
2. Não pode conter acentos:
- 👎 ```variável```
- 👍 ```variavel```
3. Não pode conter símbolos, exceto o underscore &quot;_&quot;:
- 👎 ```minha-variável```
- 👍 ```minha_variavel```

#### Boas práticas:
Ainda que alguns nomes de variáveis sejam válidos, eles devem ser evitados para seguir as boas práticas de programação.
1. Os nomes devem começar com letras minúsculas: ```valor_do_investimento```
2. Os nomes devem descrever o seu conteúdo: ```taxa_de_juros```
3. Deve-se evitar nomes genéricos: ```n1```, ```n2```, ```var```, etc...

#### Atribuição de valores à variáveis
Para criar uma variável, devemos simplesmente criar um nome e atribuir um valor a ele, como em: ```taxa_de_juros = 2```.
Usamos o sinal de igual para dizer que a variável taxa_de_juros tem o valor 2.

### Terminal Python
Para testar a criação de uma variável, podemos usar o terminal Python (IDLE). Para imprimir um valor na tela, usaremos a função ```print()``` que será explicada mais detalhadamente adiante. Para tanto, teste o seguinte código (desconsiderando os números à esquerda, que indicam apenas a numeração da linhas):
```
1 meu_nome = “Nathan”
2 print(meu_nome)
3 meu_nome = “Bahia”
4 print(meu_nome)
```

A função ```print``` recebe um valor ou uma variável dentro de um par de parêntesis e exibe seu valor na tela. Mais adiante abordarei com mais detalhes essa função. Observe que na linha 1, atribuímos à variável ```meu_nome``` o valor “Nathan”, e na linha dois imprimimos seu valor. Fazemos o mesmo procedimento nas linhas 3 e 4, obtendo um resultado diferente. O que acontece é que um script é lido de cima para baixo, e quando fazemos a atribuição de valor em alguma variável que já existe, estamos sobrescrevendo seu valor. Ou seja, nas linhas 1 e 3, estamos alterando o valor da mesma variável.

#### Números e textos
No Python, existem diversas estruturas de dados, mas para uma rápida introdução, é importante conhecer os números e textos. 

##### Números
Os números são divididos em dois grupos: inteiros (int) e de ponto flutuante (float). Os ```int``` são qualquer número sem casas decimais, enquanto que os ```float``` os que têm casas decimais com separação entre a parte inteira e a decimal com uso do ponto (3.14 por exemplo). A criação de variáveis numéricas se dá basicamente com a passagem do valor ao nome, como:
```
taxa_de_juros_mensal = 0.2
valor_do_investimento = 15000
```
As strings (str), são textos, espaços em branco, números, etc. que são delimitados por aspas (simples ou duplas) no seu início e fim, como:
```
meu_nome = "Nathan"
nome_e_sobrenome = "Nathan Bahia"
espaço = " "
pi = "3.14"
telefone = "11 99911 1234"
email = "python@email.com"
```
Observe que mesmos números declarados entre aspas serão considerados textos.

#### Cálculos no terminal
Para a realização de cálculos, o Python utiliza dos seguintes operadores aritméticos:
```
*  multiplicação
/  divisão
+  adição e concatenação
-  subtração
** potências e raízes
```
Uma vez declaradas as variáveis, podemos realizar cálculos e operações usando-as, como exemplo:
```
1 taxa_de_juros_mensal = 0.2
2 valor_do_investimento = 15000
3 retorno_mensal = valor_do_investimento * taxa_de_juros_mensal
4 print(retorno_mensal)
```
No código acima criamos nossas variáveis nas linhas 1 e 2, realizamos o cálculo na linha 3 e atribuímos à variável ```retorno_mensal``` o resultado da operação, em seguida imprimimos o resultado usando a função ```print()```.

Assim como na matemática tradicional, é importante entender a ordem na qual as operações são executadas. Isso se chama ordem de precedência. Exemplos:
```
4 + 5 * 2 = 14
(4 + 5) * 2 = 18
10 / 2 + 3 = 8
10 / (2 + 3) = 2
2 ** 2 + 6 = 10
```
Outro exemplo:
```
1 meu_nome = “Nathan”
2 texto_a = “Olá, “
3 texto_b = “. É um prazer te conhecer.”
4 texto_final = texto_a + meu_nome + texto_b
4 print(texto_final)
```
Criamos nossas variáveis de texto nas linhas de 1 a 3. Na linha 4 realizamos uma operação de concatenação de string, ou seja, juntamos o conteúdo das variáveis ```meu_nome```, ```texto_a``` e ```texto_b``` na variável ```texto_final```, em seguida imprimimos o conteúdo da variável ```texto_final``` com a função ```print()```.

### Conclusão
O uso das variáveis num primeiro contato pode parecer estranho, mas é de suma importância, já que ao longo do desenvolvimento de um software precisamos guardar diversos valores e usá-los em várias operações. Se usássemos apenas valores literais (uso de valores diretamente), todo o processo de desenvolvimento seria extramamente complicado. Veja o seguinte exemplo sem o uso de variáveis:

```
print( (-5 + (5**2 - 4 * 2 * 3) ) / (2 * 3))
print( (-5 - (5**2 - 4 * 2 * 3) ) / (2 * 3))
```

Agora com o uso de variáveis:

```
# Fórmula de baskara
a = 3
b = 5
c = 2
delta = (5**2) - (4 * a * c)
x1 = ( -b + delta ** (1/2) ) / (2 * a)
x2 = ( -b - delta ** (1/2) ) / (2 * a)
print(f"As raízes da equação são: {x1} e {x2}")
```

No primeiro exemplo, somente saberá do que se trata o código a pessoa que o está escrevendo, enquanto que no segundo, mesmo uma pessoa que não saiba que se trata de um código de programação conseguirá entender o raciocínio do programador. Além disso, caso seja necessário alterar os valores da equação, essa mudança se dará apenas nas atribuições das variáveis ```a```, ```b``` e ```c```, enquanto que no primeiro exemplo, todos os valores deverão ser alterados manualmente, o que pode (e com grande problabilidade vai) causar erros na execução do programa e no resultado esperado.
