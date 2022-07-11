# Singleton

## O que é?
Singleton garante que uma classe só tenha uma única instância e prover um ponto de acesso global a ela.

## Observações:

- Estado global mutável não é visto com bons olhos, precisa pensar com cuidado antes de usar. Ao contrário de alguma constante final, que não apresenta nenhum problema.
- Um problema do Singleton é que você não consegue trabalhar por meio de uma interface, você necessariamente tem que trabalhar com classes concretas. A possibilidade de trabalhar com interfaces te ajuda a depender menos de implementações específicas e conseguir trocar a implementação sem necessariamente sair gerando efeitos colaterais dentro da sua aplicação.
- A Dificuldade de gerar interface utilizando Singleton é devido ao utilizar o método estático <em>getInstance()</em>. Método estático não esta sujeito a ser colocado dentro de uma interface, visto que método estático pertence a uma instância.
- Outro princípio que o Singleton fere é no que diz respeito ao SOLID. A classe reponsável, nesse exemplo a <strong>ConnectionPool</strong>, ela além de cria a conexão ela lida com o gerenciamento.
- O Monostate acaba resolvendo esses problemas observados acima.
