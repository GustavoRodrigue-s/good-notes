
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
  <h2>Readme Idiomas</h2>
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
      <strong>Por motivos educacionais e porque este é minha primeira aplicação "grande", eu não usei nenhuma biblioteca que me fornecesse coisas prontas.</strong>
    </p>
    <h3>Funcionalidades Principais</h3>
    <dl>
      <dt>Explicação curta</dt>
      <dd>
        <p>
          Com o <em>good notes</em> você pode criar uma conta e armazenar suas anotas organizando-as em categorias.
        </p>
      </dd>
      <dt>Explicação técnica</dt>
      <dd>
        <p>
          Neste projeto nós temos três entidades, usuário, categoria e nota. Para cada um, nós temos um <code>CRUD</code> (Create, Read, Update, Delete), essas entidades estão relacionadas, é por isso que nós usamos o <code>SQL</code> (Structured Query Language; Usado para relacionar tabelas).
        </p>
        <p>
          Para menter tudo organizado, nós usamos o <code>MVC</code> (Model View Controller) no backend, padrões de <code>Factory</code> e <code>Observer</code> no frontend (Mais detalhes sobre arquitetura de software serão citados abaixo).
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
    Para o servidor indentificar cada usuário, entre vários tipos de autenticação eu escolhi a autenticação via <code>JWT</code> (Json Web Token). O <strong>access token</strong> permite as ações principais, <strong>refresh token</strong> pode criar um novo <strong>access token</strong> e <strong>emailConfirmation token</strong> permite e altoriza todas as ações de email.
  </p>
</div>

<div>
  <h2>Architecture</h2>
  <p>
    An organized and architected project makes your code more readble, scalable and maintainable. I "suffered" a lot until understood that i need an achitecture. For these reasons i used the <strong>MVC</strong> (Model View Controller), <strong>factory</strong> and <strong>observer</strong> pattern. 
  </p>
  <p>
    <code>M</code> The model is an entity representation, responsible for storing business rules and database queries.
  </p>
  <p>
    <code>V</code> The view is the client interface, responsible for makes to communication between the user and the <strong>model</strong>.
  </p>
  <p>
    <code>C</code> The controller is an intermediary between the <strong>view</strong> and the <strong>model</strong>, responsible for autorizing the <strong>view</strong> to access the <strong>model</strong> action.
  </p>
  
  &nbsp;
  
  <p>With factory, we can create a layer (represents an application component) and with observer you can separate these layers.</p>
  
  <h3>Layer example with factory:</h3>
  
  <img src="https://user-images.githubusercontent.com/81722068/180630295-399d2183-0538-42bf-a178-bd05d1b6f1d7.png" />

  <p>The state stores the layer's global values. Creating layers like this, we can organize what are the private and public values and functions.</p>

  <h3>Layer example with factory and observer:</h3>

  <img src="https://user-images.githubusercontent.com/81722068/180630756-8b6450f9-5060-4b36-ab22-b8979272cab3.png" />

  <p>Every time the counter state is updated, all counter observers are notified. So we can decouple/separate the layers, improving code control and maintainability.</p>

  <p><strong>Important</strong>: It is not always good to use the <strong>observer pattern</strong>, because this pattern adds a (sometimes unnecessary) complexity that is considered <em>"over engineering"</em>. For these reasons, i don't use it on every layer.</p>
</div>

<div>
  <h2>Important Details</h2>
  <p>
    All sensitive keys are hidden in the <code>.env</code> file and all error handling like database connection and user actions are implemented. Other basic security implementations such as database password encryption were also introduced.
  </p>
</div>


<div>
  <h2>Possible Improvements</h2>
  <p>
    In everything we do, there is always a way to improve and this project is no different. Here are some improvements i would make if i were to redo it.
  </p>
  <ul>
    <li>
      <div>
        <span>Rich Text</span>
        <p>
          The rich text is a <em>good notes</em> feature used to edit notes but this feature is limited, because it was created with pure <code>Javascript</code> and the only way to make a rich text is using the <em>execCommand</em> method of the <em>document</em> (this method is deprecated). To solve this problem i would add a rich text library, so the rich text would have more functionality and would also improve the user experience.
        </p>
      </div>
    </li>
    <li>
      <div>
        <span>Switch to React.js</span>
        <p>
          I would add <code>React.js</code> to increase development scalability and productivity.
        </p>
      </div>
    </li>
    <li>
      <div>
        <span>Category Filters and Customizations</span>
        <p>
          Maybe it would be interesting to add category filters and more customizations, also improving the user experience.
        </p>
      </div>
    </li>
    <li>
      <div>
        <span>Pagination of Categories and Notes</span>
        <p>
          For improving categories and notes loadings, i would add a pagination of up to 15 items, reducing the amount of traffic on the first load. 
        </p>
      </div>
    </li>
  </ul>
</div>

<div>
  <h2>Thanks for Reading</h2>
  <p>
    Thank you so much for reading this far! I hope this helps a lot of people, maybe with inpiration, learning or something else. See you later. 👋
  </p>
</div>
