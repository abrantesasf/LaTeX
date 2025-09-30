%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%% Modelo de Prova para a UVV (ou outra escola qualquer).
%%% Por: Abrantes Araújo Silva Filho
%%%      abrantesasf@gmail.com


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%% CONFIGURAÇÕES GERAIS

A arquivo prova.tex é o arquivo de configuração e montagem geral da prova.
Você precisa alterar o conteúdo aqui.

Você pode ajustar:

    1) Cabeçalhos e rodapés: a prova tem um cabeçalho e rodapé padronizado. Você
       alterar as inforamções.
    
    2) Links e informações do PDF: o arquivo PDF final gerado terá uma série de
       propriedades e metadados que você pode ajustar aqui.
    
    3) Capa: a prova é impressa por padrão com uma capa clássica (geralmente eu
       coloco um trecho de algum livro importante). Você pode desabilitar.
    
    4) Intruções: aqui na UVV é obrigatória uma capa padronizada de instruções,
       contendo o nome do professor, valor da prova, etc. Você DEVE ALTERAR
       o arquivo main/instrucoes.tex para informar os dados corretos.
    
    5) As questões são digitadas no arquivo "main/questoes1.tex". Crie aqui
       as questões de sua prova!
       
    6) Bloco final: é possível incluir um bloco final padronizado nas provas.
       Por padrão esse bloco está desabilitado. Você pode habilitar aqui e
       escrever seu bloco final em "main/final.tex".

As figuras, gráficos e demais elementos visuais devem ser organizados dentro do
diretório "imagens", e referenciadas nas questões.

Se você incluir código externo, pode colocar esse código no diretório "codigo" e
usar includes padrão do LaTeX.


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%% AJUSTE DAS FONTES:

Este modelo de prova utiliza diversos arquivos de configuração que já estão OK,
exceto o arquivo que configura as fontes a serem utilizadas no documento.

Eu utilizo fontes comerciais produzidas por Matthew Butterick
(https://mbtype.com) que NÃO PODEM ser distribuídas. Para você indicar quais as
fontes vai utilizar, você PRECISA ALTERAR o arquivo

               utils/fontes.tex

e indicar o caminho das fontes que você quer utilizar.


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%% NÃO ALTERE O DIRETÓRIO "utils"!

Este modelo LaTeX é configurado em diversos módulos separados e contém muitas,
muitas configurações mesmo. Essas configurações estão todas em arquivos
separados no diretório "utils". Você NÃO DEVE ALTERAR ESSAS CONFIGURAÇÕES,
exceto de você for um usuário experiente de LaTeX e souber exatamente o que está
fazendo.

Por que o diretório "utils" tem tanta coisa? Pois esse é o diretório "utils" que
eu uso em TODOS os meus documentos LaTeX, com todas as configurações que fui
fazendo e acumulando durante 25 anos de uso de LaTeX. Não se preocupe: você
aprenderá a criar e acumular configurações também!


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%% COMO GERAR O DOCUMENTO FINAL:

Todas configurações foram atualizadas para utilizar o XeTeX na produção da
versão final em PDF do documento. Para produzir, basta fazer:

               xelatex prova.tex

O XeTeX utiliza o xdvipdfmx para gerar o PDF e, por padrão, cria PDFs com
versão 1.5. Se você quiser gerar um PDF com versão mais nova, basta rodar
o comando abaixo, trocando o número "5" por outra versão mais atualizada (se
você especificar um número de versão errado, o xdvipdfmx usará como fallback
a versão 5).

xelatex --output-driver="xdvipdfmx -V 5" prova.tex


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%% EM CASO DE DÚVIDA:

Se vire.
