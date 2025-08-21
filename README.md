# Predictive Buying Strategy - Business Driven

Projeto de **Predição e Decisão** aplicado para **otimizar compras de produtos para revenda**.  
O foco é **maximizar lucro esperado**, **reduzir perdas com itens defeituosos** e **padronizar decisões** do time de compras.

---

## 🎯 Problema de Negócio
Empresas que compram lotes para revenda enfrentam dois riscos principais:
1. **Comprar itens defeituosos** → prejuízo direto.  
2. **Rejeitar itens bons** → perda de receita.  

**Objetivo:** Definir uma **estratégia preditiva de compra** que maximize o retorno esperado por produto.

---

## 💰 Lucro Esperado

A decisão de compra é baseada no **lucro esperado**:

$$
\mathbb{E}[\text{Lucro}] \;=\; (1 - \hat p_{\text{defeito}})\cdot P_{\text{revenda}} \;-\; C_{\text{compra}}
$$

**Regra de decisão:**

$$
\text{Comprar se } \mathbb{E}[\text{Lucro}] > 0 
\;\;\Longleftrightarrow\;\;
\hat p_{\text{defeito}} \;<\; 1 - \frac{C_{\text{compra}}}{P_{\text{revenda}}}
$$

**Onde:**
- $\hat p_{\text{defeito}}$ = probabilidade prevista de defeito (modelo preditivo)  
- $P_{\text{revenda}}$ = preço de revenda  
- $C_{\text{compra}}$ = custo de compra  

> 🔒 **Governança de risco:** o limiar pode ser calibrado para metas do negócio (ex.: reduzir taxa de defeituosos < 5%).

---

## ✅ Resultados Principais

- **Melhor modelo:** SVM (AUC = 0.989, Acurácia = 95,5%)  
- **Validação:** AUC = 0.857, Acurácia = 82,8%  
- **Decisão de Compra:**  
  - 96,9% dos produtos comprados estavam realmente bons  
  - Especificidade = 75% (evitou 3 em cada 4 defeituosos)  
- **Lucro:**  
  - Lucro esperado = R$ 4.340,21  
  - Lucro real observado = **R$ 5.539,68**

---

## 📊 Impacto para o Negócio
- **Mais margem**: foco em produtos com maior retorno esperado.  
- **Menos perdas**: queda significativa em compras erradas.  
- **Decisão escalável e auditável**: cada item tem registro de probabilidade, custo e decisão.  
- **Cenários simuláveis**: gestor pode ajustar preço de revenda e política de risco.  

---

## 🗂️ Estrutura do Repositório
