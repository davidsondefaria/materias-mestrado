# Procurar por Meta-Aprendizagem!!!

# Projeto
- Título: título do projeto
- Resumo: resumo do que vai ser feito
- Qual artigo a ser implementado
- Grupo.

# Aprendizado de Máquina:

- Definição:
    - “A capacidade de melhorar o desempenho na realização de alguma tarefa por meio da experiência” (Mitchell, 1997);
    - “Processo de indução (ou aproximação de função) a partir da experiência passada.” (Faceliet al., 2011).

- Necessita:
    - Tarefa T: o que é proposto a se fazer;
    - Medida de desempenho P: mede se o algoritmo aprendeu;
    - Experiência E: dados históricos.

- Dados: https://www.kaggle.com/

- Por-que aprendizado de máquina é tão importante?
    - Resposta:
        - ***Muitos dados!***
        - Máquinas podem identificar padrões nos dados rapidamente!
    - Exemplos:
        - Deixar alguém monitorando câmeras de segurança para reconhecer suspeitos conhecidos (pode haver milhares de suspeitos!)
        - Contratar alguém para filtrar spam (além de haver muitas mensagens, há também a questão da privacidade neste caso);
        - Ler todos os comentários sobre os produtos de uma empresa e identificar a percepção das pessoas sobre cada produto.

- Tipos de Aprendizado:
    - Supervisionado (Modelo preditivo):
        - Os rótulos(classes) dos exemplos de treinamento estão disponíveis. É possível medir a capacidade de predição com esses rótulos (supervisor);
        - Usos: Classificação, regressão
    - Não-Supervisionado (modelo descritivo):
        - Os rótulosdos exemplos de treinamento nãoestão disponíveis; não há uma resposta desejada (não há supervisor);
        - Usos: Agrupamento

- Cuidado com Termos:
    - Conjunto de Dados != Banco de Dados:
        - Conjunto: não tem, necessariamente, uma organização/estrutura;
        - Banco: estruturado;
    - Classificação (pg 20 Slide):
        - Linha -> Exemplo/amostra
        - Colunas de Treinamento (**X**): Atributos (para classificação)
        - Coluna para Resutlado (y): Classe/Rótulo
        - Tudo: Conjunto de Dados
    - Hipótese = modelo
    - Parâmetros != Hyper-parâmetros (em ML)
        - Hyper-parâmetros: gera outros parâmetros;

- Classificação:
    - Algoritmo de Classificação: algoritmo para obter o modelo;
    - Classificador: output do modelo;
    - Pg 23 Slide:
        - Workflow da Classificação
    - Nem todo atributo é relevante!
    - Cuidado: *Overfitting*:

- Regressão:
    - Navalha de Occam (**Occam’s razor**):
        - Obter consistência com simplicidade;
    - Avaliar a generalização:
        - Comparar os dados de teste com os de treinamento;
        - *Overfitting*: bem no treinamento, mal no teste;
        - *Underfitting*: mal no treinamento e no teste;

- Viés Indutivo (pg 35):
    - Indução: obter conclusões sobre todos os membros de uma classe pelo exame de apenas alguns de seus membros.
    - Aprendizado de Máquina: induzirmodelosa partir de experiência (exemplos).
    - Viés indutivo:
        - Viés de representação: como o modelo é descrito (e.g. árvore de decisão, rede neural, etc)
            - Árvore de Decisão (pg 36);
            - Conjunto de Regras;
            - Rede Neural (pesos).
        - Viés de busca: como é feita a busca pelo modelo (e.g. algoritmo ID3 tem tende a buscar por árvores de decisão poucos nós)
    - Viés indutivo parece uma limitação, entretanto, a busca por um modelo pode ser impraticável se for realizada em todo o universo.

- Fronteira de Decisão
    - k-NN: cada exemplo é associado a uma região, definindo a fronteira de decisão;
    - Classificador Linear: 

- Desempenho de Modelos:
    - Necessário definir quais métricas serão usadas de acordo com o modelo:
        - Classificação: avalia exemplos classificados corretamente e incorretamente;
            - Exemplo: acurácia;
        - Regressão: avalia diferença entre o valor predito e o valor correto;
        - Agrupamento: diversas medidas (critérios internos, externos e relativos).
    - Os dados de treinamento e de testes devem ser completamente separados:
        - Não pode reescalar os dados antes do treinamento;
        - Usar valores de mínimo e máximo do treinamento no teste;

- Amostragem;
    - Separação de treino e teste;
    - Holdout:
        - Separar os dados por partições:
            - 2/3 de Treino;
            - 1/3 de Testes;
        - Mas o ideal é verificar na literatura da área;
        - Amostragem aleatória:
            - Realiza o holdout várias vezes e tira média do desempenho;

    - Validação cruzada:
        - Mais comum;
        - Quebra o conjunto em k-partições;
        - Combina as partições e tira a média do desempenho;
        - O algoritmo é treinado com (k–1) partições e testado com a partição restante; o processo é repetido, kvezes.
        - Leave-one-out: quando k = número de exemplos. (caso particular)

    - Bootstrap:
        - Faz sub-amostrasdo conjunto de dados (diversas variações).
        - Na forma mais comum: 
            - Gera sub-amostrade tamanho ncom reposição (né quantidade de exemplos no conjunto de dados); Essa amostra forma o conjunto de treinamento(aproximadamente 63,2% dos exemplos estarão presentes nessa sub-amostra);
            - Exemplos não amostrados formam o conjunto de teste.
            - O processo é repetido diversas vezes.
        - Indicado para conjuntos de dados menores

    - Separação dos Conjuntos:
        - Muitas vezes, os dados são separados em três conjuntos (ao invés de apenas dois):
            - Treinamento
            - *Validação (pode ser usado para ajustar **hyper-parâmetros** (errado no slide), por exemplo).*
            - Teste

- Medidas de Desempenho:
    - Matriz de Confusão:
        - Acurácia = (𝑉𝑃+𝑉𝑁)/(𝑃+𝑉𝑁+𝐹𝑃+𝐹𝑁)
            - Acertos/Tudo;
            - Não é recomendada quando há desbalanceamento entre as classes;
        - Taxa de Erro = (𝐹𝑃+𝐹𝑁)/(𝑉𝑃+𝑉𝑁+𝐹𝑃+𝐹𝑁)
            - Erros/Tudo;
            - Acurácia: 1 - Taxa de Erro
    - Fazer o Exemplo: PG 59
    - Análise ROC (Receiving Operating Characteristics):
        - Curva ROC: formada pela interligação de vários pontos de um mesmo algoritmo;
        - AUC (AreaUndertheCurve): medida de desempenho, quanto maior, melhor;
    - *eer* = Equal Error R... (procurar)
    - Teste de Hipóteses:
        - Inferência Estatística: processo de obter conclusões a partir dos dados.
        - Ler slides 65-68