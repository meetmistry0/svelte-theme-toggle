# svelte-theme-toggle 

[![npm](https://img.shields.io/npm/v/svelte-theme-toggle)](https://www.npmjs.com/package/svelte-theme-toggle)
![npm](https://img.shields.io/npm/dt/svelte-theme-toggle?label=Downloads)

A dead simple way to implement a dark theme toggle in your Svelte/SvelteKit application. 

## [Demo](https://svelte-theme-toggle.vercel.app/)

# Getting-Started
```
npm i svelte-theme-toggle
```

# Usage

Import the package in `<script>` in a svelte component and then declare it in the body.
```html
<script>
	import ThemeToggle from "svelte-theme-toggle";
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
        transition: ease 0.5s;  /* Change the transition time by altering this property */
}
```

### It is highly recommended to use this component on [`__layout.svelte`](https://kit.svelte.dev/docs/layouts) or it's derivatives.