# svelte + tailwind starter

Using https://github.com/matyunya/smelte to get the production build include all generated css.

## pnpm

Using [pnpm](https://pnpm.js.org/)

## Typeface install for tailwind

Not for svelte: [Google Fonts in Tailwind](https://scottw.com/blog/google-font-tailwind/)

For svelte

    - `npm i` [from typefaces repo](https://github.com/KyleAMathews/typefaces) packaged font
    - `cp -R node_modules/typeface-cooper-hewitt/files/ public/files`
    - `cp node_modules/typeface-cooper-hewitt/index.css public/font-name.css`
    - add link:css in index.html
    - configure tailwind.config.js as below
    - set <body class="font-sans">

```javascript
const defaultTheme = require('tailwindcss/defaultTheme');
module.exports = {
  theme: {
    extend: {
      fontFamily: {
        sans: ['Cooper Hewitt', ...defaultTheme.fontFamily.sans]
      }
    }
  },
  variants: {},
  plugins: []
};
```

See [tailwindcss repo](https://github.com/tailwindcss/discuss/issues/293) for font-{sans,display,...}

## Quiet dev

Filter `npm run dev` for stderr only: `npm run dev 2>&1 > /dev/null` (useful in tmux; this is fis shell, for bash use [this](https://stackoverflow.com/questions/2342826/how-to-pipe-stderr-and-not-stdout)  )

Check 'quiet' amd 'silent' in package.json scripts:

```json
"dev": "rollup -c -w --silent",
"start:dev": "sirv public --single --dev --quiet"
```

## Util

[Tailwind Cheat Sheet](https://nerdcave.com/tailwind-cheat-sheet)


