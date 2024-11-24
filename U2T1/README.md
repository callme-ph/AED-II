## Unidade 2 - Trabalho 1

● Utilizando o Gephi, aplicar os conhecimentos vistos no curso para analisar a rede de co-autoria dos professores permanentes do Programa de Pós-Graduação em Engenharia Elétrica e de Computação (PPgEEC)

● Base de dados: https://abre.ai/ltcE

## Rede 1
#### ● O tamanho do vértice deverá ser proporcional a quantidade de vizinhos.

#### ● As cores devem ser relacionadas com Closeness ou Betweenness ou Eigenvector Centrality

#### ● Adotar um layout que seja razoável perceber a diferença entre as cores do vértices

O banco de dados foi importado para o Gephi para manipulação do grafo, um layout circular foi adotado para melhor visualização do conjunto de nós e suas ligações. Como requisitado, a primeira alteração foi feita no tamanho dos nós, definido baseado no grau do nó. Na Aba "Aparência" da interface "Visão Geral", o tamnho do nó foi definido baseado no Ranking e a opção escolhida foi o grau com tamanho entre 10 e 50. As cores foram definidas de acordo com a métrica betweenness centrality que mede quão central um nó é em relação aos caminhos de todos os pares de nós da rede. O grafo resultante no Gephi foi este:

This is from GitHub's support:

Markdown doesn't allow you to tweak alignment directly (see docs here: http://daringfireball.net/projects/markdown/syntax#img), but you can just use a raw HTML 'img' tag and do the alignment with inline css.

So it is possible to align images! You just have to use inline CSS to solve the problem. You can take an example from my GitHub repository. At the bottom of README.md there is a centered aligned image. For simplicity you can just do as follows:

<p align="center">
  <img width="300" src="Rede 1/img/Rede1.png">
  <img width="300" src="Rede 1/img/Rede1.svg">
</p>
