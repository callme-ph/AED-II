## Avaliação de complexidade de algorítmos

Link do vídeo: https://www.loom.com/share/a012fc35c013430cae6900a881c109ad?sid=37183d79-1a8d-49a7-a2fd-0bb64ba5a2f5

O trabalho teve como objetivo analisar a complexidade dos algorítmos de busca em uma árvore de busca binária. O algoritmo solver_closest que busca o elemento com valor mais próximo de um alvo e o o algoritmo solver_kth_largest que recebe um inteiro N e busca o N-ésimo maior valor da BST.

Comparação dos algorítmos usando um gráfico de tempos em função do tamanhos dos vetores:

<p align="center">
 <img width="850" src="img/Time_Complexity.png">
</p>  

É perceptível a diferença de complexidade de execução dos algorítmos, comparando os dois em conjunto não é possível ver uma variação no tempo de execução do algoritmo solver_closest mas podemos tentar visualizar o comportamento dele isoladamente para ver se há ou não variação do tempo de execução:

<p align="center">
 <img width="850" src="img/Variação closest.png">
</p> 
