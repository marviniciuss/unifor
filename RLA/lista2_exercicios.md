
# Unifor
## Lista 02
### Exercício 1

Calcule a média de quatro números inteiros dados

```mermaid
flowchart TD
A([INÍCIO])-->B{{Informe os 4 números inteiros}}
B-->C[/N1, N2, N3, N4/]
C-->D[M=N1+N2+N3+N4/4]
D-->E{{A média é M}}
E-->F([FIM])
```

```
ALGORITMO
DECLARE N1,N2,N3,N4,M INTEIRO
INICIO
ESCREVA "Informe os 4 números inteiros: "
LEIA N1,N2,N3,N4
M=(N1+N2+N3+N4)/4
ESCREVA " A média é: ",M
FIM

```

### Exercício 2

Leia uma temperatura dada na escala Celsius (C) e imprima o equivalente em Fahrenheit (F). (Fórmula de conversão: F = (9/5) * C + 32)

```mermaid
flowchart TD
A([INÍCIO])-->B{{Informe a temperatura em Celsius}}
B-->C[/TC, TF/]
C-->D["TF = (9/5) * TC + 32"]
D-->E{{A temperatura em Fahrenheit é TF}}
E-->F([FIM])
```
```
ALGORITMO converter_temperatura
DECLARE TC, TF: REAL
ESCREVA "Digite a temperatura em gaus Celsius: "
LEIA TC
TF = (9/5) * TC + 32
ESCREVA "A temperatura em graus Fahrenheit é: ",TF
FIM
```

### Exercício 3

Leia uma quantidade de chuva dada em polegadas e imprima o equivalente em milímetros (25,4 mm = 1 polegada)

```mermaid
flowchart TD
A([INÍCIO])-->B{{Informe o volume de chuva em polegadas}}
B-->C[/VP, VM/]
C-->D["VM = VP * 25,4"]
D-->E{{O volume de chuva em milímetros é VM}}
E-->F([FIM])
```

```
ALGORITMO converter_volume
DECLARE VP, VM: REAL
ESCREVA "Informe o volume de chuva em polegadas: "
LEIA VP
VM = VP * 25,4
ESCREVA "O volume de chuva em milímetros é: ",VM
FIM
```
### Exercício 4

O custo ao consumidor de um carro novo é a soma do custo de fábrica com a porcentagem do distribuidor e dos impostos, ambos aplicados ao custo de fábrica. Supondo que a porcentagem do distribuidor seja de 12% e a dos impostos de 45%, prepare um algoritmo para ler o custo de fábrica do carro e imprimir o custo ao consumidor


```mermaid
flowchart TD
A([INÍCIO])-->B{{Informe o custo de fábrica do carro}}
B-->C[/CF, CC/]
C-->D["CC = 1.57 * CF "] 
D-->E{{O  custo ao consumidor é CC}}
E-->F([FIM])
```

```
ALGORITMO custo_carro
DECLARE CF, CC: REAL
ESCREVA "Informe o custo de fábrica do carro: "
LEIA CF
CC = 1.57 * CF
ESCREVA "O  custo ao consumidor é: ",CC
FIM
```

### Exercício 5

Calcule o quadrado de um número


```mermaid
flowchart TD
A([INÍCIO])-->B{{Informe um número}}
B-->C[/numero, numero_quadrado/]
C-->D["numero_quadrado = numero * numero "] 
D-->E{{O  quadrado do número informado é: numero_quadrado}}
E-->F([FIM])
```

```
ALGORITMO quadrado_numero
DECLARE numero, numero_quadrado: REAL
ESCREVA "Informe um número: "
LEIA numero
numero_quadrado = numero * numero
ESCREVA "O  quadrado do número informado é: ",numero_quadrado
FIM
```

### Exercício 6

O cardápio de uma lanchonete é dado abaixo. Prepare um algoritmo que leia a quantidade de cada item que você consumiu e calcule a conta final. 
a) Hambúrguer................ R$ 3,00 
b) Cheeseburger.............. R$ 2,50 
c) Fritas.................... R$ 2,50 
d) Refrigerante ............. R$ 1,00 
e) Milkshake................. R$ 3,00

