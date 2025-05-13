
![logo](../ppgc_logo.png)

---

Modelos Generativos Profundos – 2025.1

**Prof. Dr. Saulo Oliveira**

Data de Entrega: Uma semana após a definição.

Meio de Entrega: ```Relatório | Colab```.


---

**Parte A. Gerando Amostras**

1. Baixe a versão do conjunto de dados [Coluna Vertebral](https://archive.ics.uci.edu/ml/datasets/vertebral+column).
2. Treine um classificador Naïve Bayes, com apenas 50% das amostras disponíveis. Em seguida, aumente o conjunto de dados de modo que cada classe passe a ter 300 amostras. Avalie a distribuição dos dados gerados
Plote os dados em 2D (com PCA ou seleção de atributos) e compare com os dados reais.
3. Agore treine uma Regressão logística com toda a base original. Repita o processo de gerar 300 amostras por classe usando o método da rejeição. 
Amostre de uma distribuição de proposta — pode ser uma normal multivariada centrada na média dos dados originais. Aceite a amostra com probabilidade proporcional a essa densidade — ou seja, aceite se
$u < \sigma(\mathbf{x}^\intercal \mathbf{w}), u \sim \mathcal(U)(0, 1)$. Plote os dados sintéticos em 2D (com PCA ou seleção de atributos) e compare-os com os dados reais.

**PARTE B. Preenchendo Lacunas**
 1. Em posse do conjunto de dados da Íris, apague 10% dos atributos, isto é, em uma matriz de $150 \times 4$, apague 180 valores.
 2. Complete esses atributos com base no Valor Esperado, K-NN e por Regressão linear simples. Avalie e comente os resultados com base no RMSE entre o conjunto original e o imputado.




