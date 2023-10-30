# Jogo-De-Luta-Em-Python
Machines x Humans Em Python

import random
print ("machines x humans\n")


computador =50
jogador = 50


while  jogador > 0  and computador > 0:
    print ("Lista de ataques possíveis do jogador")
    print ("a - soco")
    print ("b - cabeçada")
    print ("c – voa dora")


    ataque = input("Escolha qual ata que você quer usar: ")


    if ataque == "a":
         print ("Você usou o soco")
         computador = computador - 12
    elif ataque == "b":
         print ("Você usou a cabeçada")
         computador = computador - 7
    else:
         print ("Você usou a voa dora ")
         computador = computador - 18


    print("A vida do computador agora é", computador)


    if computador <= 0:
        break


    print("O computador te ataca")
    ataque_inimigo_chance = random.randint(0,1)


    if ataque_inimigo_chance == 1:
        print("computador taca o gabinete em voce ")
        jogador = jogador - 15
    else:
        print("computador usa ping +999 em voce ")
        jogador = jogador - 8
    print("Sua vida agora é", jogador, "\n")


if jogador > 0:
    print("Parabens, o jogador venceu")
else:
    print("Que pena, o computador venceu")

