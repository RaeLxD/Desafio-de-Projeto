import datetime
menu = """
---------- MENU ----------
[ 1 ] - DEPOSITAR
[ 2 ] - SACAR
[ 3 ] - VISUALIZAR EXTRATO
[ 4 ] - ENCERRAR
"""
deposito = saldo = 0
depositos = 0
limite = 500
saldo = 0
extrato = ""
data = datetime.date.today()
saque = 0
saques = 0
depositoS = saldoS = 0



while True:
    opcao = int(input(f'{menu}Qual a operação o senhor(a) deseja: '))
    if opcao == 1:
        deposito = saldo = float(input('Qual o valor que você quer depositar: R$ '))
        depositoS += deposito
        saldoS += saldo
    if opcao == 2:
        saque = float(input('Qual o valor do saque: R$ '))
        saques += 1
        if saques > 3:
            print('Você excedeu o limite de saques diários!')
        elif saques <= 3:
            if saque <= 500:
                saldoS -= saque
            elif saque > 500:
                print('Limite máximo por saque é R$ 500')
    elif opcao == 3:
        extrato = input(f"""Extrato bancário: 
                        Saldo Atual: R$ {saldoS}
                        Depósito: {depositoS}
                        Depósitos: {depositos}
                        Data: {data}""")
















