capa-epusp-abntex2
==================

Customizações do abntex2 (capa e folha de rosto) para monografias (trabalhos de conclusão de curso, dissertações e teses) da Escola Politécnica da USP

Para utilizar, copie o arquivo capa-epusp-abntex2.sty para a pasta do seu projeto e adicione \usepackage{capa-epusp-abntex2} ao seu arquivo latex.


Dicas:

- Não se esqueçam de colocar o \caption{} das tabelas e das figuras no início, antes da inserção do objeto. Deste modo o título ficará acima das ilustrações (figura, tabela, gráfico...), como pede as diretrizes da Escola Politécnica da USP.
    Ex.: \caption{Diagrama de blocos do projeto conceitual}

- Para adicionar as fontes embaixo das figuras use o comando \legend{}.
    Ex.: \legend{Fonte: o autor}

- Exemplo de inserção de figura (notar a posição do \caption{} e do \legend{}):
    \begin{figure}[H]
	\centering
	\caption{Diagrama de blocos do projeto conceitual}
		\setlength\fboxsep{1.1pt}
		\setlength\fboxrule{0.3pt}
		\fbox{\includegraphics[width=16cm]{Figuras/DiagramaBlocos.png}}
	\legend{Fonte: o autor}
	\label{fig:DiagramaBlocos}
    \end{figure}

- A área de concentração pode ser inserida com o comando \areaconcentracao{} no arquivo topo do latex.
    Ex.: \areaconcentracao{Engenharia Elétrica - Sistemas Eletrônicos}

- Salve todos os arquivos do projeto com a codificação UTF8!
