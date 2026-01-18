# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas. Neste Lab DIO, você aprenderá a usar o SageMaker Canvas para criar previsões de estoque baseadas em Machine Learning (ML). Siga os passos abaixo para completar o desafio!

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira nosso repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).


## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)


### 1. Selecionar Dataset  
Naveguei até a pasta **transferência** do meu computador e selecionei o dataset **"mapa_estoque_ficticio_produtos_eletronicos.csv"**, que eu mesmo criei com o Gemini e o ChatGPT. Este dataset tem mais linhas em relação ao modelo sugerido pelo professor, por isso achei que ficou adequado para treinar e testar o modelo de *machine learning* para previsão de estoque.

### 2. Construir/Treinar  
Importei o dataset que selecionei.  
Configurei as variáveis de entrada e saída, tendo a variável **quantidade vendida** como foco de saída e a variável **stock atual** como ponto de partida.  
Iniciei o treinamento do modelo escolhendo o modo **Quick Build**. Não descartei (droping) nenhuma coluna porque não havia necessidade.

### 3. Analisar  
Após o treinamento, examinei as métricas de desempenho do modelo, e estes foram os resultados:

- **Overall Confidence**: 95%  
- **Avg. wQL**: 0.045 — *Average Weighted Quantile Loss*  
- **MAPE**: 0.035 — *Mean Absolute Percentage Error*  
- **WAPE**: 0.038 — *Weighted Absolute Percentage Error*  
- **RMSE**: 2.450 — *Root Mean Square Error*  
- **MASE**: 0.650  

Verifiquei quais foram as principais características que mais influenciaram as previsões.  
Testei também um dos datasets sugeridos pelo professor: **"dataset-1000-com-preco-variavel-e-renovacao-estoque.csv"**.

### 4. Prever  
Usei o modelo treinado para gerar previsões na linha temporal de um dia, tanto do **estoque completo** quanto de **um produto individualmente**.  
Exportei os resultados e analisei cuidadosamente as previsões produzidas.  

Estas são as análises estratégicas sugeridas pela IA:

#### 1º Do estoque completo  
**AI Strategic Analysis**  
**Sustain High Stock Levels**  
*Medium Risk*  
Sales have rebounded strongly in the last 3 days (Avg ~44.6), recovering from the dip seen on days 43-45. Forecast suggests demand will remain elevated near the P50 of 43.8.  

**Recommended Action**  
Ensure inventory coverage for at least 52 units to capitalize on the current upward trend.


#### 2º De um produto individual (número 107)  
**Monitor Emerging Demand**  
*High Risk*  
Data is extremely sparse (single data point), making trend analysis difficult. Forecast predicts stable volume around 6 units, but volatility remains unknown.  

**Recommended Action**  
Maintain conservative stock levels and manually review next orders until more history is gathered.


## A experiência foi ótima, muito gratificante, agradeço à DIO pela oportunidade concedida, muito obrigado!
