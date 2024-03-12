
### Exercício 1

1) Represente, em fluxograma e pseudocódigo, um algoritmo para determinar se um número inteiro e positivo é par ou impar.

#### Fluxograma

```mermaid
flowchart TD
A([Início])-->B{{Digite um número}}
B-->C[/Número/]
C--> D{Número < 0}
D--SIM-->E{{O número deve ser positivo!}}
E-->B
D--NÃO-->F{Número>=0}
F-->G[resto = número % 2]
G-->H{resto == 0}
H--NÃO-->I{{O número é impar!}}
I-->K
H--SIM-->J{{O número é par!}}
J-->K([FIM])
```
```
ALGORITMO verifica_par_ímpar
DECLARE numero, resto INTEIRO
ESCREVA "Digite um número positivo: "
LEIA numero, resto
ENQUANTO numero < 0 FAÇA
    ESCREVA "Digite um número positivo: "
    LEIA numero
FIM_ENQUANTO
resto = numero % 2
    SE resto == 0 ENTAO
       ESCREVA "O número é par"
    SENÃO 
       ESCREVA "O número é ímpar" 
FIM_ALGORITMO
```

