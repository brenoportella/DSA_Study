# LINKED LIST

A linked list não está sequencialmente alocada na memória. É uma lista de itens não sequenciais, onde o primeiro item aponta para o endereço do segundo item.

Caso os ponteiros apontem em ambas as direções, ou seja, tanto para o item a seguir como para o item anterior, ela deixa de ser uma Single Linked List (onde item aponta apenas para o próximo) e passa ser uma Double Linked List (onde o item aponta para o próximo e para o anterior).

## Array x Linked List

#### Leitura:
Array:
- É sequencial ou seja, encontrar um item nele é C.T. O(1);
- A velocidade de LEITURA do array é mais rápida, já que os itens estão sequencialmente alocados na memória.

Linked List:
- Para encontrar o tamanho de uma linked list, é necessário percorrer toda a linked list. E para procurar um item na linked list, também é necessário percorrer toda ela, já que o item atual somente aponta para o próximo item. Sendo assim uma LEITURA C.T. O(n). Mas também pode ser O(1), no melhor dos casos.

#### Inserção:
Array:
- Muito complexo, porque é necessário percorrer todos os items do array e realocar em outro espaço sequencial do tamanho da memória nova desejada. Portanto C.T. O(n).

Linked list:
- No melhor dos casos, quando é necessário inserir algo no inicio ou no fim da linked list, a complexidade temporal é O(1), já que é fácil saber onde está o inicio e o fim da linked list.
- Mas caso a inserção seja no meio da linked list, será O(n), porque será necessário percorrer toda a linked list para identificar a posição desejada.
#### Deletar:
Array:
- Se eu souber qual item estou deletando, é C.T. O(1).
- Mas se eu não souber, então é C.T. O(n).

Linked list:
- No melhor dos casos, quando eu já tenho o ponteiro para aquele item, C.T. O(1). No pior dos casos, quando tenho de procurar pelo item C.T. O(n).