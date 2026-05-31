# Quickstart for Bitasmbl project (Vue.js)

## 1) Install Bitasmbl-CLI package

```bash
npm i bitasmbl-cli
```

## 2) Run bitasmbl command to set up the project

```bash
bitasmbl pull --repoUrl https://github.com/he1snber8/Bitasmbl_skkrrrt-vue_765_340 --appId 340 --repoId 168
```

## 3) Enter into the main directory and start coding!

```bash
cd Bitasmbl_skkrrrt-vue_765_340
```

## Customize requirements in a way you like

Bitasmbl organizes development into requirements. Each requirement describes a feature or implementation goal and can define suggested file locations through a `paths` array.

The `paths` property acts as a mapping guideline, helping contributors understand where related code should live.

You can customize `paths` mappings through the `bitasmbl.json` file.

```json
{
  "requirement": "Implement authentication flow",
  "paths": ["**/src/features/auth/**", "**/src/components/auth/**"]
}
```

## Requirements

### About Me Section

Implement a dedicated 'About Me' page displaying personal information, professional summary, and relevant experiences.

Suggested paths:

```txt
**/src/views/AboutView.vue/**
```

### Skills Section

Create a comprehensive 'Skills' page to showcase technical proficiencies, tools, and technologies with appropriate categorisation.

Suggested paths:

```txt
**/src/views/SkillsView.vue/**
```

### Projects Listing

Develop a 'Projects' page displaying a high-level overview of all projects, including titles, brief descriptions, and thumbnails.

Suggested paths:

```txt
**/src/views/ProjectsView.vue/**
**/src/components/project/ProjectCard.vue/**
```

### Contact Section

Implement a 'Contact' page with contact details and a functional form for inquiries or direct messaging.

Suggested paths:

```txt
**/src/views/ContactView.vue/**
**/src/components/contact/ContactForm.vue/**
```

### Project Detail View

Enable navigation to a dedicated detail page for each project, showing detailed descriptions, tech stack, and images/videos.

Suggested paths:

```txt
**/src/views/ProjectDetailView.vue/**
**/src/components/project/ProjectDetails.vue/**
**/src/router/index.js/**
```

### Project Resource Links

Within each project's detail page, provide clickable links to live demos, GitHub repositories, or other external resources.

Suggested paths:

```txt
**/src/components/project/ProjectLinkButton.vue/**
**/src/utils/externalLinkHandler.js/**
```

### Global Search Functionality

Integrate a global search bar enabling users to filter projects, skills, or other content across the portfolio.

Suggested paths:

```txt
**/src/components/common/SearchBar.vue/**
**/src/store/modules/search.js/**
**/src/composables/useSearch.js/**
```



## Requirement Evaluation

Bitasmbl includes a requirement evaluation workflow that lets contributors select a task and submit work for validation.

Run:

```bash
bitasmbl evaluate
```

Example output:

<pre>
? Available Requirements:

❯ [<span style="color:#9333ea">1</span>] <span style="color:#9333ea"> Define portfolio layout </span>            [3]
  [2] Build showcase components            [3]
  [3] Implement navigation routing         [3]
</pre>

`[x]` on the right represents the number of submission attempts remaining for a requirement.

## Example evaluation result

```vue
<!--
|--------------------------------------------------------------------------
| BITASMBL EVALUATION
|--------------------------------------------------------------------------
| REQUIREMENT:
| Implement product catalog UI
|
| SCORE: 18/100
| STATUS: FAIL ✕
|
| INSIGHT:
| Product data is static and the component does not use reusable cards,
| loading states, filtering, routing, or state management.
|--------------------------------------------------------------------------
-->

<script setup>
const products = [
  { id: 1, name: "Keyboard", price: 89.99 },
  { id: 2, name: "Mouse", price: 49.99 },
];
</script>

<template>
  <main class="catalog">
    <h1>Products</h1>

    <section>
      <div v-for="product in products" :key="product.id">
        <h2>{{ product.name }}</h2>
        <p>${{ product.price }}</p>
      </div>
    </section>
  </main>
</template>
```

## Learn More

For complete command references, workflow explanations, and additional documentation, visit:

👉 [Bitasmbl Documentation](https://bitasmbl.com/docs)