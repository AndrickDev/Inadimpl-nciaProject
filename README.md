
# Modelo Preditivo para Risco de Inadimplência com XGBoost

## 1\. Objetivo do Projeto

Este projeto de Ciência de Dados tem como objetivo principal desenvolver um modelo de Machine Learning capaz de prever com alta acurácia a probabilidade de um cliente de cartão de crédito se tornar inadimplente no mês seguinte. A implementação de um modelo como este é crucial para instituições financeiras, pois permite a tomada de decisões mais estratégicas na concessão de crédito, mitigando riscos e reduzindo perdas financeiras.

## 2\. Resultados e Conquistas

O modelo final, um `XGBoost` otimizado, alcançou uma performance robusta, demonstrando sua eficácia na distinção entre clientes adimplentes e inadimplentes.

  * **Métrica Principal (AUC):** **0.78** no conjunto de teste.
  * **Técnicas Aplicadas:** Otimização de Hiperparâmetros com `GridSearchCV` e Validação Cruzada Estratificada (`StratifiedKFold`).
  * **Principal Preditor de Risco:** A análise de importância das features revelou que o **histórico de pagamentos do último mês (`PAY_1`)** é o fator mais influente nas previsões do modelo.

## 3\. Metodologia

O projeto foi estruturado seguindo o ciclo de vida padrão de um projeto de Ciência de Dados:

1.  **Análise Exploratória de Dados (EDA):** Análise inicial para entender a distribuição dos dados, identificar correlações entre as variáveis e verificar o desbalanceamento da variável alvo (inadimplência).
2.  **Pré-processamento:** Aplicação de `StandardScaler` para padronizar as features numéricas, garantindo que o modelo não seja enviesado por diferentes escalas de valores.
3.  **Divisão dos Dados:** Os dados foram divididos em conjuntos de treino (80%) e teste (20%) utilizando a função `train_test_split` com o parâmetro `stratify`, para manter a proporção de classes desbalanceadas em ambas as amostras.
4.  **Otimização e Treinamento:**
      * Foi utilizado o algoritmo **XGBoost**, conhecido por sua alta performance.
      * A técnica **GridSearchCV** foi aplicada para realizar uma busca exaustiva pelos melhores hiperparâmetros (`n_estimators`, `max_depth`, `learning_rate`, etc.).
      * Para garantir a robustez do modelo, foi empregada a **Validação Cruzada Estratificada (`StratifiedKFold` com 5 splits)**, uma abordagem essencial para dados desbalanceados.
5.  **Avaliação:** O modelo final foi avaliado no conjunto de teste com as seguintes métricas:
      * **Curva ROC e AUC:** Para medir a capacidade geral de discriminação do modelo.
      * **Matriz de Confusão:** Para visualizar os erros de classificação (Falsos Positivos e Falsos Negativos).
      * **Relatório de Classificação:** Analisando `Precision`, `Recall` e `F1-Score` para ambas as classes.

## 4\. Tecnologias Utilizadas

  * **Linguagem:** Python
  * **Bibliotecas de Análise de Dados:** Pandas, NumPy
  * **Bibliotecas de Machine Learning:** Scikit-learn, XGBoost
  * **Bibliotecas de Visualização:** Matplotlib, Seaborn
  * **Ambiente:** Jupyter Notebook / Google Colab

## 5\. Como Executar o Projeto

Para replicar os resultados, siga os passos abaixo:

1.  Clone este repositório:
    ```bash
    git clone (https://github.com/AndrickDev/Inadimpl-nciaProject)
    ```
2.  Navegue até o diretório do projeto:
    ```bash
    cd Inadimpl-nciaProject
    ```
3.  Instale as dependências necessárias:
    ```bash
    pip install pandas numpy scikit-learn xgboost matplotlib seaborn jupyter
    ```
4.  Certifique-se de que o dataset `UCI_Credit_Card.csv` esteja no mesmo diretório.
5.  Inicie o Jupyter Notebook e execute o arquivo `inadimplência.ipynb`:
    ```bash
    jupyter notebook inadimplência.ipynb
    ```

## 6\. Autor

  * **Andrick Rodrigues**
      * **LinkedIn:** [https://www.linkedin.com/in/seu-linkedin/](https://www.google.com/search?q=https://www.linkedin.com/in/andrick-rodrigues/)
      * **GitHub:** [https://github.com/seu-github](https://www.google.com/search?q=https://github.com/AndrickDev)
      * **Email:** andrickneer@gmail.com
