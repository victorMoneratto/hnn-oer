---
order: 7
title: Implementação em FPGA
subtitle:
previous_page: neuromorfico
next_page: ram
---
Devido a sua praticidade, hardwares programáveis são uma opção tentadora ao design de HNNs, e as FPGAs são uma ótima escolha para prototipação e teste.

## Motivação
O custo de se criar um chip era um impecilho para o desenvolvimento de hardwares dedicados. As FPGAs vieram como alternativa lógica, permitindo mudanças rápidas, por um custo baixíssimo.

Porém, a densidade de circuitos de uam FPGA é bem menor que a de um circuito dedicado, o que limita a implementação de redes com grandes quantidades de neurônios.

Há também o problema da multiplicação sináptica, que é relativamente custosa quando implementada em FPGAs, posto que seu custo cresce com o quadrado dos neurônios.

FPGAs também são especialmente eficientes para a implementação de redes neurais baseadas em modelos estocásticos, utilizando look-up tables.

## Vantagens
* Baíxissimo custo.
* Maior tolerância a erros de projeto.
* Maior agilidade nas fases de teste e desenvolvimento.

## Desvantagens
* Menor densidade de circuitos.
* Multiplicação de sinapses volta a se tornar um problema.

## Exemplos
* R. Gadea, J. Cerda, F. Ballester, A. Macholi, Artificial neural network implementation on a single fpga of a pipelined on-line backpropagation, in: Proceedings of the 13th International symposium on system synthesis, 2000, pp. 225–230.
* B. Schrauwen, M. D‘Haene, Compact digital hardware implementations of spiking neural networks, in: J. Van Campenhout (Ed.), Sixth FirW PhD Symposium, 2005,p. on CD.

{% include default-references.md %}