```mermaid
flowchart TD
A([INÍCIO])-->B{{Informe a quantidade de Hambúrguer: }}
B-->C{{Informe a quantidade de Cheeseburger: }}
C-->D{{Informe a quantidade de Fritas: }}
D-->E{{Informe a quantidade de Refrigerante: }}
E-->F{{Informe a quantidade de Milkshake: }}
F-->G[/quant_chees,quant_hamb,quant_frita,quant_refrig,quant_milk,total_chees,total_hamb,total_frita,total_refrig,total_milk,conta/]
G-->H["total_chees=quant_chees*2.50
total_hamb=quant_hamb*3
total_frita=quant_frita*2.50
total_refrig=quant_refrig*1
total_milk=quant_milk*3
conta=total_chees+total_hamb+total_frita+total_refrig+total_milk"]
H-->I{{A sua conta final é: conta}}
I-->J([FIM])
```

```
ALGORITMO conta_final
DECLARE quant_chees,quant_hamb,quant_frita,quant_refrig,quant_milk,total_chees,total_hamb,total_frita,total_refrig,total_milk,conta: REAL
ESCREVA "Informe a quantidade de Hambúrguer: "
LEIA quant_hamb
ESCREVA "Informe a quantidade de Cheeseburger: "
LEIA quant_chees
ESCREVA "Informe a quantidade de Fritas: "
LEIA quant_frita
ESCREVA "Informe a quantidade de Refrigerante: "
LEIA quant_refrig
ESCREVA "Informe a quantidade de Milkshake: "
LEIA quant_milk
total_chees=quant_chees*2.50
total_hamb=quant_hamb*3
total_frita=quant_frita*2.50
total_refrig=quant_refrig*1
total_milk=quant_milk*3
conta=total_chees+total_hamb+total_frita+total_refrig+total_milk
ESCREVA "A sua conta final é:",conta
FIM
```


```
ALGORITMO conta_final
DECLARE conta=0: REAL 
		valor[5]={3.00, 2.50, 2.50, 1.00, 3.00}: REAL
		quantidade[5]: INTEIRO
INICIO
ESCREVA "Item 1-Hambúrguer, item 2-Cheeseburger, item 3-Fritas, item 4-Refrigerante, item 5-Milkshake"
PARA i de 0 até 4 passo 1 
	ESCREVA "Quantidade de item ", i + 1, " consumidos: " 			
	LEIA quantidade[i] 
FIM PARA
PARA i de 0 até 4 passo 2
	conta = valor + valor[i]*quantidade[i]
FIM PARA
ESCREVA "O valor da final da conta é:", conta
FIM
```
### Exercício 7

Uma companhia de carros paga a seus empregados um salário de R$ 500,00 por mês mais uma comissão de R$ 50,00 para cada carro vendido e mais 5% do valor da venda. Elabore um algoritmo para calcular e imprimir o salário do vendedor num dado mês recebendo como dados de entrada o nome do vendedor, o número de carros vendidos e o valor total das vendas.

```mermaid
flowchart TD
A([INÍCIO])-->B{{Informe seu nome: }}
B-->C{{Informe o número de carros vendidos: }}
C-->D{{Informe o valor total das vendas: }}
D-->E[/nome, nc, vv, salario/]
E-->F["salario = 500+(50 * nc + 0.05 * vv)"] 
F-->G{{O salário do funcionário é: salario}}
G-->H([FIM])
```

```
ALGORITMO salario_vendas
DECLARE nome: CARACTERE
		nc: INTEIRO
		vv, salario: REAL
ESCREVA "Informe seu nome: "
LEIA nome
ESCREVA "Informe o número de carros vendidos: "
LEIA nc
ESCREVA "Informe o valor total das vendas: "
LEIA vv
salario = 500+(50 * nc + 0.05 * vv)
ESCREVA "O salário do funcionário ", nome, "é :", salario
FIM
```
### Exercício 8

Calcule a média de um aluno na disciplina de RLA. Para isso solicite o nome do aluno, a nota da prova e a nota qualitativa. Sabe-se que a nota da prova tem peso 2 e a nota qualitativa peso 1. Mostre a média como resultado.

```mermaid
flowchart TD
A([INÍCIO])-->B{{Informe seu nome: }}
B-->C{{Informe a nota da prova: }}
C-->D{{Informe a nota qualitativa: }}
D-->E[/nome, media, NP, NQ/]
E-->F["media = (NP*2 + NQ*1)/3"] 
F-->G{{A média do aluno é: media}}
G-->H([FIM])
```
```
ALGORITMO media_ponderada
DECLARE nome: CARACTERE
		media, NP, NQ: REAL
ESCREVA "Informe seu nome: "
LEIA nome
ESCREVA "Informe a nota da prova: "
LEIA NP
ESCREVA "Informe a nota qualitativa: "
LEIA NQ
media = (NP*2 + NQ*1)/3
ESCREVA "A média do aluno é: ", media
FIM
```
### Exercício 9

