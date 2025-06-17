Markdown

# NCbank Guardian: Análise Preditiva de Churn de Clientes

## 📜 Sumário Executivo

O **NCbank Guardian** é um projeto de Ciência de Dados desenvolvido para enfrentar um dos maiores desafios do setor bancário: a **rotatividade de clientes (churn)**. Este fenômeno não apenas impacta diretamente a receita, mas também eleva os custos de aquisição de novos clientes e pode afetar a reputação do banco.

O objetivo deste projeto vai além da simples medição da taxa de churn. Utilizando técnicas avançadas de Machine Learning, desenvolvemos um modelo preditivo robusto, capaz de prever com alta performance a probabilidade de um cliente abandonar o banco. Mais crucialmente, o modelo identifica os **fatores determinantes** por trás dessa decisão, com destaque para o **comportamento transacional e o nível de engajamento** do cliente.

O resultado final é uma ferramenta estratégica que arma o NCbank com a capacidade de:

1.  Atribuir uma **pontuação de risco de churn** a cada cliente.
2.  Segmentar a base de clientes em diferentes níveis de risco.
3.  Implementar **ações de retenção proativas, personalizadas e eficientes**.

Ao focar os esforços nos clientes de maior valor e risco, o NCbank Guardian visa fortalecer a base de clientes, aumentar a lucratividade e solidificar a posição do banco em um mercado cada vez mais dinâmico e competitivo.

---

## 🎯 O Problema de Negócio

A perda de clientes no setor bancário acarreta consequências significativas:

- **Perda de Receita Recorrente:** Clientes que saem levam consigo o potencial de receita futura (taxas, juros de empréstimos, investimentos).
- **Alto Custo de Aquisição:** Adquirir um novo cliente é consideravelmente mais caro do que reter um existente.
- **Dano à Reputação:** Altas taxas de churn podem sinalizar insatisfação com os serviços, afetando a imagem da marca.

A abordagem tradicional de analisar o churn de forma reativa (após o cliente já ter saído) é ineficaz. A necessidade é de um sistema proativo que identifique os sinais de alerta _antes_ que a decisão de sair seja tomada.

---

## 💡 A Solução Proposta

Para solucionar este desafio, o projeto foi estruturado em um pipeline completo de Ciência de Dados, desde o tratamento dos dados até a disponibilização dos insights em um dashboard interativo.

O coração da solução é um modelo de **Random Forest Tunado**, que demonstrou uma performance excelente para identificar os clientes com maior propensão ao churn.

### Principais Resultados do Modelo

- **Recall (Sensibilidade): 83.0%**
  - _Isto significa que o modelo é capaz de identificar corretamente 83% de todos os clientes que realmente iriam entrar em churn. É uma métrica crucial para garantir que o mínimo de clientes em risco passe despercebido._
- **Precisão (Precision): 86.0%**
  - _Das previsões de churn feitas pelo modelo, 86% estão corretas. Isso garante que os esforços de retenção sejam direcionados a clientes que de fato apresentam um risco real, otimizando recursos._

---

## 🛠️ Tecnologias Utilizadas

Este projeto foi construído utilizando um ecossistema de ferramentas robustas de Python e visualização de dados:

- **Linguagem de Programação:** Python 3.x
- **Bibliotecas de Análise e Manipulação de Dados:**
  - **Pandas:** Para manipulação e análise de dados tabulares.
  - **NumPy:** Para computação numérica e operações com arrays.
- **Bibliotecas de Machine Learning:**
  - **Scikit-learn:** Para criação, treinamento e avaliação de modelos preditivos.
  - **Imbalanced-learn:** Para aplicar técnicas de balanceamento de dados, como o SMOTE.
  - **Feature-engine:** Para engenharia de variáveis de forma otimizada.
- **Bibliotecas de Visualização de Dados:**
  - **Matplotlib** e **Seaborn:** Para a criação de gráficos exploratórios durante a análise.
- **Ambiente de Desenvolvimento:**
  - **Jupyter Notebook:** Para desenvolvimento iterativo e análise exploratória.
- **Ferramenta de Business Intelligence:**
  - **Microsoft Power BI:** Para a criação do dashboard final, permitindo a exploração interativa dos resultados.

---

## ⚙️ Metodologia e Pipeline do Projeto

O projeto seguiu uma metodologia estruturada em 5 etapas principais:

### 1. Coleta e Entendimento dos Dados

A primeira fase focou em compreender o conjunto de dados, a definição de cada variável e a formulação de hipóteses iniciais sobre os possíveis fatores de churn.

### 2. Pré-processamento e Engenharia de Features (`Tratamento_De_Dados.ipynb`)

Esta é uma das etapas mais críticas do projeto, executada no notebook `Tratamento_De_Dados.ipynb`. As principais atividades incluíram:

- **Limpeza de Dados:** Tratamento de valores ausentes e inconsistências.
- **Transformação de Variáveis:** Conversão de variáveis categóricas em numéricas (One-Hot Encoding).
- **Balanceamento de Dados:** Aplicação da técnica SMOTE (Synthetic Minority Over-sampling Technique) para corrigir o desbalanceamento entre as classes de "churn" e "não churn", garantindo que o modelo aprendesse com ambas as classes de forma eficaz.
- **Seleção de Features:** Utilização do modelo Random Forest para identificar as variáveis mais importantes e relevantes para a previsão do churn.

