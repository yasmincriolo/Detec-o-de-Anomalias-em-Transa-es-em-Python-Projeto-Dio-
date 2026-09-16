# Detecção de Anomalias em Transações Financeiras

## Descrição do Projeto
Neste projeto, desenvolvi um sistema inteligente de detecção de fraudes e anomalias em transações financeiras utilizando Python. O objetivo é identificar comportamentos atípicos e compras suspeitas em meio a um grande volume de dados, simulando um mecanismo antifraude real utilizado por instituições financeiras.

## Tecnologias Utilizadas
* **Python**
* **Pandas & NumPy** (Manipulação e estruturação de dados)
* **Scikit-learn** (`StandardScaler` para normalização e `IsolationForest` para modelagem)
* **Matplotlib & Seaborn** (Construção do painel visual e gráficos analíticos)
* **Jupyter Notebook / Google Colab**

## Estrutura e Etapas do Projeto
O código foi desenvolvido de forma modular e limpa, dividido nas seguintes etapas:

1. **Geração e Estruturação dos Dados:** 
   * Simulação de uma base de dados realista contendo **4 variáveis chave**:
     * `Valor_Transacao` (Valor financeiro da compra)
     * `Distancia_Local` (Distância geográfica do local da transação)
     * `Hora_Do_Dia` (Horário da operação, identificando padrões suspeitos de madrugada)
     * `Tentativas_Senha` (Número de tentativas de autenticação)

2. **Pré-processamento e Padronização:**
   * Aplicação do `StandardScaler` para colocar todas as variáveis na mesma escala matemática, garantindo que o algoritmo processe os dados de forma correta e sem viés.

3. **Treinamento do Modelo de Machine Learning:**
   * Utilização do algoritmo **Isolation Forest** (uma técnica de aprendizado não supervisionado altamente eficiente para isolar *outliers* e anomalias sem a necessidade de rótulos prévios de fraude).
   * Configuração do parâmetro de contaminação (`contamination=0.01`) para isolar o percentual esperado de comportamentos suspeitos.

4. **Geração de Painel Gráfico (Visualizações):**
   * O script gera **5 gráficos profissionais** para validação e interpretação dos resultados:
     * **Gráfico 1:** Mapa de Correlação (Heatmap) entre as variáveis.
     * **Gráfico 2:** Gráfico de Dispersão (Valor da Transação vs Distância do Local).
     * **Gráfico 3:** Gráfico de Dispersão (Horário da Compra vs Valor).
     * **Gráfico 4:** Boxplot analítico de Tentativas de Senha por status da transação.
     * **Gráfico 5:** Gráfico de Barras comparativo do volume total de transações Normais versus Fraudes detectadas.

## Conclusão
Este projeto permitiu aplicar conceitos práticos de Ciência de Dados e Inteligência Artificial na resolução de um problema crítico de segurança digital, estruturando um pipeline completo desde a simulação e tratamento dos dados até a modelagem preditiva e visualização avançada dos resultados.
