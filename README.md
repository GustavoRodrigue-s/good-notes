<div>
  <h1 style="color: skyblue;">good-notes</h1>
  <p>
    The good notes project is a simple and functional notes web application.
  </p>
  <blockquote>
    The link to access it's: <a href="https://good-notes-app.herokuapp.com">good notes</a>
  </blockquote>
</div>

<div>
  <strong>Attention!! The good notes is not a "real application", good notes is just a project.</strong>
</div>

<div>
  <h2>Readme languages</h2>
  <div>
    <a href="#" style="cursor: pointer; color: skyblue;">English</a>
  </div>
  <div>
    <a href="#" >Portuguese</a>
  </div>
</div>

<div>
  <div>
    <h2>About the project</h2>
    <h3>What is purpose?</h3>
    <p>
      Initially it was to learn about <code>Javascript</code> and how the flow of a "real application" works, however i learned a lot more than i expected. For these reasons, i would like to share about the project study and development process.
    </p>
    <p>
      <strong>For educational reasons and because this was my first "big" application, i didn't use any library that provided me with ready-made stuff.</strong>
    </p>
    <h3>Main Features</h3>
    <dl>
      <dt>Short explanation</dt>
      <dd>
        <p>
          With <em>good notes</em> you can create an account and store your notes by organizing them into categories.
        </p>
      </dd>
      <dt>Technical explanation</dt>
      <dd>
        <p>
          In this project we have three entities, user, category and note. For each one, we have a <code>CRUD</code> (Create, Read, Update, Delete), this entities are related, that's why we use <code>SQL</code> (Structured Query Language; Used to relate tables).
        </p>
        <p>
          To keep everything organized, we use <code>MVC</code> (Model View Controller) in the backend, <code>Factory</code> and <code>Observer</code> patterns in the frontend (More details about the software architecture will be cited bellow).
        </p>
      </dd>
    </dl>
  </div>
</div>

<div>
  <h2>Repositories</h2>
  <blockquote>
    The links to access the repositories are:
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
  <h2>Technologies and services used 🛠️</h2>
  <div>
    <h3>Front-end (Client side)</h3>
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
    <h3>Back-end (Server side)</h3>
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
  <h2>Why use all this?</h2>
  <div>
    <p>
      On the frontend, <code>HTML</code>, <code>CSS</code> and <code>JS</code> are used to build all interfaces. The <code>Serve</code> library is used to create a static server on <code>Heroku</code> (heroku only allows you to deploy a repository if it is a server).
    </p>
    <p>
      On the backend, i'm using <code>Python</code> as main language (but today i would use <code>Node.js</code>). <code>Flask</code> is a framework used to create APIs (Application Programming Interface, are used to create communication points between the frontend and backend in an application).
    </p>
    <p>
      <code>Heroku</code> is a hosting service used to "go up" an application (create a domain, ex: https://github.com), so everyone can access it. <code>Cloudinary</code> is a simple service used to store images. <code>PostgreSQL</code> is a relational database used to store system and user information.
    </p>
  </div>
</div>

<div>
  <h2>Authentication</h2>
  <p>
    For the server to identify each user, between various authentication types i chose <code>JWT</code> (Json Web Token) authentication. The <strong>access token</strong> allows the main actions, <strong>refresh token</strong> can create new <strong>access token</strong> and <strong>emailConfirmation token</strong> allows and autorizes all email actions.
  </p>
</div>

<div>
  <h2>Architecture</h2>
  <p>
    An organized and architected project makes your code more readble, scalable and maintainable. I "suffered" a lot until understood that i need an achitecture. For these reasons i used the MVC (Model View Controller), factory and observer pattern. 
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

  <p><strong>Important</strong>: It is not always good to use the observer pattern, because this pattern adds a (sometimes unnecessary) complexity that is considered "over engineering". For these reasons, i don't use it on every layer.</p>
</div>

<div>
  <h2>Important Details</h2>
  <p>
    All sensitive keys are hidden in the .env file and all error handling like database connection and user actions are implemented. Other basic security implementations such as database password encryption were also introduced.
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
          The rich text is a <em>good notes</em> feature used to edit notes but this feature is limited, because it was created with pure <code>Javascript</code> and the only way to make a rich text is using the execCommand method of the document (this method is deprecated). To solve this problem i would add a rich text library, so the rich text would have more functionality and would also improve the user experience.
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

