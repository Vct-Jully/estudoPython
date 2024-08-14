# Algumas funções básicas e algoritmos de base em Python


# Guia de Estruturas e Funções em Python

---

## 1. Listas e Manipulação de Listas

### 1.1 Criando e Acessando Listas

```python
# Criando uma lista
frutas = ["maçã", "banana", "cereja"]

# Acessando elementos da lista
print(frutas[0])  # Saída: maçã
print(frutas[1])  # Saída: banana
```

### 1.2 Modificando Listas:

```python
# Adicionando elementos
frutas.append("laranja")
print(frutas)  # Saída: ["maçã", "banana", "cereja", "laranja"]

# Removendo elementos
frutas.remove("banana")
print(frutas)  # Saída: ["maçã", "cereja", "laranja"]

# Inserindo elementos em uma posição específica
frutas.insert(1, "kiwi")
print(frutas)  # Saída: ["maçã", "kiwi", "cereja", "laranja"]
```

### 1.3 Listas Aninhadas

```python
# Lista de listas
matriz = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

# Acessando elementos
print(matriz[0][1])  # Saída: 2
print(matriz[2][2])  # Saída: 9
```
---

## 2. Tuplas

### 2.1 Criando e Acessando Tuplas

```python
# Criando uma tupla
coordenadas = (10, 20)

# Acessando elementos
print(coordenadas[0])  # Saída: 10
print(coordenadas[1])  # Saída: 20
```
---

## 3. Dicionários

### 3.1 Criando e Acessando Dicionários

```python
# Criando um dicionário
aluno = {"nome": "Alice", "idade": 22, "curso": "Engenharia"}

# Acessando elementos
print(aluno["nome"])  # Saída: Alice
print(aluno["idade"])  # Saída: 22
```

### 3.2 Modificando Dicionários

```python
# Adicionando elementos
aluno["universidade"] = "USP"
print(aluno)  # Saída: {"nome": "Alice", "idade": 22, "curso": "Engenharia", "universidade": "USP"}

# Removendo elementos
del aluno["curso"]
print(aluno)  # Saída: {"nome": "Alice", "idade": 22, "universidade": "USP"}
```
---

## 4. Funções

### 4.1 Criando Funções

```python
def saudacao(nome):
    return f"Olá, {nome}!"

print(saudacao("Carlos"))  # Saída: Olá, Carlos!
```

### 4.2 Passando Argumentos

```python
def soma(a, b):
    return a + b

print(soma(5, 7))  # Saída: 12
```

## 5. Compreensões de Listas e Generators

### 5.1 Compreensões de Listas

```python
# Criando uma lista de quadrados
quadrados = [x**2 for x in range(10)]
print(quadrados)  # Saída: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

### 5.2 Funções map, filter e reduce

```python
# Usando map para dobrar os valores
numeros = [1, 2, 3, 4]
dobrados = list(map(lambda x: x * 2, numeros))
print(dobrados)  # Saída: [2, 4, 6, 8]

# Usando filter para filtrar números pares
pares = list(filter(lambda x: x % 2 == 0, numeros))
print(pares)  # Saída: [2, 4]

# Usando reduce para somar todos os valores
from functools import reduce
soma = reduce(lambda x, y: x + y, numeros)
print(soma)  # Saída: 10
```
---

## 6. Controle de Fluxo

### 6.1 Estruturas Condicionais

```python
x = 10
if x > 5:
    print("Maior que 5")
elif x == 5:
    print("Igual a 5")
else:
    print("Menor que 5")
```

### 6.2 Estruturas de Repetição

```python
# Usando for
for i in range(5):
    print(i)

# Usando while
contador = 0
while contador < 5:
    print(contador)
    contador += 1
```
---

## 7. Manipulação de Strings

### 7.1 Métodos de Strings

```python
texto = "  Olá, Mundo!  "

# Remover espaços em branco
print(texto.strip())  # Saída: "Olá, Mundo!"

# Dividir uma string
palavras = texto.split()
print(palavras)  # Saída: ["Olá,", "Mundo!"]

# Juntar uma lista de strings
frase = " ".join(palavras)
print(frase)  # Saída: "Olá, Mundo!"
```

### 7.2 Expressões Regulares

```python
import re

# Encontrar todas as ocorrências de um padrão
texto = "O preço é R$100. O desconto é R$20."
padrao = r'R\$\d+'
matches = re.findall(padrao, texto)
print(matches)  # Saída: ['R$100', 'R$20']
```
---

## 8. Leitura e Escrita de Entrada/Saída

### 8.1 Leitura de Entrada

```python
nome = input("Digite seu nome: ")
print(f"Olá, {nome}!")
```

### 8.2 Formatação de Saída

```python
idade = 25
print(f"Eu tenho {idade} anos.")  # Saída: Eu tenho 25 anos.
```
---

## 9. Simulação e Algoritmos de Caminho

### 9.1 Simulação de Movimentos

```python
# Simulação de movimento em uma matriz 2D
posicao = [0, 0]

def mover(direcao):
    if direcao == "cima":
        posicao[1] += 1
    elif direcao == "baixo":
        posicao[1] -= 1
    elif direcao == "esquerda":
        posicao[0] -= 1
    elif direcao == "direita":
        posicao[0] += 1

mover("cima")
print(posicao)  # Saída: [0, 1]
mover("direita")
print(posicao)  # Saída: [1, 1]
```

### 9.2 Algoritmo de Caminho Mínimo

```python
# Algoritmo de Busca em Largura (BFS)
from collections import deque

def bfs(grafo, inicio):
    visitados = set()
    fila = deque([inicio])
    while fila:
        vertice = fila.popleft()
        if vertice not in visitados:
            visitados.add(vertice)
            fila.extend(grafo[vertice] - visitados)
    return visitados

