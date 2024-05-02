# You're at commit 'second commit'
To see this app run ``bun run dev`` to view the app in the browser there is a vueprime button that shows a toast, However there is an issue.
After we imported the tailwind reset (preflight) in `app.vue`, vueprime styles are now not working as they should, i.e compare the button in this commit versus the previous commit.

This project uses unocss + vueprime, the purpose is to have unocss to do any extra styles on pages + any hand-crafted components etc..
Vueprime will be used on other parts of this app with its original styles, to see the app with correct vueprime styles head to the 'first commit' ``git log --oneline``.

# Additional note
Vueprime suggests the use of custom ordered css layers, so that their styles don't get overridden by preflights, Here is how they achieve that with tailwindcss
[primevue csslayer tailwind](https://primevue.org/csslayer/#tailwind). Due to my lack of understanding of how css layers work in unocss and specifically for this use-case in a nuxt app, i am not exactly sure how to apply that same concept in unocss, so that the preflight doesn't override vueprime's styles. Help is appreciated.
