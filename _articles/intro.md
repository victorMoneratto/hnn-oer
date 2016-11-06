---
order: 1
title: Introdução
subtitle: Redes Neurais Artificiais e por que implementá-las em hardware.
next_page: design
---
# Conceitos Importantes
Redes Neurais Artificiais (RNA) são um paradigma em aprendizado de máquina inspirado pelo cérebro. Elas são utilizadas em aplicações de reconhecimento de padrões, memória, mapeamento, etc. e possuem dois componentes principais, *Neurônios,* que correspondem aos vértices de um grafo, e *Sinapses*, que correspondem aos vértices. 

Conforme a RNA aumenta de tamanho, o número de sinapses aumenta quadraticamente, o que torna uma rede neural completamente interconectada algo difícil de se construir.

# Vantagens sobre Implementações em Software
A maior parte das RNAs utilizadas atualmente são implementadas em software. Isso ocorre, principalmente, por causa da flexibilidade oferecida pelo software durante o desenvolvimento, fase de testes e updates. Entretanto, certas aplicações de RNAs, como a compressão de uma stream de vídeo, demandam alto volume de processamento adaptativo em tempo real, em conjunto com o aprendizado de grandes datasets em tempo razoável.

Tais aplicações necessitam o uso de implementações de Integração Em Grande Escala (IEGE) que sejam eficientes e com capacidade de processamento realmente paralela. Hardware especializado, que pode tanto suplementar quanto substituir o software, muitas vezes oferece muitas vantagens nessas situações. 

Algumas dessas vantagens são:

* **Velocidade**: Hardware especializado pode oferecer um poder computacional muito alto a um preço limitado e, portanto, um speed-up de varias ordens de magnitude, especialmente reino das RNAs, onde paralelismo e computação distribuída estão inerentemente entrelaçados.

* **Custo**: Uma implementação em hardware pode prover margens para a redução do custo do sistema ao diminuir o numero de componentes e o gasto de energia. Isso mostra sua importância em produtos produzidos em massa, por exemplo.

* **Degradação Suave**: uma limitação intrínseca a qualquer aplicação sequencial mono-processador é sua vulnerabilidade a falhas no sistema. Em contraste, essa arquitetura paralela e distribuída permite que as aplicações continuem funcionando apenas com uma performance reduzida (graceful degradation) mesmo na presença de falhas em alguns de seus componentes. Para aplicações críticas, esse é um ponto fundamental, e a implementação em Hardware tem grande vantagem.

* **Sigilo**: Hardware especializado pode oferecer melhor proteção contra engenharia reversa por parte de potenciais competidores, quando comparado com a mesma função implementada em hardware.

Um Hardware realizando uma RNA é geralmente chamado de uma Rede Neural em Hardware (RNH). Informalmente, RNHs podem ser definidas como dispositivos projetados para implementar arquiteturas neurais e algoritmos de aprendizado, tirando vantagem da natureza inerentemente paralela das RNAs.

# Desafios Encontrados
Como a maior parte dos problemas resolvidos por redes neurais requerem um mínimo de 100 a 1000 neuronios, o número de sinapses cai em algum lugar entre 10^4 e 10^6. Para o aprendizado ocorrer, essas interconexões precisam ser modificáveis. Já que limitações de hardware introduzem erros deprecisão, a degradação do aprendizado e a falta de acurácia são grandes desafios ao se criar uma RNH, já que podem levar ao aumento no numero de ciclos até o aprendizado.

Outro desafio é a criação das interconexões entre os neurônios. No cérebro, os neurônios possuem sinapses que se ligam em três dimensões. Um chip não possui essa liberdade, o que impõe limitações no design de RNHs. As abordagens mais utilizadas incluem a Digital <sup>[1](#1), [2](#2), [3](#3)</sup>, analógico <sup>[4](#4), [5](#5)</sup>, híbrida <sup>[6](#6), [7](#7)</sup>, e implementações óticas não-eletrônicas.

Os blocos estruturais em cada uma dessas implementações consiste em pesos, somadores e multiplicadores, e Funções de Ativação (FAs) que definem um unico Neurônio. Apesar de não tão popular quanto as RNAs em software, existem várias RNHs sendo aplicadas no mundo real.

<br/>

----------------

# Referências

1. S. Y. Kung, Digital Neural Networks, Prentice-Hall, 1992.
    <a name="1" />

2. [P. Ienne, Digital hardware architectures for neural networks, Speedup Journal 9 (1) (1995) 18–25.](https://www.researchgate.net/publication/null?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
    <a name="2" />

3. [A. Bermak, D. Martinez, A compact 3-d vlsi classifier using bagging threshold network ensembles, IEEE Transactions on Neural Networks 14 (5) (2003) 1097–1109.](https://www.researchgate.net/publication/220279953_A_Compact_3D_VLSI_Classifier_using_Bagging_Threshold_Network_Ensembles?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
    <a name="3" />

4. [C. Mead, Analog VLSI and Neural systems, Addison-Wesley, 1989.](https://www.researchgate.net/publication/260477020_Analog_VLSI_and_neural_systems?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
    <a name="4" />

5. [B. Brown, X. Yu, S. Garverick, Mixed-mode analog vlsi continuous-time recurrent neural network, in: Proceedings of International Conference on Circuits, Signals and Systems, 2004.](https://www.researchgate.net/publication/221435849_Mixed-mode_analog_VLSI_continuous-time_recurrent_neural_network?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
    <a name="5" />

6. [S. Haykin, Neural Networks: A Comprehensive Foundation, Macmillan, 1994.](https://www.researchgate.net/publication/265439255_Neural_Networks_A_Comprehensive_Foundation?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
    <a name="6" />

7. [A. Schmid, Y. Leblebici, D. Mlynek, A mixed analog digital artificial neural network with on chip learning, IEE Proceedings - Circuits, Devices and Systems 146 (1999) 345.](https://www.researchgate.net/publication/null?el=1_x_8&enrichId=rgreq-d0c76f22295154d4af489f34654935c4-XXX&enrichSource=Y292ZXJQYWdlOzIyMzkzODA3ODtBUzoyMDQ4MjU5OTczODU3MjhAMTQyNTg0NTczMTI2Mg==)
    <a name="7" />

8. [J. Misra, I. Saha, Artificial neural networks in hardware: A survey of two decades of progress](https://www.researchgate.net/publication/223938078_Artificial_neural_networks_in_hardware_A_survey_of_two_decades_of_progress)