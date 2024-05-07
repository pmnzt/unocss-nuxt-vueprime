To see this app run ``bun run dev`` to view the app in the browser there is a vueprime button that shows a toast.

``bun install`` first to install the dependencies before running this project for the first time.

# Background
After spending time studying css layers and how they work i came up with this temporarily solution, here is an explanation about the workaround i came up with:

1. pasted the contents of the tailwind preflight (reset) in a new file `~/assets/css/reset.css`.
2. wrapped everything in the new file inside
```css
@layer tailwind-reset {}
```
[reset.css](assets/css/reset.css).

3. updated vueprime config in `nuxt.config.ts`, letting vueprime orders the css layers as follow:
```ts
primevue: {
  cssLayerOrder: 'tailwind-reset,primevue'
}
```
[nuxt.config.ts](nuxt.config.ts)

---
checkout previous commits if you are curios of the original issue `git log --oneline`.
