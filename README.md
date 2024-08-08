🔬Teste T Pareado - Aplicação prática e necessidade de transformações
(Hoje aprendi duas novas ferramentas em estatística!)

Você já ouviu falar sobre "weekend effect"❓

O "efeito final de semana" ganhou notoriedade no mercado financeiro nas décadas de 80 e 90, quando estudos demonstraram que os retornos médios das ações na segunda-feira eram consistentemente menores que os retornos das sextas-feiras anteriores. Apesar das diversas teorias propostas, a razão exata para esse fenômeno ainda é debatida.

Para investigar se esse efeito ainda é relevante, foram realizados alguns testes e os resultados são muito interessantes!

1️⃣ Aplicado o 'Teste T Pareado' aos dados do IBOVESPA, comparando os retornos médios das segundas e sextas-feiras.

Pergunta: Esse efeito ainda pode ser visto nos retornos do IBOV, desde 2022 até a atualidade?

"Hipótese H0 (nula): As médias de retorno não diferem estatisticamente
Hipótese H1 (alternativa): As médias de retorno diferem estatisticamente"

Neste primeiro cenário concluímos que em um curto período de tempo, falhamos em rejeitar H0, portanto não há "weekend effect". 

Mas como minha curiosidade foi aguçada, resolvi analisar toda a linha temporal do IBOV. Aqui a análise fica bem interessante:

2️⃣ Para reforçar a investigação se esse efeito foi relevante em toda a linha temporal, o mesmo teste é aplicado, obtendo download de todos os dados do IBOV através da biblioteca 'yfinance'.

"Hipótese H0 (nula) e H1 (alternativa) continuam as mesmas"

Neste trecho, como a premissa de normalização das amostras é exigida pelo Teste T Pareado, concluí que não houve normalização, impossibilitando a validade do teste.

3️⃣ Mesmo após aplicar a transformação logarítmica, as diferenças entre os retornos não seguiram uma distribuição normal.

Abaixo, os dois testes que aprendi:

4️⃣ A transformação de 'Box-Cox' foi aplicada na tentativa de normalizar as diferenças, mas ainda assim, a normalidade não foi alcançada, invalidando o uso do Teste T Pareado.

5️⃣ E finalmente: o Teste de Wilcoxon foi utilizado como uma alternativa não paramétrica ao Teste T Pareado. Esse teste não requer normalidade das diferenças. O 'p-valor' obtido foi 0.0027, indicando uma diferença estatisticamente significativa entre os retornos de sexta-feira e segunda-feira. Este resultado sugere que o "weekend effect" está presente no histórico completo do IBOVESPA.

✅ Conclusão: Podemos afirmar que quanto maior a diferença temporal, mais é notado que os retornos médios das segundas e sextas-feiras diferem estatisticamente.
