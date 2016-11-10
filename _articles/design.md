---
order: 2
title: Design de Neurônios
subtitle: Diferentes implementações dos blocos básicos de uma rede neural.
previous_page: intro
next_page: digitais
---
A transmissão de sinais biológicos no cérebro através de sinapses é um processo químico complexo, em que diversas substâncias específicas são utilizadas. Essas substâncias têm o efeito de mudar o potencial elétrico na célula receptora e, quando esse potencial atinge um certo limite, o neurônio dispara.

O Neurônio Artificial procura imitar esse processo. Os inputs e pesos são modelados como valores reais, que estimulam ou inibem o disparo baseado nos valores inseridos. O output neuronal é sua Função de Ativação, análoga a sequência de disparo do neurônio biológico, que pode ser de Limite, linear, exponencial ou sigmoidal.

Aqui, comparamos dois métodos de se implementar um neurônio artificial, a Digital e a Analógica. A Analógica é muito eficiente em termos de espaço físico e velocidade de processamento, entretanto perde acurácia. A digital, por sua vez, ganha precisão ao custo de eficiência.

{% include image.html url='/public/images/ArtificialNeuron.jpg' desc='Um neurônio artificial.' %}

## Neurônios Digitais

A implementação digital<sup>[1](#1)</sup> de um unico neurônio é relativamente simples, já que todas operações necessárias para implementa-lo podem ser feitas de forma direta. No neurônio digital, pesos sinápticos são guardados em registradores ou memórias, cujas alternativas incluem um a tres RAMs de transistores dinâmicos, ou quatro ou seis RAMs de transistores estáticos. Somadores, subtratores e multiplicadores são disponíveis como circuitos padrões<sup>[2](#2)</sup>, e Funções de Ativação não lineares como hardware especializado.

## Neurônios Analógicos

Em neurônios analógicos pesos são geralmente guardados usando um dos seguintes: resistores<sup>[3](#3)</sup>, capacitores <sup>[4](#4), [5](#5)</sup> e floating-gate EEPROMs<sup>[7](#7)</sup>. Com eles, a funcionalidade não-linear da Função de Ativação pode, às vezes, ser capturada diretamente, porém um conjunto coerente de todos os elementos básicos é difícil de ser alcançada.

Como as Funções de Ativação utilizadas em redes neurais em software não podem ser facilmente implementadas em Integrações em Larga Escala, algumas funções aproximadas, ou lookup tables, são utilizadas como FAs no lugar. A implementação analógica se beneficia de explorar efeitos físicos simples para executar algumas das funções de rede [6](#6).

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

7. [M. Holler, S. Tam, H. Castro, R. Benson, An electrically trainable artificial neural network (ETANN) with 10240 “Floating Gate” synapses, in: Proceedings of Inter- national Joint Conference on Neural Networks, Vol. II, Washington D.C., 1989, pp. 91–96.](https://www.researchgate.net/publication/224740406_Electrically_trainable_artificial_neural_network_ETANN_with_10240_'floating_gate'_synapses?el=1_x_8&enrichId=rgreq-0408120c6aa15b9ee8d1aa389dc92ec8-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
    
    <a name="7" />