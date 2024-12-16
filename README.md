# Tailwind </br>

**Como instalar?**
```src: https://tailwindcss.com/docs/installation```

1) No seu vscode, use o diretório que você desejar. Dentro dele, insira este código:
```
npm init
```
Aperte o "Enter" até que o procedimento termine. Com isso, você precisa instalar o <b>Tailwind</b> dentro deste diretório usando este código:
```
npm install -D tailwindcss
npx tailwindcss init
```
</br>
2) Com o primeiro processo feito com sucesso, precisamos configurar o <b>tailwind.config.js</b> para que fique assim (copiar e colar):
``` 
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
</br>
3) Crie uma nova pasta chamada <b>src</b>. Dentro desta pasta, crie um aquivo chamado <b>input.css</b> e copie e cole este código:
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
</br>
4) No terminal, copie e cole este código e execute:
```
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```

5) Por fim, no seu arquivo HTML, faça o link:css usando o arquivo <b>output.css</b> em vez do css que usamos.
</br>
---

**Por que usar TAILWIND e não CSS?**

Tailwind é um framework de estilização que tem o objetivo de simplificar e facilitar a estilização do seu site. </br>
Enquanto nós utilizamos características e classes no CSS, <b>Tailwind</b> aproveita as classes para estilizar o elemento por exemplo:

No CSS, para estilizar um header:
```html
<p class="header">
  Hello World"
</p>
```

```css
.header {
  text-align: center;
  font-weight: bold;
  font-size: 500;
  color: red;
}
```

Enquanto isso, o TAILWIND use as classes para já dar um estilo ao elemento:
```html
<p class="text-center text-lg text-red-400">
  Hello World!
</p>
```
