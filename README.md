# Curso-Python-Basics-Let-s-Code
# Módulo 1 - Exercícios
# 1) Faça um programa que peça um valor monetário e diminua-o em 15%. Seu programa deve imprimir a mensagem “O novo valor é [valor]”.

valor = input('Digite o valor: ')
valor = float(valor)

valor1 = valor * 0.85
print(f´O novo valor é: {valor1:.2f}')

# 2. Faça um programa que leia a validade das informações:
# a. Idade: entre 0 e 150;
# b. Salário: maior que 0;
# c. Sexo: M, F ou Outro;
# O programa deve imprimir uma mensagem de erro para cada informação inválida

def validade_informacoes():
    
    idade = int(input('Digite uma idade entre 0 - 150: '))
    if idade < 0 or idade > 151:
        print('Opção inválida.')

    salario = float(input('Digite o salário: '))
    if salario <0:
        print('Opção inválida.')

    sexo = input('Digite o sexo: ')
    if sexo != 'F' and sexo != 'M' and sexo != 'Outro':
        print('Opção inválida.')
     
validade_informacoes()

# 3. Vamos fazer um programa para verificar quem é o assassino de um crime. Para descobrir o assassino, a polícia faz um pequeno questionário com 5 
# perguntas onde a resposta só pode ser sim ou não:
# a. Mora perto da vítima?
# b. Já trabalhou com a vítima?
# c. Telefonou para a vítima?
# d. Esteve no local do crime?
# e. Devia para a vítima?
# Cada resposta sim dá um ponto para o suspeito. A polícia considera que os suspeitos com 5 pontos são os assassinos, com 4 a 3 pontos são cúmplices e 
# 2 pontos são apenas suspeitos, necessitando outras investigações. Valores iguais ou abaixo de 1 são liberados.

p1 = int(input('Mora perto da vítima? Digite 1 para sim e 0 para não: '))
p2 = int(input('Já trabalhou com a vítima? Digite 1 para sim e 0 para não: '))
p3 = int(input('Telefonou para a vítima? Digite 1 para sim e 0 para não: '))
p4 = int(input('Esteve no local do crime? Digite 1 para sim e 0 para não: '))
p5 = int(input('Devia para a vítima? Digite 1 para sim e 0 para não: '))

apuracao = p1+p2+p3+p4+p5

if apuracao == 3 or apuracao == 4:
    print(f'Pontuação: {apuracao}. Resultado da apuração: Cúmplice...')
elif apuracao == 2:
    print(f'Pontuação: {apuracao}. Resultado da apuração: Suspeito. Necessita outras investigações.')
elif apuracao <= 1:
    print(f'Pontuação: {apuracao}. Resultado da apuração: Liberado.')
else: 
    print(f'Pontuação: {apuracao}. Resultado da apuração: Culpado!')

# 4. Faça um programa que imprima a tabuada do 9 (de 9*1 a 9*10) usando loops

for i in range(1, 11):
    print(f'9 * {i} = {9 * i}')



