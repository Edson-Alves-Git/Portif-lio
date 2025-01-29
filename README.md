"""
Crie um programa que leia vários números inteiros pelo teclado. No
final da execução, mostre a média entre todos os valores e qual foi o
maior e o menor valores lidos. O programa deve perguntar ao usuário
se ele quer ou não continuar a digitar valores
"""
i     = 0
soma  = 0
maior = 0
menor = float('inf')
while True:
    numero = int(input(f"Digite o {i+1}º número: "))
    soma+=numero
    i+=1
    if numero > maior:
        maior = numero
    if numero < menor:
        menor = numero
    oper = input("\n Deseja digitar mais números: (S/N)").upper()
    if oper == 'N':
        break

print(f"\nMédia: \033[0;32m{soma/i}\033[0m")
print(f"\nMaior: \033[0;32m{maior}\033[0m")
print(f"\nMenor: \033[0;32m{menor}\033[0m")
