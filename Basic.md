# Introdução ao Python

## O que é Python?

Python é uma linguagem de programação de alto nível, interpretada e de propósito geral. É conhecida por sua simplicidade e legibilidade, o que a torna uma ótima escolha para iniciantes.

## Como começar

Para escrever e executar código Python, você precisará instalar o Python em seu computador. Você pode baixar o Python [aqui](https://www.python.org/downloads/).

## Primeiros Passos

Vamos começar com alguns conceitos básicos de Python, incluindo como definir a função principal (`main`), como fazer entradas (`input`), saídas (`print`), e como usar estruturas de controle (`if`, `else`, `elif`).

### Definindo a Função Principal

Em Python, você pode definir uma função principal para organizar melhor o seu código. É uma boa prática colocar o código principal do seu programa dentro de uma função.

```python
def main():
    print("Olá, Mundo!")

if __name__ == "__main__":
    main()
```

### Entrada de Dados

Para ler dados do usuário, usamos a função `input()`. Ela retorna os dados como uma string, então você pode precisar convertê-los para outros tipos de dados, como inteiros ou floats.

```python
def main():
    nome = input("Digite seu nome: ")
    print(f"Olá, {nome}!")

if __name__ == "__main__":
    main()
```

### Saída de Dados

A função `print()` é usada para exibir dados na tela.

```python
def main():
    print("Esta é uma mensagem para o usuário.")

if __name__ == "__main__":
    main()
```

### Estruturas de Controle: if, else, elif

As estruturas de controle permitem que você execute código condicionalmente, dependendo de certas condições.

#### if

O bloco `if` executa um bloco de código se uma condição for verdadeira.

```python
def main():
    numero = int(input("Digite um número: "))
    if numero > 0:
        print("O número é positivo.")

if __name__ == "__main__":
    main()
```

#### else

O bloco `else` executa um bloco de código se a condição no `if` for falsa.

```python
def main():
    numero = int(input("Digite um número: "))
    if numero > 0:
        print("O número é positivo.")
    else:
        print("O número é zero ou negativo.")

if __name__ == "__main__":
    main()
```

#### elif

O bloco `elif` (abreviação de "else if") permite testar múltiplas condições.

```python
def main():
    numero = int(input("Digite um número: "))
    if numero > 0:
        print("O número é positivo.")
    elif numero == 0:
        print("O número é zero.")
    else:
        print("O número é negativo.")

if __name__ == "__main__":
    main()
```

### Estruturas de Decisão

Além dos condicionais, Python possui outras estruturas de decisão, como loops (`for`, `while`) e a construção `match` (disponível a partir do Python 3.10).

#### For Loop

O `for` loop é usado para iterar sobre uma sequência (como uma lista, tupla ou string).

```python
def main():
    for i in range(5):
        print(f"Número {i}")

if __name__ == "__main__":
    main()
```

#### While Loop

O `while` loop continua a executar um bloco de código enquanto a condição é verdadeira.

```python
def main():
    contador = 0
    while contador < 5:
        print(f"Contador: {contador}")
        contador += 1

if __name__ == "__main__":
    main()
```

#### Match Case

A construção `match` é semelhante ao `switch` em outras linguagens e permite combinar padrões.

```python
def main():
    comando = input("Digite um comando: ")

    match comando:
        case "start":
            print("Iniciando o programa...")
        case "stop":
            print("Parando o programa...")
        case _:
            print("Comando desconhecido.")

if __name__ == "__main__":
    main()
```
