Programa em python que receba como entrada uma lista de números e um valor e produza<br> 
como saída os pares de números da lista que somados resultam no valor de entrada.

Exemplo 01:<br>
Entrada: lista1 = [1, 5, 7, -1], soma = 6<br>
Saída: 2 Pares com soma 6 são (1, 5) e (7, -1)<br>

Exemplo 02:<br>
Entrada: lista2 = [1, 5, 7, -1, 5], soma = 6<br>
Saída: 3 Pares com soma 6 são (1, 5), (7, -1) e (1, 5)<br>

## Resolução do exercício

Observações:
1. Os dados da lista são inseridos pelo usuário através da função <b>input</b>
2. Em Python, a função, a estrutura de repetição (while ou for) e a estrutura condicional Se (if) <br>
   são finalizados pelo simples fato de estarem indentadas

```
def gera_pares(p_lista, p_soma):
       v_pares = ''
       n = len(p_lista)
       i = 0
       j = 0
       while (i <= n-2):
           j = i + 1
           while (j <= n-1):
             if (int(p_lista[i])+int(p_lista[j]) == p_soma):
               v_pares = v_pares + '[' + p_lista[i].strip() + ',' + p_lista[j].strip() + '], '
             j = j + 1
           i = i + 1
       return v_pares

lista = input("Informe a lLista de números: ")
soma = int(input("Informe o valor da soma dos números: "))

string_lista = lista.split(',')

pares = gera_pares(string_lista, soma)
pares = pares[0:len(pares)-2]
print("Pares: " + pares)
```
