# Questão 4
## Podemos implementar, nos sistemas distribuídos, o controle de mudança de estado com duas abordagens distintas: o algoritmo de Paxos (e derivados) e os relógios vetoriais. Explique as principais diferenças dessas duas abordagens, focando principalmente nos aspectos relacionados à consistência e o desempenho.

## Resposta:
### O algoritmo de Paxos, é um modelo rígido de consistência, no qual consiste em pelo menos três participantes, sendo eles: proponente, aceitador e aprendiz. Além disso, para cada ciclo (round), é efetuado sequencial de requisições iniciado pelo proponente.
### Porém, apesar de útil, algoritmos baseados nesse modelo são de alto custo, ou seja, para aplicações que exigem uma baixa latência acabam tendo seu funcionamento prejudicado, pois um sequencial seria executado à cada mudança de estado.

### Já o algoritmo baseado em Relógio Lógico, temos um paradigma construído em cima da arquitetura cliente-servidor, onde busca uma comunicação de via dupla, já que o próprio algoritmo se consiste em um comportamento de causa e efeito.
### Para a consistência em si, o servidor será o responsável por manter a "verdade absoluta" e a troca de informações entre ele e o cliente se baseia na troca do sequencial mais recente de cada um. Em cima disso, o Relógio Vetorial vem como solução para o problema de Lamport, onde procurar consistir a ordenação partir de um vetor de contadores em cada processo.