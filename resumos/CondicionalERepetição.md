# Estruturas COndicionais e de Repetição

## Identação

É o que define um bloco do código, onde o interpretador determina onde há o inicio e o fim de um bloco de comando. 

Java ou C é utilizado {}, em python é utilizado 4 espaços em branco (ou um tab). 

## Estruturas Condicionais

### if / if-else / elif

É o que permite o desvio de fluxo de controle a depender de uma expressão lógica.

```python
saldo = 2000.0
saque = float(input("Informe o valor de saque:"))

if saldo >= saque:
    print("Realizando saque!")
if saldo < saque:
    print("Saldo insuficiente")
```
Uma estrutura com dois ou mais desvios, pode-se utilizar o if e else. Caso if não seja verdadeira, executará o próximo elif/if else, e caso também seja não verdadeiro, executará por ultimo o else. 

```python
saldo = 2000.0
saque = float(input("Informe o valor de saque:"))

if saldo >= saque:
    print("Realizando saque!")
else:
    print("Saldo insuficiente")
```

Usando elif:

```python
opt = int(input("Qual operação desejada? [1] Sacar: \n[2] Extrato:"))

if opt == 1:
    saque = float(input("Informe o valor de saque:"))
elif opção == 2:
    print("Exibindo o extrato...")
else:
    print("Opção inválida.")
```
## Condicional aninhada

```python
conta_normal = True
conta_universitaria = False

if conta_normal:
    if saldo >= saque:
        print("Saque realizado com sucesso!")
    elif saque <= (saldo + cheque especial):
        print("Saque realizado com uso do cheque especial!")
elif conta_universitaria:
    if saldo >= saque:
        print("Saque realizado com sucesso!")
    else:
        print("Saldo insuficiente!")
else:
    print("O sistema não reconheceu seu tipo de conta, favor entrar em contato com o gerente da agência!")
```

## If ternário 

QUando a condicional é realizada na mesma linha.

```python
saldo = 2000
saque = 2500 

status = "SUcesso" if saldo >= saque else "Falha"
print(f"{status} ao realizar o saque!")
```
## Estrutura de Repetição

### O que são?

São estruturas para repetir um bloco de código em um número n de vezes, pode ser definido ou pode ser determinado através da lógica. 

### for

```python
texto = input("Informe um texto: ")
VOGAIS = "AEIOU"

for letra in texto:
    if letra.upper() in VOGAIS:
        print(letra, end="")

print()
```
### range

```python
for numero in range(0,11):
    print(numero, end="")
```
```python
# Exibindo de 5 em 5:
for numero in range(0,50, 5):
    print(numero, end="")
```

### while

Utilizado quando não temos um parâmetro de parada.

```python
opção = -1

while opção != 0:
    opção = int(input("[1] Sacar \n[2] Extrato \n[0] Sair \n:"))
    if opção == 1:
        print("Sacando")
    elif opção == 2:
        print("Exibindo o extrato")
    elif opção == 0:
        print("Saindo")
    else:
        print("Opção inválida")
```

### continue, break e pass

O while as vezes é utilizado como loop infinito com uma condição de parada:

Quando se querer parar uma execução numa determinada condição:

```python
while True:
    numero = int(input("Informe um número: "))
    if numero == 10:
        break
    print(numero)
```

```python
for numero in range(100)
    if numero == 12:
        break
    print(numero, end=" ")
```
Quando quer se pular alguma execução do bloco se utiliza o continue.

```python
for numero in range(100)
    if numero % 2 == 0:
        continue

    print(numero, end=" ")
```

```python
while True:
    numero = int(input("Informe um número: "))
    if numero == 10:
        break
    if numero % 2 == 0:
        continue
    
    print(numero)
```

```python

```
# Cobrar ficar pronto

Alinhar a subida do EMEJ junto com as entradas a serem pagas pelos membros

Descobrir com a BJ como funcionaria a questão

Perguntar pra Mara sobre a Federação de novas EJs