

[![logo](ppgc_logo.png)](https://ppgcc.ifce.edu.br/)

---

# DGM - Modelos Generativos Profundos (2025)

Conhecer os conceitos fundamentais de aprendizado profundo e os fundamentos
probabilísticos e algoritmos de aprendizagem para modelos generativos profundos, incluindo
autocodificadores variacionais, redes adversariais generativas, modelos autorregressivos,
modelos de difusão.

[Clique aqui e baixe o Programa de Unidade Didática da disciplina.](pud.md)

## Professores
Prof. Dr. Saulo Oliveira [Lattes](http://lattes.cnpq.br/9883694006602467) | [Google Scholar](https://scholar.google.com.br/citations?user=rRTkRcAAAAAJ) | [ORCID](http://orcid.org/0000-0001-6362-6113)

e-mail: saulo.oliveira@ifce.edu.br

## Informações
**Horário**: Às segundas e terças, das 07:30 às 09:30.

**Local**: Sala 204, Bloco de Pós-graduação. Instituto Federal de Educação, Ciência e Tecnologia do Ceará | *campus* Fortaleza.

**Endereço**: Avenida Treze de Maio, nº 2081 - Benfica - CEP: 60040-215 - Fortaleza/CE.

## Pré-requisitos
Apesar das disciplinas do PPGCC não exigirem ```pré-requisitos```, o conhecimento das seguintes ferramentas será de grande valia para acelarar a curva de aprendizado durante a disciplina.

| 🐍  Python (Numpy & PyTorch)                                  | 🔢  Álgebra Linear                                            | 🧮 Cálculo e Probabilidade (Derivadas)                                        |
| :----------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Todas as atividades serão em Python e usaremos o formato de Notebooks do Jupyter para entrega. | Usaremos transposição de matriz, inversa e operações algébricas com expressões de matrizes. | Você precisará obter uma derivada e maximizar uma função descobrindo onde a derivada = 0, bem como conhecimento de propriedades de PDFs.|

## Como vai ser a nota?
A avaliação da disciplina é qualitativa e visa o caminho da aprendizagem. Assim, ao invés de um valor número na escala 0-10, uma letra é atribuída. Esta letra indica um conjunto de fatores que são observados ao se realiazar as atividades avaialiativas durante a disciplina. A seguir, nos cards abaixo, são listados os fatores observados e a letra associada a cada um deles.

| A                                                            | B                                                            | C                                                            | D                                                            |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| $\bullet$ Compreendeu por completo a proposta da atividade;<br/>$\bullet$ O trabalho está ótimo e completo;<br/>$\bullet$ O discente está pronto para o próximo assunto. | $\bullet$ Compreendeu a maior parte da proposta da atividade;<br/>$\bullet$ O trabalho está bom e completo;<br/>$\bullet$ O discente tem condições de progredir. | $\bullet$ Compreendeu parte da proposta da atividade;<br/>$\bullet$ O trabalho está incompleto;<br/>$\bullet$ O discente precisa de auxílio para compreender o assunto. | $\bullet$ Não compreendeu por completo a proposta da atividade;<br/>$\bullet$ O trabalho precisa ser refeito;<br/>$\bullet$ O discente não tem condições objetivas de progredir. |

Além do resultado da avaliação qualitativa, cada atividade avaliativa possui um peso associado. Em posse de cada avaliação e seu respectivo peso, a nota final que é a que vai para o histórico é calculada conforme a seguinte fórmula:

$$\text{Nota final} = \dfrac{\sum\limits^N_{i} a_i * w_i }{\sum\limits^N_{i} a_i} \text{ em que } a_i=\begin{cases}
    4, & \text{se } a_i = A;\\
    3, & \text{se } a_i = B;\\
    2, & \text{se } a_i = C;\\
    1, & \text{se } a_i = D;\\
    0, & \text{se não entregue.}
\end{cases},$$

em que $N$ representa o número de atividades na disciplina. 

Observe um caso ilustrativo -- o número entre parênteses representa o peso da atividade:

|          | Prova (2) | Simulação (1) | Relatório (1) | Seminário (1) | Nota final |
| -------- | :-------: | :-----------: | :-----------: | :-----------: | :--------: |
| Huguinho |     A     |       A       |       B       |       A       |    9,5     |
| Zezinho  |     B     |       B       |       B       |       C       |    7,0     |
| Luizinho |     C     |       A       |       B       |       B       |    8,0     |
| Donald   |     B     |       D       |       C       |       C       |    4,5     |

## Cronograma e Conteúdo Programático

> Este é o plano de estudos da turma de 2025 do curso (em construção).


| **TIPO**  | **Data** | **Descrição**                                           | **Material** |
| --------- | -------- | ------------------------------------------------------- | ------------ |
| Aula      | 15/4     | Introdução à Aprendizagem profunda                        |  [Slides](https://docs.google.com/presentation/d/1zTfnrLA7xyylOnYB28RNAldQZWhyprYIGcfai4q4OB8/edit?usp=sharing) • [Atividade](atividades/resumo.md) • [Artigo do Pedro Domingos](https://dl.acm.org/doi/pdf/10.1145/2347736.2347755)            |
| Aula      | 22/4     |    Revisão apressada de Probabilidade                    | [Slides](https://docs.google.com/presentation/d/1d0anEQEiUGor9KmMmyMf2YuNwWs1U-xlgg-7Byovmmc/edit?usp=sharing) • [Atividade](atividades/iris.md)              |
| Aula      | 5/5      | GMM                                                     |              |
| Aula      | 12/5     | PyTorch/Otimizadores                                    |              |
| Aula      | 19/5     | Seleção de Modelos e Projeto de Experimentos            |              |
| Avaliação | 26/5     | Prova LogReg, NB e Tarefas                              |              |
| Aula      | 2/6      | Redes convolucionais                                    |              |
| Aula      | 9/6      | Redes convolucionais famosinhas                         |              |
| Aula      | 16/6     | Problemas comuns                                        |              |
| Aula      | 23/6     | Modelos autorregressivos                                |              |
| Aula      | 21/7     | Redes autocodificadoras e Redes adversárias generativas |              |
| Aula      | 28/7     | Modelos de Difusão                                      |              |
| Aula      | 4/8      | Avaliação de modelos generativos                        |              |
| Avaliação | 11/8     | Trabalho final                                          |              |
|           | 12/8     | Repasso                                                 |              |


<small>Cronograma básico. Ele pode ser alterado a qualquer momento por eventos diversos.</small>

## Diretrizes da Sessão de Pôsteres

O objetivo de um pôster é dar ao espectador um resumo rápido do trabalho, que não apenas atrai seu interesse, mas também o motiva a aprender mais sobre o projeto. Para uma introdução à criação de pôsteres acadêmicos, consulte [Guia de postêres](https://guides.nyu.edu/posters) da Universidade de Nova Iorque. Aqui está um exemplo de estrutura que pode ser útil:

| Problema                                                     | Antecedentes                                                 | Métodos                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| O que você está tentando resolver? Consulte os desafios atuais e por que seu trabalho é significativo. | Configuração do problema + notação; talvez trabalhos anteriores. | Explique suas contribuições técnicas; números podem realmente ajudar a entender especialmente para um modelo neural! |

| Experimentos                                                 | Análise                                                      | Conclusão e referências                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Qual é a tarefa? Quais são as entradas e saídas do modelo? O que são as resultados? Compare com as linhas de base; para resultados, um gráfico pode dizer muito mais do que uma tabela do mesmo tamanho! | Forneça uma análise aprofundada de certos casos de interesse ou contextualize seus resultados na literatura existente! Adicione alguns gráficos/exemplos/visualizações. | Tire brevemente algumas conclusões do trabalho.<br/>Se o espaço permitir, considere adicionar 1-3 referências muito importantes (não faça mais do que isso!) |

