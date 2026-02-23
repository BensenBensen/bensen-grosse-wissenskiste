
---
## 🍉 Manifest

##### Ich installiere auf dem lokalen Server *Local* eine WordPress-Installation, um das Thema nach meinen gestalterischen Vorstellungen zu entwerfen oder anzupassen. Ich möchte dafür Tailwind CSS und eine Versionswerwaltung durch GitHub nutzen.


----
## 🍏 Timber installieren

**Mit Timber einfachen Template-Code für WordPress-Themes schreiben. Basierend auf der einfachen PHP-Sprache *Twig* ermöglicht Timber das Trennen von Template-Daten aus der WP-Basis und dem Template-Code. Mit Tailwind-CSS – einem CSS-Framework – schreibst du schnell konsistentes CSS-Styling** 

### Links

-  [Alle YT-Tutorials](https://buildawesomewebsites.com/) zum Timber-Tailwind-Workflow
 
### Steps

1. WordPress-Installation in Local aufsetzen
2. Timber nach diesem [Guide](https://timber.github.io/docs/v2/installation/installation/) installieren (PHP muss installiert sein) 
3. Timber-Theme über VSC im Themes-Ordner downloaden mit `git clone` 

> [!info]
> Mit `brew install php` installierst du PHP
>  Das Timber-WP-Plugin wird nicht mehr unterstützt

---
## 🍋 Tailwind installieren

---
## Ruhig, so startest du

1. Lokalen Server installieren ([Local](https://localwp.com/))
2. NPM einrichten
3. [Tailwind](https://serversideup.net/installing-tailwindcss-in-a-wordpress-theme/) installieren


**In den Theme-Folder navigieren**

`/Users/bensen/Local Sites/wp-bensen/app/public/wp-content/themes`

Mit SSH Git Clone URL das Repository in den Ordner kopieren (wenn du auf der Dateibasis des Repository aufbauen möchtest)

[Anleitung](https://docs.github.com/de/get-started/getting-started-with-git/about-remote-repositories)

Oder mit VSC loscoden 🙂


**Im WP-Backend das geklonte Theme auswählen**

---
## Konfiguration

1. [WP Local](ttps://localwp.com/) als lokaler Server
2. VSC als Editor

---
## Vite, Tailwind mit ChatGPT

To install Tailwind CSS using PostCSS with Vite, follow these steps:

### 1. **Install Vite (if not already installed)**
If you haven't installed Vite, first set up a Vite project:
```bash
npm create vite@latest my-project
cd my-project
npm install
```

### 2. **Install Tailwind CSS and PostCSS**
Install Tailwind CSS, PostCSS, and Autoprefixer as development dependencies:
```bash
npm install -D tailwindcss postcss autoprefixer
```

### 3. **Create Tailwind Configuration Files**
Generate the Tailwind and PostCSS config files:
```bash
npx tailwindcss init -p
```
This will create two files:
- `tailwind.config.js`
- `postcss.config.js`

### 4. **Configure Tailwind in your `tailwind.config.js`**
Open the `tailwind.config.js` file and configure the `content` option to point to your template files:
```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    './index.html',
    './src/**/*.{js,ts,jsx,tsx,vue}'
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### 5. **Set Up Tailwind in Your CSS**
In your main CSS file (e.g., `src/index.css` or `src/style.css`), include the Tailwind directives:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 6. **Update `vite.config.js` (Optional)**
Vite will automatically handle PostCSS, so you usually don't need to manually configure it unless you want to customize PostCSS further. If needed, the `vite.config.js` file might look something like this:
```js
import { defineConfig } from 'vite'
import vue from '@vitejs/plugin-vue'

export default defineConfig({
  plugins: [vue()],
  css: {
    postcss: {
      plugins: [
        require('tailwindcss'),
        require('autoprefixer'),
      ],
    },
  },
})
```

### 7. **Run Vite**
Now, run the development server with:
```bash
npm run dev
```

This will compile Tailwind with PostCSS and serve your app with Vite.

Now you're ready to use Tailwind CSS in your Vite project!
---
## 🍉 NPM einrichten

**Open Source Software-Library**

- [An Absolute Beginner's Guide to Using npm](https://nodesource.com/blog/an-absolute-beginners-guide-to-using-npm/)
- [Installing TailwindCSS in a WordPress Theme](https://serversideup.net/installing-tailwindcss-in-a-wordpress-theme/)

1. Über Command-Line `brew install npm` Befehl zur Installation von NPM eingeben
2. Mit Befehl `npm init` ein NPM-Paket im aktuellen Ordner anlegen

---


---
## SSH Zugang in VSC für Git

- [Anleitung](https://medium.com/codex/git-authentication-on-macos-setting-up-ssh-to-connect-to-your-github-account-d7f5df029320)

---
## Tools

- [Timber](https://upstatement.com/timber/)
- [Tailwind](https://tailwindcss.com/)  

---
## Gute Artikel

- [Tailwind für WordPress einrichten ](https://bonnick.dev/posts/tailwind-css-with-wordpress#installing-tailwind-and-required-packages)
- [Firefox DevTools benutzen](https://www.smashingmagazine.com/2023/06/popular-devtools-tips/)

