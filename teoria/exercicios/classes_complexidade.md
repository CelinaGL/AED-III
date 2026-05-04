Análise de Algoritmos e Classes de Complexidade

1. O que o prefixo N indica nas classes de complexidade?
Não determinístico

2. O que o sufixo C indica nas classes de complexidade?
Completo

3. Explique o conceito de redução polinomial em teoria da complexidade e dê um exemplo de como ela pode ser usada para provar que um problema é NP-Completo.
Redução polinomial é solucionar uma problema A com a solução de um problema B, executando A com um tempo aproximado da execução de B acrescentado de no máximo um polinômio, estabelecendo que A não pode ser mais difícil que B.
Ao reduzir polinomialmente um problema que temos certeza que é NP-Completo a um outro problema, se essa redução for possível então o problema NP-Completo não pode ser mais dificil que o novo problema, levando em consideração que nenhum problema NP é mais difícil que problemas NP-Completo, logo o novo problema é NP-Completo.

4. Explique a diferença entre a complexidade de tempo e a complexidade de espaço em teoria da complexidade e dê um exemplo de um problema que pode ser resolvido em tempo polinomial, mas requer espaço exponencial.
Complexidade de tempo: tempo de execução necessário para resolver o problema em relação ao tamanho da entrada
Complexidade de espaço: a quantidade máxima de memória que um problema precisa durante a execução em relação a entrada
Um exemplo de tempo polinomial e espaço exponencial seria um algoritmo que simula circuitos lógicos

5. Descreva a classe de complexidade PSPACE.
Todos os problemas de decisão que podem ser solucionados por uma MT que utilize uma quantidade no máximo polinomial, sem distinção entre MTD e MTND, poir o espaço utilizado independe do tipo de MT

6. Explique o que significa dizer que um problema é NP-intermediário e dê um exemplo de um problema que se acredita ser NP-intermediário.
Problemas NP-Intermediário não possuem algoritmos de tempo polinomial em MTD e também não pode haver redução polinomial de qualquer problema NPC a ele. Um problema candidato a ser NPI seria o reconhecimento de isomorfismo de grafos.

7. Explique a relação entre NP-completo e NP-difícil e dê um exemplo de como uma prova de NP-completude pode ser usada para mostrar que um problema é NP-difícil.
Os problemas em NPD são pelo menos tão difíceis quanto os problemas mais difíceis em NP, por isso a classe NPC é a intersecção entre NP e NPD.

8. Explique o conceito de uma máquina de Turing não determinística e como ela é usada para definir a classe de complexidade NP.
Uma MTND é um modelo teorico de computação que explora varias instâncias de um problema simultaneamete, o fato de ela ser usada para definir a classe NP é por causa dessa capacidade. 

9. Descreva a diferença entre os problemas de decisão e os problemas de otimização em teoria da complexidade, e explique por que é útil restringir nossa atenção aos problemas de decisão.
Em problemas de decisão pergunta se uma determinada solução existe, tendo as soluções possívies como sim ou não. Já problemas de otimização envolvem encontrar a melhor solução possível.

10. Descreva a diferença entre a classe de complexidade P e a classe de complexidade NP, e explique por que é tão difícil determinar se essas duas classes são iguais ou não.
Classe P: Problemas verificáveis e solucionáveis em uma MTD em tempo polinomial
Classe NP: Problemas verificáveis em uma MTD em tempo polinomial e possuindo uma solução possível em uma MTND em tempo polinomial.
A dificuldade se dá por não sabermos se existe uma forma de converter uma MTND para uma MTD de forma que execute em tempo polinomial, então esta solução pode ou não exixtir.

11. Descreva a classe de complexidade NL e dê exemplos de problemas que pertencem a ela. Explique como essa classe se relaciona com outras classes de complexidade, como P e L.
(Não foi visto em aula pelo que me lembro)

12. Descreva a classe de complexidade co-NP-Completo.

13. Como a relação entre as classes NP e co-NP se relaciona com a questão da existência de provas verificáveis?