### 3. Modelagem e Treinamento

- **Escolha do Algoritmo:** Optou-se pelo Random Forest devido à sua robustez, alta performance e capacidade de fornecer a importância das features.
- **Treinamento e Validação:** O conjunto de dados foi dividido em treino e teste para garantir que o modelo fosse capaz de generalizar para novos dados.
- **Tuning de Hiperparâmetros:** Foi realizada uma otimização dos parâmetros do modelo para extrair a máxima performance.

### 4. Avaliação do Modelo

A performance do modelo foi avaliada com base nas métricas de Recall e Precisão, que são fundamentais para este problema de negócio, garantindo um equilíbrio entre identificar o máximo de clientes em risco e não desperdiçar recursos.

### 5. Visualização e Entrega (`Apresentacao_Dashboard_NCbank_Guardian.docx`)

Os resultados do modelo (probabilidade de churn para cada cliente) e a importância das features foram exportados para serem consumidos em um dashboard no Power BI. O dashboard **NCbank Guardian** foi projetado para ser uma ferramenta de fácil utilização, permitindo que gestores e analistas:

- Visualizem o risco de churn de toda a base de clientes.
- Filtrem e segmentem clientes por nível de risco (Crítico, Alto, Moderado, Baixo).
- Compreendam quais fatores mais contribuem para o churn de forma geral.

---

## 🚀 Como Utilizar este Repositório

Siga os passos abaixo para replicar o ambiente e executar o projeto.

### 1. Pré-requisitos

- Python 3.8 ou superior
- Git

### 2. Clonar o Repositório

```bash
git clone [https://github.com/leoncio90/CLASSIFICACAO_RISCO_DE_CHURN.git](https://github.com/leoncio90/CLASSIFICACAO_RISCO_DE_CHURN.git)
cd CLASSIFICACAO_RISCO_DE_CHURN
```

### 3. Criar e Ativar um Ambiente Virtual (Recomendado)

```bash
# Para Windows
python -m venv venv
venv\Scripts\activate

# Para macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 4. Instalar as Dependências

Todas as bibliotecas necessárias estão listadas no arquivo `requirements.txt`. Instale-as com um único comando:

```bash
pip install -r requirements.txt
```

### 5. Executar a Análise

O notebook `Tratamento_De_Dados.ipynb` contém todo o código para o pipeline de dados e modelagem. Abra-o utilizando o Jupyter Notebook ou Jupyter Lab:

```bash
jupyter notebook Tratamento_De_Dados.ipynb
```

Execute as células sequencialmente para reproduzir a análise.

### 6. Visualizar o Dashboard

As instruções detalhadas para configurar e utilizar o dashboard no Power BI estão no documento `Apresentacao_Dashboard_NCbank_Guardian.docx`.

---

## 📂 Estrutura do Repositório

```
.
├── Tratamento_De_Dados.ipynb         # Notebook com todo o processo de ETL e modelagem.
├── Infografico.html                  # Infográfico apresentando insights hospedado no Github.
├── README.md                         # Este arquivo.
├── requirements.txt                  # Lista de dependências Python para o projeto.
├── logo.png                          # Logomarca do NCbank.
├── Dados_Tratados/                   # Pasta (gerada pelo notebook) com os dados processados.
│   ├── importancia_features_rf.csv   # Importância das features para o Power BI.
│   └── resultados_RandomForest.csv   # Previsões de churn para cada cliente.
│   └── BankChurners_Tratado.xlsx     # DataFrame Tratado a ser utilizado no Power BI
│   └── modelo_rf_tunado.pkl          # Modelo Random Forest Tunado
├── Dashboard/                        # Pasta com Dashboard gerado no Power BI.
│   ├── Dashboard_Monitoramento_Estratégico_do_Risco_de_Churn.pbix   # Dashboard de monitoramento do risco de Churn.
│   ├── Dashboard_Monitoramento_Estratégico_do_Risco_de_Churn.pdf   # pdf do Dashboard de monitoramento do risco de Churn.
│   └── Tema_NCbank_dashboard.json    # Tema do Dashboard.
└── Datasets/                         # Pasta com arquivo dataframe e metadados.
    ├── BankChurners.csv              # Dataframe sem tratamento.
    └── metadados.xlsx                # metadados sem tratamento.

```

---

## 🔮 Próximos Passos e Melhorias Futuras

Este projeto estabelece uma base sólida, mas pode ser expandido para agregar ainda mais valor:

- **Análise de Sentimento:** Integrar a análise de sentimentos de interações de clientes (e-mails, chats de suporte) como uma feature adicional para capturar a satisfação do cliente em tempo real.
- **Implementação de MLOps (Machine Learning Operations):**
  - **Deployment:** Publicar o modelo em um ambiente de produção para gerar previsões em tempo real ou em lotes.
  - **Monitoramento:** Acompanhar a performance do modelo ao longo do tempo para detectar _drift_ (degradação da performance).
  - **Retreinamento Automático:** Criar um pipeline para retreinar o modelo com novos dados periodicamente, garantindo que ele se mantenha relevante e preciso.

---

## 👨‍💻 Autor

**[Jhonata Leoncio Pereira]**

- **LinkedIn:** [Jhonata Leoncio](https://www.linkedin.com/in/jhonataleoncio/)
