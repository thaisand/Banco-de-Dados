Responder as seguintes questões:

O escalonamento Sa é completo? Justifique sua resposta.
Considerando que as últimas operações no escalonamento Sa sejam c2, c3, c1, nessa ordem, o escalonamento Sa é recuperável? Justifique sua resposta apresentando todas as leituras sujas existentes.
O escalonamento Sa é serializável? Justifique sua resposta apresentando o grafo de precedência completo.
Considere que o escalonamento Sa apresentado abaixo foi constituído a partir das transações T1, T2 e T3 também apresentadas abaixo. Ressalta-se que, em um SGBDR diversas transações devem ser escalonadas para executarem simultaneamente, aumentando assim a concorrência e, consequentemente, diminuindo o tempo de processamento. No entanto, tal concorrência demanda a utilização de técnicas de controle de concorrência para garantir as propriedades de Atomicidade, Consistência, Isolamento e Durabilidade (ACID).

T1 = r(x), r(y), w(x), r(z)

T2 = r(z), r(x), r(y), w(z)

T3 = r(y), r(z), w(y), r(x)

Sa = r3(y), r2(z), r1(x), r2(x), r3(z), r2(y), w3(y), r1(y), w2(z), w1(x), r3(x), r1(z)
