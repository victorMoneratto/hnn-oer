---
order: 4
title: Chips Analógicos
subtitle: Aproveitando de fenômenos físicos para melhorar os resultados.
previous_page: digitais
next_page: hibridos
---
Chips Analógicos são mais rápidos que sua contraparte digital, porém apresentam desafios no armazenamento de pesos das sinapses, além um alto custo energético.

# Motivação
Para melhorar a precisão e a velocidade dos chips digitais, foram projetados chips analógicos, explorando fenômenos físicos, o problema de multiplicação de sinapses foi praticamente sanado, e o das funções de ativação, significantemente reduzido.

Porém, novos problemas surgiram: Os chips analógicos são consideravelmente mais dificeis de projetar, e apresentam um aquecimento muito superior, há também o problema de gerenciamento de pesos, que embora minimizado usando "floating gates", ainda é um gargalo para a arquitetura.

# Vantagens
* Maior velocidade de processamento
* Maior precisão
* Maior robustez
* Melhor implementação de Funções de Ativação

# Desvantagens
* Dificuldade no armazenamento de pesos
* Potência elevada e superaquecimento
* Dificuldade de se projetar
* Menor paralelismo e escalabilidade

# Exemplos
* Intel’s Electrically Trainable Analog Neural Network (ETANN) 80170NX
* Synaptic’s Silicon Retina
* B. Brown, X. Yu, S. Garverick, Mixed-mode analog vlsi continuous-time recurrent neural network, in: Proceedings of International Conference on Circuits, Signals and Systems, 2004.

{% include default-references.md %}

1. [M. Forssell, Hardware Implementation of Artificial Neural Networks](https://users.ece.cmu.edu/~pgrover/teaching/files/NeuromorphicComputing.pdf)