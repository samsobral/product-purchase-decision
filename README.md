#Business_Driven


Empresas que compram lotes para revenda enfrentam dois riscos:

Comprar itens defeituosos (prejuízo direto);

Rejeitar itens bons (perda de receita).
Objetivo: Maximizar o lucro esperado por item, decidindo comprar ou não comprar com base no risco (probabilidade de defeito) e no trade-off preço de compra × preço de revenda.

🧩 Abordagem

Modelos de classificação estimam a probabilidade de defeito por item (features x1…x20).

Regra de decisão econômica: compra apenas quando o lucro esperado é positivo:

Lucro Esperado
=
(
1
−
𝑝
^
(
defeito
)
)
×
Pre
c
¸
o de Revenda
−
Custo de Compra
Lucro Esperado=(1−
p
^
	​

(defeito))×Pre
c
¸
	​

o de Revenda−Custo de Compra

Governança de risco: o limiar pode ser calibrado para metas (ex.: reduzir taxa de defeituosos < X%).


## ✅ Resultados Principais
- **Melhor Modelo:** SVM (AUC = 0.989, Acurácia = 95,5%)  
- **Validação:** AUC = 0.857 no conjunto de validação  
- **Decisão de Compra:** 96,9% de acerto nas compras, com lucro observado de R$ 5.539,68  


💼 O que o negócio ganha

Mais lucro por lote (seleção economicamente ótima, não só “acurácia”).

Menos devoluções e custos de “retrabalho”.

Processo escalável e auditável para times de compras.

Alavancas claras: preço de revenda, limiar de risco e orçamento.

🔑 KPIs de Gestão

Lucro total e por item comprado

Taxa de acerto das compras (itens bons comprados / itens comprados)

% de defeituosos evitados

Receita perdida estimada (bons não comprados)

ROI do modelo (ganho incremental vs. política anterior)

🛠️ Implementação (visão prática)

Modelagem: testamos múltiplos algoritmos (ex.: SVM, árvore, etc.) e escolhemos o que maximiza resultado econômico no conjunto de validação.

Decisão: cada item recebe “Comprar / Não comprar” com base no lucro esperado.

Calibração: o limiar pode ser movido conforme objetivos (ex.: “ser conservador em épocas de caixa curto”).
