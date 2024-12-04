## Queue

Fila FIFO (first in first out)
Uso para buffering, streaming de dados.

Basicamente uma lista onde o primeiro que entra é o primeiro que sai. É uma implementaçãod e Linked Lists.

Pode haver um acréssimo de um item, usando append() ou a remoção de um item usando pop(), mas o append sempre acresentará na ultima posição e o pop removerá a primeira posição. Ambos movendo os ponteiros de Head (inicio da lista) e Tail (fim da lista).
C.T. O(1).
## Dequeue

Basicamente uma queue mas para Double Linked Lists, portanto tanto o append() quanto o pop() podem ocorrer no inicio ou fim da lista, já que não faz diferença de Head e Tail.
C.T. O(1).