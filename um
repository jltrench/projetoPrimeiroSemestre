'''
Simulador de ímpar ou par, podendo escolher jogar contra o computador ou contra algum amigo ao lado
Projeto da Aula de Algoritmos - Desenvolver um programa com os conhecimentos adquiridos durante o curso
Professor: Patrick Pedreira
Alunos: João Lucca Trench Bragagnolo; José Eduardo Iahn Gonçalves; Lucas Rodrigues Ubaldo Walylo e Pedro Zanette Silva
Data de criação: 24/05/2021 | Última atualização: 29/05/2021 - 19:30
'''
import random #importação para número aleatório da máquina.
import time #importação para aplicar tempo entre os comandos.

students = ['João Lucca', 'Lucas Ubaldo', 'José Eduardo', 'Pedro Zanette'] #variável com os nomes dos Alunos.
separate = '=-=' * 20 #variável para separar linhas

print('\nBem-vindo ao Simulador de ímpar ou par!: \n' # Explicação do Jogo.
      + '\nRegras do jogo: \n'
      + '1.Escolha se deseja ser ímpar ou par. \n'
      + '2.Decida qual número (0-10) irá jogar. \n'
      + '3.O ganhador será através do resultado da soma dos números entre os oponentes!\n')
time.sleep(2)

decision = 'S'
while decision == 'S': #Estrutura de Repetição do Jogo.
    try:
        mode = input('Você deseja jogar contra o computador ou contra um amigo ao seu lado? \n' #Modo no qual o Usuário vai escolher jogar.
                     + '| Digite [bot] para jogar contra o computador. \n'
                     + '| Digite [friend] para jogar contra um amigo. \n'
                     + '-> ').lower()
    except:
        print("Informe os dados corretamente!")
    else:
        while mode != 'bot' and mode != 'friend':
            mode = input('Você deseja jogar contra o computador ou contra um amigo ao seu lado? \n'
                         + '| Digite [bot] para jogar contra o computador. \n'
                         + '| Digite [friend] para jogar contra um amigo. \n'
                         + '-> ').lower()
        if mode == 'bot': #Modo contra o Computador.
            numBot = random.randint(0, 10)
            try:
                choiceUser = input("\nEscolha-> Par ou Ímpar? \n" #Escolha do Usuário entre Ímpar ou Par.
                                   + "(1) para Par \n"
                                   + "(2) para Ímpar \n"
                                   + "->")
            except:
                print("Informe os dados corretamente!") #Correção de Valor Inválido.
            else:
                while choiceUser != '1' and choiceUser != '2':
                    try:
                        choiceUser = input("\nEscolha-> Par ou Ímpar? \n"
                                           + "(1) para Par \n"
                                           + "(2) para Ímpar \n"
                                           + "->")
                    except:
                        print("Digite os números CORRETAMENTE!")

                if choiceUser == '1': #Escolha Par.
                    try:
                        numPar = float(input("\nInsira um número de 0 a 10-> "))
                        numPar = int(numPar)
                        sumPar = numPar + numBot
                    except(NameError, KeyError, KeyboardInterrupt, TabError, TypeError, IndexError, SyntaxError):
                        print("Ocorreu um erro, digite corretamente!")
                    except(ValueError):
                        print("Algo foi digitado errado, por favor digite corretamente!")
                    else:
                        while numPar < 0 or numPar > 10:
                            try:
                                numPar = float(input("\nInsira um número de 0 a 10-> "))
                                numPar = int(numPar)
                                sumPar = numPar + numBot
                            except:
                                print("Digite os valores corretamente!")
                        print(
                            f"\nO seu número foi: {numPar:.0f} \nO número do computador foi: {numBot} \nA soma deu: {sumPar:.0f}")
                        if sumPar % 2 == 0: #Verificação de número Par.
                            print(separate)
                            print("\tO ganhador foi o PAR! Parabéns você ganhou!")
                            print(separate)
                        else:
                            print(separate)
                            print("\tO ganhador foi o ÍMPAR! Quem sabe na próxima você tenha mais sorte...")
                            print(separate)

                if choiceUser == '2': #Escolha Ímpar.
                    try:
                        numIm = float(input("Insira um número de 0 a 10-> "))
                        numIm = int(numIm)
                        sumIm = numIm + numBot
                    except(NameError, KeyError, KeyboardInterrupt):
                        print("Ocorreu um erro, digite corretamente!")
                    except(ValueError):
                        print("Foi digitado uma letra, por favor digite corretamente!") #Correção caso o Usuário responda com string.
                    else:
                        while numIm < 0 or numIm > 10:
                            try:
                                numIm = float(input("Insira um número de 0 a 10-> "))
                                numIm = int(numIm)
                                sumIm = numIm + numBot
                            except:
                                print("Digite os valores corretamente!")
                        print(
                            f"\nO seu número foi: {numIm:.0f} \nO número do computador foi: {numBot} \nA soma deu: {sumIm:.0f}")
                        if sumIm % 2 == 0: #Verificação de número Par.
                            print(separate)
                            print("\tO ganhador foi o PAR! Quem sabe na próxima você tenha sorte...!")
                            print(separate)
                        else:
                            print(separate)
                            print("\tO ganhador foi o ÍMPAR! Parabéns você ganhou!")
                            print(separate)

        elif mode == 'friend': #Modo contra Amigo.
            try:
                p1 = input("\n|Player1| - escolha: \n" #Escolha do Jogador 1 entre Ímpar ou Par.
                           + "(1) para Par \n"
                           + "(2) para Ímpar \n")
            except:
                print("Digite os valores corretamente!")
            else:
                while p1 != '1' and p1 != '2':
                    try:
                        p1 = input("|Player1| - escolha: \n"
                                   + "(1) para Par \n"
                                   + "(2) para Ímpar \n")
                    except:
                        print("Digite os valores corretamente!")
            try:
                p2 = input("|Player2| - escolha: \n" #Escolha do Jogador 2 entre Ímpar ou Par.
                           + "(1) para Par \n"
                           + "(2) para Ímpar \n")
            except:
                print("Digite os valores corretamente!") #Correção de Valor Inválido para comando.
            else:
                while p2 != '1' and p2 != '2':
                    try:
                        p2 = input("|Player2| - escolha: \n"
                                   + "(1) para Par \n"
                                   + "(2) para Ímpar \n")
                    except:
                        print("Digite os valores corretamente!")

                while p1 == '1' and p2 == '1' or p1 == '2' and p2 == '2': #Correção caso os jogadores escolham o mesmo tipo numérico.
                    print("Os jogadores não podem escolher a mesma opção!\n\tEscolha corretamente!")
                    try:
                        p1 = input("|Player1| - escolha: \n"
                                   + "(1) para Par \n"
                                   + "(2) para Ímpar \n")
                        p2 = input("|Player2| - escolha: \n"
                                   + "(1) para Par \n"
                                   + "(2) para Ímpar \n")
                    except:
                        print("Digite os valores corretamente!")
            if p1 == '1': #Jogador 1 Par.
                try:
                    numP1 = float(input("Player1: Digite um número de 0 a 10-> "))
                    numP1 = int(numP1)
                    numP2 = float(input("Player2: Digite um número de 0 a 10-> "))
                    numP2 = int(numP2)
                    sumP1P2 = numP1 + numP2
                except(NameError, KeyError, KeyboardInterrupt):
                    print("Ocorreu um erro, digite corretamente!")
                except(ValueError):
                    print("Foi digitado uma letra, por favor digite um NÚMERO corretamente!") #Correção caso o Usuário responda com string.
                else:
                    while numP1 < 0 or numP1 > 10 or numP2 < 0 or numP2 > 10:
                        try:
                            numP1 = float(input("Player1: Digite um número de 0 a 10-> "))
                            numP1 = int(numP1)
                            numP2 = float(input("Player2: Digite um número de 0 a 10-> "))
                            numP2 = int(numP2)
                            sumP1P2 = numP1 + numP2 #Resultado da Soma entre os dois números.
                        except:
                            print("Digite os valores corretamente!")
                    print(
                        f"\nNúmero escolhido pelo Player1: {numP1:.0f} \nNúmero escolhido pelo Player2: {numP2:.0f} \nA soma ficou igual a '{sumP1P2:.0f}'")
                    if sumP1P2 % 2 == 0: #Verficação de número Par.
                        print(separate)
                        print("\tO ganhador foi o Player1!")
                        print(separate)
                    else:
                        print(separate)
                        print("\tO ganhador foi o Player2!")
                        print(separate)
            elif p1 == '2': #Jogador 1 Ímpar.
                try:
                    numP1 = float(input("Player1: Digite um número de 0 a 10-> "))
                    numP1 = int(numP1)
                    numP2 = float(input("Player2: Digite um número de 0 a 10-> "))
                    numP2 = int(numP2)
                    sumP1P2 = numP1 + numP2 #Resultado da Soma entre os dois números.
                except(NameError, KeyError, KeyboardInterrupt):
                    print("Ocorreu um erro, digite corretamente!")
                except(ValueError):
                    print("Foi digitado uma letra, por favor digite um NÚMERO corretamente!") #Correção caso o Usuário responda com string.
                else:
                    while numP1 < 0 or numP1 > 10 or numP2 < 0 or numP2 > 10:
                        try:
                            numP1 = float(input("Player1: Digite um número de 0 a 10-> "))
                            numP1 = int(numP1)
                            numP2 = float(input("Player2: Digite um número de 0 a 10-> "))
                            numP2 = int(numP2)
                            sumP1P2 = numP1 + numP2 #Resultado da Soma entre os dois números.
                        except:
                            print("Digite os valores corretamente!")
                    print(
                        f"\nNúmero escolhido pelo Player1: {numP1:.0f} \nNúmero escolhido pelo Player2: {numP2:.0f} \nA soma ficou igual a '{sumP1P2:.0f}'")
                    if sumP1P2 % 2 == 0: #Verficação de número Par.
                        print(separate)
                        print("\tO ganhador foi o Player2!")
                        print(separate)
                    else:
                        print(separate)
                        print("\tO ganhador foi o Player1!")
                        print(separate)
            elif p2 == '1': #Jogador 2 Par.
                try:
                    numP1 = float(input("Player1: Digite um número de 0 a 10-> "))
                    numP1 = int(numP1)
                    numP2 = float(input("Player2: Digite um número de 0 a 10-> "))
                    numP2 = int(numP2)
                    sumP1P2 = numP1 + numP2 #Resultado da Soma entre os dois números.
                except(NameError, KeyError, KeyboardInterrupt):
                    print("Ocorreu um erro, digite corretamente!")
                except(ValueError):
                    print("Foi digitado uma letra, por favor digite um NÚMERO corretamente!") #Correção caso o Usuário responda com string.
                else:
                    while numP1 < 0 or numP1 > 10 or numP2 < 0 or numP2 > 10:
                        try:
                            numP1 = float(input("Player1: Digite um número de 0 a 10-> "))
                            numP1 = int(numP1)
                            numP2 = float(input("Player2: Digite um número de 0 a 10-> "))
                            numP2 = int(numP2)
                            sumP1P2 = numP1 + numP2 #Resultado da Soma entre os dois números.
                        except:
                            print("Digite os valores corretamente!")
                    print(
                        f"\nNúmero escolhido pelo Player1: {numP1:.0f} \nNúmero escolhido pelo Player2: {numP2:.0f} \nA soma ficou igual a '{sumP1P2:.0f}'")
                    if sumP1P2 % 2 == 0: #Verficação de número Par.
                        print(separate)
                        print("\tO ganhador foi o Player2!")
                        print(separate)
                    else:
                        print(separate)
                        print("\tO ganhador foi o Player1!")
                        print(separate)
            elif p2 == '2': #Jogador 1 Ímpar.
                try:
                    numP1 = float(input("Player1: Digite um número de 0 a 10-> "))
                    numP1 = int(numP1)
                    numP2 = float(input("Player2: Digite um número de 0 a 10-> "))
                    numP2 = int(numP2)
                    sumP1P2 = numP1 + numP2 #Resultado da Soma entre os dois números.
                except(NameError, KeyError, KeyboardInterrupt):
                    print("Ocorreu um erro, digite corretamente!")
                except(ValueError):
                    print("Foi digitado uma letra, por favor digite um NÚMERO corretamente!") #Correção caso o Usuário responda com string.
                else:
                    while numP1 < 0 or numP1 > 10 or numP2 < 0 or numP2 > 10:
                        try:
                            numP1 = float(input("Player1: Digite um número de 0 a 10-> "))
                            numP1 = int(numP1)
                            numP2 = float(input("Player2: Digite um número de 0 a 10-> "))
                            numP2 = int(numP2)
                            sumP1P2 = numP1 + numP2 #Resultado da Soma entre os dois números.
                        except:
                            print("Digite os valores corretamente!")
                    print(
                        f"\nNúmero escolhido pelo Player1: {numP1:.0f} \nNúmero escolhido pelo Player2: {numP2:.0f} \nA soma ficou igual a '{sumP1P2:.0f}'")
                    if sumP1P2 % 2 == 0: #Verficação de número Par.
                        print(separate)
                        print("\tO ganhador foi o Player1!")
                        print(separate)
                    else:
                        print(separate)
                        print("\tO ganhador foi o Player2!")
                        print(separate)

    decision = input("Deseja jogar novamente? [S/N] \n" #Comando para rodar novamente o programa.
                     + "-> ").upper()
    if decision == 'N': #Créditos do Trabalho.
        time.sleep(2)
        print('Projeto de Algoritmos - Primeiro Semestre - Professor Patrick Pedreira - Unisagrado')
        time.sleep(2)
        print(f"Alunos: {students[:]}")
