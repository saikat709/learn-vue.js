# Creating a Vue.js Project Guide

## Method 1: Using Vite

```bash
npm create vue@latest
```
```bash
Follow the CLI prompts:
- Project name
- Add TypeScript? (Yes/No)
- Add JSX Support? (Yes/No)
- Add Vue Router? (Yes/No)
- Add Pinia? (Yes/No)
- Add Vitest? (Yes/No)
- Add End-to-End Testing? (Yes/No)
- Add ESLint? (Yes/No)
- Add Prettier? (Yes/No)
```
Then:
```bash
cd <your-project-name>
npm install
npm run dev
```

## Method 2: Using Vue CLI (Legacy)

```bash
npm install -g @vue/cli
vue create my-project
```

## Project Structure Explained

```
my-vue-project/
├── public/                 # Static assets that won't be processed by Vite/Webpack
│   ├── favicon.ico
│   └── index.html
│
├── src/                    # Source code
│   ├── assets/            # Images, fonts, etc.
│   │   └── logo.png
│   │
│   ├── components/        # Reusable Vue components
│   │   ├── Header.vue
│   │   └── Footer.vue
│   │
│   ├── views/             # Page components
│   │   ├── Home.vue
│   │   └── About.vue
│   │
│   ├── router/            # Vue Router configuration
│   │   └── index.js
│   │
│   ├── store/             # Pinia/Vuex store
│   │   └── index.js
│   │
│   ├── App.vue           # Root component
│   └── main.js           # Application entry point
│
├── .gitignore            # Git ignore rules
├── index.html            # Entry HTML file
├── package.json          # Project dependencies and scripts
├── README.md            # Project documentation
├── vite.config.js       # Vite configuration
└── env.d.ts             # Environment variables types (if using TS)
```

## Key Files Explained

- `index.html`: The main HTML file where your app is mounted
- `src/App.vue`: The root Vue component
- `src/main.js`: Where you initialize your Vue application
- `src/router/index.js`: Defines your application routes
- `src/store/index.js`: Manages your application state
- `components/*.vue`: Reusable components across your application
- `views/*.vue`: Page-level components

## Common Commands

```bash
# Development
npm run dev          # Start development server

# Production
npm run build        # Build for production
npm run preview      # Preview production build

# Testing (if configured)
npm run test:unit    # Run unit tests
npm run test:e2e     # Run end-to-end tests

# Linting
npm run lint         # Lint and fix files
```

## Best Practices

1. **Component Organization**
   - Use PascalCase for component names
   - Keep components focused and single-purpose
   - Use the composition API for new projects

2. **File Naming**
   - Use kebab-case for file names
   - Match component names with their filenames

3. **State Management**
   - Use Pinia for simpler state management
   - Use Vuex for more complex applications

4. **Routing**
   - Keep route names consistent
   - Use lazy loading for routes