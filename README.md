# CB-Times-Series
Previsão de vendas semanal 

Projeto - Prever a quantidade de vendas de cada produto para a proxima semana.

1 - Dados coletados e processados:
 - Coleta de dados do sistema de vendas da empresa, a quantidade de venda de cada produto semanalmente, dados sobre o tempo(temperatura media da semana) durante o periodo.

2: Analise exploratoria dados, engenharia de recursos e modelagem:
 - Os dados foram analisados e existe uma grande correlação entre a temperatura e a data em relação as vendas, o melhor resultado sobre a baseline foi o       Diff(Diferença entre a semana atual para as anteriores), na parte da modelagem foi escolhido um LighGBM.
 - Baseline : 9.5 - (Median_Absolute_Error)
 - Diff - LighGBM: 6.6 - (Median_Absolute_Error)

3: Tunning do LightGBM:
 - Foi utilizado o scikit-optimizer para tunar o modelo.
 - Diff - LighGBM Tunning: 5.7 - (Median_Absolute_Error)

4: Validação avançada para times series:
 - Todos os dados foram dividos em 7 blocos para a validação.
 - Prequential Expanding - Diff - LighGBM Tunning: Media : 7.3 - (Median_Absolute_Error)
 - Prequential Sliding - Diff - LighGBM Tunning: Media : 9.9 - (Median_Absolute_Error)

5: Deploy com Flask:
 - Em andamento
