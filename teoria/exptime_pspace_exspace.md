# EXPTIME, PSPACE, EXPSPACE

- [Link mediun](https://ricardomatsumura.medium.com/outras-classes-de-interesse-a55bd90486e6)

## EXPTIME
- Classe de todos os problemas de decisão que podem ser solucionados em tempo exponencial, o que não quer dizer que eles SÓ podem ser solucionados nesse tempo
- Então os solucionados de tempo igual ou menor também estão inclusos, todo NP

### EXPTIME-Completo
- Há problemas EXPTIME-Completo que não são P
- "Em outras palavras, mesmo que toda classe NP seja facilmente solucionável, ainda existem problemas que exigem tempo exponencial para serem solucionados."

## PSPACE
- Todos os problemas de decisão que podem ser solucionados por uma MT utilizando uma quantidade no máximo polinomial de espaço
- Sem distinção entre MTD e MTND, pois o espaço utilizado independe do tipo de MT
- " nem toda operação consome memória; podemos simplesmente ficar movendo a cabeça da MT sem escrever nada, ou escrevendo sobre as mesmas células, por exemplo. Isso implica que NP está contida em PSPACE."

## EXPSPACE
- Classe dos problemas que podem ser solucionados por uma MT com uma quantidade exponencial de espaço
- Esta classe contém PSPACE
- Há problemas EXPSPACE-Completos, que exigem uma quantidade exponencial de espaço para serem solucionandos

## Constatações
- "A relação advém de observarmos que escrever na fita é uma operação da MT e toda operação consome tempo. Logo, a MT não pode utilizar tempo inferior ao espaço utilizado. O tempo estará limitado inferiormente" por espaço S.