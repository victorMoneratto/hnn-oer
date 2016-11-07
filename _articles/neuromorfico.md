---
order: 6
title: Hardware Neuromórfico
subtitle: Novas modelagens neuronais inspiradas pelos avanços da biologia.
previous_page: hibridos
next_page: fpga
---
Numa tentativa de se aproximar mais da biologia, os hardwares neuromórficos emulam mais precisamente os comportamentos de neuronios reais.

## Motivação
Paralelo ao desenvolvimento dos chips digitais/analógicos, pesquisadores tentaram se aproximar mais do funcionamento dos neurônios reais, utilizando estudos e descobertas mais recentes de seu funcionamento.

De tais estudos, surgiu o conceito de neurônios de pico/pulso (Spike/Pulse), que levam em conta o tempo de ativação dos neurônios, o potencial da menbrana e mantém limites de ativação dinâmicos.

Tal abordagem é provadamente mais poderosa que os neurônios padrões em termos de computação, porém, devido a sua modelagem complexa, tem um tempo de execução e resposta significativamente maior.

Desenvolver sistemas complexos, com uma grande quantidade de neurônios, é por si só, um desafio. Para isso, foi criado o protocolo de "Adress Event Representation", AER, que emula conexões ponto-a-ponto de neurônios para redes de tamanhos consideráveis.

Para evitar uma sobrecarga de sinais nos neurônios em redes complexas, foi criado o mecanismo de Atenção Seletiva, que transforma o processamento de vários sinais em paralelo no processamento de apenas alguns sinais relevantes, de maneira serial.

Tal processamento é necessário pois, para neurônios de pico/pulso, a ordem e o tempo dos sinais se torna, também, relevante.

## Vantagens
* Mais computacionalmente poderosa
* Capaz de abordar problemas extremamente complexos

## Desvantagens
* Dificeis de projetar e escalar
* Maior tempo de execução e resposta

## Exemplos
* R. Serrano-Gotarredona, M. Oster, P. Lichtsteiner, A. Linares-Barranco, R. Paz-Vicente, F. Gómez-Rodriguez, H. K. Riis, T. Delbruck, S. C. Liu, S. Zahnd, A. M. Whatley, R. Douglas, P. Hafliger, G. Jimenez-Moreno, A. Civit, T. Serrano-Gotarredona, A. Acosta-Jimenez, B. Linares-Barranco, AER building blocks for multi-layer multi-chip neuromorphic vision systems, Advances in Neural Information Processing Systems 18.

* A. Schaik, Building blocks for electronic spiking neural networks, Neural Networks 14 (2001) 617–628.

{% include default-references.md %}

1. [M. Forssell, Hardware Implementation of Artificial Neural Networks](https://users.ece.cmu.edu/~pgrover/teaching/files/NeuromorphicComputing.pdf)
2. [P. Merolla, J. Arthur, F. Akopyan,N. Imam, R. Manohar, D. S. Modha, A Digital Neurosynaptic Core Using Embedded Crossbar Memory with 45pJ per Spike in 45nm](http://www.modha.org/papers/012.CICC1.pdf)