Suponha que você deseja preencher a seguinte ficha de inscrição de um estudante: nome, matrícula, curso, idade, e-mail. Imprima os dados do usuário como uma ficha preenchida

```mermaid
flowchart TD
A([INÍCIO])-->B{{Informe seu nome: }}
B-->C{{Informe sua matrícula: }}
C-->D{{Informe seu curso: }}
D-->E{{Informe sua idade: }}
E-->F{{Informe seu e-mail: }}
F-->G[/nome, matricula,curso, idade, email/]
G-->H{{"Nome: nome
		Matrícula: matricula
		Curso: curso
		Idade: idade
		E-mail: email"}}
H-->I([FIM])
```
```
ALGORITMO ficha_inscricao
DECLARE nome, curso, email: CARACTERE
		matricula, idade: INTEIRO
ESCREVA "Informe seu nome: "
LEIA nome
ESCREVA "Informe sua matrícula: "
LEIA matricula
ESCREVA "Informe seu curso: "
LEIA curso
ESCREVA "Informe sua idade: "
LEIA idade
ESCREVA "Informe seu e-mail: "
LEIA email
ESCREVA "Nome: ", nome
	"Matricula: ", matricula
	"Curso: ", curso
	"Idade: ", idade
	"E-mail: , email
FIM
```
### Exercício 10

Calcule e mostre a área e o perímetro de um círculo. Sabe-se que a área = Ⲡ * raio2 e o perímetro = 2 * Ⲡ * raio.

```mermaid
flowchart TD
A([INÍCIO])-->B{{Informe o raio do círculo: }}
B-->C[/raio, p, a /]
C-->D[p = 2 * 3.14 * raio]
D-->E[a = 3.14 * raio * raio ]
E-->F{{"Área: a ; Perímetro: p"}}
F-->G([FIM])
```
```
ALGORITMO area_circulo
DECLARE raio, p, a: REAL
ESCREVA "Informe o raio do círculo: "
LEIA raio
p = 2 * 3.14 * raio
a = 3.14 * raio * raio
ESCREVA "Área do círculo é ", a, " e o perímetro é ", p
FIM
```
### Exercício 11

Faça um programa que receba um número positivo e maior que zero, calcule e mostre:
a) o número digitado ao quadrado;
b) o número digitado ao cubo;
c) a raiz quadrada do número digitado;
d) a raiz cúbica do número digitado

```mermaid
flowchart TD
A([INÍCIO])-->B{{Informe um número: }}
B-->C[/numero, num_quadrado, num_cubo, raiz_quad, raiz_cub/]
C-->D{numero > 0}
D--NÃO-->H{{O número deve ser positivo e maior que zero!}}
H-->G
D--SIM-->E["num_quadrado = numero ** 2 
			num_cubo = numero ** 3
			raiz_quad = numero ** 1/2
			raiz_cub = numero ** 1/3"]
E-->F{{"Quadrado: num_quadrado; Cubo: num_cubo; Raiz quadrada: raiz_quad; Raíz cúbica: raiz_cub"}}
F-->G([FIM])
```
```
ALGORITMO exponencial
DECLARE numero, num_quadrado, num_cubo, raiz_quad, raiz_cub: REAL
ESCREVA "Informe um número: "
LEIA numero
SE numero > 0 ENTAO
	num_quadrado = numero ** 2 
	num_cubo = numero ** 3
	raiz_quad = numero ** 1/2
	raiz_cub = numero ** 1/3
SENÃO
	ESCREVA "O número deve ser positivo e maior que zero!"
FIM_SE
ESCREVA "Quadrado: ", num_quadrado "Cubo: ", num_cubo "Raiz quadrada: ", raiz_quad "Raíz cúbica: ", raiz_cub
FIM
```
### Exercício 12

Faça um algoritmo que lê três números inteiros e mostra-os em ordem crescente.

