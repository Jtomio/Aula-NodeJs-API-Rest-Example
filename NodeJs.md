<!-- Aula 2 - BackEnd e FrontEnd -->

>>> FRONT-end
Todo código da aplicação responsável pela apresentação do software, conhecida como "client side".

>>> Desenvolvedor Front-end
Trabalha com linguagens como HTML,CSS e JAVASCRIPT, além de frameworks, tais como REACT, ANGULAR, VUE. etc.

>>>  BACK - END
É a parte do software que roda no servidor, por isso também é conhecida como "server side"

>>> Desenvolvedor BAck-end
Trabalha com linguagens de programação tais como JAVA, C#, PHP, PYTHON, RUBY, JAVASCRIPT(Sim, tem jeito de rodar JS no servidor também).

>>> Desenvolvedor Fullstack
Quem trabalha tanto com front-end quanto back-end.


<!-- Aula 3 - NodeJS -->

>>> Desenvolvedor NodeJS
São desenvolvedores JS, pois NodeJS não é uma linguagem de programação.

>>> NodeJS não depende do browser
Utilizado para criação de páginas dinâmicas, conexão com banco de dados, acesso ao sistema operacional, criação de CLI (utilitários de linha de comando) etc.

>>> Afinal, o que é NodeJS
É uma plataforma voltada para o desenvolvimento de aplicações utilizando JS.

>>> NodeJS
Criado por Ryan Dahl (2009), possibilitou rodarmos o JS independente do browser. Logo podemos trabalhar com front-end e back-end utilizando uma linguagem.

>>> por que grandes empresas trabalhando com NodeJs

>>> Benefícios em utilizar
ter um time de engenharia focado em uma linguagem utilizada para front-end e back-end.

>> Aolicações leves e escaláveis. Veja um exemplo de resultado com NodeJS no Paypal:
 + O aplicativo foi desenvolvido quse duas vezes mais rápido com menos pessoas.
 + com 33% menos linhas de código e 40% menos arquivos (em comparação com o aplicativo anterior baseado em Java)
 + Dobrou o número de requests atendidas por segundo e ao mesmo tempo diminiu o tempo médio de resposta em 35%.

>>> Javascript
Possui uma arquitetura não bloqueante de THREAD única (Single thread, baseada em eventos).

>>> Arquitetura do JavaScript
>> CAll Stack
    + Respnosável por empilhar as chamadas de funções

>> CAllback Queue
    + Responável por empilhar os callbacks (funções enviadas como parâmetro para funções assíncronas)

>> Event Loop
    + Responsável por checar continuamente se algum evento assíncrono foi disparado para posteriormente executar o callback.

Ex:
    + Um restaurante podemos chamar de = Aplicação Web
    + Clientes = Usuários
    + Garçom = Single thread
    + Cozinha = Processos de regra de negócio. Acesso ao banco.

    Ou seja, o garçom não espera o pedido ficar pronto para retornar as mesas, ele vai recebendo os pedidos e quando um ficar pronto 
    ele retorna a mesa solicitante. 

    isso torna a operação fluída.

    console.log('Node.js');
    setTimeout(function callback() {console.log('é') }, 0);
    console.log('Sensasional!');

fim Ex:

>>> NodeJS
Não é a solução para todos os problemas.

>> Vantagens
Ideal para aplicações com um grande colume de i/o, tais como chats, streaming, servidores web e comunicações de rede

>> Desvantagem
Não é recomendado por aplicações que utilizam alto uso do CPU, como por exemplo, manipulação de vídeos e imagens.

<!-- Aula 4 - Instalação do NodeJS -->
>>> Instalando o NodeJS
acessar:  https://nodejs.org/

    + Escolher a opção Versão LTS
    + No cmd verificar a versão: node -v
    instalar a versão recente.


<!-- Aula 5 - Gerenciador de pacotes NPM -->

>>> NPM - Node Packege Manager
utilitário de linha de comando para gerenciar as dependências/ pacotes do Node.

>>> instalação do NPM
Necessário instalar o node.js, visto que eles são empacotados juntos.
    + npm -v //verificar a versão
    + npm install -g npm

utilizando pacotes NPM no projeto Node
O projeto deve conter um arquivo chamado de package.json

acessar: npmjs.com

<!-- Aula 6 - Iniciando um projeto em NodeJS -->

>>> Para iniciar um novo projeto e criar o package.json utilizar
    + npm init //iniciar um novo projeto
    + npm install //instalar atualização de pacotes

<!-- Aula 7 - Função Callback na pratica -->

>>> O que é callback?
É uma função executada após o processamento de outra função.

<!-- Aula 8 - Introdução e Promises -->

>>> Qual o problema em utilizar o callbacks?
um dos problemas é o "callback hell"


>>>Paralelismo
    let dados1 = null, dados2 = null;

        readFile('file1.json', fuction(error, dados) {
            dados1 = dados;
            exibir();
        });

        readFile('file2.json', function(error, dados) {
            dados2 = dados;
            exibir();
        });

    function exibir() {
        if(dados1 && dados2) {
            console.log(dados1);
            console.log(dados2);
        }
    }
----------------------

>>> Promises
É um objeto para trabalhar com a assincronismo em javascript

>>> E por que Promises?
A questão é mais organização do código do que a funcionalidade em si.

>>> Ciclo de Vida das Promises
    Pending: estado inicial.
    Fulfilled: executou com sucesso.        .then()
    Rejected: a operação falhou.            .catch()

