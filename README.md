## Styleguide

### 1. Linter

Por mais que existam diversos styleguides, nós utilizamos o [StandardJS](https://standardjs.com/). É simples, não tem configuração e formata seu código _automagicamente_. Caso você queira integrar com o seu editor de código favorito, [aqui tem uma lista de opções](https://standardjs.com/#are-there-text-editor-plugins).

### 2. Typescript

A tipagem do javascript é essencial para mantermos projetos de grande porte. Nossos boilerplates já entregam a configuração necessária para o melhor funcionamento do TS.

### 3. Testes
>TODO

### 4. Camadas definidas

As camadas de renderização e dados externos (APIs) são isoladas. O middleman para conectar as duas é o `redux-saga`

### 5. Redux

Usamos `redux-sagas` e seguimos [`ducks-modular-redux`](https://github.com/erikras/ducks-modular-redux). Pra reduzir o boilerplate, preferimos o `reduxsauce`.

### 6. Functional Programming

Utilizar sempre que possível os conceitos de **Functional Programming** (FP). Estamos migrando nosso mindset para uma codebase 100% funcional. Em caso de dúvidas, [consulte esse link](https://medium.com/dailyjs/functional-js-1-introduction-7908bfe5ef8d).


### 7. Formatação de arquivos

Limitamos nossos arquivos a 80 colunas e, sempre que possível, até 50 linhas. Essas duas regras facilitam a escrita e leitura do código.

### 8. Estrutura do projeto
>WIP
```
.
├── 📄 index.js
├── 📄 package.json
├── ...
└── 📁 src
    ├── 📁 assets
    │   ├── 📁 images
    │   │   └── 📄 logo.png
    │   │
    │   └── 📁 svg
    │       └── 📄 tree.svg
    │
    ├── 📁 app
    │   ├── 📁 components
    │   │   └── 📁 Button
    │   │       ├── 📄 index.ts
    │   │       ├── 📄 Button.tsx
    │   │       ├── 📄 Button.story.ts
    │   │       └── 📄 ButtonInterface.ts
    │   │
    │   └── 📁 screens
    │       └── 📁 Home
    │           ├── 📄 index.ts
    │           ├── 📄 Home.tsx
    │           └── 📄 HomeInterface.ts
    │
    ├── 📁 config
    │   ├── 📁 router
    │   │   ├── 📄 index.ts
    │   │   ├── 📄 router.ts
    │   │   └── 📄 routeList.ts
    │   │
    │   └── 📁 themes
    │       ├── 📄 index.ts
    │       ├── 📄 MyTheme.ts
    │       ├── 📄 AnotherTheme.ts
    │       └── 📄 ThemeInterface.d.ts
    │
    ├── 📁 core
    │   ├── 📁 redux
    │   │   ├── 📁 reducers
    │   │   │   ├── 📄 index.ts
    │   │   │   └── 📄 products.ts
    │   │   │
    │   │   ├── 📁 sagas
    │   │   │   ├── 📄 index.ts
    │   │   │   └── 📄 products.ts
    │   │   │
    │   │   └── 📁 store
    │   │       └── 📄 index.ts
    │   │
    │   └── 📁 services
    │       └── 📁 API
    │           ├── 📄 index.ts
    │           └── 📄 someEndpoint.ts
    │
    └── 📁 utils
        └── 📁 foo
            ├── 📄 foo.ts
            └── 📄 index.ts
```

### 9. Pacotes

Pacotes javascript que usamos em praticamente todos os projetos:

* `formik`: Gestão de formulários;
* `formik-enhancer`/`coreui-formik-enhancer`: Automações para o `formik`;
* `yup`: Validação de formulários (e outros objetos);
* `ramda`: Canivete suíço de funções para arrays e objetos;
* `date-fns`: Manipulação de datas;
* `react-toastify`: Notificações.
