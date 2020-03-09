# Busca Local
Baseado nas aulas e nos slides do professor [Paulo Henrique Pisani](http://professor.ufabc.edu.br/~paulo.pisani/).

## O que é?

Algoritmos de busca local partem um estado inicial e então, por meio de estados vizinhos, caminham até uma solução.

> Os algoritmos de pesquisa que vimos até agora são projetados para explorar espaços de pesquisa sistematicamente. Essa sistemática é alcançada mantendo um ou mais caminhos na memória e registrando quais alternativas foram exploradas em cada ponto do caminho. Quando um objetivo é encontrado, o caminho para esse objetivo também constitui uma solução para o problema. Em muitos problemas, no entanto, o caminho para a meta é irrelevante. Os algoritmos de pesquisa local operam usando um único nó atual (em vez de vários caminhos) e geralmente movem-se apenas para os vizinhos desse nó [Russel & Norvig].

### Algoritmos

- Hill-Climbing
- Simulated Annealing
- Local Beam Search, Stochastic Beam Search

## Anotações

- Só importa estado final;
- Utilizam pouca memória;
- Uteis em problemas de Otimização:
    - Maximizar ou Minimizar uma função objetiva:
        - Encontrar pontos máximos e mínimos de uma função;
        - Busca a melhor solução a partir de um espaço de busca;
    - Caixeiro Viajante;
    - *Vehicle Routing Problem (VRP)*:
        Cálculo de rotas de entregas a partir de um ponto;
    - Escalonameto de Recursos;