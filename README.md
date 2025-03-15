# 📊 Análise RFM para Segmentação de Clientes em E-commerce  

## 🎯 Objetivo  
Este projeto tem como objetivo **calcular os indicadores de Recência (R), Frequência (F) e Ticket Médio (M) dos clientes** de um e-commerce. Esses indicadores permitem segmentar os clientes com base no seu comportamento de compra, auxiliando na criação de estratégias de marketing mais eficazes.  

---

## 📌 Contexto  
Uma empresa de **e-commerce** contratou um time de dados para analisar o comportamento de seus clientes e identificar padrões de consumo. O principal desafio é determinar **quais clientes compram com mais frequência, quanto gastam em média e há quanto tempo realizaram sua última compra**.  

Para isso, foi fornecido um **dataset contendo informações das compras realizadas por clientes de 37 países**, que deve ser tratado, limpo e analisado para a extração das métricas RFM.  

---

## 📂 Dados  
O dataset contém as seguintes colunas:  

| **Coluna**     | **Descrição**                                         |
|---------------|-----------------------------------------------------|
| **CustomerID** | Código de identificação do cliente                 |
| **InvoiceNo**  | Código da fatura                                    |
| **StockCode**  | Código do produto no estoque                       |
| **Description** | Descrição do produto                               |
| **Quantity**   | Quantidade do produto na compra                    |
| **InvoiceDate** | Data da compra                                     |
| **UnitPrice**  | Preço unitário do produto                          |
| **Country**    | País onde a compra foi realizada                   |

🔹 **Cálculo do Ticket Médio:**  
> **Ticket Médio = Total Gasto / Quantidade de Compras**  

🔹 **Cálculo das Métricas RFM:**  
- **R (Recency):** Tempo desde a última compra do cliente.  
- **F (Frequency):** Quantidade de compras realizadas.  
- **M (Monetary):** Valor médio gasto por pedido.  

---

# 🛠️ Ferramentas Utilizadas  
- **Python** para manipulação de dados  
- **Pandas** para limpeza e análise do dataset  
- **Matplotlib e Seaborn** para visualização dos dados  
- **SQL** para consultas e agregação de métricas  
- **Google Colab** para desenvolvimento do código  

---

# 📌 Etapas de Desenvolvimento  

### 📍 Etapa 1: Carregamento e Inspeção dos Dados  
✔️ Leitura do dataset utilizando Pandas  
✔️ Verificação da distribuição dos dados com `describe()`  
✔️ Identificação de inconsistências, tipos de dados e possíveis problemas  

### 📍 Etapa 2: Tratamento de Dados  
✔️ Remoção de valores nulos em **CustomerID**  
✔️ Exclusão de registros com **preços e quantidades negativas**  
✔️ Verificação e remoção de **linhas duplicadas**  

### 📍 Etapa 3: Ajuste de Tipos de Dados  
✔️ Conversão da coluna **InvoiceDate** para **datetime**  
✔️ Ajuste do tipo de **CustomerID** para inteiro  

### 📍 Etapa 4: Tratamento de Outliers  
✔️ Remoção de registros com **quantidades extremas (>10.000 unidades)**  
✔️ Exclusão de preços **acima de R$ 5.000,00**, que podem indicar erros  

### 📍 Etapa 5: Criação de Coluna de Valor Total da Compra  
✔️ **TotalGasto = Quantity * UnitPrice**  

### 📍 Etapa 6: Identificação da Última Data de Compra  
✔️ Uso da função `max()` para encontrar a data mais recente no dataset  

### 📍 Etapa 7: Cálculo das Métricas RFM  
✔️ **R (Recência)**: Diferença entre a última compra do cliente e a data máxima do dataset  
✔️ **F (Frequência)**: Contagem do número de compras por cliente  
✔️ **M (Ticket Médio)**: Média do total gasto por pedido  

---

# 📊 Visualização dos Dados  
Foram gerados gráficos para melhor interpretação dos insights:  
📌 **Top 10 países com maior volume de vendas**  
📌 **Top 10 produtos mais vendidos**  
📌 **Evolução do valor total de vendas por mês**  
📌 **Vendas por país ao longo do tempo**  

---

# 📌 Conclusões e Próximos Passos  
✔️ As métricas RFM ajudam a **identificar clientes mais ativos e rentáveis**.  
✔️ O e-commerce pode **criar campanhas personalizadas** com base no comportamento dos clientes.  
✔️ Sugere-se implementar um **modelo de segmentação de clientes** utilizando Machine Learning para otimizar estratégias de marketing.  

🚀 **Próximos passos:**  
🔹 Criar clusters de clientes com base nos dados RFM.  
🔹 Integrar as métricas ao CRM da empresa para melhorar as ações comerciais.  

---

# 📎 Como Executar o Projeto?  
1️⃣ Clone o repositório no seu ambiente de trabalho  
2️⃣ Abra o notebook no **Google Colab** ou **Jupyter Notebook**  
3️⃣ Execute cada célula do código seguindo as etapas descritas  
4️⃣ Analise os gráficos e as métricas geradas  

---

Esse README proporciona **clareza e organização**, facilitando a compreensão do projeto por recrutadores ou colaboradores que desejam visualizar seu trabalho. 🚀💡
