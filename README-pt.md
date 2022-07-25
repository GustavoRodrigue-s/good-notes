
<div>
  <h1 style="color: skyblue;">good-notes</h1>
  <p>
    O projeto good notes é uma aplicação web de notas simples e funcional.
  </p>
  <blockquote>
    O link para acessá-lo é: <a href="https://good-notes-app.herokuapp.com">good notes</a>
  </blockquote>
</div>

<div>
  <strong>Atenção!! O good notes não é uma "aplicação real", o good notes é apenas um projeto.</strong>
</div>

<div>
  <h2>Idiomas do Readme</h2>
  <div>
    <a href="https://github.com/GustavoRodrigue-s/good-notes/blob/main/README.md" style="cursor: pointer; color: skyblue;">English</a>
  </div>
  <div>
    <a href="https://github.com/GustavoRodrigue-s/good-notes/blob/main/README-pt.md" >Portuguese</a>
  </div>
</div>

&nbsp;

<div>
  <img src="http://img.shields.io/static/v1?label=Status&message=Finished&color=green&style=flat" />
</div>

<div>
  <div>
    <h2>Sobre o projeto</h2>
    <h3>Qual é o propósito?</h3>
    <p>
      Inicialmente foi em aprender <code>Javascript</code> e como funciona o fluxo de uma "aplicação real", porém eu aprendi mais do que eu esperava. Por esses motivos, eu gostaria de compartilhar sobre o processo de estudo e desenvolvimento do projeto.
    </p>
    <p>
      <strong>Por motivos educacionais e por ser a minha primeira aplicação "grande", eu não usei nenhuma biblioteca que me fornecesse coisas prontas.</strong>
    </p>
    <h3>Funcionalidades Principais</h3>
    <dl>
      <dt>Explicação curta</dt>
      <dd>
        <p>
          Com o <em>good notes</em> você pode criar uma conta e armazenar suas notas organizando-as em categorias.
        </p>
      </dd>
      <dt>Explicação técnica</dt>
      <dd>
        <p>
          Neste projeto nós temos três entidades, usuário, categoria e nota. Para cada um, nós temos um <code>CRUD</code> (Create, Read, Update, Delete), essas entidades estão relacionadas, é por isso que nós usamos o <code>SQL</code> (Structured Query Language; Usado para relacionar tabelas).
        </p>
        <p>
          Para manter tudo organizado, eu utilizo o <code>MVC</code> (Model View Controller) no backend, padrões de <code>Factory</code> e <code>Observer</code> no frontend (Mais detalhes sobre arquitetura de software serão citados abaixo).
        </p>
      </dd>
    </dl>
  </div>
</div>

<div>
  <h2>Repositórios</h2>
  <blockquote>
    Os links para acessar os repositórios são:
    <div>
      <a href="https://github.com/GustavoRodrigue-s/good-notes-frontend">good-notes-frontend</a>
    </div>
    <div>
      <a href="https://github.com/GustavoRodrigue-s/good-notes-backend">good-notes-backend</a>
    </div>
  </blockquote>
</div>

&nbsp;

<div>
  <img src="https://user-images.githubusercontent.com/81722068/179663448-29abe138-01c8-48fd-bbe9-d1183490db6b.png" />
</div>

&nbsp;

<div>
  <h2>Tecnologias e serviços usados 🛠️</h2>
  <div>
    <h3>Front-end (Lado do cliente)</h3>
    <ul>
      <li style="vertical-align: middleware;">
        HTML5 & CSS3
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original-wordmark.svg" width="30" />
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original-wordmark.svg" width="30" />
      </li>
      <li>
        Javascript
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" width="20" />
      </li>
      <li>Api (Backend)</li>
      <li>Serve</li>
    </ul>
    <h3>Back-end (Lado do servidor)</h3>
    <ul>
      <li>
        Python
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="20" />
      </li>
      <li>Flask</li>
    </ul>
    <h3>Cloud (Storage)</h3>
    <ul>
      <li>
        Heroku
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/heroku/heroku-plain.svg" width="20" />
      </li>
      <li>Cloudinary</li>
       <li>
        PostgreSQL
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" width="20" />
      </li>
    </ul>
  </div>
</div>

