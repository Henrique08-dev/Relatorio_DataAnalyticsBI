# 📊 Relatório de Vendas - Análise Financeira com Power BI

Este repositório apresenta um **relatório de vendas interativo** desenvolvido com Power BI, utilizando a sample financials para demonstrar técnicas avançadas de análise de dados, medidas DAX personalizadas e princípios de UX design.

## 🎯 Objetivo do Projeto

Criar um dashboard financeiro completo que permita explorar dados de vendas através de análises temporais, segmentações avançadas e visualizações interativas, com foco na experiência do usuário e insights acionáveis.

## ✨ Funcionalidades Principais

### 📈 **Análise de Dados Avançada**
- **Medidas TOP N com DAX**: Identificação dos produtos e segmentos mais relevantes
- **Clusterização Automática**: Agrupamento inteligente de dados por performance
- **Análise Temporal Dinâmica**: Variação de vendas ao longo do tempo com interação play

### 🎨 **Experiência do Usuário (UX)**
- **Design Intuitivo**: Navegação fluida entre diferentes perspectivas de análise
- **Visualizações Interativas**: Gráficos que respondem a filtros e seleções
- **Hierarquia de Informações**: Dos KPIs gerais aos detalhes específicos

### ⏱️ **Análise Temporal Interativa**
- **Timeline com Play**: Reprodução automática da evolução mensal das vendas
- **Comparativo Anual**: Análise side-by-side entre 2013 e 2014
- **Variação Percentual**: Identificação de tendências e sazonalidades

## 🏗️ Estrutura do Relatório

### **Página 1: Visão Executiva**
- **KPIs Principais**: 
  - Total de Vendas: 118,73 Mi
  - Unidades Vendidas: 1,13 Mi
  - Descontos Aplicados: 9,21 Mi
  - Custo de Mercadorias: 101,83 Mi
- Filtros temporais interativos

### **Página 2: Dashboard de Vendas**
- **Análise por Período**: Evolução mensal das vendas
- **Segmentação por Categoria**:
  - Por Segmento (Government, Small Business, Enterprise, etc.)
  - Por Produto (Paseo, VTT, Velo, etc.)
  - Por Localização Geográfica (Mapa interativo)
- **Distribuição Percentual**: Gráficos de pizza e treemap

### **Página 3: Detalhamento e Métricas**
- **Análise Semestral/Trimestral**: Comparativo entre períodos
- **Histograma de Unidades Vendidas**: Distribuição de volume
- **Performance por Produto**: Ranking e volumes específicos

### **Página 4: Análise Avançada** ⭐
- **Variação Temporal com Play**: Animação da evolução mensal/anual
- **Clusterização de Produtos**: Agrupamento por performance
- **Medidas TOP N**: 
  - TOP N Máx Vendido: 4,49 Mil
  - Média de Vendas: 169,61 Mil
- **Análise Multidimensional**: Vendas × Unidades × Lucro por Produto
- **TOP 3 Produtos por País**: Análise geográfica segmentada

## 🛠️ Técnicas Implementadas

### **DAX Avançado**
```DAX
-- Medidas TOP N
TOP N Products = 
CALCULATE(
    [Total Sales],
    TOPN(
        3,
        VALUES(Products[Product Name]),
        [Total Sales]
    )
)

-- Clusterização por Performance
Sales Cluster = 
SWITCH(
    TRUE(),
    [Sales Amount] > 1000000, "High Performer",
    [Sales Amount] > 500000, "Medium Performer",
    "Low Performer"
)
```

### **Análise Temporal**
- **Funções de Intelligence Temporal**: SAMEPERIODLASTYEAR, DATESYTD
- **Variação Percentual**: Cálculos de crescimento mês a mês
- **Análise de Sazonalidade**: Padrões recorrentes identificados

### **Visualizações Interativas**
- **Gráfico de Dispersão**: Vendas vs Unidades vs Lucro
- **Mapas Geográficos**: Performance por país/região
- **Gráficos de Área Temporal**: Evolução com play automático

## 📊 Insights Principais Descobertos

### **Performance por Segmento**
- **Channel Partners**: 16,52% do total de vendas
- **Enterprise**: 14,22% com crescimento consistente
- **Government**: Segmento com maior ticket médio

### **Análise Geográfica**
- **Estados Unidos**: 35,74% das vendas totais
- **França e Alemanha**: Mercados em crescimento acelerado
- **Canadá e México**: Potencial de expansão identificado

### **Performance de Produtos**
- **Paseo e VTT**: Líderes em volume de vendas
- **Carretera**: Maior margem de lucro
- **Velo**: Crescimento mais acelerado no período

## 🚀 Como Utilizar

1. **Navegação Básica**: Use os filtros de data para ajustar o período
2. **Análise Temporal**: Na página 4, clique no botão "Play" para ver a evolução
3. **Drill-down**: Clique em qualquer gráfico para detalhamento
4. **Comparativos**: Use as segmentações para análise por categoria
5. **Exportação**: Exporte insights específicos para relatórios

## 📋 Requisitos Técnicos

- **Power BI Desktop** (versão mais recente)
- **Sample Financials** (dataset incluso)
- **Conhecimento Avançado em DAX** (para customizações)

## 🎓 Contexto Educacional

**Desenvolvido como parte da Formação Suzano - Análise de Dados com Power BI - Digital Innovation One**

Este projeto demonstra na prática:
- Análise exploratória de dados
- Medidas avançadas com DAX
- Princípios de UX em BI
- Storytelling com dados
- Clusterização e segmentação

---

**⭐ Destaque**: A última página do relatório oferece uma experiência única de análise temporal com função play, permitindo acompanhar a evolução das vendas mês a mês durante todo o período analisado, revelando padrões e tendências que análises estáticas não capturam.
