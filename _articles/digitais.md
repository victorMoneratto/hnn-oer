---
order: 3
title: Chips Digitais
subtitle: Implementação com chips digitais e a importância de arquiteturas SIMD.
previous_page: design
next_page: analogicos 
---
Englobando maior parte dos chips disponíveis no mercado, as arquiteturas digitais tem processo de fabricação bem conhecido, design flexivel e facilidades para o armazenamento de pesos.
Porém, as funções de ativação e os multipĺicadores de sinapse são dificuldades frequentes no desenvolvimento.
Várias subdivisões da arquitetura surgiram, como arquitaturas "bit-slice", SIMD e de vetores sistólicos.
Em geral, têm o treinamento feito por um computador associado, feito fora do chip.

# Motivação
Fáceis de projetar, as arquiteturas digitais foram a primeira tentativa de implementação em hardware de sistemas neurais.
Por serem dedicadas, tem uma grande melhora de desempenho comparadas à sistemas idênticos rodando em software em hardwares de uso geral.
Arquiteturas "bit-slice" são fáceis de escalar, sendo projetadas em blocos de baixo custo, cada um processando um ou uma fatia de bits da entrada.

Arquiteturas SIMD trabalham com blocos de dados de maneira simultânea. Por não terem lógica de endereçamento, tem um tempo de resposta menor.
Arquiteturas de Vetores Sistólicos têm um processamento com pipeline, com os elementos de processamento trabalhando de forma síncrona, e repassando os dados processados para o próximo elemento no pipeline.

# Vantagens:
* Facil alocação de pesos.
* Desempenho superior à hardwares de uso geral.
* Modular.

# Desvantagens:
* Precisão deteriorada.
* Dificuldade na implementação de funções de ativação e multiplicadores sinápticos.

# Exemplos
* Micro Devices’ MD1220 Neural Bit Slice
* Adaptive Solutions’ N64000
* Siemens’ MA-16

{% include default-references.md %}

1. [M. Forssell, Hardware Implementation of Artificial Neural Networks](https://users.ece.cmu.edu/~pgrover/teaching/files/NeuromorphicComputing.pdf)