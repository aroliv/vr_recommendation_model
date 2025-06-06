# Estudo de Caso: Sistema de Recomendação de Estabelecimentos - VR Benefícios

## 🧠 Visão Geral

Este repositório contém o código e a apresentação desenvolvidos para o estudo de caso proposto pela área de Recomendação/CRM da VR Benefícios. O objetivo do projeto é construir um sistema de recomendação de estabelecimentos (ECs) que maximize o **lucro da empresa**, calculado como:

**lucro = taxa recolhida do EC × valor da transação**

Somente usuários que aceitaram as flags de recomendação e de termos podem receber recomendações. A solução foi inteiramente desenvolvida em Python, utilizando abordagem baseada em sistemas de recomendação com dados reais de transações e perfis de usuários/estabelecimentos.

---

## 📂 Conteúdo

- **Notebook**: Contém todas as etapas do processo, desde a análise exploratória até a modelagem do sistema de recomendação e a estimativa de ganho financeiro para a empresa.
- **Apresentação (PDF)**: Arquivo com até 4 slides, resumindo o problema, abordagem adotada, resultados obtidos e impacto da solução.

---

## 🗂 Dados Utilizados

Os seguintes arquivos CSV foram utilizados:

- `usuarios.csv`: informações dos usuários, incluindo aceite de recomendação.
- `transacoes.csv`: histórico de transações realizadas entre usuários e estabelecimentos.
- `estabelecimento.csv`: dados dos estabelecimentos, incluindo a taxa que a VR recolhe de cada um.

As informações foram integradas para gerar uma matriz de interação entre usuários e ECs, e enriquecer o modelo com dados financeiros.

---

## 🔧 Bibliotecas Principais

- **Manipulação de dados**: `pandas`, `numpy`
- **Visualização**: `matplotlib`, `seaborn`, `plotly`
- **Modelagem e Recomendação**: `lightfm`, `scipy.sparse`, `sklearn`
- **Avaliação e Estatísticas**: `precision_at_k`, `auc_score`, `mean_squared_error`, `scipy.stats`

---

## 🔍 Etapas do Projeto

1. **Pré-processamento e Filtragem**
   - Remoção de usuários sem aceite nas flags obrigatórias
   - Criação de métricas de lucro por transação

2. **Análise Exploratória**
   - Compreensão do comportamento de uso por tipo de EC
   - Distribuições de lucro por estabelecimento

3. **Criação da Matriz de Interação**
   - Matriz usuário × estabelecimento ponderada por lucro gerado
   - Normalização dos dados com `MinMaxScaler`

4. **Modelagem com LightFM**
   - Uso de algoritmo híbrido (content + collaborative)
   - Avaliação com `precision_at_k` e `auc_score`

5. **Simulação de Recomendação**
   - Simulação de top-N recomendações por usuário
   - Estimativa do ganho financeiro incremental em relação ao cenário atual

6. **Resultados e Justificativas**
   - Demonstração do potencial de aumento de lucro com o modelo
   - Justificativa da escolha do LightFM: boa performance em sistemas com dados esparsos e métricas personalizadas

---

## 💰 Ganhos Esperados para a Empresa

Com base em simulações sobre o conjunto de teste:

- **Aumento estimado no lucro total**: R$ XX.XXX,XX (valores fictícios substituíveis)
- **Melhor aproveitamento de ECs com maior taxa**
- **Maior assertividade na recomendação para usuários com comportamento histórico consistente**

---

## 📎 Apresentação

A apresentação em PDF inclui:

- Descrição do desafio
- Abordagem de modelagem e justificativa
- Métricas de avaliação e comparação com baseline
- Projeção de impacto financeiro para a VR

---

## 🔮 Trabalhos Futuros

- Incorporar perfis demográficos e contextuais nos embeddings do modelo
- Testar abordagens baseadas em deep learning ou modelos seqüenciais
- Avaliar o impacto das recomendações em tempo real com dados transacionais recentes
- Criar um sistema de feedback contínuo para atualização do modelo

---

## 👤 Contribuidora

**Andressa Ribeiro de Oliveira**
