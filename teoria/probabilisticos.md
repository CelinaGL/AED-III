# Algoritmos Probabilísticos
- [Algoritmos Probabilísticos - P1](https://ricardomatsumura.medium.com/algoritmos-probabilísticos-ab257852cf11)
- [Algoritmos Probabilísticos - P2](https://ricardomatsumura.medium.com/algoritmos-probabilísticos-parte-2-algoritmos-monte-carlo-ff86f53fc0a1)
- [Algoritmos Probabilísticos - P3](https://ricardomatsumura.medium.com/algoritmos-probabilísticos-parte-3-las-vegas-d35b574d6623)

- Algoritmos probabilisticos são aqueles que tomam decisões aleatórias durante sua execução. "Decisões aleatórias independem da entrada e podem ser diferentes quando se executa o algoritmo para uma mesma entrada."
- "Por vezes, tomar uma decisão rápida, ainda que potencialmente errada, pode ser mais interessante do que levar um longo tempo para tomar a decisão correta."
- "Tomar uma decisão rápida e sem custo, no longo prazo, se mostra melhor que tomar uma decisão lenta ou custosa."
- "A Máquina de Turing Probabilística é a formalização de um algoritmo probabilístico. Esta é uma Máquina de Turing Determinística mas que tem acesso a uma fonte de valores aleatórios."
- O computador não possui a capacidade de gerar números 100% aleatórios, então usa-se números pseudoleátorios gerados por uma semente.

## Monte Carlo
- "Dizemos que o algoritmo é 0,5-correto e que possui um viés para verdadeiro (i.e. a resposta Verdadeiro está sempre correta e a resposta Falso tem 50% de chances de estar incorreta)."
- "De forma geral, um algoritmo de decisão p-correto possui probabilidade p associada a pelo menos uma das respostas."(viés verdadeiro ou falso) ver em **Definições**
- "Se não estivermos satisfeitos com uma probabilidade de 0,5, podemos melhorar ao custo de mais computação. Se o algoritmo retornar Falso, podemos executar novamente o algoritmo. Podemos repetir o processo para reduzir ainda mais a probabilidade de erro."
- Amplificação da vantagem estocástica: executar mais de uma vez o algoritmo para receber um resultado melhor
- Exemplo de algoritmo: Freivald(verificar multiplicação de matrizes)
- "Dizemos que algoritmos de Monte Carlo executam em tempo determinístico, mas dão respostas probabilísticas. Isto é, executar múltiplas vezes o algoritmo sobre uma mesma entrada levará o mesmo tempo em cada execução, mas dará respostas diferentes com uma probabilidade de erro associada." "Isto significa que o tempo entre diferentes execuções não se altera, mas a resposta pode se alterar e há uma probabilidade de estar incorreta."
- Quanto mais tempo deixarmos o algoritmo rodar, melhor será a solução obtida

## Las vegas
- Apenas retorna quando encontra uma solução correta, portanto nunca retorna uma resposta incorreta, porém o tempo de execução é incerto.
- "Um algoritmo Las Vegas é de certa forma complementar a um algoritmo Monte Carlo. Um algoritmo Las Vegas tem tempo de execução probabilístico, mas resposta determinística". 
- "Nem todo algoritmo Las Vegas é um Monte Carlo com uma etapa de verificação."
- Exemplo: Quick Sort(ele escolhe um pivô aleatório e vai demorar dependendo deste pivô, mas sempre vai retornar o vetor ordenado, e não possui uma verificação para isso), Bozo Sort, Problema das N Rainhas
### Completo
- Tempo máximo de execução dependendo do tamanho da entrada, como o Quick Sort
### Aproximadamente Completo
- Para um tempo que se aproxima de infinito o algoritmo garante encontrar a solução
### Essencialmente Incompletos
- Algoritmos que podem nunca terminar

## Adendos

### Definições
- Algoritmos Deterministicos: executa sempre a mesma sequência de instruções para uma mesma entrada.
- Viés para verdadeiro: a resposta Verdadeiro está sempre correta e a resposta Falso tem 50% de chances de estar incorreta.

### Constatações