<!-- Aula 9 - Refatorar Callback para Promises -->

>>> Exemplo no 04-aula-refatorar

<!-- Aula 10 - Promises com async/await -->

>>> possibilita trabalhar com códigos assíncrono em um estilo similar ao código síncrono.

<!-- Aula 11 - Conhecendo For, ForIn e ForOf -->

>>> O laço FOR é responsável por percorrer elementos de um array
    
    const alunos = ['Rafael', 'Fernanda', 'Gabriel', 'Jorge'];
        for (let i=0, i<alunos.length; i++) {
            console.log(alunos[i]);
        }

>>> O laço FOR IN é responsável por percorrer pelas propriedades de um objeto.

    const alunoRafael = {
        id: 1,
        name: 'Rafael Ribeiro',
        github: 'rprrafa'
    };

    for (let prop in alunoRafael) {
        console.log(prop);
    }

>>> o laço FOR OF é responsável por percorrer valores de objetos que sejam iterativos

    const alunos = ['Rafael', 'Fernanda', 'Gabriel', 'Jorge'];
    
    for (aluno of alunos) {
        console.log(aluno);
    }

<!-- Aula 13 - Conhecendo o Array.Map -->

>>> Executa uma função em todo os tiens de um array e retorna um novo array após a manipulação.

    conteúdo na prática 

    07-aula-Map

<!-- Aula 14 - Conhecendo o Array.Filter -->

>>> Filter ()
    Aplica uma condição em todos os itens do array e aqueles que se enquadrarem na condição serão retornados e adicionados ao novo array de saída.

    Prática - 08-aula-Filter

<!-- Aula 15 - Conhecendo o Array.Reduce -->

>>> reduce()
Reduz todos os valores de um array em um único resultado com base na função
informada. Utilizado para realizar uma somatória ou mesclar vários arrays em um único.

    Prática - 09-aula-reduce

<!-- Aula 16 - Introdução a APIs -->

>>> Application Programming interface (API)
Conjunto de especificações de possíveis interações para que sistemas ou aplicativos diferentes se comuniquem.

É uma das principais formas de comunicação entre sistemas.

>>> o que é REST (Representational State Transfer)?
Criado por Roy Fielding, é conceito arquitetural para ciração APIs.
Uma API que aplica o conjunto de padrões REST é conhecida como RESTFul


METODO                  ESCOPO                      SEMÂNTICA
GET                     coleção                     Recuperar todos os recursos em uma coleção
GET                     recurso                     Recuperar um recurso em uma coleção
POST                    coleção                     Criar um novo recurso
PUT                     recurso                     Atualizar um recurso
PATCH                   recurso                     Atualizar um recurso
DELETE                  recurso                     Deletar um recurso
OPTIONS                 recurso ou coleção          Retorna todos os métodos HTTP disponíveis

>>> Códigos HTTP
2xx: Confirmação
    a. 200 (OK): A solicitação foi tratada e concluida com êxito.
    b. 201 (Criado): indica a criação bem sucedida de um recurso.

3xx: Redirecionamento
    a. 301 Movido permanentemente

4xx: Solicitação inválida
     Representa um erro do lado do cliente, porque a solicitação foi malformada ou faltam parâmetros de solicitação
     a. 401 (Não autorizado): você tentou acessar um recurso para o qual não tem permissão.
     b. 404 (Não encontrado): o recurso solicitado não existe.

5xx (Erro interno do servidor)
    Sempre que o servidor levanta uma exceção durante a execução da solicitação.

>>> Parâmetros das Requisições
    Header Params: enviados no cabeçalho da requisição
    Query Params: enviados pela URL com chave e valor
    Route Params: enviados pela rota
    Body Params: enviados no corpo da requisição

>>> Boas Práticas API Rest
Considerando recursos para a entidade usuários, temos:

    Obter lista de usuários GET/users(status 200)
    Obter detalhes de um usuário GET/users/{id} (status 200)
    Obter detalhes de um usuário POST/users (status 200)
    Remover um usuário DELETE/users/{id}(status 204)
    Atualizar um usuário PUT/users/{id} (status 200)
    Atualizar apenas alguns dados do usuário PATCH/users/{id} (status 200)

Prática 10-aula-API-Rest

<!-- Aula 17 - Iniciando Servidor com Express -->

>>> Express
Framework que facilita o desenvolvimento de aplicações web e APIs, como um sistema de rotas completo, tratamento de execuções, gerenciamento de requisições HTTP e etc.

>>> Instalação 
npm install express

Prática 10-aula-API-Rest

<!-- Aula 18 - Trabalhando com GET -->

>>> Recursos de GET
Obter lista de usuários GET/users (status 200)
Obter detalhes de um usuário GET/users/{id} (status 200)

Prática 11-aula-API-Get

<!-- Aula 19 - Trabalhando com POST -->

>>> Recursos com POST
Obter detalhes de um usuário POST/users (status 201)


Prática 12-aula-API-Post

<!-- Aula 20 - Trabalhando com PUT -->

>>> Recurso com PUT
Atualziar um usuário PUT/users/{id} (status 200)

Prática 13-aula-API-Put

<!-- Aula 21 - Trabalhando com DELETE -->

>>> Recursos com DELETE
Remover um usário DELETE/users/{id} (status 204)

Prática 13-aula-API-Put

<!-- Aula 22 - Disponibilizando nossa API utilizando o Heroku -->

>>> Heroku
É uma plataforma em nuvem como serviço que suporta várias linguagens de programação.
