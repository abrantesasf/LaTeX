%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% Como gerar o documento PDF final
%
% Por: Abrantes Araújo Silva Filho
%      abrantesasf@gmail.com


Todas configurações foram atualizadas para utilizar o XeTeX na produção da
versão final em PDF do documento. Para produzir, basta fazer:

xelatex prova.tex

O XeTeX utiliza o xdvipdfmx para gerar o PDF e, por padrão, cria PDFs com
versão 1.5. Se você quiser gerar um PDF com versão mais nova, basta rodar
o comando abaixo, trocando o número "5" por outra versão mais atualizada (se
você especificar um número de versão errado, o xdvipdfmx usará como fallback
a versão 5).

xelatex --output-driver="xdvipdfmx -V 5" prova.tex
