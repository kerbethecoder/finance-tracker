# ✨ Front-End

For front-end, I'd like to have these two for linting.

- **[ESLint](https://eslint.org/)**. It statically analyzes your code to quickly find problems.
- **[Prettier](https://prettier.io/)**. It is an opinionated code formatter.

Packages:

- `eslint` <small>[source](https://www.npmjs.com/package/eslint)</small>
- `prettier` <small>[source](https://www.npmjs.com/package/prettier)</small>
- `eslint-plugin-prettier` <small>[source](https://www.npmjs.com/package/eslint-plugin-prettier)</small>
- `eslint-config-prettier` <small>[source](https://www.npmjs.com/package/eslint-plugin-prettier)</small>
- `eslint-plugin-vue` <small>[source](https://eslint.vuejs.org/user-guide/)</small>
- `vite-plugin-vue-devtools` <small>[source](https://devtools-next.vuejs.org/guide/vite-plugin)</small>
- `@types/node` <small>[source](https://www.npmjs.com/package/@types/node)</small>
- `@vue/tsconfig` <small>[source](https://www.npmjs.com/package/@vue/tsconfig)</small>
- `@tsconfig/node20` <small>[source](https://www.npmjs.com/package/@tsconfig/node20)</small>
- `eslint-config-airbnb-base` <small>[source](https://www.npmjs.com/package/eslint-config-airbnb-base)</small>

### Creating the Project

> [!NOTE]
>
> This is a Vite-based build setup. Go to [official docs](https://vuejs.org/guide/quick-start.html) if you want to use `create-vue` scaffolding tool.

**1. Initialize project.**

```bash
npm create vite@latest
```

Select answers to the provided prompts that best align with the needs of your project. This project is built with `Vue` framework with `TypeScript` variant.

**2. Install packages.**

```bash
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-vue vite-plugin-vue-devtools @types/node @vue/tsconfig @tsconfig/node20
```

**3. Include airbnb styling, or not.**

```bash
npx install-peerdeps --dev eslint-config-airbnb-base
```

**4. Configure `.prettierrc.*`.**

Feel free to add your own configurations.

```json
{
  "singleQuote": true,
  "printWidth": 80,
  "tabWidth": 2,
  "semi": true,
  "trailingComma": "es5"
}
```

**5. Configure `.eslintrc.cjs`.**

```js
module.exports = {
  extends: [
    'eslint:recommended',
    'plugin:vue/vue3-essential',
    'airbnb',
    'prettier',
  ],
  parserOptions: {
    ecmaVersion: 'latest',
  },
};
```

**6. Configure Vite.**

```js
import { fileURLToPath, URL } from 'node:url';

import { defineConfig } from 'vite';
import vue from '@vitejs/plugin-vue';
import vueDevTools from 'vite-plugin-vue-devtools';

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [vue(), vueDevTools()],
  resolve: {
    alias: {
      '@': fileURLToPath(new URL('./src', import.meta.url)),
    },
  },
});
```

**7. Install and configure Vue Router.** <small>[source](https://router.vuejs.org/installation.html)</small>

```bash
npm install vue-router@4
```

```ts
// main.ts
import './style.css';

import { createApp } from 'vue';

import App from './App.vue';
import router from './router';

const app = createApp(App);
app.use(router);
app.mount('#app');
```

**8. Install Tailwind CSS.**

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

**9. Configure template paths.**

```js
// tailwind.config.js
/** @type {import('tailwindcss').Config} */
export default {
  content: ['./index.html', './src/**/*.{vue,js,ts,jsx,tsx}'],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

**10. Add Tailwind directives to your CSS.**

```css
/* style.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

**11. Start build process.**

```bash
npm run dev
```

**12. Happy Coding! ^^**

# 🗂️ Back-End

# 📝 Notes

- If you're encountering issues like `Cannot find module '@/views/HomeView.vue' or its corresponding type declarations.ts(2307)`, you might want to add `shims-vue.d.ts` to your `src/` and add this:

```ts
// shims-vue.d.ts
declare module '*.vue';
```

> [!NOTE]
>
> The file or solution may vary depending on the framework you're using. I don't have specific sources on this, so you might want to research further online.

- For config references in `@vue/tsconfig` and `@tsconfig/node20`, you may refer to the `tsconfig` files in the app.
