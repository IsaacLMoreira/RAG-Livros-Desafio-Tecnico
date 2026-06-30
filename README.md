# RAG-Livros-Desafio-Tecnico
Analisando a entrega do meu desafio, notei que haviam melhorias necessárias para melhorar a busca semântica, trazendo resultados corretos.

No desenvolvimento do projeto, utilizei chunks muito longos na esperança de aumentar a área de busca e evitar que o modelo retorne um trecho errado. Entretanto notei que essa decisão causou o efeito contrário, no geral, o modelo retorna o livro correto, mas nem sempre o trecho esperado.

Além disso, mantive os cabeçalhos do Project Gutenberg indexados para facilitar a identificação da origem dos documentos. Hoje percebo que essa escolha também pode ter influenciado negativamente a recuperação, já que esses trechos possuem alta similaridade com muitas consultas, mas raramente contêm a resposta procurada.

Tendo em vista os problemas acima, eu diminuiria o tamanho de cada chunk e ajustaria a quantidade de overlap proporcionalmente, para que cada embedding represente informações mais específicas e coerentes.

Também removeria o cabeçalho excessivamente longo e extenso para facilitar a saída e interpretação do usuário, pois, mesmo sendo útil para mim saber onde o modelo está buscando o texto, para o usuário final, a informação pode atrapalhar mais do que ajudar.
