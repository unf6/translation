# Translation Guide for Backupie and Givify

Welcome! This guide will help you contribute translations for the Backupie and Givify websites. Please follow the instructions below to add translations.

## Prerequisites

1. Basic knowledge of Git and GitHub.
2. Familiarity with MDX (Markdown with JSX).

## Website Links

- [Backupie](https://backupie.js.org)
- [Givify](https://givify.js.org/)

## How to Contribute Translations

### 1. Fork the Repository

Start by forking the repository you want to contribute to:

```bash
git clone https://github.com/unf6/translation.git
```

```bash
cd translation
```

### 2. Create a new branch

```bash
git checkout -b add-spanish-translation
```

### 3. Locate the MDX Files and _meta.json

Navigate to the `docs` and `pages` directory within the relevant project folder (backupie or givify).

### 4. Translate mdx files and _meta.jsons

1. Create new files for the language you are translating (e.g., index.es.mdx/_meta.es.json for Spanish).
2. Copy the content from the existing English MDX And Meta Json files (e.g., `index.mdx`/`_meta.json`) to the new language files (e.g., `index.es.mdx`/`_meta.es.json`).
3. Open the new language files and translate the content while keeping the MDX and Meta Json structure intact.


### 5. Update Configuration

### For Backupie

1. Open [`backupie/i18n.ts`](https://github.com/unf6/translation/blob/main/backupie/i18n.ts).
2. Add the new language to the `languages` configuration:
   ```js
   export const defaultLanguage = 'en';
   export const languages = ['en', 'cn',]; // Add your language codes here
   ```

### For Givify

1. Open [`backupie/next.config.js`](https://github.com/unf6/translation/blob/main/givify/next.config.js) And [`backupie/theme.config.tsx`](https://github.com/unf6/translation/blob/main/givify/theme.config.tsx).
2. Add the new language to the `i18n` and `locale` and `text` configuration:
   ```js
    module.exports = {
    i18n: {
    locales: ['en', 'cn', 'es'], // Add your language codes here
    defaultLocale: 'en',
   },
   }; // Add your language codes here
   ```
   ```js
   export default {  
   i18n: [
    { locale: "en", text: "English" },
    { locale: "ko", text: "한국어" },
   ],
   };
   ```

#### 6. Commit and Push Your Changes

```bash
git add .
```
```bash
git commit -m "Add Spanish translation for index and guide"
```
```bash
git push origin add-spanish-translation
```

#### 7. Open a pull request 

Go to the GitHub repository and open a pull request from your forked repository. Provide a clear description of the translations you have added.
