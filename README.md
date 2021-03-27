#TEST PLAN
Stack de testes:

Python
Robot framework
Selenium Webdriver

Ferramenta escolhida
Foi escolhido o Robot Framework como ferramenta para realizar os testes, pois possibilita que sejam realizados testes em diferentes camadas da pirâmide de testes (UI, API). O Robot Framework tem uma proposta de fácil instalação, configuração e utilização, além de ser enxuto e leve. Com pequenos passos e poucas configurações já é possível criar um teste automatizado na camada de UI. Atendendo o objetivo de modo simples, leve e rápido. Seguem alguns pontos que pesaram bastante na escolha do Robot:

Open source
Abordagem de palavras chave (Keywords)
Automação genérica dos testes ( Sites, Webapps, APIs, desktop e mobile)

Ambiente

Python (3.8) 32bits
Chrome Driver 89.0.4389.23

Após instalar o python, precisamos instalar as bibliotecas necessárias para rodar o Robot Framework, basta acessar a pasta raiz do projeto utilizando o prompt ou o gitbash e digitar o seguinte comando:

pip install -r requirements.txt

Estrutura do Projeto
O projeto está dividido em :


Logs: Pasta responsável por armazenar as evidências geradas após a execução dos testes. Dentro dela temos os arquivos do relatório (report.html, log.html) e prints que são capturados no final da execução dos testes.


Resources: Pasta responsável por armazenar o core da aplicação.Dentro dela temos os seguintes arquivos:





Components: Aqui estão os componentes mapeados da aplicação.


Pages: Aqui estão os PagesObjects mapeados.


Base: Arquivo responsável por gerir os imports que serão utilizados  em todo o projeto.


Hooks: Aqui estão os “ganchos” que serão utilizados por todo o projeto.


Ksw: Aqui estão as implementações dos steps descritos na Pasta de Tests.





Tests: Pasta responsável por armazenar as features que serão executadas.

Padrões de Projeto utilizados
Pensando no futuro, caso o escopo do projeto aumente e consequentemente surjam novos fluxos mais extensos, se torna necessário além das boas práticas a utilização de alguns padrões de projeto para facilitar o entendimento e manutenção do código-fonte.
No projeto foi utilizado PageObject com o objetivo de reduzir o acoplamento entre os casos de testes e aplicação a ser testada, dividindo assim as responsabilidades corretamente.
Escolha do teste

Para a terceira parte do desafio foi escolhido o cenário de realizar login para ser codificado.

Execução dos testes
Os testes podem ser executados da seguinte forma :
Por Cenário:

Para executar os testes do cenário positivo, basta acessar a pasta raiz do projeto utilizando o prompt e digitar:

robot -d ./logs -i positive ./tests

Para executar os testes do cenário negativo, basta acessar a pasta raiz utilizando o prompt e digitar:

robot -d ./logs -i negative ./tests


Por nome da feature:

Para executar apenas uma feature, basta acessar a pasta tests utilizando o prompt e digitar:

robot -d ../logs nome_feature.robot


Todos os testes:

Para executar todos os testes,basta acessar a pasta raiz utilizando o prompt e digitar:
robot -d ./logs tests

Testes Não funcionais
Visando garantir a qualidade da aplicação foram executados testes de acessibilidade utilizando a ferramenta Wave onde foi identificado alguns pontos de melhoria:

Evidencia 1
Evidência 2
Evidência 3
Evidência 4

Também foi utilizado o PageSpeed Insights para avalidar a conformidade da página com as práticas recomendadas comuns para o desempenho, seguem as evidências:
Mobile

Evidencia 1
Evidência 2

Desktop

Evidência 1
Evidência 2

Observações
Caso houvesse mais tempo para entrega do desafio, poderia ser executado um teste de  performance na aplicação, porém a equipe de Infra deveria ser avisada com antecedência para que a execução do teste não impacte na disponibilidade da aplicação.
