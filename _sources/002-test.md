# Conceitos Gerais da Linguagem Python


## A Linguagem Python


```python
print('Primeiro código!')
```

    Primeiro código!


## Tipos Básicos e Variáveis


```python
valor_int = 3  # Tipo inteiro
valor_float = 1.5  # Tipo ponto flutuante
string = "Olá Mundo!"  # Tipo string
var_bool = True  # Tipo booleano

print(type(valor_int))
print(type(valor_float))
print(type(string))
print(type(var_bool))
```

    <class 'int'>
    <class 'float'>
    <class 'str'>
    <class 'bool'>



```python
valor_int  = 15
valor_float = 1.5
soma = valor_int + valor_float
print(soma)
print(type(soma))
```

    16.5
    <class 'float'>



```python
# Conversão de um valor do tipo inteiro para um valor do tipo string
a = 100
b = str(a)
print(b)
print(type(b))

# Conversão de um valor do tipo float para um valor do tipo inteiro
c = 12.0
d = int(c)
print(d)
print(type(d))

# Conversão de um valor do tipo inteiro para um valor do tipo float
e = 10
f = float(e)
print(f)
print(type(f))
```

    100
    <class 'str'>
    12
    <class 'int'>
    10.0
    <class 'float'>


## Expressões


```python
a = 10
b = 3

# Soma do valor de duas variáveis
soma = a + b

# Subtração do valor de duas variáveis
sub = a - b

# Divisão do valor de duas variáveis
div = a / b

# Multiplicação do valor de duas variáveis
mult = a * b

print('Soma: %d' % (soma))
print('Subtração: %d' % (sub))
print('Divisão: %d' % (div))
print('Multiplicação: %d' % (mult))
```

    Soma: 13
    Subtração: 7
    Divisão: 3
    Multiplicação: 30



```python
# Resto de uma divisão de um valor do tipo inteiro por outro valor do tipo inteiro
res = a % b

# Resultado de elevar um valor do tipo inteiro a outro valor do tipo inteiro
exp = a ** b

# Piso, parte inteira de uma divisão de valores do tipo inteiro
pis = a // b

print('Resto: %d' % (res))
print('Exponencial: %d' % (exp))
print('Piso da divisão: %d' % (pis))
```

    Resto: 1
    Exponencial: 1000
    Piso da divisão: 3



```python
nome = 'Robson'
idade = 28
altura = 1.85

print('Meu nome é %s, tenho %d anos e %.2f de altura!' % (nome, idade, altura))
```

    Meu nome é Robson, tenho 28 anos e 1.85 de altura!



```python
aux_01 = 2
aux_02 = 3

print('O valor da primeira variável é {} enquanto o da segunda é {}'.format(aux_01, aux_02))
```

    O valor da primeira variável é 2 enquanto o da segunda é 3


## Operadores Relacionais


```python
a = 5
b = 2

c = a < b
d = a > b
e = a == b

print('Valor de c:', c)
print('Valor de d:', d)
print('Valor de e:', e)
print(a >= b)
print(b <= b)
```

    Valor de c: False
    Valor de d: True
    Valor de e: False
    True
    True



```python
a = 10
b = 2

a += b  # a + b
print(a)

a -= b  # a - b
print(a)

a /= b  # a / b
print(a)

a *= b  # a * b
print(a)
```

    12
    10
    5.0
    10.0



```python
nome = input('Qual seu nome? ')
idade = int(input('Qual sua idade? '))
altura = float(input('Qual sua altura? '))
peso = float(input('Qual seu peso? '))

print('Nome: %s' % nome)
print('Idade: %d' % idade)

imc = peso / ( altura * altura )
print('O IMC =', imc)
print('Muito abaixo do peso:', imc < 17)
print('Abaixo do peso normal:', imc >= 17 and imc < 18.5)
print('Peso dentro do normal:', imc >= 18.5 and imc < 25.0)
print('Acima do peso normal:', imc >= 25 and imc < 30)
print('Muito acima do peso:', imc >= 30)
```


    ---------------------------------------------------------------------------

    StdinNotImplementedError                  Traceback (most recent call last)

    Cell In[11], line 1
    ----> 1 nome = input('Qual seu nome? ')
          2 idade = int(input('Qual sua idade? '))
          3 altura = float(input('Qual sua altura? '))


    File ~/miniconda3/envs/book/lib/python3.9/site-packages/ipykernel/kernelbase.py:1190, in Kernel.raw_input(self, prompt)
       1188 if not self._allow_stdin:
       1189     msg = "raw_input was called, but this frontend does not support input requests."
    -> 1190     raise StdinNotImplementedError(msg)
       1191 return self._input_request(
       1192     str(prompt),
       1193     self._parent_ident["shell"],
       1194     self.get_parent("shell"),
       1195     password=False,
       1196 )


    StdinNotImplementedError: raw_input was called, but this frontend does not support input requests.


