# Redes Neurais Artificiais

”Redes neurais artificiais são modelos computacionais inspirados pelo sistema nervoso de seres vivos. Elas possuem a habilidade de adquirir e manter conhecimento (baseadas em informação) e podem ser definidas como um conjunto de unidades processadoras,representadas por neurônios artificiais, interligadas por muitas interconexões.” {cite}`ivannunes2017ann`

```{figure} ../_static/img/monografia/fundamentos/Neurônio.png
---
name: neuron
---
Implementação do modelo de neurônio proposto por McCulloch e Pitts {cite}`mcculloch1943logical`.
```

Neste modelo, destaca-se os seguintes elementos:

* Sinal de entrada do neurônio, representado pelo vetor ${x_1,x_2,...,x_n}$.
* Pesos associados a cada entrada, representados pelo vetor ${w_1,w_2,...,w_n}$.
* Agregador linear, representado pelo símbolo do somatório $\sum$.
* Bias, representado pelo símbolo $\theta$.
* Potencial de ativação, representado por $u$.
* Função de ativação, representado por $g(·)$.
* Sinal de saída, representado por $y$.
  

E é regido pelas equações {eq}`neuron1` e {eq}`neuron2`

$$
    u = \sum_1^n w_ix_i - \theta
$$ (neuron1)

$$
    y = g(u)
$$ (neuron2)

## Redes multiple-layer feedforward

Um modelo neuronal moderno, derivado do trabalho de McCulloch e Pitts {cite}`mcculloch1943logical` é o multiple-layer feedforward. Ele possui uma ou mais camadas intermediárias (além das camadas de entrada e saída), e o fluxo da informação sempre segue uma mesma direção, da entrada até a saída {cite}`ivannunes2017ann`. Isto significa que as saídas dos neurônios de uma camada conectam-se apenas com os neurônios de camadas posteriores, mais próximas à camadade saída, nunca com a própria camada ou com camadas anteriores.

```{figure} ../_static/img/monografia/fundamentos/multi-layer_feedforward.png
---
name: multilayer_feedforward
---
Representação de uma rede multiple-layer feedforward.
```

## Redes recorrentes

Redes recorrentes são caracterizadas pelo fato de que a saída de um ou mais neurônios serve de retroalimentação para outros neurônios {cite}`ivannunes2017ann`, servindo de entrada de neurônios na mesma camada ou em camadas anteriores, fazendo com que o fluxo de informação não seja unidirecional.

```{figure} ../_static/img/monografia/fundamentos/recorrente.png
---
name: recorrente
---
Representação de uma rede recorrente.
```

## Redes de Elman

Proposta por Elman em 1990 {cite}`elman1990finding`, a rede que leva seu nome é um tipo específico de rede recorrente. Ela é composta pela camada de entrada, uma camada intermediária e a camada de saída. Cada neurônio da camada intermediária é retroalimentada a todos os outros neurônios da mesmacamada com uma unidade de atraso (representado pelas unidades $z^{−1}$), permitindo que a rede reconheça padrões temporais


```{figure} ../_static/img/monografia/fundamentos/elman2.png
---
name: elman
---
Representação de uma rede de Elman, adaptada de {cite}`ElmanFig`.
```

## Long Short-Term Memory (LSTM)




```{figure} ../_static/img/monografia/fundamentos/LSTM.png
---
name: lstm
---
Representação de uma célula de memória utilizada na arquitetura LSTM. Adaptada de {cite}`depEEGlstm`
```