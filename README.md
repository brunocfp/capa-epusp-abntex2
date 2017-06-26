capa-epusp-abntex2
==================

Customizações do abntex2 (capa e folha de rosto) para monografias (trabalhos de conclusão de curso, dissertações e teses) da Escola Politécnica da USP

Para utilizar, copie o arquivo capa-epusp-abntex2.sty para a pasta do seu projeto e adicione \usepackage{capa-epusp-abntex2} ao seu arquivo latex.

Última modificação: 26/06/17
- Inclusão do comando "\imprimirfalsafolhaderosto" para impressão da falsa folha de rosto;
- Remoção de "warnings".


Dicas para elaboração do trabalho:

- A falsa folha de rosto, se necessária, deve ser inserida entre a capa e a folha de rosto, por meio do comando \imprimirfalsafolhaderosto.
	Ex.: 	\imprimircapa
		\imprimirfalsafolhaderosto
		\imprimirfolhaderosto

- Não se esqueçam de colocar o \caption{} das tabelas e das figuras no início, antes da inserção do objeto. Deste modo o título ficará acima das ilustrações (figura, tabela, gráfico...), como pede as diretrizes da Escola Politécnica da USP.

        Ex.: \caption{Diagrama de blocos do projeto conceitual.}

- Para adicionar as fontes embaixo das figuras use o comando \legend{}.

        Ex.: \legend{Fonte: Autor.}

- Exemplo de inserção de figura (notar a posição do \caption{} e do \legend{}):

		\begin{figure}[!ht]
			\centering
			\caption{Resposta ao degrau da planta.}
			\setlength\fboxsep{1.1pt}
			\setlength\fboxrule{0.3pt}
			\fbox{\includegraphics[width=\hboxtextwidth]{Figuras/dados_ensaio.png}}
			\legend{Fonte: Autor.}
			\label{fig:dados_ensaio}
		\end{figure}

- A área de concentração e o tipo de trabalho podem ser inseridos com os comandos "\areaconcentracao{}" e "\tipotrabalho{}", respectivamente:

		Ex.: \areaconcentracao{Engenharia Elétrica - Sistemas Eletrônicos}
		Ex.: \tipotrabalho{Dissertação}

- O seguinte comando pode ser utilizado para evitar quebra de notas de rodapé entre páginas:
	
		\interfootnotelinepenalty=10000
	
- Os seguintes comandos podem ser utilizados para evitar que parágrafos se iniciem com uma única linha no final de uma página:
OBS: Neste caso, o parágrafo inteiro é jogado para a próxima página.

		\widowpenalty=10000
		\clubpenalty=10000
	
- O comando seguinte pode ser utilizado para redução de warnings do tipo "underfull \vbox" quando se opta pelo trabalho no modo "twoside" (frente e verso):
	
		\raggedbottom

- Salve todos os arquivos do projeto com a codificação UTF8!

- Dúvidas: brunocfp@gmail.com

Bom trabalho!
Bruno Fernandes