## Comandos Condicionais - if


```python
nota = int(input('Digite uma nota: '))

if nota < 60:
    print('Reprovado')
else:
    print('Aprovado')
```


```python
nota = int(input('Digite uma nota: '))

if nota < 30:
    print('Reprovado')
elif nota <= 50:
    print('Recuperação')
else:
    print('Aprovado')
```


```python
n1 = int(input('Digite o primeiro número: '))
n2 = int(input('Digite o segundo número: '))

if n1 > n2:
    print(n1, 'maior que', n2)
elif n1 < n2:
    print('%d maior que %d' % (n2, n1))
else:
    print('Os números são iguais')
```

## Comandos de Repetição - while


```python
while (expressão condicional):
    bloco de comandos
```


```python
contador = 1

while contador <= 5:
    print(contador)
    contador += 1
```


```python
nota = -1
while nota < 0 or nota > 10:
    nota = int(input('Digite uma nota válida de 0 a 10: '))

print('Nota: %s' % nota)
```

## Comandos de Repetição - for


```python
for (número de iterações):
    bloco de comandos
```


```python
print(list(range(5)))
print(list(range(1, 5)))
print(list(range(2, 10, 3)))
```


```python
for i in range(5):
    print('Bem-vindo ao curso de Python!')
```


```python
for i in range(0, 5):
    print(i)
```


```python
for i in range(0, 10, 2): # Varia de 0 a 10, mas aumentando de 2 em 2
    print(i)
```


```python
total = 0

for i in range(0, 5):
    num = int(input('Digite um num: '))
    total += num

print('Soma: %s' % (total))
print('Media: %s' % (total/5))
```


```python
tab=int(input('Tabuada do número: '))

for i in range(10):
    print('%d x %d = %d' % (tab, i + 1, tab * (i + 1)))
```

## Estruturas de Dados - Listas


```python
lista = []

print(lista)
```


```python
lista_num = [1, 2, 3]
lista_nomes = ['André', 'Ângelo', 'Robson']
lista_misturada = [37, 'Ângelo', 'Robson', 9, 0, 'Maria', 2]

print(lista_num)
print(lista_nomes)
print(lista_misturada)
```


```python
for item in lista_num:
    print(item)
    
print(lista_nomes[0])
print(lista_nomes[1])
```


```python
lista = [1, 2, 3, 3, 3, 4, 5, 6, 7]

print('Tamanho da lista: %d' % len(lista))

lista.append(8)
print(lista)

lista.pop()
print(lista)

lista.pop(0)
print(lista)

lista.remove(2)
print(lista)
```


```python
lista.insert(0, 1)  # Posição 0, item 1
print(lista)

print(lista.count(3))

print(lista.index(1))

lista.clear()
print(lista)
```


```python
lista = [1, 2, 3, 4, 5]

print(lista[::-1])  # Inverte a ordem dos itens em uma lista

print(lista[0:2])  # Retorna os valores que estão nas posições do intervalo

print(lista[-1])  # Retorna o último item da lista

lista.sort()  %# Ordenar

print(lista)

lista[0] = 2  # Alterar item

print(lista)
```

## Estruturas de Dados - Tuplas


```python
tupla_num = (1, 2, 3, 4)
print(tupla_num)
```


```python
print(tupla_num.count(1))
print(tupla_num.index(2))
print(len(tupla_num))
```


```python
# Convertendo tupla em lista
tupla_conv = list(tupla_num)

# Adicionando um item na última posição
tupla_conv.append(5)
print("Elemento 5 adicionado: %s" % (tupla_conv))

# Removendo o item adicionado
tupla_conv.pop()
print("Elemento 5 removido: %s" % (tupla_conv))
```

