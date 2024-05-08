# camadas-solid
Resumo sobre criar e desacoplar camadas do SOLID

Camada não tem relação com pasta, mas sim com o relacionamento com os componentes.

## Cenário do Resumo:
Transição de pagamento
Use cases de Create Transaction e GetTransaction
Entities Transaction e Installment
API com Banco de Dados

### Pontos falados no video, depois elaborarei um texto com 30 linhas em outro arquivo

Começar um projeto por conta própria é a melhor forma de entender as decisões.
Completar método e corrigir BUG a vida inteira não nos trás experiência
Entender usuário e aquilo que ele está fazendo
CDD Console-Driven Development
Front-End-Driven 
Main importando express, instânciando ele e abrindo na porta 3000
Nodemon no SRC
Cannot Get / Já mostra API no ar
Se não tendo as camadas definidas precisamos partir já para testes de integração
axios para fazer requisições para api
fez post com dados para transação
TDD precisa de Givem When Then - Arrange, Act, Assert

Teste como uma alavanca para executar algo no console
Nós pulamos etapas ao querer enviar rapidamente os dados para o BD
Criando tabelas no SQL, para transaction e installment
Aplicação de uma camada só por enquanto
Desacoplar camadas é saudável para a aplicação com o tempo
Deixar os testes mais estáveis
Começar uma tinha de TDD
Se a gente não cria uma expectativa exclusiva antes, ficamos flutuando
Criar o teste pensando nas 3 etapas
Ter o teste antes é super relevante independente do cenário
Antes de desenvolver já faz o teste
Misturar regras de negócio com banco de dados high level é horrível
Objetivos é passar por todos os asserts
Até aqui quebramos o Single Responsability Principle - Separar coisas que mudam por motivos diferentes tanto no nível de negócio quanto no nível de responsabilidade, camada e tipo de tecnologia
O teste pode ter várias assertions desde que possuam a mesma proposta do teste
Misturar conteúdo com ports adapters
Existem 2 lados = Driver Side e Driven Side
É importante organizar o código também
DTO - Passar um Input
Trocou o Req Body por input
Ao descer um nível passou a testar a camada de application
Regra de negócio dentro do controller está errado, bloqueia a capacidade de testar o nível de abstração adequado
Testando a fronteira da aplicação
outro princípio do solid para separar o banco de dados, é a inversão de dependências
Uma classe é protegemos o estado interno da aplicação
Com o transaction repository na mão, podemos desmembrar 
Ao persistir uma transaction também persistimos uma installment?
application é um regra específica
osquestrando as regras de negócio
O Teste garante a coragem para fazer a implementação
Camada de aplication misturada com conceitos de I/O me torna fragil
O repositório não deveria conhecer o driver que ele está usando
deve olhar de forma mais desacoplada
toda connection deve ter um query, statement, params
criando padrão para encapsular o pgp e implementar o contrato
o repositório não conhece mais o pg promise
objetivo é fazer as camadas deixarem de se conhecer
main component age como um root, entry point da aplicação
dependency invertion
todo http server tem on e method string, url, callback, listen port number
tiramos o acoplamento com express, tipode pattern ainda é o mesmo
get e post é [method]
invocar o callback de params e body
res.json com o output que vai voltar
separando dependências
main conhece a httpserver
init define as rotas e faz o listen
começamos com uma aplicação totalmente acoplada e agora temos uma aplicação instanciada
quem sabe o tipo de conexão é o main
deixou a aplicação mais flexível
Open Close Principle
Aberta para expansão
Pelos testes estamos livres
implementação em memória
ganhamos muitas possibilidades ao desacoplar camadas
aplicação guia com mecanismos de I/O
aderentes a clean architecture
use cases das entidades
deveria ter um teste de unidade
tecnologia em direção ao domínio
é muito mais rápido testar a nível de unidade do que de integração
poderíamos ter diversos cenários
para ter os testes precisamos de uma boa estruturação de camadas da aplicação


