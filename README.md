# Predição de Interação entre Proteínas utilizando NLP
Este repositório contém o código e os dados utilizados para o trabalho final da disciplina de Processamento de Linguagem Natural (NLP). O objetivo do projeto é construir um modelo capaz de prever se duas proteínas irão interagir com base em suas sequências de aminoácidos. A predição de interações proteína-proteína (PPI) é essencial para entender redes biológicas, interações celulares e o desenvolvimento de vácinas, fármacos, dentre outros.

## Dados:
Os dados foram obtidos do STRING Database. Foi filtrado para baixar apenas interações com confiança acima de 40% de proteínas humanas e apenas um par de interações das mesmas proteínas (ou seja, apenas interações AB, ao invés de AB  e BA).

## Estrutura do Repositório

- **`dados/`**: Contém os dados brutos e processados utilizados no projeto.
  
    - `processed_ppi_data.zip`: Dataset processado e balanceado com interações positivas e negativas. Precisa ser descompactado para acessar o arquivo `processed_ppi_data.csv`.
    
    - `processed_ppi_data_sample.csv`: Dataset de amostra.
    
    - `metricsRF1.json`: Métricas de avaliação do Random Forest na primeira avaliação do notebook.

    - `metricsRF2.json`: Métricas de avaliação do Random Forest na segunda avaliação do notebook.
    
    - `metrics_lstm_attention1.json`: Métricas de avaliação da LSTM com atenção na primeira avaliação do notebook.
    
    - `metrics_lstm_attention2.json`: Métricas de avaliação da LSTM com atenção na segunda avaliação do notebook.
      
 - **`NLP_TP_FINAL.ipynb`**: Notebook contendo todo o código utilizado para o pré-processamento, geração de embeddings, treinamento e avaliação dos modelos. Além das análises e discussões.

## Dependências

Para executar o código, é necessário instalar as seguintes bibliotecas:

``` pip install --upgrade transformers datasets evaluate nltk sklearn pandas biopython seaborn matplotlib requests tqdm ```

Além disso, é recomendado o uso de uma GPU para acelerar o treinamento dos modelos.

