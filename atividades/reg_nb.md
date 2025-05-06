
![logo](../ppgc_logo.png)

---

Modelos Generativos Profundos – 2025.1

**Prof. Dr. Saulo Oliveira**

Data de Entrega: Uma semana após a definição.

Meio de Entrega: ```Relatório```.

---

Com base no código abaixo, responda:

1. O conjunto de dados é desbalanceado (90% não fraudulento). Como isso pode impactar os modelos? Qual modelo parece lidar melhor com o desbalanceamento?
2. Altere o parâmetro ```weights``` para ```[0.5, 0.5]``` e reexecute. O desempenho melhora? O comportamento dos classificadores muda?
3. Compare o número de parâmetros dos dois modelos (use ```.coef_``` e ```.class_prior_```). Qual modelo parece mais "compacto"? O que isso implica em termos de uso prático?
4. Altere algumas amostras em ```X_test``` para valores extremos (ex: ```X_test[0] += 10```). Como cada modelo reage? Qual é mais robusto a outliers?
5. Use os métodos ```predict_proba``` para interpretar a confiança de cada modelo nas predições. As probabilidades geradas parecem calibradas (por exemplo, uma transação com 0.9 de chance de fraude é mesmo fraudulenta)?
6. Pense em um sistema bancário real: qual modelo você escolheria e por quê? Considere tempo de inferência, interpretabilidade e risco de erro.



```python
from sklearn.datasets import make_classification
from sklearn.model_selection import train_test_split
from sklearn.naive_bayes import GaussianNB
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import classification_report
from sklearn.decomposition import PCA

# Gerar dados sintéticos simulando transações financeiras
X, y = make_classification(n_samples=2000, n_features=20, n_informative=10, n_redundant=5,
                           n_clusters_per_class=2, weights=[0.9, 0.1], flip_y=0.01, random_state=42)

# Reduzir dimensão para visualização
X_vis = PCA(n_components=2).fit_transform(X)

# Dividir em treino e teste
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, stratify=y, random_state=42)

# Treinar Naive Bayes
nb = GaussianNB()
nb.fit(X_train, y_train)
y_pred_nb = nb.predict(X_test)
y_proba_nb = nb.predict_proba(X_test)[:, 1]

# Treinar Regressão Logística
lr = LogisticRegression(max_iter=1000)
lr.fit(X_train, y_train)
y_pred_lr = lr.predict(X_test)
y_proba_lr = lr.predict_proba(X_test)[:, 1]

# Métricas e inferência
print("Regressão Logística\n", classification_report(y_test, y_pred_lr))
print("Naive Bayes\n", classification_report(y_test, y_pred_nb))
```
