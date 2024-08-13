Hoje falaremos sobre tipos de dados, inputs e exercícios envolvendo lógica matemática. Estamos avançando aos poucos por aqui!
---

## Tipos de Dados

### Tipos de dados são categorias pré-definidas pela linguagem para classificar e tratar as informações presentes em um programa. Alguns deles incluem:

- Inteiros (`int`): representam números positivos, negativos ou zero, sem parte decimal. Por exemplo: `1`, `0`, `-23`.
- Flutuantes (`float`): representam números reais, com casas decimais. Por exemplo: `2.5`, `-3.14`, `0.0`.
- Booleanos (`bool`): possui apenas duas opções, True or False. Representam condições verdadeiras ou falsas.
- Strings (`str`): sequências de caracteres, geralmente representadas por aspas simples ('') ou duplas ("") ou triplas (''' ''' ou """ """) caso haja necessidade de multi-linha. Por exemplo: `'olá!'`, `"Python"`.
- Listas (`list`): conjunto ordenado de elementos mutável, separados por vírgulas e encapsulados por colchetes []. Podem incluir diversos tipos de dados. Por exemplo: `[1, 2, 3]`, `['a', 'b', 'c']`, `["banana", 12, true]`.
- Tuplas (`tuple`): conjunto ordenado de elementos imutável, similar a listas, mas que não pode sofrer alterações. Separadas por vírgulas e encapsuladas por parêntesis (). Também podem incluir vários tipos de dados. Por exemplo: `(1, 2, 3)`, `('a', 'b', 'c')`, `("banana", 12, true)`.
- Conjuntos (`set`): conjunto desordenado de elementos únicos e imutáveis. Encapsulados por chaves {}, não admite repetições. Por exemplo: `{1, 2, 3}` ou `{"a", "b", "c"}`.
- Dicionários (`dict`): conjunto de itens organizados em formato de pares chave-valor. Chaves são sempre únicas e servem como identificador para cada valor. Usam chaves {} e separam cada item por vírgula. Por exemplo: `{'name': 'John Doe'}`.

---
### Esse é um exemplo de input básico:

```python
texto = input('Entre com algum texto: ')
print(f'Texto digitado: {texto}')
```
---
### Segundo, aqui está o exemplo de um input que recebe apenas int `int(input())`:

```python
numero = int(input('Digite um número inteiro: '))
print(f'Você digitou o número inteiro: {numero}')
```
---
## Input Aprimorado

Como discutido ontem, a função `input()` permite obter entradas do usuário. No entanto, existem situações em que queremos trabalharmos com valores numéricos diretamente, evitando conversões posteriores. Para isso, podemos combinar o método `strip()` com `typecast` ingenuamente, veja o exemplo abaixo:

```python
idade = int(input('Digite sua idade: ').strip()) # Remove espaço extra e converte para inteiro
peso = float(input('Informe seu peso: ').strip().replace(",",".")) # Troca virgula por ponto e converte para flutuante
```

Observe que adicionamos o método `strip()` para remover quaisquer espaços extras indesejáveis e substituímos eventuais vírgulas por pontos para adequarmos às convenções numéricas internacionais. Isso facilita o processamento posterior nestes dados.

---

## Problema Matemático (NIVEL FÁCIL)

Finalmente, implementaremos um problema simples referente à fórmula de Pitágoras, aqui receberemos os catetos a e b via input para calcular a hipotenusa de um triângulo:

```python
def calcular_hipotenusa():
    ca = float(input('Insira o comprimento do cateto a: '))
    cb = float(input('Insira o comprimento do cateto b: '))

    hipotenusa = (ca ** 2 + cb ** 2) ** 0.5
    print(f'Hipotenusa: {round(hipotenusa, 2)}')

calcular_hipotenusa()
```

Nessa última implementação, pedimos ao usuário que insira os valores dos catetos a e b. Após validarmos os dados, calculamos o valor da hipotenusa usando a fórmula de Pitágoras e, por fim, exibimos o resultado formatado. Note que usamos a biblioteca `math` para calcularmos a raiz quadrada, pois esta funcionalidade não está inclusa nativamente na linguagem Python.

---

## Problema Matemático (NÍVEL MÉDIO)

Agora que dominamos melhor as bases, testemos nossos novos conhecimentos com um problema divertido. Considere a série abaixo:

```
1, 1, 2, 3, 5, 8, ...
```

Trata-se da **Sequência Fibonacci**, onde cada termo é obtido somando os dois anteriores. Implemente uma solução em Python que receba um número inteiro positivo `n` e retorne o enésimo termo dessa sequência. Caso o usuário insira um número inválido, informe-o e reinicie a obtenção do dado.

Tentativa de solução:

```python
def fibonacci(n: int):
    if n <= 0:
        return None
    elif n == 1 or n == 2:
        return 1
    else:
        a, b = 1, 1
        for _ in range(n - 2):
            a, b = b, a + b
        return b

while True:
    try:
        numero = abs(int(input('Insira um número natural válido: ')))
        break
    except ValueError:
        print('Entrada Inválida, tente novamente.')

resultado = fibonacci(numero)

if resultado is not None:
    print(f'O {numero}-ésimo termo da Sequência de Fibonacci é {resultado}.')
else:
    print('Entrada inválida, tente um número maior ou igual a 1.')
```

---

Espero que este material tenha sido útil para consolidar seus conhecimentos e prepará-los para enfrentar novos desafios. Continue praticando e descubra todo o potencial que há em si e em Python. Até a próxima!
