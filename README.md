# basic-calculator
a basis calculator just for training code, still in process

def adicao(x, y):
    return x + y

def subtracao(x, y):
    return x - y

def multiplicacao(x, y):
    return x * y

def divisao(x, y):
    if y != 0:
        return x / y
    else:
        return "Não é possível dividir por zero."

# Função para obter um número float válido do usuário
def obter_numero():
    while True:
        try:
            return float(input("Digite um número: "))
        except ValueError:
            print("Por favor, insira um número válido.")

# Função para imprimir o menu
def imprimir_menu():
    print("Selecione a operação:")
    print("1. Adição")
    print("2. Subtração")
    print("3. Multiplicação")
    print("4. Divisão")

# Entrada de usuário para escolher a operação
opcao = input(imprimir_menu())

# Entrada de números
num1 = obter_numero()
num2 = obter_numero()

# Realizar operação com base na escolha do usuário
if opcao == '1':
    print(num1, "+", num2, "=", adicao(num1, num2))
elif opcao == '2':
    print(num1, "-", num2, "=", subtracao(num1, num2))
elif opcao == '3':
    print(num1, "*", num2, "=", multiplicacao(num1, num2))
elif opcao == '4':
    if num2 != 0:
        print(num1, "/", num2, "=", divisao(num1, num2))
    else:
        print("Não é possível dividir por zero.")
else:
    print("Opção inválida")
