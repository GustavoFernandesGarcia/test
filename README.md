#atividade 1
 #Faça um programa que leia a idade de uma pessoa expressa em dias e
 #mostre-a expressa em anos, meses e dias.

idade_em_dias = int(input("Digite a idade em dias: "))

anos = idade_em_dias // 365
meses = (idade_em_dias % 365) // 30
dias = (idade_em_dias % 365) % 30

print(f"A idade em anos, meses e dias é: {anos} anos, {meses} meses e {dias} dias.")



#atividade2
#Elaborar um programa que lê 3 valores a,b,c e verifica se eles formam
#ou não um triângulo. Supor que os valores lidos são inteiros e positivos. Caso
#os valores formem um triângulo, calcular e escrever a área deste triângulo. Se
#não formam triângulo escrever os valores lidos. (Se a &gt; b + c não formam
#triângulo algum, se a é o maior).

a = int(input("Digite o valor de a: "))
b = int(input("Digite o valor de b: "))
c = int(input("Digite o valor de c: "))

if a + b > c and a + c > b and b + c > a:

    s = (a + b + c) / 2
    
    area = (s * (s - a) * (s - b) * (s - c)) ** 0.5
    print("Esses valores formam um triângulo.")
    print("A área deste triângulo é:", area)
else:
    print("Esses valores não formam um triângulo.")
    print("Valores lidos: a =", a, "b =", b, "c =", c)

#atividade3
#Faça um programa que leia 3 números inteiros e mostre o menor deles.

a = int(input("Digite o valor de a: "))
b = int(input("Digite o valor de b: "))
c = int(input("Digite o valor de c: "))

if a <= b and a <= c:
    print("Esse valor é o menor:", a)
elif b <= a and b <= c:
    print("Esse valor é o menor:", b)
else:
    print("Esse valor é o menor:", c)

#atividade4
#implementar uma função que retorne verdadeiro se o número for primo
#(falso caso contrário). Testar de 1 a 100.

def is_prime(n):
    if n <= 1:
        return False
    if n <= 3:
        return True
    if n % 2 == 0 or n % 3 == 0:
        return False
    i = 5
    while i * i <= n:
        if n % i == 0 or n % (i + 2) == 0:
            return False
        i += 6
    return True

# Teste de números de 1 a 100
for num in range(1, 101):
    if is_prime(num):
        print(f"{num} é primo.")

#ativdade5AeB

def inverter_letras(frase):
    
    palavras = frase.split()
    
    palavras_invertidas = []
    
    for palavra in palavras:
    
        palavra_invertida = palavra[::-1]
        
        palavras_invertidas.append(palavra_invertida)
   
    frase_invertida = ' '.join(palavras_invertidas)
   
    return frase_invertida
frase_original = "Esta é uma frase de exemplo"
frase_invertida = inverter_letras(frase_original)
print(frase_invertida)  # Saída: "atsE é amu esarf ed olpmexe"

