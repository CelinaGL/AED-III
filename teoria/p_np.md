# P vs NP
- [P vs NP](https://ricardomatsumura.medium.com/p-vs-np-c37368838dfb)
- [NP e NP-Completeza](https://ricardomatsumura.medium.com/np-e-np-completeza-3ca168d5b3a1) - texto ótimo, ler mais de uma vez
- [Vídeo do canal Tem Ciência](https://www.youtube.com/watch?v=O-OLFG0WJpc)

## P
- São resolvidos em tempo polinomial, então também são verificáveis em tempo polinomial
- Os problemas em P possuem ambos certificados sucintos para SIM e para NÃO, mas não se sabe se todo problema que possui ambos certificados é P.

## NP
- Probelmas de decisão(resposta = sim ou não) 
- São verificáveis em tempo polinomial (colocar a solução correta em uma MTD "Uma MTD, porém, pode verificar um caminho polinomial em tempo polinomial se este lhe for dado — basta seguir o caminho e verificar se ele termina em um estado de aceitação. Este caminho é chamado de certificado ou prova pois é uma prova que a MTND soluciona o problema em tempo polinomial. Mais ainda, por ser um certificado curto (polinomial no seu tamanho), ele é chamado de certificado sucinto.")
- São solucionáveis em MTND(Máquina de Turing Não Deterministica) em tempo polinomial mas não possuem tempo polinomial se for convertido para MTD
- Se é fácil checar que a solução de um problema é correta, então é fácil resolver o problema?

- "Para uma MTND solucionar um problema em tempo polinomial, ela deve gerar caminhos (sequência de estados) que cheguem a um estado final (parada) e que pelo menos um destes caminhos deve ter comprimento que cresce polinomialmente com o tamanho da entrada; do contrário, o tempo para gerar este caminho seria maior que polinomial. Podemos portanto considerar a classe NP como sendo a classe contendo problemas que possuem pelo menos um caminho polinomial até uma solução."
- "Note que a existência de uma solução polinomial não garante que uma MTD pode solucionar este mesmo problema em tempo polinomial, pois a MTD não sabe necessariamente como encontrar esse caminho e pode ter que testar exponencialmente muitos caminhos até encontrá-lo, mas a MTND, de certa forma, explora todos caminhos de forma simultânea."
- "Um problema de decisão é NP se ele possui um certificado sucinto para SIM."

### co-NP
- "Nesta definição, pode ou não haver um certificado sucinto para NÃO, mas a existência de um para SIM garante que o problema pertence a NP. Por outro lado, se um problema possui certificado sucinto para NÃO, dizemos que ele pertence à classe co-NP." explicação de certificado sucinto para NÃO em **Definições**
- Então não será co-NP se o tempo para provar que nunca se chegará em uma resposta sim, não for polinomial

## NP-Completos
- Problemas NP tais que qualquer outro problema em NP pode ser reduzido a ele. explicação de redução polinomial em **Definições**
- "Um problema é dito pertencer a classe NP-Completo se ele pertence a NP e todo problema em NP possui uma redução polinomial para ele." 
(existe uma forma de traduzir qualquer NP para NP-Completo e essa tradução é polinomial)
- Se qualquer problema em NP pode ser verificado em uma MTND e o funcinamento dessa máquina pode ser escrita como o SAT, como qualquer processo em NP pode ser descrito como uma fórmula de SAT, SAT é NP-Completo. SAT em **Definições**
- "Se um problema pertence a NP-Completo, isso implica que nenhum problema em NP é mais difícil que ele. Isto é, os problemas em NP-Completo são os mais difíceis da classe NP."
- "Todos problemas NP-Completo tem a mesma complexidade assintótica. Todos são assintoticamente igualmente difíceis. "
- Ao reduzir polinomialmente um problema que sabemos que é NP-Completo a um novo problema, "Se essa redução for possível estabelecemos que o problema NP-Completo não pode ser mais difícil que o nosso novo problema. Como sabemos também que nenhum problema NP é mais difícil que problemas NP-Completos, concluímos que nosso problema é exatamente tão difícil quanto o NP-Completo: ou seja, ele é também NP-Completo."
- Problemas: SAT, TSP(Caixeiro viagente), Mochila cheia

## NP-Difícil
- Ele não necessariamente é verificável em tempo polinomial, ou seja, que esteja em NP
- Se A é NP Difícil, então todos os problemas em NP podem ser reduzidos a A


## Adendos

### Definições
- Resposta sucinta para NÃO = provar que nunca se chegará em uma resposta sim
- SAT (Problema de satisfatibilidade booliana): "Este problema pergunta se, dada uma fórmula em lógica booleana arbitrária, existe uma atribuição para as variáveis da fórmula que a torne verdadeira."
#### Redução polinomial:
- "O problema A é internamente solucionado por uma solução para o problema B. Para tanto, a entrada x do problema A é transformada por uma função f em uma entrada x' para o problema B. A solução dada por B coincide com a solução para A."
- "A redução polinomial nos dá uma forma de executar A com o tempo aproximado de execução de B acrescentado de no máximo um polinômio — isto é, sem acréscimos significativos de tempo." A ≤p B
- "**A redução estabelece que A não pode ser mais difícil que B.** Isso ocorre por que a redução estabelece uma forma de solucionar A com a complexidade de B, e a complexidade de um problema é sempre dada pelo melhor algoritmo para solucioná-lo."
- Então redução polinomial seria utilizar a solução de um problema para resolver outro problema, adaptando-a, e com tempos aproximados


### Constatações
- P são problemas "facilmente" solucionáveis
- NP são problemas "facilmente" verificáveis, mas não necessariamente solucionáveis
- Problemas solucionáveis em MTND(Máquina de Turing Não Deterministica) em tempo polinomial: NP
- Se converter para MTD e continuar tempo polinomial: P
- "Assim, uma forma informal de diferenciar a classe P e NP é dizer que a classe P contém problemas que são eficientemente solucionáveis por um computador enquanto a classe NP contém problemas que são eficientemente verificáveis por um computador."
- "Com esta definição de NP é muito mais simples provar que um problema pertence a NP: basta mostrar que é possível verificar em tempo polinomial uma solução cuja resposta seja SIM para o problema."
- Ser reduzido = interpretar o problema A dentro de um problema B, então se sabe resolver o problema B então sabe resolver o problema A e vice versa. "Se eu sei resolver B, e A pode ser "disfarçado" de B, então eu também sei resolver A."
