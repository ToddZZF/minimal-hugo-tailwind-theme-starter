# Minimal Hugo Tailwind Theme Starter

A minimal Hugo theme starter with only TailwindCSS.

What it has:

- tailwindcss
- postcss & postcss-cli
- autoprefixer

This is how it's set up:

1. use `hugo new theme` create basic theme structure.
2. create `exampleSite` directory, `cd` to it and:
   - move `content` in theme root to here
   - create `config` direcory, `cd` to it and:
     - create `_default` directory for exampleSite development
     - create `theme` directory for theme development
3. install & initialize tailwindcss following [TailwindCSS document](https://tailwindcss.com/docs/installation)
   - setup `tailwind.config.js`
4. setup PostCSS following [Hugo document](https://gohugo.io/hugo-pipes/postcss/)
   - setup `postcss.config.js`
5. set up css file
6. set up `layout/head/css.html`
7. start theme development

To Preview ExampleSite:

```sh
hugo server --logLevel=debug --environment=theme --source=exampleSite --themesDir=../.. --disableFastRender -D --port 1313
# or
npm run dev:theme
```

To build theme:

```sh
npx postcss --config postcss.config.js --env production assets/css/styles.css -o assets/css/main.css
# or
npm run build:css
```

## Reference

- [Hextra](https://github.com/imfing/hextra)
- [Hugo Basic Starter for TailwindCSS v3.x](https://github.com/bep/hugo-starter-tailwind-basic)
