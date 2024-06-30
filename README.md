# Testes

## Pirâmide de Testes

A _pirâmide de testes_ é **uma forma gráfica** de demonstrar de maneira simples os tipos de testes, seus níveis, velocidade de implementação e complexidade dos testes realizados.

- **Base**
- **Meio**
- **Topo**

## Tipo de testes de cada nível da pirâmide

[Testes Unitários - Base](https://www.notion.so/Testes-Unit-rios-Base-307fa060369e42bdbfcc49480142e1d8?pvs=21)

[Testes de Integração - Meio](https://www.notion.so/Testes-de-Integra-o-Meio-989c4c0d2c224238a8f8aa60f18cf293?pvs=21)

[Testes de Ponta a Ponta(E2E) - Topo](https://www.notion.so/Testes-de-Ponta-a-Ponta-E2E-Topo-b711974439f74bbc8774cbaeac9af950?pvs=21)

A conclusão que podemos chegar é: quanto mais perto da base os testes, menos tempo de execução e complexidade teremos na sua implementação.

## Test Doubles

Podemos utilizar esse tipo de teste quando não temos os dados completos de uma integração ou outros sistemas, sem precisar que testemos uma parte do nosso sistema sem esses dados, que com certeza retornara resultados imprecisos e com falta de informações.

Os *Doubles* são como **dublês de atores de um filme:** Substituem aplicações reais durante os testes p/ simular aparência e comportamento, sem que precisemos ficar presos a uma parte do sistema que dependa de outra parte.

*Doubles* ajudam a eliminar dependências em uma aplicação de forma simples.

### Fakes

Os *Fakes* são como um atalho que pegamos para testar uma aplicação real. Eles simulam algo diferente do que está em produção, mas que de fato ele é real para aquele teste.

### Mocks

Os *Mocks* esperam ser chamados de um jeito, porém, se não for realizado do jeito deles, o teste falhará. Eles são ótimos para testar dois métodos interligados. E são úteis onde não há como verificar algumas mudanças de estado ou retornos do método testado diretamente.

### Spies(revisar)

São “Stubs” que conseguem verificar a interação entre métodos e gravar informações do jeito que foram chamados. O exemplo é um serviço de e-mail que grava quantas mensagens foram enviadas.

### Stubs

São similares aos “fakes” e aos ”spies”, porém ao contrário, ele consegue alterar seu comportamento com base na maneira como ele foi chamado no teste.

### Dummy

Substituem dados reais, só que não são utilizados de fato no teste. Geralmente servem para satisfazer determinados parâmetros.

> Como uso de dummies é possível diminuir a complexidade durante a escrita de um teste, ignorando o que não é relevante no cenário e focando no que realmente importa.
> 

## Test Driven Development(TDD)

O TDD consiste na criação do teste antes do desenvolvimento de alguma implementação e carrega 3 tipos de ciclos diferentes que ajudam a entender melhor a sua aplicação, que são Red, Green e Refactor.

- Red: Basicamente o *red* consiste em criar o teste pensando na funcionalidade, esperando que dê o resultado esperado, obviamente o teste falhará pois a funcionalidade não foi desenvolvida, que será na nossa próxima etapa.
- Green: O *green* consiste em ter a funcionalidade pronta, nessa etapa o código apenas precisa estar funcionando, deixando para melhorar ele na próxima etapa, aqui o teste gerado para essa implementação deve ser positivo.
- Refactor: Aqui no *refactor*, o teste já está pronto e a funcionalidade também, ambos estão funcionando como o esperado, porém, como dito o próprio nome, é a hora de refatorar o código e melhorar ele, garantindo que passe no processo do teste, porém com a melhor escrita.

### Tempo

> “A antecipação é a melhor arma contra o problema”.
> 

Uma das vantagens do TDD é a economia do tempo, pois as correções de futuros bugs podem melhorar exponencialmente na resolução de algum problema, fora que o acrescento de bugs na aplicação será bem menor do que normalmente seria.

## Testes de Mutações

Os *testes de mutações* são basicamente testes dos testes que criamos para as nossas aplicações, eles servem para saber se realmente os testes de unidade, integração ou e2e estão realmente cumprindo o seu papel e retornando de fato os resultados desejados.

O “mutante” criado é uma cópia da estrutura interna do sistema, porém com certas modificações a fim de testar os testes que temos aplicados, as seguintes modificações que podem acontecer são:

- Remoção ou duplicação de algum comando ou expressão.
- Troca de operadores, por exemplo, troca de um operador de adição (+) por um de subtração (-).
- Inserção um operador, por exemplo, `empty()` vira `!empty()`.
- Troca de alguma constante, por exemplo, `True` por `False`.

### Score de Mutações

São uma contagem de quantos mutantes foram gerado e quantos foram mortos pelos testes existentes no sistema, o desejado é sempre 100% do score.

---

## Referências

https://blog.onedaytesting.com.br/piramide-de-teses/

https://blog.onedaytesting.com.br/test-driven-development/

[https://engsoftmoderna.info/artigos/testes-mutacao.html#ferramentas-para-testes-de-mutação](https://engsoftmoderna.info/artigos/testes-mutacao.html#ferramentas-para-testes-de-muta%C3%A7%C3%A3o)
