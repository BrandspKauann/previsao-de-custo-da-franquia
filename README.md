# 📈 Previsão de Custos de Implementação de Franquias (Machine Learning)

## 💡 Visão Geral do Projeto

Este projeto implementa um modelo de **Regressão Linear** para criar um sistema de estimativa de custos altamente preciso e transparente para novas unidades franqueadas.

O principal objetivo é fornecer à franqueadora e aos investidores uma ferramenta para prever o **Custo Total de Implementação** e desmembrar esse valor, justificando o orçamento com base em fatores objetivos.

---
### ⚙️ Metodologia e Modelagem

Utilizamos o **Regressão Linear** por sua **interpretabilidade inerente**, o que é crucial em decisões de investimento e orçamento.

| Variável de Entrada (Feature) | Descrição |
| :--- | :--- |
| **`Area_m2`** | Tamanho físico da unidade. |
| **`Taxa_Franquia_Base`** | Custo inicial fixo da franqueadora. |
| **`Nivel_Risco_Cid`** | Fator de custo local (aluguel, mão de obra). |
| **`Populacao_Local`** | População da área de abrangência. |

---
### ✅ Resultados e Performance

O modelo foi avaliado usando métricas de regressão, demonstrando uma capacidade de ajuste e precisão excepcionais:

| Métrica | Resultado | Significado |
| :--- | :--- | :--- |
| **R-Quadrado ($\mathbf{R}^2$)** | **0.9935** | O modelo explica **99.35%** da variação nos custos de implementação. |
| **RMSE (Erro Médio)** | **R\$ 5.244,10** | O erro médio de previsão do custo total (que varia entre R\$ 110k e R\$ 320k) é marginal. |

---
### 🔎 Explicabilidade e Análise de Sensibilidade

A análise dos Coeficientes (pesos) do modelo revela a contribuição direta de cada fator para o custo final, provendo a base para a justificativa orçamentária:

| Fator | Coeficiente (Peso) | Impacto no Custo |
| :--- | :--- | :--- |
| **Taxa\_Franquia\_Base** | **+2.65** | **Principal Fator:** Cada R\$ 1,000 extra na taxa base aumenta o custo total em R\$ 2.650. |
| **Nivel\_Risco\_Cid** | +0.68 | O aumento de 1 ponto no Nível de Risco da Cidade adiciona R\$ 681,36 ao custo. |
| **Area\_m2** | +0.55 | Cada $\text{m}^2$ adicional aumenta o custo em R\$ 550,24. |
| **Populacao\_Local** | +0.07 | Fator de impacto marginal no custo total. |

## 🎯 Conclusão

O projeto entrega um sistema de previsão de custos de **alta precisão e transparência total**. O modelo pode ser diretamente implementado para:

1.  **Orçamento Preciso:** Gerar estimativas de custo com uma margem de erro inferior a $\text{1\%}$.
2.  **Justificativa de Custos:** Dissecando a previsão, o modelo permite à franqueadora justificar a alocação de capital e negociar termos de investimento com base em dados.
