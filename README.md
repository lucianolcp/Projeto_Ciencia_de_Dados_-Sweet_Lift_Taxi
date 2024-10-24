# Projeto Sweet Lift Taxi: Previsão de Pedidos de Táxi

## Descrição do Projeto
O objetivo deste projeto é prever a quantidade de pedidos de táxi para a próxima hora, a fim de atrair mais motoristas durante o horário de pico. Para isso, foi desenvolvido um modelo preditivo.
A métrica **REQM** no conjunto de teste não deve ser superior a 48.

## Ferramentas e Bibliotecas Utilizadas
- **Python**: Linguagem principal utilizada para a análise.
- **Pandas**: Biblioteca para manipulação e análise de dados.
- **NumPy**: Biblioteca para computação numérica e manipulação de arrays.
- **statsmodels**: Biblioteca para modelagem estatística, incluindo SARIMA.
- **Prophet**: Biblioteca para previsão de séries temporais desenvolvida pelo Facebook.
- **TensorFlow/Keras**: Bibliotecas para construção e treinamento de modelos de LSTM.

## Descrição dos Dados
Os dados são armazenados no arquivo `taxi.csv`. 
- **num_orders**: coluna que contém o número de pedidos de táxi.

## Passo a Passo do Projeto

1. **Carregamento dos Dados**:
   - Download do conjunto de dados a partir do arquivo `taxi.csv`.

2. **Amostragem dos Dados**:
   - Realização de uma nova amostragem para que cada ponto dos dados originais fique dentro de intervalos de uma hora.

3. **Análise dos Dados**:
   - Inspeção inicial dos dados para entender sua estrutura e identificar possíveis problemas.

4. **Treinamento de Modelos**:
   - Treinamento de diferentes modelos com diferentes hiperparâmetros, utilizando 10% do conjunto de dados inicial como amostra de teste.
   - Modelos testados incluem:
     - SARIMA
     - Prophet
     - LSTM

5. **Avaliação dos Modelos**:
   - Teste dos modelos usando a amostra de teste e cálculo da métrica REQM.

6. **Conclusões**:
   - Compilação dos resultados obtidos e recomendações baseadas no desempenho dos modelos.

## Conclusão
A empresa Taxi Corrida Maluca solicitou a criação de um modelo preditivo para estimar o número de pedidos de táxi na próxima hora, utilizando dados históricos. O objetivo principal era desenvolver um modelo que apresentasse um Erro Quadrático Médio (REQM) menor que 48 no conjunto de teste, para que pudesse ser implementado em um sistema de previsão em tempo real.

Os modelos foram avaliados com base na métrica REQM utilizando o conjunto de teste. Os resultados foram os seguintes:

- **SARIMA**: REQM = 44.4601
- **Prophet**: REQM = 44.4765
- **LSTM**: REQM = 45.5489

Todos os modelos alcançaram um REQM inferior ao limite de 48 estabelecido como critério de sucesso.

Com base nos resultados, o modelo **SARIMA** é recomendado para implementação em produção, dada sua leve superioridade em precisão e sua natureza mais transparente e fácil de ajustar. O modelo **Prophet** pode ser considerado como uma alternativa, especialmente em cenários onde se deseje maior flexibilidade ou ajuste a múltiplas sazonalidades.

## Aprendizados
Este projeto permitiu-me desenvolver as seguintes habilidades:
- **Análise de Séries Temporais**: Compreensão dos princípios e técnicas de previsão, incluindo modelos como SARIMA e Prophet.
- **Treinamento de Modelos de Machine Learning**: Aprendizado sobre como configurar e treinar diferentes modelos de aprendizado de máquina, como LSTM.
- **Avaliação de Modelos**: Habilidade em utilizar métricas como REQM para medir a performance dos modelos e comparar seus resultados.
- **Implementação Prática**: Experiência prática na aplicação de algoritmos de previsão em um contexto do mundo real, visando a otimização de operações em um negócio.

## Como Executar o Projeto

- Clone o repositório.
- Navegue até o diretório do projeto.
- Abra o projeto no seu IDE favorito.
- Instale as dependências.
- Execute o script principal.

## Contato

Luciano Pinto
[LinkedIn](https://www.linkedin.com/in/lucianolcp/)  
Email: dslucianopinto@gmail.com





