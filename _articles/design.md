---
order: 2
title: Design de Neurônios
subtitle:  
previous_page: intro
next_page: digitais
---
A transmissão de sinais biológicos no cérebro através de sinapses é um processo químico complexo, em que diversas substâncias específicas são utilizadas. Essas substâncias têm o efeito de mudar o potencial elétrico na célula receptora e, quando esse potencial atinge um certo limite, o neuronio dispara.

O Neuronio Artificial procura imitar esse processo. Os inputs e pesos são modelados como valores reais, que estimulam ou inibem o disparo baseado nos valores inseridos. O output neuronal é sua Função de Ativação, análoga a sequência de disparo do neurônio biológico, que pode ser de Limite, linear, exponencial ou sigmoidal.

Aqui, comparamos dois métodos de se implementar um neuronio artificial, a Digital e a Analógica. A Analógica é muito eficiente em termos de espaço físico e velocidade de processamento, entretanto perde acurácia. A digital, por sua vez, ganha precisão ao custo de eficiência.

## Neuronios Digitais

A implementação digital [39] de um unico neuronio é relativamente simples, já que todas operações necessárias para implementa-lo podem ser feitas de forma direta. No neuronio digital, pesos sinápticos são guardados em registradores ou memórias, cujas alternativas incluem um a tres RAMs de transistores dinâmicos, ou quatro ou seis RAMs de transistores estáticos. Somadores, subtratores e multiplicadores são disponíveis como circuitos padrões [119], e Funções de Ativação não lineares como hardware especializado.

### Vantagens

* Simplicidade

* Alta taxa Sinal-para-Ruído

* Flexibilidade facilmente alcançável

* Fabricação barata

### Desvantagens

* Operações mais devagares, especialmente na operação de multiplicação entre peso e input

* Conversão das representações digitais de e para sinal analógico pode ser necessária

### Exemplos

[120], [121], [95]

## Neuronios Analógicos

Em neurônios analógicos pesos são geralmente guardados usando um dos seguintes: resistores[126], capacitores [128, 129] e floating-gate EEPROMs[130]. Com eles, a funcionalidade não-linear da Função de Ativação pode, às vezes, ser capturada diretamente, porém um conjunto coerente de todos os elementos básicos é difícil de ser alcançada.

Como as Funções de Ativação utilizadas em redes neurais em software não podem ser facilmente implementadas em Integrações em Larga Escala, algumas funções aproximadas, ou lookup tables, são utilizadas como FAs no lugar. A implementação analógica se beneficia de explorar efeitos físicos simples para executar algumas das funções de rede [4].

### Vantagens

* Menores

* Processamento mais rápido

* Função de Ativação mais rápida

## Desvantagens

* Menor precisão

* Maior aquecimento

* Dificil de projetar

## Exemplos

[22], [78], [135]