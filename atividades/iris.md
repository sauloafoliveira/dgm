

![logo](../ppgc_logo.png)

---

Modelos Generativos Profundos – 2025.1

**Prof. Dr. Saulo Oliveira**

Data de Entrega: Uma semana após a definição.

Meio de Entrega: ```Relatório```.

---

O *dataset da íris* contém informações sobre 150 flores, divididas em 3 espécies: *Iris setosa*, *Iris versicolor* e *Iris virginica*. Cada flor tem 4 atributos numéricos:

- Comprimento da sépala (*sepal length*)
- Largura da sépala (*sepal width*)
- Comprimento da pétala (*petal length*)
- Largura da pétala (*petal width*)

Vamos considerar apenas **duas classes** (*Setosa* e *Versicolor*) e **um atributo contínuo discretizado**: o **comprimento da pétala**.

Suponha que os dados abaixo foram extraídos e discretizados da seguinte forma:

| Comprimento da pétala (discretizado) | Classe     | Contagem |
| ------------------------------------ | ---------- | -------- |
| Curta (≤2.5 cm)                      | Setosa     | 40       |
| Curta (≤2.5 cm)                      | Versicolor | 5        |
| Média (2.5–5.0 cm)                   | Setosa     | 5        |
| Média (2.5–5.0 cm)                   | Versicolor | 40       |
| Longa (>5.0 cm)                      | Setosa     | 0        |
| Longa (>5.0 cm)                      | Versicolor | 10       |

## 1. Sobre as probabilidades, marginais, conjuntas e condicionais, calcule:

- A **probabilidade marginal** de que uma flor seja da classe *Setosa*.
- A **probabilidade conjunta** de que uma flor tenha pétalas curtas e seja da classe *Setosa*.
- A **probabilidade condicional** de que uma flor seja da classe *Setosa*, dado que ela tem pétalas curtas.


## 2. Utilize os dados acima para classificar uma nova flor com **comprimento de pétala "Curta"**, usando o **classificador Naïve Bayes**.
Assuma que:
- P(Classe) é estimado a partir dos dados (frequência relativa),
- P(Comprimento da pétala ∣ Classe) também é estimado a partir das frequências observadas,
- O objetivo é determinar a classe mais provável (MAP).
> Dica: utilize a regra de Bayes sem a evidência - não normalizada.



## 3. Considere agora um modelo de regressão logística binária onde o atributo de entrada é o **comprimento da pétala** (sem discretizar). O modelo é dado por:

$$P(y=1 \mid x) = \dfrac{1}{1+\exp(-(\alpha x + \beta ))}$$

   em que:

   - $y=1$ representa a classe Versicolor;
   - $y=0$ representa as Setosas; e
   - $x$ é o comprimento da pétala.

Suponha também que após o treinamento, obteve-se: $\alpha=2$ e $\beta=-7$.
- Calcule a probabilidade de que uma flor com comprimento da pétala $x=3.5$ cm seja *Versicolor*.
- Encontre o ponto de decisão (valor de $x$) onde a probabilidade de ambas as classes é igual.

## 4. Considerando novamente o modelo de regressão logística, adote $\alpha=2.5$ e $\beta=-9$. Responda:

- Qual é a probabilidade de uma flor com **comprimento da pétala igual a 4 cm** ser da classe *Versicolor*?
- Para qual comprimento de pétala a flor tem **80% de chance de ser da classe Versicolor**?

## 5. Você está utilizando **Naïve Bayes como estimador de densidade** para detectar flores com características raras (anômalas).

   O modelo é treinado usando apenas flores da espécie **Setosa**, com os seguintes atributos discretizados:

| Comprimento da pétala | Largura da pétala | Frequência |
| --------------------- | ----------------- | ---------- |
| Curta                 | Estreita          | 35         |
| Curta                 | Larga             | 10         |

- Suponha que uma flor tenha comprimento **curto** e largura **estreita**. Estime a **probabilidade conjunta** dessa amostra.
- Suponha agora que a flor tem comprimento **médio** e largura **larga**. Essa combinação não apareceu no treinamento. O que o modelo Naïve Bayes indicaria? Como você interpretaria isso na perspectiva de **anomaly detection**?
- Proponha um limiar para classificar uma flor como anômala baseado na **probabilidade conjunta mínima** observada no conjunto de treino, isto é, 
