# Introdução à redes de computadores - T1

Descrição
O trabalho consiste na implementação de um codificador/decodificador para as técnicas NRZ-I, Manchester Diferencial, HDB3, 8B6T, 6B/8B.
OBS:

    O decodificador deverá indicar a existência de erros, quando permitir sua detecção
    O sinal no NRZ-I e do Manchester Diferencial deve começar em negativo (-)
    No HDB3 deve ser considerado que o próximo sinal a ser enviado é positivo (+) (pulso anterior é negativo) e a diferença entre positivos e negativos inicial é igual a 0
    A técnica 6B/8B deve utilizar o codificador NRZ-I após a conversão de 6 para 8 bits

Ambos programas (codificador e decodificador) devem ser executados em linha de comando (sem GUI ou execução via IDE). O codificador deve ser executado da seguinte forma:
$ codificador <técnica> <dados_hexa>
Onde:
<técnica> pode ser nrzi, mdif, hdb3, 8b6t ou 6b8b
<dados_hexa> são os dados de entrada em formato hexa que devem ser codificados
A saída deve utilizar os caracteres + (sinal positivo), 0 (sinal neutro), ou - (sinal negativo)
Por exemplo:
$ codificador nrzi 1234
---+++----+--+++
O decodificador funciona de maneira similar, porém recebe como entrada a mensagem codificada (usando +,0 e -) e retorna os dados em hexa.
Por exemplo:
$ decodificador nrzi ---+++----+--+++
1234