```mermaid
flowchart TD
A([INÍCIO])-->B{{Informe o primeiro número: }}
B-->C{{Informe o segundo número: }}
C-->D{{Informe o terceiro número: }}
D-->E[/N1, N2, N3, temp/]
E-->F{N1>N2}
F--SIM-->G["temp=N1
			N1=N2
			N2=temp"]
F--NAO-->H
G-->H{N1>N3}
H--SIM-->I["temp=N1
			N1=N3
			N3=temp"]
H--NÃO-->J
I-->J{N2>N3}
J--SIM-->K["temp=N2
			N2=N3
			N3=temp"]
J--NÃO-->L
K-->L{{"Os números em ordem crescente são: N1, N2 e N3"}}
L-->M([FIM])
```
```
ALGORITMO ordem_crescente
VAR N1, N2, N3, temp: INTEIRO
INICIO
ESCREVA "Informe o primeiro número: "
LEIA N1
ESCREVA "Informe o segundo número: "
LEIA N2
ESCREVA "Informe o terceiro número: "
LEIA N3
SE N1 > N2 ENTÃO
	temp=N1
	N1=N2
	N2=temp
FIM_SE
SE N1 > N3 ENTÃO
	temp=N1
	N1=N3
	N3=temp
FIM_SE
SE N2 > N3 ENTÃO
	temp=N2
	N2=N3
	N3=temp
FIM_SE
ESCREVA "O números em ordem crescente são: " N1, N2, N3
FIM
```
### Exercício 13

Elaborar um algoritmo que, dada a idade de um nadador, classificá-lo nas categorias:
a) infantil A (5 - 7 anos),
b) infantil, B (8 -10 anos),
c) juvenil A (11 - 13 anos),
d) juvenil B (14 -17 anos) e
e) adulto (maiores que 18 anos).
SE idade<5 
Não pode nadar
SE idade 

```mermaid
flowchart TD
A([INÍCIO])-->B{{"Informe a idade do nadador(a): "}}
B-->C[/idade/]
C-->D{idade<5}
D--SIM-->E{{Muito novo para nadar: }}
D--NÃO-->F{idade>=5 e idade<=7}
F--SIM-->G{{O nadador está na categoria infantil A: }}
G-->Q
F--NÃO-->H{idade>=8 e idade<=10}
H--SIM-->I{{O nadador está na categoria infantil B: }}
I-->Q
H--NÃO-->J{idade>=11 e idade<=13}
J--SIM-->K{{O nadador está na categoria juvenil A: }}
K-->Q
J--NÃO-->L{idade>=14 e idade<=17}
L--SIM-->M{{O nadador está na categoria juvenil B: }}
M-->Q
L--NÃO-->O{idade>=18}
O--SIM-->P{{O nadador está na categoria adulto : }}
P-->Q([FIM])

```
```
ALGORITMO categoria_nadador
VAR idade: INTEIRO
INICIO
ESCREVA "Informe a idade do nadador(a): "
LEIA idade
SE idade<5 ENTÃO
	ESCREVA "Muito novo para nadar"
FIM_SE
SE idade>=5 e idade<=7 ENTÃO
	ESCREVA "O nadador está na categoria infantil A"
FIM_SE
SE idade>=8 e idade<=10 ENTÃO
	ESCREVA "O nadador está na categoria infantil B"
FIM_SE
SE idade>=11 e idade<=13 ENTÃO
	ESCREVA "O nadador está na categoria juvenil A"
FIM_SE
SE idade>=14 e idade<=17 ENTÃO
	ESCREVA "O nadador está na categoria juvenil B"
FIM_SE
SE idade>=18 ENTÃO
	ESCREVA "O nadador está na categoria adulto"
FIM
```
### Exercício 14

Dado três inteiros crie um algoritmo para retornar o menor deles.

```mermaid
flowchart TD
A([INÍCIO])-->B{{"Informe o 1º número inteiro: "}}
B-->C{{"Informe o 2º número inteiro: "}}
C-->D{{"Informe o 3º número inteiro: "}}
D-->E[/N1, N2, N3/]
E-->F{N1<N2 e N1<N3}
F--SIM-->G{{"O menor número é N1"}}
G-->K
F--NÃO-->H{N2<N1 e N2<N3}
H--SIM-->I{{"O menor número é N2"}}
I-->K
H--NÃO-->J{{"O menor número é N3"}}
J-->K([FIM])
```
```
ALGORITMO numero_menor
VAR N1, N2, N3: INTEIRO
INICIO
ESCREVA "Informe o 1º número inteiro:  "
LEIA N1
ESCREVA "Informe o 2º número inteiro:  "
LEIA N2
ESCREVA "Informe o 3º número inteiro:  "
LEIA N3
SE N1<N2 e N1<N3 ENTÃO
	ESCREVA "O menor número é N1"
SENÃO
	SE N2<N1 e N2<N3 ENTÃO
		ESCREVA "O menor número é N2"
	SENÃO
		ESCREVA "O menor número é N3"
FIM
```
