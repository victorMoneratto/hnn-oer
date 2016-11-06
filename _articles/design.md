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

A implementação digital<sup>[1](#1)</sup> de um unico neuronio é relativamente simples, já que todas operações necessárias para implementa-lo podem ser feitas de forma direta. No neuronio digital, pesos sinápticos são guardados em registradores ou memórias, cujas alternativas incluem um a tres RAMs de transistores dinâmicos, ou quatro ou seis RAMs de transistores estáticos. Somadores, subtratores e multiplicadores são disponíveis como circuitos padrões<sup>[2](#2)</sup>, e Funções de Ativação não lineares como hardware especializado.

### Vantagens

* Simplicidade

* Alta taxa Sinal-para-Ruído

* Flexibilidade facilmente alcançável

* Fabricação barata

### Desvantagens

* Operações mais devagares, especialmente na operação de multiplicação entre peso e input

* Conversão das representações digitais de e para sinal analógico pode ser necessária

### Exemplos

* [V. Salapura, M. Gschwind, O. Maischberger, A fast FPGA implementation of a general purpose neuron, in: R. W. Hartenstein, M. Z. Servit (Eds.), FieldProgrammable Logic: Architectures, Synthesis and Applications, Springer-Verlag, Berlin, 1994, pp. 175–182.](https://www.researchgate.net/publication/null?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)

* [A. Muthuramalingam, S. Himavathi, E. Srinivasan, Neural network implementation using fpga: Issues and application, International Journal of Information Technology 4 (2) (2007) 2–12.](https://www.researchgate.net/publication/242600969_Neural_Network_Implementation_Using_FPGA_Issues_and_Application?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)

* [H. Hikawa, A digital hardware pulse-mode neuron with piecewise linear activation function, IEEE Transactions on Neural Networks 14 (5) (2003) 1028– 1037.](https://www.researchgate.net/publication/null?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)

## Neuronios Analógicos

Em neurônios analógicos pesos são geralmente guardados usando um dos seguintes: resistores<sup>[3](#3)</sup>, capacitores <sup>[4](#4), [5](#5)</sup> e floating-gate EEPROMs[130]. Com eles, a funcionalidade não-linear da Função de Ativação pode, às vezes, ser capturada diretamente, porém um conjunto coerente de todos os elementos básicos é difícil de ser alcançada.

Como as Funções de Ativação utilizadas em redes neurais em software não podem ser facilmente implementadas em Integrações em Larga Escala, algumas funções aproximadas, ou lookup tables, são utilizadas como FAs no lugar. A implementação analógica se beneficia de explorar efeitos físicos simples para executar algumas das funções de rede [6](#6).

### Vantagens

* Menores

* Processamento mais rápido

* Função de Ativação mais rápida

## Desvantagens

* Menor precisão

* Maior aquecimento

* Dificil de projetar

## Exemplos

* [A. M. Chiang, et al., A CCD programmable image processor and its neural network applications, IEEE Journal of SolidState Circuits 26 (1991) 1894–1901.](https://www.researchgate.net/publication/null?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
* [M. Verleysen, L. luc Voz, J. Madrenas, An analog processor architecture for a neural network classifier, IEEE Micro 14 (1994) 16–28.78](https://www.researchgate.net/publication/null?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
* [A. P. Almeida, J. E. Franca, Digitally programmable analog building blocks for the implementation of artificial neural networks, IEEE Transactions on Neural Networks 7 (2) (1996) 506–514.](https://www.researchgate.net/publication/null?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)

<br/>

----------------

# Referências

1. [M. Glesner, W. Poechmueller, Neurocomputers: An overview of Neural Networks in VLSI, Chapman and Hall, London, 1994.](https://www.researchgate.net/publication/245362345_An_Overview_of_Neural_Networks_in_VLSI?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)

    <a name="1" />
    

2. [Y. Dong, S. Bagga, W. A. Serdijn, An inherently linear cmos multiplier, in: Proceedings of the program for research on integrated systems and circuits (ProRISC’04), 2004, pp. 483–486.](https://www.researchgate.net/publication/228905529_An_inherently_linear_CMOS_multiplier?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
    
    <a name="2" />


3. [ H. P. Graf, L. D. Jackel, R. E. Howard, B. Straughn, J. S. Denker, W. Hubbard, D. M. Tennant, D. Schwartz, Vlsi implementation of a neural network memory with several hundreds of neurons, in: AIP Conference Proceedings 151 on Neural Networks for Computing, American Institute of Physics Inc., Woodbury, NY, USA, 1987, pp. 182–187.](https://www.researchgate.net/publication/234857555_VLSI_implementation_of_a_neural_network_memory_with_several_hundreds_of_neurons?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
    
    <a name="3" />


4. [S. Eberhardt, T. A. Duong, A. Thakoor, Design of parallel hardware neural network systems from custom analog vlsi ‘building block’ chips, in: IJCNN International Joint Conference on Neural Networks, 1989, pp. 183–190.](https://www.researchgate.net/publication/224740405_Design_of_parallel_hardware_neural_network_systems_from_custom_analog_VLSI_'building_block'_chips?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
    
    <a name="4" />


5. [T. Morishita, Y. Tamura, T. Otsuki, A bicmos analog neural network with dynamically updated weights, in: IEEE International Solid-State Circuits Conference, 1990, pp. 142–143.](https://www.researchgate.net/publication/null?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
    
    <a name="5" />


6. [C. Mead, Analog VLSI and Neural systems, Addison-Wesley, 1989.](https://www.researchgate.net/publication/260477020_Analog_VLSI_and_neural_systems?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
    
    <a name="6" />