grafo = {
    'A': {'B', 'C'},
    'B': {'A', 'D', 'E'},
    'C': {'A', 'F'},
    'D': {'B'},
    'E': {'B', 'F'},
    'F': {'C', 'E'}
}

print(bfs(grafo, 'A'))  # Saída: {'A', 'B', 'C', 'D', 'E', 'F'}
```
---

# Conceitos de lógica e manipulação de entradas/saídas em Python:

---

## 10. Estruturas de Dados Avançadas

### 10.1 Conjuntos (Sets)

```python
# Criando um conjunto
conjunto = {1, 2, 3, 4, 5}

# Adicionando elementos
conjunto.add(6)

# Removendo elementos
conjunto.remove(3)

print(conjunto)  # Saída: {1, 2, 4, 5, 6}
```

### 10.2 Pilhas (Stacks) e Filas (Queues)

```python
# Pilha usando lista
pilha = []
pilha.append(1)
pilha.append(2)
pilha.pop()  # Remove o último elemento

# Fila usando deque
from collections import deque
fila = deque()
fila.append(1)
fila.append(2)
fila.popleft()  # Remove o primeiro elemento

print(pilha)  # Saída: [1]
print(fila)   # Saída: deque([2])
```
---

## 11. Manipulação Avançada de Strings

### 11.1 Formatação de Strings

```python
nome = "Ana"
idade = 30
print(f"{nome} tem {idade} anos.")  # Saída: Ana tem 30 anos.
```

### 11.2 Métodos de Strings Avançados

```python
texto = "Python é uma linguagem de programação poderosa"
# Encontrar a posição da palavra "linguagem"
print(texto.find("linguagem"))  # Saída: 14

# Substituir uma palavra por outra
novo_texto = texto.replace("poderosa", "versátil")
print(novo_texto)  # Saída: Python é uma linguagem de programação versátil
```
---

## 12. Manipulação de Arquivos

### 12.1 Leitura de Arquivos

```python
with open("arquivo.txt", "r") as arquivo:
    conteudo = arquivo.read()
    print(conteudo)
```

### 12.2 Escrita de Arquivos

```python
with open("saida.txt", "w") as arquivo:
    arquivo.write("Escrevendo no arquivo.")
```
---

## 13. Funções Lambda e Higher-order Functions

### 13.1 Funções Lambda

```python
# Função lambda para calcular o quadrado de um número
quadrado = lambda x: x ** 2
print(quadrado(5))  # Saída: 25
```

### 13.2 Map, Filter e Reduce com Funções Lambda

```python
numeros = [1, 2, 3, 4, 5]
# Usando map para calcular o cubo de cada número
cubos = list(map(lambda x: x ** 3, numeros))
print(cubos)  # Saída: [1, 8, 27, 64, 125]

# Usando filter para filtrar números pares
pares = list(filter(lambda x: x % 2 == 0, numeros))
print(pares)  # Saída: [2, 4]

# Usando reduce para somar todos os valores
from functools import reduce
soma = reduce(lambda x, y: x + y, numeros)
print(soma)  # Saída: 15
```

---

# Manipulação de matrizes de inteiros e uso da biblioteca `math` 

---

## 14. Manipulação de Matrizes de Inteiros

### 14.1 Criando Matrizes

```python
# Matriz manual
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

# Matriz com zeros
matriz_zeros = [[0] * 3 for _ in range(3)]

# Matriz identidade
identidade = [[1 if i == j else 0 for j in range(3)] for i in range(3)]
```

### 14.2 Acessando Elementos

```python
# Acessando um elemento
elemento = matriz[1][2]  # Acesso à linha 1, coluna 2 (valor: 6)
```

### 14.3 Operações com Matrizes

#### Adição de Matrizes

```python
def adicionar_matrizes(matriz1, matriz2):
    resultado = [[matriz1[i][j] + matriz2[i][j] for j in range(len(matriz1[0]))] for i in range(len(matriz1))]
    return resultado

# Exemplo de uso
matriz_resultante = adicionar_matrizes(matriz1, matriz2)
```

#### Multiplicação de Matrizes

```python
def multiplicar_matrizes(matriz1, matriz2):
    resultado = [[sum(matriz1[i][k] * matriz2[k][j] for k in range(len(matriz1[0]))) for j in range(len(matriz2[0]))] for i in range(len(matriz1))]
    return resultado

# Exemplo de uso
matriz_resultante = multiplicar_matrizes(matriz1, matriz2)
```
---

## 15. Uso da Biblioteca `math`

### 15.1 Funções Matemáticas

```python
import math

# Raiz quadrada
raiz_quadrada = math.sqrt(16)  # Resultado: 4.0

# Seno de um ângulo em radianos
seno = math.sin(math.radians(30))  # Resultado: 0.5

# Valor absoluto
absoluto = math.fabs(-10)  # Resultado: 10.0
```

### 15.2 Constantes Matemáticas

```python
# Valor de pi
pi = math.pi  # Resultado: 3.141592653589793

# Constante de Euler
euler = math.e  # Resultado: 2.718281828459045
```

### 15.3 Funções de Arredondamento

```python
# Arredondar para baixo
arred_baixo = math.floor(3.7)  # Resultado: 3

# Arredondar para cima
arred_cima = math.ceil(3.2)  # Resultado: 4

# Arredondar para o inteiro mais próximo
arred_int = round(3.5)  # Resultado: 4
```
---

Este documento cobre a maior parte dos conceitos iniciais, com exemplos práticos para cada um. Estude e pratique esses tópicos para desenvolver uma boa base em Python e estar preparada para resolver problemas mais complexos.