## Estruturas de Dados - Conjuntos


```python
frutas = ['maçã', 'laranja', 'maçã', 'pera', 'laranja', 'banana']

frutas_n_duplicados = set(frutas)

print(frutas_n_duplicados)
```

## Estruturas de Dados - Dicionários


```python
dic = {}  # chave e valor

dic = dict()

print(dic)
```


```python
# Criação de um dicionário com preço de frutas por kg
dic_frutas = {'Maçã': 5.50,
              'Banana': 2.50,
              'Pera': 6.50,
              'Uva': 7.20}

# Inserção de um novo item, fruta e seu preço, em um dicionário
dic_frutas['Manga'] = 6.20

print(dic_frutas)
```


```python
# Alteração do preço de uma fruta, banana, armazenada em um dicionário
dic_frutas['Banana'] = 1.50
print(dic_frutas)
```


```python
# Consulta do preço de uma fruta armazenada em um dicionário
print('Uva: %s' % dic_frutas['Uva'])
print('Pera: %s' % dic_frutas['Pera'])
```


```python
# Criação de um dicionário com o desempenho de atletas
atletas = {}  

# Atribuição de um nome fictício, início, a um dicionário
nome_atleta = 'início'  

# Inclusão do nome de atletas em um dicionário
while nome_atleta != '': 
    nome_atleta = input('Atleta: ')
    if nome_atleta != '':
        saltos = []  # Lista para armazenar a distância dos saltos
        for i in range(0, 2):  # 2 saltos
            saltos.append(float(input('%s Salto: ' % (i + 1))))
        
        # Adicionando uma lista de saltos ao dicionário
        atletas[nome_atleta] = saltos 


# Percorrer um dicionário  retornando seus itens  
print('\nResultado Final:')
for nome_atleta, saltos in atletas.items():
    print('Atleta: %s' % nome_atleta)
    print('Saltos: ', str(saltos))
    print('Média dos Saltos: %.2f m' % (sum(saltos)/2))
```


```python
dic_frutas = {'Maçã': 5.50,
              'Banana': 2.50,
              'Pera': 6.50}

for fruta, valor in dic_frutas.items():
    print('Fruta: %s' % fruta)
    print('Preço: %s' % valor)
```

## Funções


```python
def nome_funcao(parametro_um, parametro_dois, ...):
    comando
    ...
    comando
    return dados
```


```python
# Trecho que define a função
def soma(x, y, z):
    return x + y +z

# Trecho em que a função é chamada
s = soma(10, 20, 40)
print(s)
```


```python
# Trecho que define a função
def par_impar(n):
    if n % 2 == 0:
        return True
    else:
        return False

# Trecho em que a função é chamada
print(par_impar(10))
print(par_impar(15))
```


```python
# Trecho que define a função
def imc(nome, idade, altura, peso):
    print('Nome: %s' % nome)
    print('Idade : %d' % idade)
    
    imc = peso / ( altura * altura )
    print('O IMC = ', imc)

    if imc < 17:
        print('Muito abaixo do peso')
    elif imc >= 17 and imc < 18.5:
        print('Abaixo do peso normal')
    elif imc >= 18.5 and imc < 25.0:
        print('Peso dentro do normal')
    elif imc >= 25 and imc < 30:
        print('Acima do peso normal')
    else:
        print('Muito acima do peso')

# Trecho em que a função é chamada
imc('Robson', 28, 1.85, 98)
```

## Funções de Entrada e Saída


```python
doc = open('doc.txt', 'r')
for linha in doc.readlines():
    print(linha)
doc.close()
```


```python
# Utilização da função split() para decompor uma \textit{string} em uma lista.
doc = open('doc.txt', 'r')

# Decomposição do \textit{string} separando componentes por vírgulas para gerar um arquivo do tipo csv
for linha in doc:
    valores = linha.split(',')
    print(valores[0], valores[1], valores[2], valores[3])
```


```python
doc = open('doc.txt', 'a')

# Adição de uma nova linha
doc.write('Iris, ')
doc.write('01414, ')
doc.write('8.5, ')
doc.write('7.5 ')
doc.write("\n")  # Quebra de linhas
doc.close()

# Leitura do arquivo com a nova linha
doc = open('doc.txt', 'r')
for linha in doc.readlines():
    print(linha)
doc.close()
```
