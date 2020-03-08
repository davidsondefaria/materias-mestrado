# Redes Neurais

## Neurônio Artificial
- Valores de Entrada: x_n:
- Pesos: w_n;
- Somatório: u = sum_i(x_i * w_i + b)
    - Bias: b;
- Função de Ativação: f(u)
    - Degrau:
        - f(u) = {0, se u<theta
                 {1, se u>theta
    - Linear:
    - Sigmoide: mais usada
    - Tangente Hiperbólica:
    - ReLU (Rectified Linear Unit):
    - Softmax:
- Saída: y

# Perceptron
Rede Neural com uma camada de neurônios

## Aprendizado
Perceptron é capaz de ajustar os pesos.

> Treinamento em Rede Neural é sempre ajuste de peso.

- Algoritmo:
    1. Inicializa os pesos de forma aleatória;
    2. Repetir:
        1. Atualiza os pesos com:
            - w_ji(t+1) = w_ji(t) + taxa_de_aprendizado*(y_d-y)*x_i

- Perceptron só lida com problemas linearmente separáveis.
- Para lidar com problemas não linearmente separáveis, precisa de multicamadas.

# Perceptron de Multi-Camadas
- Possui camadas adicionais de neurônios;
- A saída das camadas alimentam a próxima camada de neurônios;
- Um MLP com uma camada intermediária aproxima qualquer função continua ou Booleana.
- Um MLP de duas camadas pode aproximar qualquer função (qualidade da aproximação depende da complexidade da rede).

## Aprendizado
O aprendizado é realizado pelo ajuste dos pesos sinápticos (e do bias)

## Algoritmo Backpropagation
~descrever~
- Minimizando o erro E
    - Delta w = - taxaAprendizado (dE)/(dw)
    ... descrever