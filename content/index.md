---
seo:
  title: nuxt-osdd
  description: Separate business and technical concerns in Nuxt with simple OSDD configuration and layer generators.
---

::u-page-hero{class="dark:bg-gradient-to-b from-neutral-900 to-neutral-950"}
---
orientation: horizontal
---
#top
:hero-background

#title
Build composable [Nuxt applications]{.text-primary} with OSDD.

#description
`nuxt-osdd` brings Open Source Driven Development to Nuxt. It gives you a simple way to declare `technical/` and `functional/` layers, and CLI commands to generate them quickly.

#links
  :::u-button
  ---
  to: /getting-started/installation
  size: xl
  trailing-icon: i-lucide-arrow-right
  ---
  Install nuxt-osdd
  :::

  :::u-button
  ---
  icon: i-simple-icons-npm
  color: neutral
  variant: outline
  size: xl
  to: https://www.npmjs.com/package/nuxt-osdd
  target: _blank
  ---
  View on npm
  :::

#default
  :::prose-pre
  ---
  code: |
    import { defineOSDDNuxtConfig } from 'nuxt-osdd'

    export default defineOSDDNuxtConfig({
      osdd: {
        technical: ['Authentication', 'Permission'],
        functional: ['Contracts', 'Posts']
      }
    })
  filename: nuxt.config.ts
  ---

  ```ts [nuxt.config.ts]
  import { defineOSDDNuxtConfig } from 'nuxt-osdd'

  export default defineOSDDNuxtConfig({
    osdd: {
      technical: ['Authentication', 'Permission'],
      functional: ['Contracts', 'Posts']
    }
  })
  ```
  :::
::

::u-page-section{class="dark:bg-neutral-950"}
#title
Why OSDD?

#features
  :::u-page-feature
  ---
  icon: i-lucide-briefcase
  ---
  #title
  `functional/` for business features

  #description
  Keep product domains like `Users`, `Contracts`, or `Posts` inside `functional/`. Each layer can own its pages, components, composables, and assets without mixing in infrastructure concerns.
  :::

  :::u-page-feature
  ---
  icon: i-lucide-cpu
  ---
  #title
  `technical/` for shared infrastructure

  #description
  Put authentication, permissions, API clients, database adapters, and other cross-cutting concerns in `technical/` so they stay reusable and independent from business code.
  :::

  :::u-page-feature
  ---
  icon: i-lucide-layers
  ---
  #title
  Explicit separation of concerns

  #description
  In many Nuxt projects, business features and technical building blocks end up mixed together. OSDD gives each concern a clear place: `functional/` for product domains and `technical/` for shared infrastructure.
  :::

  :::u-page-feature
  ---
  icon: i-lucide-settings-2
  ---
  #title
  Simple configuration

  #description
  `defineOSDDNuxtConfig` lets you declare your `technical` and `functional` layers in one small `osdd` block instead of wiring conventions manually.
  :::

  :::u-page-feature
  ---
  icon: i-lucide-terminal
  ---
  #title
  Built-in layer generation

  #description
  Generate a new layer in `technical/` or `functional/` with a ready-to-use structure including `nuxt.config.ts`, `app/`, and `README.md`.
  :::

  :::u-page-feature
  ---
  icon: i-lucide-expand
  ---
  #title
  Scales with your app

  #description
  Add new domains and technical modules as the project grows while keeping a structure that stays predictable for the whole team.
  :::
::

::u-page-section{class="dark:bg-neutral-950"}
#title
What `nuxt-osdd` changes in practice

#features
  :::u-page-feature
  ---
  icon: i-lucide-folder-tree
  ---
  #title
  Before: concerns are easy to mix

  #description
  In a growing Nuxt app, authentication, API code, permissions, and product features can easily evolve side by side with no shared convention. That makes ownership and boundaries less obvious over time.
  :::

  :::u-page-feature
  ---
  icon: i-lucide-folders
  ---
  #title
  With OSDD: the role of each folder is clear

  #description
    :::prose-pre
    ---
    filename: OSDD organization
    icon: i-lucide-folder-tree
    ---

    ```text
    .
    ├── technical
    │   ├── Authentication
    │   └── Permissions
    └── functional
        ├── Contracts
        └── Posts
    ```
    :::
  :::

  :::u-page-feature
  ---
  icon: i-lucide-settings-2
  ---
  #title
  One config entrypoint

  #description
  Declare your nuxt config with

    :::prose-pre
      ```typescript
      defineOSDDNuxtConfig({
        osdd: {
          technical: [...],
          functional: [...]
          }
        })
      ```
    :::
  and let the module wire the setup for you.
  :::
::

::u-page-section{class="dark:bg-gradient-to-b from-neutral-950 to-neutral-900"}
  :::u-page-c-t-a
  ---
  links:
    - label: Get started
      to: '/getting-started/installation'
      trailingIcon: i-lucide-arrow-right
  title: Ready to organize your Nuxt app with OSDD?
  description: Install `nuxt-osdd`, generate your first layers, and keep business logic and infrastructure concerns cleanly separated.
  class: dark:bg-neutral-950
  ---

  :stars-bg
  :::
::
