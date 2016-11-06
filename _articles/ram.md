---
order: 8
title: Implementação em RAM
subtitle:
previous_page: fpga
next_page: optica
---
Podendo ser implementadas em hardwares de uso geral, possuem um treinamento rápido, sendo uma alternativa plausível para algumas aplicações.

## Motivação
Diferenciando-se das implementações em hardware dedicado, foi proposto um modelo baseado em memória RAM, com neurônios binários, sem pesos nas entradas.

As funções neuronais são armazenadas em uma look-up table, e seu treinamento consiste em atualizar o conteudo das tabelas de acordo com as necessidades da aplicação.

Embora não tenha a velocidade de um hardware dedicado, tal abordagem é amplamente adotada em aplicações de reconhecimento de padrões, podendo ser implementada em computadores pessoais e hardwares de uso geral.

## Vantagens
* Tempo de treinamento extremamente reduzido.
* Implementação fácil e acessível.

## Desvantagens
* Capacidade computacional reduzida
* Velocidade muito inferior à um hardware dedicado

## Exemplos
* J. Austin, S. Buckle, J. Kennedy, A. Moulds, R. Pack, A. Turner, The cellular neural network associative processor, c-nnap, IEEE Monograph on Associative Computers.

{% include default-references.md %}