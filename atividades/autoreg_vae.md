
![logo](../ppgc_logo.png)

---

Modelos Generativos Profundos – 2025.1

**Prof. Dr. Saulo Oliveira**

Data de Entrega: Uma semana após a definição.

Meio de Entrega: ```Relatório | Colab```.


---

# Parte A. Crédito alemão

1. Baixe a versão do conjunto de dados [German Credit (Statlog)](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data).
2. Implemente um modelo auto-regressivo simples, onde a predição de cada feature depende das anteriores. Para simplificação, use camadas nn.Linear de PyTorch, modelando cada $p(x_i | x_{<i})$ como uma regressão ou classificação. Modele as variáveis categóricas com softmax e as contínuas com distribuição normal.
3. Treine o modelo com a máxima verossimilhança de modo que:
   a. Para variáveis contínuas, minimize o MSE ou maximize a log-verossimilhança gaussiana;
   b. Para variáveis categóricas, use ```nn.CrossEntropyLoss```.
4. Calcule a probabilidade total p(x) para cada amostra de teste. Considere como outliers as amostras com menor verossimilhança. Mostre em um gráfico com PCA quais amostras são marcadas como outiliers. Além disso, indique, como em um trabalho de Ciência de dados, quais valores de atributos são os mais outliers.


# Parte B. Roupinhas 

1. Carregue o Fashion MNIST com ```torchvision.datasets``` e treine um VAE.
2. Com o VAE treinado, classifique como outliers as imagens com maior erro de reconstrução ou baixa evidência.
3. Use o espaço latente como entrada para um classificador linear peba para prever a categoria da roupa. Compare o desempenho com CNNs – criadas por você também – treinados diretamente na imagem original.
4. Gere novas imagens sintéticas com o decoder.
