menu = '''
Seja bem vindo!     

[1] Depositar
[2] Sacar
[3] Extrato
[0] Sair

Selecione uma das opções acima:
'''
saldo = 0
limite = 500
extrato =""
numero_saques = 0
LIMITE_SAQUES = 3

while True:
    opcao = input(menu)

    if opcao == "1":
        deposito = float(input("Digite o valor para depositar:"))

        if deposito > 0:
            saldo += deposito
            extrato += f"Depósito: R${deposito:.2f}\n"
            print("Depósito realizado com sucesso!")
        
        else:
            print("Não foi possível realizar depósito. Valor informado é inválido.")

    elif opcao == "2":
        saque = float(input("Digite o valor que quer sacar:"))

        excedeu_saldo = saque > saldo
        excedeu_limite = saque > limite
        excedeu_saques = numero_saques >= LIMITE_SAQUES

        if excedeu_saldo:
            print("Não foi possível realizar sua operação. Não há saldo suficiente.")

        elif excedeu_limite:
            print("Não foi possível realizar sua operação. Limite por saque excedido")
        
        elif excedeu_saques:
            print("Não foi possível realizar sua operação. Numero de saques diário excedido")

        elif saque > 0:
            saldo -= saque
            extrato += f"Saque: R$ {saque:.2f}\n"
            numero_saques += 1
            print("Saque realizado com sucesso!")

        else:
            print("Não foi possível realizar saque. Valor informado é inválido.")

    elif opcao == "3":
        print("\n========EXTRATO========")
        print("Não foram realizadas movimentações." if not extrato else extrato)
        print(f"\nSaldo R${saldo:.2f}")
        print("=======================")

    elif opcao =="0":
        break
    else:
         print("Por favor selecione uma opção válida!")
