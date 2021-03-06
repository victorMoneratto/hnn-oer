---
order: 4
title: Chips Analógicos
subtitle: Aproveitando de fenômenos físicos para melhorar os resultados.
previous_page: digitais
next_page: hibridos
---
Mais rápidos que sua contraparte digital, tem dificuldades com o armazenamento de pesos, e alto custo energético, necessitando um melhor resfriamento.

## Motivação
Para melhorar a velocidade dos chips digitais, foram projetados chips analógicos.
Explorando fenômenos físicos, o problema de multiplicação de sinapses foi praticamente sanado, e o das funções de ativação, significantemente reduzido.
Porém, novos problemas surgiram: Os chips analógicos são consideravelmente mais dificeis de projetar, e apresentam um aquecimento muito superior.
Há também o problema de gerenciamento de pesos, que embora minimizado usando [floating gates](https://en.wikipedia.org/wiki/Floating-gate_MOSFET), ainda é um gargalo para a arquitetura.

## Vantagens
* Maior velocidade de processamento
* Maior robustez
* Melhor implementação de Funções de Ativação

## Desvantagens
* Dificuldade no armazenamento de pesos
* Potência elevada e superaquecimento
* Dificuldade de se projetar
* Menor paralelismo e escalabilidade
* Precisão deteriorada

## Exemplos
* Intel’s Electrically Trainable Analog Neural Network (ETANN) 80170NX
* Synaptic’s Silicon Retina
* B. Brown, X. Yu, S. Garverick, Mixed-mode analog vlsi continuous-time recurrent neural network, in: Proceedings of International Conference on Circuits, Signals and Systems, 2004.

{% include default-references.md %}

* [M. Forssell, Hardware Implementation of Artificial Neural Networks](https://users.ece.cmu.edu/~pgrover/teaching/files/NeuromorphicComputing.pdf)