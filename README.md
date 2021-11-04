<!-- [![npm (scoped)](https://img.shields.io/npm/v/@meetmistry0/svelte-theme-toggle)](https://www.npmjs.com/package/@meetmistry0/svelte-theme-toggle)
![npm bundle size (scoped)](https://img.shields.io/bundlephobia/minzip/@meetmistry0/svelte-theme-toggle) -->

# svelte-theme-toggle
A dead simple way to implement a dark theme toggle in your Svelte/SvelteKit application. 

# Getting-Started
```
npm i @meetmistry0/svelte-theme-toggle
```

# Usage

Import the package in `<script>` in a svelte component and then declare it in the body.
```html
<script>
	import ThemeToggle from "@meetmistry0/svelte-theme-toggle";
</script>

<main>
	<!-- Some Stuff here -->
	<ThemeToggle />
	<!-- Some other stuff here -->
</main>
```

# Set styles

Use the following parameters in your global styles to actually change the colors on theme change
```css
:root {
        --bg: #fff;
        --text-color: #000;
}

:global([data-theme="dark"]) {
        --bg: #121212;
        --text-color: #fff;
}

:global(body) {
        background-color: var(--bg);
        color: var(--text-color);
        transition: 0.4s;  /* Change the transition time by altering this property */
}
```

### It is highly recommended to use this component on [`__layout.svelte`](https://kit.svelte.dev/docs#layouts) or it's derivatives.