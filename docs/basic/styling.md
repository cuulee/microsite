# Styling

## Adding a Global Stylesheet

Create a `src/global` directory with an `index.css` file. This file will automatically be included on every page.

## Adding Component-level CSS

Microsite supports [CSS Modules](https://github.com/css-modules/css-modules) using the `[name].module.css` file naming convention.

**Example** Consider a shared Button component in the `src/components/` directory:

```css
/* components/button.module.css */
.button {
    color: white;
    background-color: blue;
}
```

```tsx
// components/button.tsx
import css from './button.module.css'

export function Button({ children }) {
  return (
    <button
      type="button"
      class={css.button}
    >
      { children }
    </button>
  )
}
```

## PostCSS

Microsite automatically detects if you have a PostCSS configuration file and will enable PostCSS accordingly.

## CSS-in-JS

Microsite does not currently support CSS-in-JS solutions, but this is a high priority for the next release.