%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% Como gerar o documento PDF final
%
% Por: Abrantes Araújo Silva Filho
%      abrantesasf@gmail.com


Todas configurações foram atualizadas para utilizar o XeTeX na produção da
versão final em PDF do documento. Para produzir, basta fazer:

xelatex artigo.tex

O XeTeX utiliza o xdvipdfmx para gerar o PDF e, por padrão, cria PDFs com
versão 1.5. Se você quiser gerar um PDF com versão mais nova, basta rodar
o comando abaixo, trocando o número "5" por outra versão mais atualizada:

xelatex --output-driver="xdvipdfmx -V 5" artigo.tex
