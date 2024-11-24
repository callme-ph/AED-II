## Unidade 2 - Trabalho 1

● Utilizando o Gephi, aplicar os conhecimentos vistos no curso para analisar a rede de co-autoria dos professores permanentes do Programa de Pós-Graduação em Engenharia Elétrica e de Computação (PPgEEC)

● Base de dados: https://abre.ai/ltcE

## Requisito 1
#### ● O tamanho do vértice deverá ser proporcional a quantidade de vizinhos.

#### ● As cores devem ser relacionadas com Closeness ou Betweenness ou Eigenvector Centrality

#### ● Adotar um layout que seja razoável perceber a diferença entre as cores do vértices

<p align="justify"> O banco de dados foi importado para o Gephi para manipulação do grafo, um layout circular foi adotado para melhor visualização do conjunto de nós e suas ligações. Como requisitado, a primeira alteração foi feita no tamanho dos nós, definido baseado no grau do nó. Na Aba "Aparência" da interface "Visão Geral", o tamnho do nó foi definido baseado no Ranking e a opção escolhida foi o grau com tamanho entre 10 e 50. As cores foram definidas de acordo com a métrica betweenness centrality que mede quão central um nó é em relação aos caminhos de todos os pares de nós da rede que passam por este nó. Os nós mais escuros possuem um grau de centralidade maior.
O grafo resultante no Gephi foi este:
</p>

<p align="center">
  <img width="400" src="Rede 1/img/Rede1.png">
  <img width="400" src="Rede 1/img/Rede1_semarestas.png">
</p>

## Requisito 2
#### ● A partir da rede construída gerar uma figura similar no gephi destacando o k-core e o k-shell da rede. O layout é de livre escolha. Os vértices devem ter um tamanho proporcional a propriedade degree. A figura deverá estar acompanhada de descrição/explicação.

<p align="justify"> A rede é exibida com o layout Fruchterman Reingold e depois, Sem sobreposição; Para fazaer a edição da rede baseda no k-core da rede é possível usar o filtro de Topologia da rede para colorir os nós de diferentes formas. Inicialmente é necessário selecionar uma cor base para os nós, filtrar os nós com k-core igual 17 e pinta-los de vermelho para representar o k-shell - ambos os nós com k-core 17 e 18 serão coloridos, porém, após colorir os nós com k-core igual a 18 os nós serão diferenciados - e o depois filtrar os nós com k-core igual à 18 e pinta-los de azul. Assim, após remover os filtros os nós com k-core igual a 18 estarão azuis, os nós em vermelho serão o k-shell pois serão os nós do k-core 18 menos os nós do k-core 17 e o restante dos nós estarão com a cor base.

Outra forma de destacar os nós do k-core e do k-shell é exportando a planilha de nós e a de arestas do Gephi para o google colaboratory e usar a biblioteca OSMNX e NetworkX para visualização, cálculo do k-core e k-shell. Além da biblioteca do Pandas para adicionar na planilha as colunas que indicam se um nó pertence ao k-core ou k-shell, que serão as propriedades usadas no Gephi para personalizar o grafo. Depois das alterações, só fazer o download do arquivo CSV e importar novamente para o Gephi. O código feito pode ser visto [aqui.](https://colab.research.google.com/drive/1b9sFtuU_ssYOIrpJj7rhgnWIUVq8_m21?usp=sharing)
</p>

A rede exibida usando o NetworkX e o Matplotlib:

<p align="center">
  <img width="400" src="Rede 2/img/Rede2_spring_layout.png">
  <img width="400" src="Rede 2/img/Rede2_circular_layout.png">
  <img width="600" src="Rede 2/img/Rede2_k-core_shell.png">
</p>

 O grafo exibido no Gephi após alteração das cores e tamanho dos nós:

 <p align="center">
  <img width="400" src="Rede 2/img/Rede2.png">
  <img width="400" src="Rede 2/img/Rede2.svg">
  <img width="600" src="Rede 2/img/Rede2_semarestas.png">
  <img width="600" src="Rede 2/img/Rede2_semarestas.svg">
</p>
