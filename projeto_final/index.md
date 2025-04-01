---
title: Projeto Final
has_children: true
has_toc: true
prazo_proposta: 14/09/2023
prazo_modelagem: 10/10/2023
prazo_codigo: 26/11/2023
formulario_proposta: https://forms.gle/txEbZAkWUZxXEvrJ7
---

# Projeto Final

* [Objetivos](#obj)
* [Requisitos mínimos](#req)
* [Critérios de avaliação](#criterios)
* [Entregas](#entregas)
  * [Proposta](#proposta)
  * [Configurando o backend](#back01)
  * [API REST de Usuários](#back02)
  * [Salvando as informações no banco de dados](#back03)
  * [Autenticação e Autorização](#back04)
  * [Página de login e cadastro](#front01)
  * [Protegendo rotas no front](#front02)
  * [Entrega final](#final)
* [Apresentação do projeto](#apresentacao)

---

## Objetivo <a name="obj"></a>

Desenvolver uma aplicação web completa que inclua tanto o **frontend** quando o **backend**.
O **backend** será desenvolvido utilizando **Node.js e Express** para criar uma **API REST**, 
enquanto o **frontend** será construído em **Vue.js**.

O trabalho pode ser feito em equipe
{: .label .label-blue }

## Requisitos mínimos <a name="req"></a>


### Frontend

- O **frontend** deve ser uma **SPA – Single Page Application** e sua página principal deve exibida automaticamente ao acessar a raiz da aplicação (**/**).
- O **frontend** da aplicação web deve ser implementado utilizando a **Composition API** do **Vue** com Vite.
 
Não serão aceitos trabalhos implementados usando **Option API**.  Para mais detalhes  <a href="https://medium.com/@victor.souza2210/vue-js-composition-api-vs-options-api-qual-abordagem-escolher-a50a2f2f932b" target="_blank">leia este artigo</a>.
{: .label .label-red }

- O **frontend** da aplicação web deve ser implementado fazendo **OBRIGATORIAMENTE** uso das bibiliotecas **VueRouter** e **Pinia**. 
  - As rotas do frontend não podem ser todas públicas.

Não serão aceitos trabalhos implementados usando VUEX.
{: .label .label-red }

- O fronted deve ser **modularizar os trechos de HTML usados em várias páginas**. 
    - Exemplo: Deixar cabeçalho e rodapé em arquivos separados e incluí-los nas páginas onde serão necessários.



### Backend

- O **backend** (API REST) com o qual a sua aplicação deve se comunicar deve ser construído utilizando o <a href="https://expressjs.com/" target="_blank">Express</a>.
- O **backend** deverá ter pelos um endpoint com paginação
- O **backend** deverá ter pelos um endpoint com opção de filtragem
- O **backend** deve forncener um serivço de autenticação e autorização via **JWT**. 
- Os dados da aplição devem ser armezandos em um banco de dados **SQLITE**.
 
 
### Conjunto da obra
- A sua aplicação deve possuir pelo menos ***x* entidades (tabelas)**, onde :
<div>
\[x =
  \begin{cases}
    3       & \quad \text{quando o trabalho for individual }\\
   n + 1  & \quad \text{para trabalhos em equipe onde } n \text{ é o tamanho da equipe}
  \end{cases}
\]
</div>

- A aplicação deve implementar os CRUDs de pelo menos **DUAS** dessas tabelas.
  - **Uma das entidades deve ser dependende da outra**, os CRUDs não podem ser totalmente independentes 
  - Para trabalhos em equipe com **mais de dois membros**, as regras de negócio serão avaliada para verificar a elegibilidade do projeto.
- A aplicação deve possuir pelo menos **3 papéis de usuários** de forma que todos os **papéis** possuam permissões diferentes.
- A aplicação deve possuir uma **área pública com páginas/serviços acessíveis a todos; e uma área restrita com páginas/serviços acessíveis somente a usuários autenticados**.
  - A página de login e cadastro de usuários não é considerada uma área pública nessa contexto.

### Atenção
  
O código do projeto que vai ser desenvolvido deve ser hospedado no <a href="http://www.github.com" target="_blank">GitHub</a>.
{: .label .label-yellow }

Caso o trabalho seja feito em equipe, cada membro da equipe deve usar seu próprio usuário para escrever código.
{: .label .label-yellow }

Não serão aceitos trabalhos implementados em um único commit.
{: .label .label-red }

TODOS os membros da equipe devem se envolver em atividades que incluem a ESCRITA de código HTML, CSS e principalmente JavaScript ou TypeScript.
{: .label .label-red }

## Critérios de avaliação <a name="criterios"></a>

- Implementação correta e completa dos requisitos funcionais definidos
- Utlização adequada dos conceitos e tecnologias discutidos ao longo do curso
- Boas práticas de desenvolvimento, incluindo organização do código, padrões de nomenclatura, e legibilidade
- Funcionalidade e desempenho da aplicação
- Qualidade da apresentação do trabalho

---

## Entregas

Com o intuito de tentar acompanhar o desenvolvimento do projeto final, X entregas são previstas.

### Entrega 00:  Envio da proposta <a name="proposta"></a>

O envio da proposta deve ser feita via SIGAA.

<!--
O autor do trabalho ou a equipe, deve escolher o domínio da aplicação, ex: um loja online de doces, e também deve descrever as funcionalidades do sistema, explicando **resumidamente os requisitos do sistema com suas entidades principais**. Essa definição deve ser enviada e **aprovada pelo professor**. 

Para auxiliar nessa tarefa, vocês irão realizar criar um repositório no GitHub a partir deste <a href="https://github.com/profBruno-UFC-Qx/qxd0020-projeto-final/generate" target="_blank">template</a>. Como vocês podem ver, o **Readme.md** já vem previamente preenchido com um modelo. 
Vocês devem alterar o modelo de acordo com a realidade da proposta de projeto final de vocês. Vocês podem consultar <a href="https://github.com/profBruno-UFC-Qx/qxd0020-manga-store" target="_blank">o repositório da MangaStore</a>.

Depois disso, a proposta deve ser enviada por meio do seguinte <a href="{{ page.formulario_proposta }}" target="_blank">formulário</a>.

Prazo final de entrega: {{ page.prazo_proposta }}
{: .label .label-red }

Os trabalhos devem necessariamente ter domínios distintos. 
{: .label .label-yellow }

A ordem de envio para o professor determina quem tem prioridade por determinado domínio. Caso o domínio já tenha sido escolhido por outro aluno, deve-se propor um novo domínio.
{: .label .label-yellow }

## Modelagem e rascunho da interface <a name="envio2"></a>

É esperado que nesse momento, a equipe já tenha em mente de forma clara as principais funcionalidades do sistema e para isso, é necessário que os dados estejam devidamente modelados.

A entrega da modelagem deve ser feita de duas formas:
  - Um digrama entidade relacional ou um diagrama de classes que deixe claro como as entidades se relacionam
  - A "implementação" dessa modelagem utilizando **Strapi**.

Com uma visão clara das funcionalidades do projeto, a equipe deve também entregrar a primeira versão das telas do sistemas. Estas telas devem ser construídas usando HTML, CSS e JavaScript (ou TypeScript). Como são primeiras versões, dados fictícios devem/podem ser utilizados.

No prazo final da entrega, todo esse conteúdo deve estar presente no repositório do GitHub do projeto final, enviado juntamente com a proposta do projeto final.
{: .label .label-yellow }


Prazo final de entrega: {{ page.prazo_modelagem }}
{: .label .label-red }

-->

### Entrega 01: Projeto do backend configurado com TypeScript <a name="back01"></a>

Nesta entrega você deve atualizar o repositório do seu projeto final adicionado uma pasta chamada **backend**.
Você deve fazer com que esta pasta seja um projeto **Nodejs** configurado para o uso do framework **Express**.
É importante que este projeto esteja configurado para fazer o uso de **TypeScript**. 

Nesta etapa o seu backend deve responder a qualquer requisição da mesma forma. A resposta deve conter
um código HTML, que contém a descrição do seu projeto final e os nomes dos autores.

<span class="label label-blue">Vale 0.5 pontos</span> <span class="label label-red">Data de entrega: 23/07/24 às 6:00</span>

### Entrega 02: API REST de usuários <a name="back02"></a>

Nesta entrega você deve atualizar o backend de forma que ele forneça uma API REST para entidade usuário.
Portanto, ela deve fornecer ENDPOINT capazes de:
  - Listar usuários
  - Criar usuários
  - Atualizar usuários
  - Remover usuários

É importante que você implemente as regras de negócio referente a usuários, ex: campos obrigatórios, papéis de usuário, dentre outros.

Nesta entrega ainda não faremos o uso de um banco de dados. Logo, você pode simular o banco de dados guardando os dados em um JSON.

<span class="label label-blue">Vale 1 ponto</span> <span class="label label-red">Data de entrega: 05/08/24 às 6:00</span>

### Entrega 03: Salvando as informações no banco de dados <a name="back03"></a>

Nesta entrega você deve alterar o **backend** da sua aplicação de forma que ele passe a guardar as informações de usuários em
um banco de dados **SQLITE**. Para isso você deve fazer uso de um **ORM - Object Relational Mapping**.

Em termos de funcionalidade, o seu backend continuará igual a versão da entrega anterior, porém agora ele estará realmente persistindo os dados da aplicação.

<span class="label label-blue">Vale 1 ponto</span> <span class="label label-red">Data de entrega: 12/07/24 às 6:00</span>

### Entrega 04: Autenticação e Autorização <a name="back04"></a>

Nesta entrega você deverá configurar o seu **backed** para que ele seja capaz de autenticar e posteriormente autorizar usuários
por meio da tecnologia **JWT - Json Web Token**.  Com isso você deve alterar a API do backend para que:
  - Os ENDPOINT de **criar usuário, listar usuários, remover usuários** sejam acessíveis somente para usuários **adminstradores**.
  - Os ENDPOINT de **atualizar usuário e listar um usuário** devem ser acessíveis somente para **usuários autenticados**. No entanto, **Um usuário não administrador  só pode atualizar o seu próprio cadastro.**

<span class="label label-blue">Vale 1 ponto</span> <span class="label label-red">Data de entrega: 26/08/24 às 6:00</span>


<!--
### Entrega 05: Regras de negócios implementadas <a name="back05"></a>

Em teoria essa é devem a última entrega do backend, portanto, ao final desta entregas todas as regras de negócios necessárias para que sua aplicação funcione corretamente devem ser implementadas.
É natural que ao longo do desenvolvimento do **frontend**, sejam necessária realizar algumas mudanças no **backend**, portanto não se preocupe com isso.

<span class="label label-blue">Vale 1 ponto</span>
-->

### Entrega 05: Página de login e cadastro <a name="front01"></a>

Esta deve ser a primeira entrega do **frontend** que já deve ser integrado ao **backend**. Nesta entrega você deve criar a página principal da aplicação,
que inicialmente pode conter apenas dados fictícios e possuir uma aparência bem simples. Além disso, você deve criar a página que vai permitir
que usuários se cadastrem na sua aplicação e a página de login. Ambas deve estar completamentes funcionais ao final da entrega.

<span class="label label-blue">Vale 1 ponto</span>

### Entrega 06: Protegendo rotas no front <a name="front02"></a>

Nesta entrega você deve utilizar o **VueRouter** de modo que algumas rotas sejam acessíveis somente para usuários com um certo papel.
Ex: rota /usuarios, acessível somente para usuários adminstradores. Importante, a página protegida pelo **VueRouter** não precisa estar funcional,
o objetivo aqui é verificar se o uso do **VueRouter** está correto.

<span class="label label-blue">Vale 1 ponto</span>


## Entrega final <a name="final"></a>

Antes de enviar o seu projeto para a avaliação será necessário realizar o preenchimento do restante do arquivo **README.md** do seu projeto.
Para facilitar a sua vida, apenas altere a segunda parte do **README.md** disponibilizado como template. Além disso, é preciso enviar asInformações 
sobre como utilizar o sistema, além de nomes de usuários e senhas devem ser enviadas por email para que eu possa testar o sistema.

### Atenção

Projetos que não disponibilizarem no README.md as informações acima serão desconsiderados.
{: .label .label-red }

Não serão aceitos trabalhos implementados em um único commit.
{: .label .label-red }

Não serão aceitos trabalhos enviados em formato compactados, ex: zip, rar e similares
{: .label .label-red }

### Apresentação do trabalho <a name="apresentacao"></a>

O trabalho também deverá necessariamente ser apresentado conforme cronograma da disciplina. A não apresentação do trabalho pelo aluno em sua anulação.
{: .label .label-red }