<div>
  <h2>Por que usar tudo isso?</h2>
  <div>
    <p>
      No frontend, <code>HTML</code>, <code>CSS</code> e <code>JS</code> são usados para contruir todas as interfaces. A biblioteca <code>Serve</code> é usada para criar um servidor estático no <code>Heroku</code> (heroku só permite fazer deploy de um repositório se ele é um servidor).
    </p>
    <p>
      No backend, eu estou usando <code>Python</code> como linguagem principal (mas hoje eu usaria o <code>Node.js</code>). <code>Flask</code> é um framework usado para criar APIs (Application Programming Interface, são usados para criar pontos de comunicação entre o frontend e o backend em uma aplicação).
    </p>
    <p>
      <code>Heroku</code> é um serviço de hospedagem usado para "subir" uma aplicação (cria um dominio, ex: https://github.com), assim todos podem acessá-lo. <code>Cloudinary</code> é um simples serviço usado para armazenar imagens. <code>PostgreSQL</code> é um banco de dados relacional usado para armazenar informações do usuário e do sistema.
    </p>
  </div>
</div>

<div>
  <h2>Autenticação</h2>
  <p>
    Para o servidor indentificar cada usuário, entre vários tipos de autenticação eu escolhi a autenticação via <code>JWT</code> (Json Web Token). O <strong>access token</strong> permite as ações principais, <strong>refresh token</strong> pode criar um novo <strong>access token</strong> e <strong>emailConfirmation token</strong> permite e autoriza todas as ações de email.
  </p>
</div>

<div>
  <h2>Arquitetura</h2>
  <p>
    Um projeto organizado e arquitetado deixa seu código mais legível, escalável e manutenível. Eu "sofri" muito até entender que eu precisava de uma arquitetura. Por esses motivos eu usei os padrões de <strong>MVC</strong> (Model View Controller), <strong>factory</strong> e <strong>observer</strong>. 
  </p>
  <p>
    <code>M</code> O model é um representação de entidade, responsável por armazenar as regras de negócio e as consultas no banco de dados.
  </p>
  <p>
    <code>V</code> A view é a interface do cliente, responsável por fazer a comunicação entre o usuário e o <strong>model</strong>.
  </p>
  <p>
    <code>C</code> O controller é um intermediário entre a <strong>view</strong> e o <strong>model</strong>, responsável por autorizar a <strong>view</strong> à acessar a ação do <strong>model</strong>.
  </p>
  
  &nbsp;
  
  <p>Com a factory, nós podemos criar uma camada (representa um componente da interface) e com o observer você consegue separar essas camadas.</p>
  
  <h3>Camada de exemplo com a factory:</h3>
  
  <img src="https://user-images.githubusercontent.com/81722068/180630295-399d2183-0538-42bf-a178-bd05d1b6f1d7.png" />

  <p>O state armazena os valores globais da camada. Criando camadas como esta, nós podemos organizar os valores e funções privadas e públicas.</p>

  <h3>Camada de exemplo com a factory e observer:</h3>

  <img src="https://user-images.githubusercontent.com/81722068/180630756-8b6450f9-5060-4b36-ab22-b8979272cab3.png" />

  <p>Toda vez que o state do contador atualizar, todos os observadores do contador são notificados. Assim nós podemos desacoplar/separar as camadas, melhorando o controle e manutenção do código.</p>

  <p><strong>Importante</strong>: Não é sempre que é bom usar o <strong>observer pattern</strong>, porque este padrão adiciona um complexidade (as vezes desnecessária) que é considerada <em>"over engineering"</em>. Por esses motivos, eu não uso em toda camada.</p>
</div>

<div>
  <h2>Detalhes Importante</h2>
  <p>
    Todas as chaves sensíveis estão escondidas no arquivo <code>.env</code> e todos os tratamento de erros como a conexão com o banco de dados e ações de usuários estão implementadas. Outras implementações básicas de segurança tal como criptografia de senha no banco de dados também foram introduzidas.
  </p>
</div>


<div>
  <h2>Possíveis Melhorias</h2>
  <p>
    Em tudo que nós fazemos, sempre há uma maneira de melhorar e este projeto não é diferente, aqui estão algumas melhorias que eu faria caso eu fosse refaze-lo.
  </p>
  <ul>
    <li>
      <div>
        <span>Rich Text</span>
        <p>
          O rich text é uma funcionalidade do <em>good notes</em> usado para editar notas mas essa funcionalidade é limitada, porque ela foi criada com <code>Javascript</code> puro e o única maneira de fazer um rich text é usando o método <em>execCommand</em> do <em>document</em> (este método está obsoleto). Para resolver este problema eu adicionaria uma biblioteca de rich text, assim o rich text teria mais funcionalidades e também melhoraria a experiência do usuário.</p>
      </div>
    </li>
    <li>
      <div>
        <span>Migrar para React.js</span>
        <p>
          Eu adicionaria o <code>React.js</code> para melhorar o desenvolvimento, escalabilidade e produtividade.
        </p>
      </div>
    </li>
    <li>
      <div>
        <span>Filtros e Customizações de Categorias</span>
        <p>
          Talvez seria interessante adicionar filros de categorias e mais curstomizações, também melhorando a experiência do usuário.
        </p>
      </div>
    </li>
    <li>
      <div>
        <span>Paginação de Categorias e Notas</span>
        <p>
          Para melhorar a carregamento das categorias e notas, eu adicionaria uma paginação de até 15 itens, reduzindo a quantidade de tráfico no primeiro carregamento. 
        </p>
      </div>
    </li>
  </ul>
</div>

<div>
  <h2>Obrigado por Ler!</h2>
  <p>
    Muito obrigado por ler até aqui! Eu espero que isso ajude muitas pessoas, talvez com inspiração, aprendizado ou qualquer coisa. See you later. 👋
  </p>
</div>
