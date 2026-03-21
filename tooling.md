# 🧰 Tooling & Dev Setup

Цей документ описує рекомендоване середовище розробки, інструменти та налаштування для ефективної та узгодженої роботи фронтенд-команди.

---

## 💻 Середовище розробки

- **Node.js**: версія LTS (наприклад, `v24.x`) — затверджується нач. відділу, або головним інженером-програмістом, обов'язково має бути єдина версія як основна
- **Node.js**: менша за LTS (наприклад, `v20.10.0`) — може бути використана для окремих проєктів, затверджується нач. відділу, або головним інженером-програмістом 
- **Node.js**: більша за LTS (наприклад, `v25.x`) — може бути використана для окремих проєктів, затверджується нач. відділу, або головним інженером-програмістом 
- **Package manager**: `npm` (рекомендовано), `pnpm` або `yarn` — затверджується нач. відділу, або головним інженером-програмістом
- **Editor VSCode**: [VS Code](https://code.visualstudio.com/) з рекомендованими розширенями
- **Editor IntelliJ Idea**: [IntelliJ Idea](https://www.jetbrains.com/idea/) з рекомендованими розширенями
- **Editor WebStorm**: [WebStorm](https://www.jetbrains.com/webstorm/) з рекомендованими розширенями
- **Git**: налаштований з SSH-доступом до репозиторіїв (в пріоритеті) або HTTPS через терміновий токен 

---

## 📦 Основні залежності

- **Білдер**: [Vite](https://vitejs.dev/) — швидкий, сучасний
- **Тестування**: [Vitest](https://vitest.dev/) + [Testing Library](https://testing-library.com/)
- **Лінтинг**: [ESLint](https://eslint.org/), [oxlint](https://oxc.rs/docs/guide/usage/linter.html)
- **Форматування**: [Prettier](https://prettier.io/), [oxfmt](https://oxc.rs/docs/guide/usage/formatter.html)
- **Типізація**: [TypeScript](https://www.typescriptlang.org/)
- **Стилі**: CSS/LESS/SCSS або CSS-in-HTML для email шаблонів
- **Менеджер стану**: Pinia
- **Маршрутизація**: Vue Router
- **HTTP клієнт**: Axios або Fetch API
- **Компонентна бібліотека**: Vuetify

---

## 🧪 Тестування

- Всі тести мають запускатися через `npm test` ("scripts": {..., "test": "vitest"})
- Покриття коду перевіряється через `vitest --coverage`
- CI має включати автоматичний запуск тестів
- Тести розташовуються в теці `tests` або `__tests__` або поруч з тестуємим файлом. 
- Назви тестових файлів обов'язково мають включати суфікс `.test.ts` (`.test.js`), або `.spec.ts` (`.spec.js`)

---

## 🧹 Лінтинг та форматування

- **ESLint** налаштований з правилами для JavaScript/TypeScript, Vue
- **Prettier** інтегрований з ESLint або запускається окремо
- **oxLint** налаштований з правилами для JavaScript/TypeScript, Vue
- **oxfmt** запускається окремо
- Автоматичне форматування при збереженні (`editor.formatOnSave: true`)

---

## 📁 Структура проєкту

- Project Name (Root)
  - src
    - components
    - views
    - store
    - services
    - utils
    - assets
    - pages
    - styles
  - tests / __tests__
  - public
  - .vscode
  - node_modules
  - package.json
  - package-lock.json
  - tsconfig.json
  - vite.config.dev.ts
  - vite.config.prod.ts
  - eslint.config.js
  - stylelint.config.js
  - .prettierrc
  - README.md


- Всі файли повинні мати зрозумілі назви в форматі:
  + компоненти Vue - PascalCase
  + звичайні ts, js - snake_case

- Компоненти мають бути розбиті на атомарні одиниці
- svg файли обробляться як Vue компоненти, при необхідності використання лише шляху до імпорту необхідно додавати `?url` в кінець шляху

---

## 🚀 CI/CD інтеграція

- GitLab Pipelines / GitLab CI / GitHub Actions / Bitbucket Pipelines
- Кроки: install → lint → test → build → deploy
- Перевірка покриття, лінтингу, форматування — обов’язкова

---

## 🔌 Рекомендовані розширення для VS Code

- ESLint, oxlint
- Prettier, oxfmt
- GitLens
- Інший функціонал за потребою

> Повний перелік знаходиться в теці `.vscode/extensions.txt`. 
> Файл `.vscode/extensions.ps1` для автоматичного встановлення рекомендованих розширень.

---

## 📚 Документація

- README з інструкцією запуску проєкту
- CONTRIBUTING.md з правилами комітів, PR, стилю коду
- TESTING.md з інструкціями по тестуванню 
- SECURITY.md з політикою безпеки 
- CHECKLIST.md з переліком порядку перевірок перед релізом

---

## 📌 Відповідальність

- **Кожен розробник** має налаштувати середовище згідно з цим документом
- **Головний інженер-програміст** контролює відповідність конфігурації
- **CI/CD** контролює начальник відділу або головний інженер-програміст за його відсутності