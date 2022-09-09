/* ============ cod 01 ======== */

#include <stdio.h>
#include <stdlib.h>

int main (void) {
    
int INDICE = 13, SOMA = 0, K = 0;

while( K < 13)

{
    K = K + 1;
    SOMA = SOMA + K;
};

printf("a soma e %d",SOMA);

}


/*===== cod 02 ==============*/

def main():
    intInput = int(input("Entre com numero:"))

    num0, num1, num2 = 0, 1, 1
    
    if intInput in set([num0, num1, num2]):
        print("Pertence a sequencia")

    while num0 < intInput:
        num0 = num1 + num2
        num2 = num1
        num1 = num0

    if num0 == intInput:
        print("Pertence a sequencia")
    else:
        print("NÃO Pertence a sequencia")


if __name__ == "__main__":
    main()
    
    
    
 /* ======= code 03 ===========*/
 
 import json

def main():
    file = open('./auxiliar/dados.json')
    vetor = json.load(file)
    file.close()

    menor = min(map(lambda x: float(x['valor']), vetor))
    print(f'• O menor valor de faturamento ocorrido em um dia do mês: {menor}')

    maior = max(map(lambda x: float(x['valor']), vetor))
    print(f'• O maior valor de faturamento ocorrido em um dia do mês: {maior}')

    soma = sum(map(lambda x: float(x['valor']), vetor))
    count = len(vetor)
    media = soma / count
    quantidade = sum(map(lambda x: 1 if int(x['valor']) > media else 0, vetor))
    print(f'• Número de dias no mês em que o valor de faturamento diário foi superior à média mensal: {quantidade}')


if __name__ == "__main__":
    main()
    
    
  /*========= code 04 ============*/
  
  def main():
    faturamento = {
        "SP": 67836.43,
        "RJ": 36678.66,
        "MG": 29229.88,
        "ES": 27165.48,
        "OUTROS": 19849.53
    }

    soma = sum(map(lambda x: float(x), faturamento.values()))

    for uf, valor in faturamento.items():
        porcentual = (valor / soma) * 100
        print(f"{uf} – {porcentual:3.2f}%")


if __name__ == "__main__":
    main()
    
    
    /* ========== code 05 ===========*/
    
    def main():
    strInput = input("Entre com a palavra: ")

    start, end = 0, len(strInput)-1

    while start < end:
        temp = strInput[end]
        strInput = strInput[:end] + strInput[start] + strInput[end+1:]
        strInput = strInput[:start] + temp + strInput[start+1:]
        start+=1
        end-=1

    print(f"A palavra invertida é: {strInput}")

if __name__ == "__main__":
    main()
    
    
