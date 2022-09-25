# Trabalho-faculdade-
Trabalhos pra faculdade

"1. Tendo como dado de entrada a altura (h) de uma pessoa, construa um algoritmo que calcule seu
peso ideal, utilizando as seguintes fórmulas:
a. Para homens: (72.7*h) - 58
b. Para mulheres: (62.1*h) - 44.7"

genero = input('Digite o seu gênero, M para masculino e F para feminino: ')
if 'M' or 'm' in genero:
    alturadapeossa = float(input('Digite aqui a sua altura e vamos lhe informar qual seria o seu peso ideal para o genêro masculino: '))
    pesoideal = (alturadapeossa * 72.7) - 58
    print (f'O seu peso ideal é: {pesoideal:.2f}')
elif 'F' in genero:
    alturadapeossa = float(input('Digite aqui a sua altura e vamos lhe informar qual seria o seu peso idealpara o genêro feminino: '))
    pesoideal = (alturadapeossa * 62.1) - 44.7
    print (f'O seu peso ideal é: {pesoideal:.2f}')
    
"2. João Papo-de-Pescador, homem de bem, comprou um microcomputador para controlar o
rendimento diário de seu trabalho. Toda vez que ele traz um peso de peixes maior que o
estabelecido pelo regulamento de pesca do estado de São Paulo (50 quilos) deve pagar uma
multa de R$ 4,00 por quilo excedente. João precisa que você faça um programa que leia a
variável peso (peso de peixes) e calcule o excesso. Gravar na variável excesso a quantidade
de quilos além do limite e na variável multa o valor da multa que João deverá pagar. Imprima
os dados do programa com as mensagens adequadas."
    
    Pesca = float(input('qual a quantidade da pesca do dia em Kg? '))
if Pesca > 50:
    PescaExcedente = (Pesca - 50)
    multa = PescaExcedente * 4.00
    print(f'a pesca de hj excedeu o limite de peso de 50Kg sendo de {PescaExcedente} alem do limite gerando uma multe de R${multa}')
    
"3. Faça um Programa que pergunte quanto você ganha por hora e o número de horas trabalhadas
no mês. Calcule e mostre o total do seu salário no referido mês, sabendo-se que são descontados
11% para o Imposto de Renda, 8% para o INSS e 5% para o sindicato, faça um programa que nos
dê:
a. salário bruto.
b. quanto pagou ao INSS.
c. quanto pagou ao sindicato.
d. o salário líquido.
e. calcule os descontos e o salário líquido, conforme a tabela abaixo:"

salario_H = float(input('Quanto é sua hora de trabalho? '))
H_trabalhada = int(input('Quantas horas trabalhou este mês? '))
salario_B = salario_H * H_trabalhada
if salario_B > 1903.98:
    IR = salario_B * 0.11
else:
    IR = 0
INSS = salario_B * 0.08
sindicato = salario_B * 0.05 
salario_L = salario_B - IR - INSS - sindicato
print(f'''Salário bruto = R$:{salario_B:.2f}
imposto de renda = R$:{IR:.2f}
INSS = R$:{INSS:.2f}
contribuiçao sindical = R$:{sindicato:.2f}
salário líquido = R${salario_L:.2f}''')

4. Faça um Programa que peça a idade e a altura de 5 pessoas, armazene cada informação no seu
respectivo índice. Imprima a idade e a altura na ordem inversa a ordem lida.

I = 0
idade_altura = []
while I < 5:
    idade = int(input("qual sua idade? "))
    altura = float(input('qual sua altura?'))
    idadealtura = (idade,altura)
    idade_altura.append(idadealtura)
    I+=1
print(idade_altura[::-1])

5. Faça um Programa que leia uma estrutura A com 10 números inteiros, calcule e mostre a soma
dos quadrados dos elementos desta estrutura.

import math
A = [1,2,3,4,5,6,7,8,9,10]
lista =[]
for a in A:
    expoente = a*a
    lista.append(expoente)
print(lista)
print(sum(lista))

6. Faça um Programa que leia duas estruturas com 10 elementos cada. Gere uma terceira estrutura
de 20 elementos, cujos valores deverão ser compostos pelos elementos intercalados das duas
estruturas.

lista1 = [1,3,5,7,9,11,13,15,17,19]
lista2 = [2,4,6,8,10,12,14,16,18,20]
lista3 = []
for i in range(10):
    lista3.append(lista1[i])
    lista3.append(lista2[i])
print(lista3)
