# Escopo
Ao conversar com o setor responsável você identificou que a aplicação precisará de ao menos dois cadastros, um cadastros de clientes e outro onde será registrado as avaliações mensais.

## Cadastro de clientes
Para o cadastro do cliente você terá 3 informações básicas: **nome**, **nome do contato responsável** e a **data em que virou cliente**.

Nesse cadastro é necessário que você faça as seguintes validações:
- Todos os campos são obrigatórios;
- Cada cliente deverá ter um sinalizador indicando a sua categoria de acordo com a sua última avaliação:
  - <span style="color:green">Promotor</span>: Nota 9 ou 10
  - <span style="color:yellow">Neutro</span>: Nota 7 ou 8
  - <span style="color:red">Detrator</span>: Nota de 0 a 6
  - Nenhum: Para casos onde o cliente ainda não tenha participado de uma avaliação

## Cadastro de avaliações
Ao cadastrar uma avaliação você duas informações, são elas: 
- Mês e ano de referência *(obrigatório)*;
- Clientes que participaram da avaliação *(seleção múltipla; obrigatório)*;

As seguintes validações devem ser observadas:
- Só deve ser possível realizar apenas uma avaliação por mês;
- Cada avaliação é composta por 20% dos clientes cadastrados;
- Os clientes da avaliação
- Após participar de uma avaliação, o mesmo cliente só poderá ser selecionado novamente depois de **duas avaliações**;
  - *Ex.: Se o cliente **Forlogic** participou da avaliação no mês **03/2018**, o mesmo só estará legivel para participar de uma nova avaliação no mês **06/2018***

### Como uma avaliação é realizada
A pesquisa de satisfação é composta de duas perguntas, feitas individualmente para cada cliente participante da avaliação, são elas:

1. Em uma escala de 0 a 10, qual a probabilidade de você recomendar nosso produto/serviço a um amigo/conhecido?
1. Qual é o motivo dessa nota?

### Como obter o resultado geral da avaliação
Dependendo da pontuação que é dada à questão 1, os participantes são classificados em três categorias:

`Promotores` = participantes que deram notas 9 ou 10

`Neutros` = participantes que deram notas 7 ou 8

`Detratores` = participantes que deram notas de 0 a 6

O resultado da avaliação é obtido através da seguinte equação:

`NPS = ((total de promotores - total de detratores) / total de participantes) * 100`

### Divulgação do resultados
Na aplicação deve ser possível visualizar o resultado de cada mês em que foi realizada uma avaliação

A meta é 80%, assim os resultados deverão ser exibidos da seguinte maneira:
- Em caso de meta atingida: Cor verde
- Em caso de meta dentro da tolerância (Entre 60% e 79,99%): Cor amarelo
- Em caso de meta não atingida: Cor vermelho

## Dúvidas?
Caso você tenha ficado com alguma dúvida [abra uma issue](https://github.com/ForLogic/desafio-4-devs/issues) e nós vamos te ajudar.

**Boa sorte! xD**
