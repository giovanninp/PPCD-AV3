# Questão 2
## 1. Na disciplina vimos que o processo de marshalling tem um papel muito importante no projeto e implementação de sistemas distribuídos. Compare as estratégias de marshalling binário e textual, focando nas vantagens e desvantagens de se usar dois dos principais representantes de cada categorias, respectivamente o ProtoBuf e o JSON.

## Resposta:
### O JavaScript Object Notation, é uma solução de marshalling textual bastante difundida no meio da comunicação de um sistema distribuído do dia-a-dia. A sua principal vantagem é a fácil legibilidade e direta integração com JS, além de ser de fácil legibilidade.
### Por outro lado, temos o Protocol Buffer, um marshalling do tipo binário, que por sua parte, possuí grande ponto forte. Sendo esse ponto, o desempenho, já por contar com um tamanho reduzido dos dados, comparado ao JS, e uma leitura mais rápida por parte do sistema - já que não é necessário fazer um tratamento de string.