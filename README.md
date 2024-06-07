#Algumas funções básicas e algoritmos de base em Python


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

### 1.2 Modificando Listas

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

Este documento cobre a maior parte dos conceitos iniciais, com exemplos práticos para cada um. Estude e pratique esses tópicos para desenvolver uma boa base em Python e estar preparada para resolver problemas mais complexos.
