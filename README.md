##  Análise de Algoritmos de Ordenação 

Este projeto implementa e analisa três algoritmos de ordenação em C: **Bubble Sort**, **Insertion Sort**, e **Heap Sort**. O objetivo é comparar o desempenho (em passos e tempo de execução) desses métodos em dois cenários:

1.  Um conjunto de dados pequeno (dígitos do RGM).
2.  Um conjunto de dados grande e aleatório.

-----

##  Algoritmos Implementados

### 1\. Bubble Sort

  * **Ideia Central:** Compara pares adjacentes de elementos e os troca se estiverem na ordem errada. O processo se repete até que o array esteja ordenado. Os maiores elementos "borbulham" para o final do array.
  * **Complexidade de Tempo (Pior e Médio Caso):** $O(n^2)$
  * **Complexidade de Tempo (Melhor Caso - Array Ordenado):** $O(n^2)$ (A implementação atual não tem o *flag* de otimização para $O(n)$).
  * **Contagem de Passos:** Contabiliza cada **comparação** (`COUNT_CMP()`) e cada **troca** (`COUNT_SWAP()`).

### 2\. Insertion Sort

  * **Ideia Central:** Constrói o array ordenado um item por vez. Ele pega um elemento da entrada e o insere na sua posição correta dentro da sublista já ordenada, movendo os elementos maiores para a direita.
  * **Complexidade de Tempo (Pior e Médio Caso):** $O(n^2)$
  * **Complexidade de Tempo (Melhor Caso - Array Ordenado):** $O(n)$
  * **Contagem de Passos:** Contabiliza a comparação (`COUNT_CMP()`) no `while` e o **deslocamento/cópia** de dados (`COUNT_SWAP()`).

### 3\. Heap Sort

  * **Ideia Central:** Utiliza a estrutura de dados **Heap Binário Máximo**. Primeiro, constrói um Max-Heap a partir do array. Em seguida, o maior elemento (a raiz do Heap) é trocado com o último elemento. O Heap é reconstruído e o processo se repete no sub-array restante.
  * **Complexidade de Tempo (Pior, Médio e Melhor Caso):** $O(n \log n)$
  * **Contagem de Passos:** Contabiliza as **comparações** na função `heapify` e as **trocas** (`COUNT_SWAP()`) na `heapify` e no loop principal.


