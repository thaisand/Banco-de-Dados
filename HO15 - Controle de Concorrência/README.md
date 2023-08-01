Responder as seguintes questões:
<ol>
<li> Considerando a técnica de controle de concorrência por bloqueio exclusivo (binário) com protocolo 2PL estrito e confirmação (commit) implícita (commit da transação ocorre logo após a última operação da transação no escalonamento), o escalonamento Sa possui deadlock? Entre quais transações? Qual o escalonamento que efetivamente será executado, considerando a técnica de resolução de deadlock que identifique o deadlock e mate a transação mais recente (aquela em que sua primeira operação se inicie depois da primeira operação das outras).
<li> Considerando a técnica de controle de concorrência por bloqueio compartilhado (ternário) com protocolo 2PL estrito e confirmação (commit) implícita (commit da transação ocorre logo após a última operação da transação no escalonamento), o escalonamento Sa possui deadlock? Entre quais transações? Qual o escalonamento que efetivamente será executado, considerando a técnica de resolução de deadlock que identifique o deadlock e mate a transação mais recente (aquela em que sua primeira operação se inicie depois da primeira operação das outras)?
<li> Considerando a técnica de controle de concorrência por ordenação de registros de timestamp, qual o escalonamento que efetivamente será executado?
</ol>
Considere que o escalonamento Sa apresentado abaixo foi constituído a partir das transações T1, T2 e T3 também apresentadas abaixo. Ressalta-se que, em um SGBDR diversas transações devem ser escalonadas para executarem simultaneamente, aumentando assim a concorrência e, consequentemente, diminuindo o tempo de processamento. No entanto, tal concorrência demanda a utilização de técnicas de controle de concorrência para garantir as propriedades de Atomicidade, Consistência, Isolamento e Durabilidade (ACID).

T1 = r(x), r(y), w(x), r(z)

T2 = r(z), r(x), r(y), w(z)

T3 = r(y), r(z), w(y), r(x)

Sa = r3(y), r2(z), r1(x), r2(x), r3(z), r2(y), w3(y), r1(y), w2(z), w1(x), r3(x), r1(z)
