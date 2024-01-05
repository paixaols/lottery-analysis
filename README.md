# Análise da loteria

Cada prêmio milionário da loteria faz surgir fórmulas de como aumentar as chances de acertar os números sorteados. Para analisar a viabilidade dessa ideia, esse projeto coleta e analisa os dados dos sorteios passados da mega-sena.

# Extração de dados

Os dados para a presente análise são os resultados dos sorteios passados da mega-sena, coletados diretamente do site da Caixa. A coleta foi automatizada utilizando a biblioteca selenium. Foram coletados os resultados de todos os sorteios desde o concurso 1, realizado em 11/03/1996, até o concurso 2670, realizado em 31/12/2023.

# Análise de dados

Nesses concursos cada número foi sorteado em média 267 vezes, naturalmente com flutuações em torno do valor médio. Como primeiro indicativo de um sorteio com probabilidade uniforme, nenhum número foi sorteado com frequência muito maior ou muito menor que a média.

Essas flutuações na frequência em torno do valor médio devem seguem uma distribuição normal para um sorteio com probabilidades iguais para todos os números. Para verificar a normalidade foi utilizado o teste de normalidade de D'Agostino e Pearson, implementado em scipy.stats.normaltest. O teste avalia a hipótese nula de que a amostra testada é gerada por uma distribuição normal. Aplicando o teste aos dados em questão, obtém-se um p-valor de 0,66. Considerando um nível de confiança de 95%, o teste implica na impossibilidade de rejeitar a hipótese nula.

# Conclusão

A análise realizada mostra que os resultados da mega-sena se comportam como esperado em sorteios com iguais probabilidades para todos os números. Não há evidência de outra estratégia para ganhar o prêmio além de contar com a sorte.
