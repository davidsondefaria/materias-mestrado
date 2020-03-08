# Redes Bayesianas

- Estudar Probabilidades

#### Conhecimento incerto
Grau de certeza/incerteza da teoria da probabilidade é ***diferente*** de grau de verdade de lógica fuzzy.



## Regra de Bayes
Regra:
- P(causa|efeito) = ( P(efeito|causa)P(causa) )/( P(efeito) )

## Redes Bayesianas
É um grafo direcionado em que cada nó possui as probabilidades da variável atual dado os valores das variáveis pai.


# Naïve Bayes
- Calcula a probabilidade de todas as classes possíveis e verifica a mais provável;
- Assumo que todos os atributos são independentes;
- Dados discretos;
- Vai filtrando pelas classes e calculando a probabilidade: a maior prob é a classe 'prevista';