## Unidade 2 - Trabalho 1

● Utilizando o Gephi, aplicar os conhecimentos vistos no curso para analisar a rede de co-autoria dos professores permanentes do Programa de Pós-Graduação em Engenharia Elétrica e de Computação (PPgEEC)

● Base de dados: https://abre.ai/ltcE

● Link do vídeo: https://drive.google.com/file/d/1-xoAY0vuk5X9kWA6TmuRhU7u3khBw1KV/view?usp=sharing

## Requisito 1
#### ● O tamanho do vértice deverá ser proporcional a quantidade de vizinhos.

#### ● As cores devem ser relacionadas com Closeness ou Betweenness ou Eigenvector Centrality

#### ● Adotar um layout que seja razoável perceber a diferença entre as cores do vértices

<p align="justify"> O banco de dados foi importado para o Gephi para manipulação do grafo, um layout circular foi adotado para melhor visualização do conjunto de nós e suas ligações. Como requisitado, a primeira alteração foi feita no tamanho dos nós, definido baseado no grau do nó. Na Aba "Aparência" da interface "Visão Geral", o tamnho do nó foi definido baseado no Ranking e a opção escolhida foi o grau com tamanho entre 10 e 50. As cores foram definidas de acordo com as métricas de centralidade como exibido nos requisitos da atividade. Os nós mais claros possuem um grau de centralidade maior.
Os grafos resultantee no Gephi foram estes:
</p>

<h3 align="center"> Centralidade por Grau e Betweenness </h3>
 <p align="center">
   <img width="500" src="Requisito 1/img/Rede1_Degree.png">
   <img width="500" src="Requisito 1/img/Rede1.png">  
 </p>
 <h3 align="center"> Centralidade por proximidade e por autovetor </h3>
 <p>
    <img width="500" src="Requisito 1/img/Rede1_Closeness.png">
    <img width="500" src="Requisito 1/img/Rede1_Eigenvector.png">    
 </p>

## Requisito 2
#### ● A partir da rede construída gerar uma figura similar no gephi destacando o k-core e o k-shell da rede. O layout é de livre escolha. Os vértices devem ter um tamanho proporcional a propriedade degree. A figura deverá estar acompanhada de descrição/explicação.

<p align="justify"> A rede é exibida com o layout Fruchterman Reingold e depois, Sem sobreposição; Para fazaer a edição da rede baseda no k-core da rede é possível usar o filtro de Topologia da rede para colorir os nós de diferentes formas. Inicialmente é necessário selecionar uma cor base para os nós, filtrar os nós com k-core igual 17 e pinta-los de vermelho para representar o k-shell - ambos os nós com k-core 17 e 18 serão coloridos, porém, após colorir os nós com k-core igual a 18 os nós serão diferenciados - e o depois filtrar os nós com k-core igual à 18 e pinta-los de azul. Assim, após remover os filtros os nós com k-core igual a 18 estarão azuis, os nós em vermelho serão o k-shell pois serão os nós do k-core 18 menos os nós do k-core 17 e o restante dos nós estarão com a cor base.

Outra forma de destacar os nós do k-core e do k-shell é exportando a planilha de nós e a de arestas do Gephi para o google colaboratory e usar a biblioteca OSMNX e NetworkX para visualização, cálculo do k-core e k-shell. Além da biblioteca do Pandas para adicionar na planilha as colunas que indicam se um nó pertence ao k-core ou k-shell, que serão as propriedades usadas no Gephi para personalizar o grafo. Depois das alterações, só fazer o download do arquivo CSV e importar novamente para o Gephi. O código feito pode ser visto [aqui.](https://colab.research.google.com/drive/1b9sFtuU_ssYOIrpJj7rhgnWIUVq8_m21?usp=sharing)
</p>

A rede exibida usando o NetworkX e o Matplotlib:

<p align="center">
  <img width="400" src="Requisito 2/img/Rede2_spring_layout.png">
  <img width="400" src="Requisito 2/img/Rede2_circular_layout.png">
  <img width="500" src="Requisito 2/img/Rede2_k-core_shell.png">
</p>

 O grafo exibido no Gephi após alteração das cores e tamanho dos nós:

<p align="center">
  <img width="400" src="Requisito 2/img/Rede2.png">
  <img width="400" src="Requisito 2/img/Rede2_semarestas.png">
</p>

É possível também destacar os nós que fazem parte do 18º core e exibir os nomes dos autores referente à esses:

<p align="center">
  <img width="500" src="Requisito 2/img/Rede2_18th_core.png">
</p>

## Requisito 3
#### ● Disponibilizar a rede em produção com o plugin do Gephi que permite criar uma página HTML para exibir o grafo de forma dinâmica.

<p align="justify"> 
  
Para o terceiro requisito houve algumas mudanças na rede: Baseado na classe de modularidade as cores dos grafos foram definidas para facilmente identificar grupos da rede, para mais informações sobre o algoritmo usado pelo Gephi para identificar as classes, ver a [documentação](https://duckduckgo.com/?q=Vincent+D+Blondel%2C+Jean-Loup+Guillaume%2C+Renaud+Lambiotte%2C+Etienne+Lefebvre%2C+Fast+unfolding+of+communities+in+large+networks%2C+in+Journal+of+Statistical+Mechanics%3A+Theory+and+Experiment+2008+(10)%2C+P1000&t=h_&ia=web) disponibilizada no Gephi. O tamanho dos nós foram definidos baseados no grau de entrada dos nós pois é uma métrica importante para uma rede de co-autoria. Assim, com essas alterações, dois layouts foram aplicados: um foi o layout Fruchterman Reingold que perimite uma boa visualização da rede pois permite que os nós sejam bem distribuidos; E o layout do ForceAtlas 2 para tentar unir os nós em grupos. A visualização de ambos os layouts podem ser vistas abaixo:
</p>
<p align="center">
  <img width="400" src="Requisito 3/img/Rede3_FR.png">
  <img width="400" src="Requisito 3/img/Rede3_Atlas.png">
</p>

<p align="justify"> Ainda analisando a rede, foi calculado uma média de grau de aproximadamente 8 grau por nó, ao fazer a filtragem para visualizar somente os nós com 8 graus ou mais é possível ver que a maioria nós ainda permanecem visíveis, corroborando com o cálculo feito pelo Gephi.
</p>
<p align="center">
  <img width="400" src="Requisito 3/img/Rede3_8_degree.png">
</p>
<p align="justify"> 
  
Usando o plug-in SigmaExport do Gephi foi feito a exportação da rede para visualização interativa. É possível ver a rede pelo GitHub Pages neste [link.](https://callme-ph.github.io/co-authorship-graduate)
</p>
