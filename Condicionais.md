
## Condicionais em Python

Condicionais são essenciais para controlar o fluxo de um programa, permitindo que diferentes ações sejam tomadas dependendo de condições específicas. A estrutura básica para realizar decisões é feita com as palavras-chave `if`, `else` e `elif` (abreviação de "else if").

### Estrutura Básica de uma Condicional

```python
if condição:
    # Código executado se a condição for verdadeira
elif outra_condição:
    # Código executado se a condição anterior for falsa e essa for verdadeira
else:
    # Código executado se nenhuma das condições anteriores for verdadeira
```
---
### Exemplo Básico de Condicionais

Vamos ver um exemplo simples para demonstrar o uso dessas estruturas:

```python
numero = int(input('Digite um número: '))

if numero > 0:
    print('O número é positivo.')
elif numero < 0:
    print('O número é negativo.')
else:
    print('O número é zero.')
```

**Explicação:**
- Se o número for maior que zero, ele entra no primeiro bloco `if` e exibe que o número é positivo.
- Se o número for menor que zero, ele entra no bloco `elif` e exibe que o número é negativo.
- Se nenhuma das condições for atendida (ou seja, o número é zero), o código entra no bloco `else`.
---
### Exemplo com Múltiplas Condições

Você pode usar condicionais para realizar verificações mais complexas, como comparar múltiplos valores:

```python
idade = int(input('Digite sua idade: '))

if idade < 18:
    print('Você é menor de idade.')
elif 18 <= idade <= 60:
    print('Você é maior de idade.')
else:
    print('Você é idoso.')
```

Aqui, estamos verificando três faixas etárias:
- Se a idade for menor que 18, a primeira condição `if` será atendida.
- Se a idade for entre 18 e 60 (inclusive), o bloco `elif` será executado.
- Se a idade for maior que 60, o bloco `else` será o escolhido.
---
### Condicional com Vários Testes

Também é possível usar operadores lógicos como `and`, `or` e `not` para combinar múltiplas condições. Veja um exemplo:

```python
temperatura = float(input('Digite a temperatura: '))

if temperatura > 30 and temperatura < 40:
    print('Está um calor intenso!')
elif temperatura >= 40:
    print('Está muito quente!')
else:
    print('Está agradável ou frio.')
```

Neste caso:
- Se a temperatura for entre 30 e 40 graus, o primeiro `if` será ativado.
- Se a temperatura for maior ou igual a 40, o `elif` será executado.
- Caso contrário, o `else` será executado.
---
### Exercício Prático: Verificando se um Número é Par ou Ímpar

Aqui está um exercício simples para aplicar o uso de condicionais:

**Problema:**
Peça para o usuário digitar um número e informe se ele é par ou ímpar.

```python
numero = int(input('Digite um número inteiro: '))

if numero % 2 == 0:
    print(f'O número {numero} é par.')
else:
    print(f'O número {numero} é ímpar.')
```
---
### Exercício Prático: Calculando a Média e Aprovando ou Reprovando

Peça para o usuário digitar três notas e calcule a média. Se a média for maior ou igual a 7, o aluno será aprovado. Caso contrário, será reprovado.

```python
nota1 = float(input('Digite a primeira nota: '))
nota2 = float(input('Digite a segunda nota: '))
nota3 = float(input('Digite a terceira nota: '))

media = (nota1 + nota2 + nota3) / 3

if media >= 7:
    print(f'Você foi aprovado com média {media:.2f}.')
else:
    print(f'Você foi reprovado com média {media:.2f}.')
```

---
