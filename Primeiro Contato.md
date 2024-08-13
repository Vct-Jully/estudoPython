 Bem-vindo à sua introdução à programação com Python! Nesta "apostila", abordaremos conceitos básicos para ajudar você a começar seu caminho neste fascinante mundo da programação dm python.

### O que é Programação?

A programação consiste em dar instruções a máquinas (computadores) sobre o que fazer através de linguagens específicas chamadas **linguagens de programação**. Com isso, criamos soluções inteligentes para problemas complexos ou automatizamos tarefas repetitivas.

---

## Introduzindo Python

Python é uma linguagem de programação interpretada, amplamente utilizada devido sua clara sintaxe, legibilidade e versatilidade. É ideal para iniciantes, mas também suporta desenvolvimento avançado graças à sua rica biblioteca padrão.
É ideal para análise de dados, e automações. Pode facilmente ser usada por qualquer profissional empenhado em estudá-la.

Para executarmos nosso primeiro programa em Python, podemos utilizar ferramentas online como [Programiz](<https://www.programiz.com/python-programming/online-compiler/>) ou [Repl.it](https://replit.com/) e também ambientes locais como [Anaconda](https://www.anaconda.com/products/individual), [PyCharm](https://www.jetbrains.com/pycharm/download/#section=windows), [vscode](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjQ8I263_KHAxV2LrkGHd-AK9wQjBB6BAgQEAE&url=https%3A%2F%2Fcode.visualstudio.com%2Fdocs%2Fpython%2Fpython-tutorial&usg=AOvVaw1gzc1jMBCBMmyPKr06Js5i&opi=89978449) ou até mesmo o próprio [IDLE](https://docs.python.org/3/tutorial/interpreter.html).

---

## Hello World: Seu Primeiro Programa

Vejamos agora como escrever um programa simples em Python. Abra qualquer das ferramentas mencionadas anteriormente e digite o seguinte código:

```python
print("Hello World!")
```

Pressione "Executar" ou use o atalho correspondente; verá a mensagem "Olá, mundo!" sendo exibida na tela. Parabéns, acabou de criar o famoso "Hello World" em Python!

---

## Variáveis

Variáveis são contêineres onde armazenamos dados durante a execução dos programas. Podemos associar nomes amigáveis a esses valores para facilitar sua manipulação. Em Python, as variáveis não precisam ser declaradas antes de serem definidas. Vejamos alguns exemplos:

```python
nome = "Joana"
idade = 25
altura = 1.68
```

Podemos misturar diferentes tipos de dados nas mesmas variáveis, conforme demonstrado abaixo:

```python
curso = "Engenharia Civil"
ano_ingresso = 2020
media = 8.9
```

---

## Operadores Aritméticos

Operadores aritméticos permitem realizar cálculos entre números. Confira a lista completa:

| Sinal | Operações   | Exemplo                     | Resultado    |
|-------|-------------|------------------------------|--------------|
| `+`   | Adição      | `4 + 5`                     | `9`          |
| `-`   | Subtração   | `7 - 2`                     | `5`          |
| `*`   | Multiplicação | `3 * 6`               | `18`         |
| `/`   | Divisão     | `10 / 2`                    | `5.0`        |
| `//`  | Divisão inteira | `11 // 3`             | `3`          |
| `%`   | Resto       | `7 % 3`                     | `1`          |
| `**`  | Potenciação | `2 ** 4`                    | `16`         |

Exemplos de uso:

```python
salario_base = 2000
imposto = salario_base * 0.15
total = salario_base + imposto

print(f'Salário base: {salario_base}')
print(f'Imposto pago: {imposto}')
print(f'Total recebido: {total}')
```

---

## Entrada e Saída de Dados

Em Python, podemos capturar entradas pelo teclado com a função `input()`, assim como exibir saídas com a já conhecida `print()`. Veja o exemplo a seguir:

```python
# Capturando entrada
nome = input('Qual é o seu nome?: ')
idade = int(input('Quantos anos você tem?: '))

# Mostrar resultado
print(f'{nome}, em {idade} anos voce terá {idade + 10}.')
```

Nesse exemplo, perguntamos ao usuário seu nome e idade e exibimos uma mensagem personalizada com a informação fornecida.

---

## Condições Simples e Compostas

As sentenças condicionais permitem tomar decisões dentro de um código, dependendo de certas condições serem verdadeiras ou falsas. Os principais operadores lógicos são:

- Igualdade (`==`)
- Desigualdade (!=)
- Maior que (`>`)
- Menor que (`<`)
- Maior ou igual a (`>=`)
- Menor ou igual a (`<=`)

Confira o exemplo a seguir:

```python
nota = float(input('Digite a nota final:'))

if nota >= 7 and nota <= 10:
    print('Parabéns, aprovação garantida!')
elif nota < 7 and nota > 3:
    print('Reprovado, infelizmente :(')
else:
    print('Estude mais... Estude bem!')
```

---

Este material é apenas um pequeno resumo dos conceitos básicos de Python. Recomendamos continuar seus estudos via plataformas especializadas como [DataCamp](https://www.datacamp.com/), [SoloLearn](https://www.sololearn.com/Course/Python/) ou [CodeAcademy](https://www.codecademy.com/learn/learn-python-3), dentre outras disponíveis no mercado. Boa sorte em seu aprendizado!
