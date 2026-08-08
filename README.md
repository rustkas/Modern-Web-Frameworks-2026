# Modern Web Frameworks 2026

## От Virtual DOM к Resumability и HTML-first архитектурам

> Книга о том, как изменилась веб-разработка после 2023 года.  
> От эпохи SPA и Virtual DOM к новой эре, где HTML снова становится платформой, а реактивность достигается через Signals и компиляторы.

---

## 📖 О книге

За последние три года веб-разработка пережила тектонический сдвиг.

То, что мы знали как «современный фронтенд» — с его SPA, Virtual DOM, тяжелым JavaScript-бандлом и дорогой гидратацией — перестало быть единственным путем. После 2023 года на сцену вышли новые парадигмы:

- **Signals** как стандарт реактивности
- **Resumability** вместо гидратации
- **Компиляторы** как основной инструмент оптимизации
- **HTML-first** подходы и возвращение к платформе
- **Server Components** как новая модель рендеринга
- **Islands Architecture** для постепенного улучшения

Эта книга — карта новой реальности. Она показывает, как фреймворки эволюционировали, куда движутся и как выбрать правильную архитектуру для вашего проекта.

Современные фреймворки:

- **Angular**
- **React**
- **Vue**
- **Svelte**
- **Qwik**
- **Astro**
- **SolidJS**
- **Next.js**
- **Nuxt**

уже не просто конкурируют. Они заимствуют лучшие идеи друг у друга, двигаясь к общей цели: **быстрее, легче, ближе к платформе**.

Эта книга показывает, как именно они это делают.

---

# 🎯 Цель книги

После изучения книги читатель должен понимать:

- почему Virtual DOM перестал быть главным;
- как работают Signals и чем они лучше предыдущих подходов;
- что такое Resumability и чем она отличается от Hydration;
- как современные компиляторы оптимизируют код;
- почему HTML-first архитектуры снова актуальны;
- как выбрать фреймворк для своего проекта в 2026 году;
- как строить производительные full-stack приложения с Server Components и Edge Computing;
- какова роль браузера как платформы в 2026 году;
- куда движется веб-разработка в ближайшие 10 лет.

---

# 👥 Для кого эта книга

Книга предназначена для:

- Frontend-разработчиков, желающих быть в курсе последних трендов;
- Full-stack разработчиков, строящих современные веб-приложения;
- Архитекторов интерфейсов и технических лидов;
- Разработчиков, которые хотят выбрать правильный фреймворк для нового проекта;
- Специалистов по Web Performance и оптимизации;
- Всех, кто хочет понимать, куда движется веб-платформа.

---

# 🧠 Главная идея

Современный frontend — это не битва фреймворков. Это эволюция веб-платформы.

```
Эволюция парадигм:

jQuery → SPA (Angular/React/Vue) → 2023+
                                      |
                                      ├── Server Components
                                      ├── Signals
                                      ├── Resumability
                                      ├── Islands Architecture
                                      └── HTML-first
```

Фреймворки становятся тоньше, умнее и ближе к браузеру:

```
┌─────────────────────────────────────────────────┐
│  Ваше приложение                                │
├─────────────────────────────────────────────────┤
│  Фреймворк (React/Angular/Vue/Svelte/Qwik/etc)  │
├─────────────────────────────────────────────────┤
│  HTML, CSS, JavaScript (Web Platform)           │
├─────────────────────────────────────────────────┤
│  Браузер (Blink/Gecko/WebKit)                   │
└─────────────────────────────────────────────────┘
```

---

# 📚 Содержание

## Предисловие

## От эпохи SPA к новой реальности

- Почему мы вообще перешли на SPA?
- Что пошло не так? Проблемы тяжелых JavaScript-приложений
- 2023 год как точка бифуркации
- Новая философия: HTML-first, Compiler-first, Platform-first
- Как читать эту книгу: карта современного фронтенда

* [📖 Читать главу](./book/preface.md)  
* [📚 Литература](./references/preface.md)  
* [💻 Примеры](./examples/preface.md)  
* [🧪 Практика](./exercises/preface.md)

---

# Часть I. Новая эпоха веб-фреймворков

## Глава 1. Почему фреймворки изменились

Темы:

- История развития фронтенда
- От jQuery к SPA
- Angular, React и Vue
- Взрыв JavaScript-экосистемы
- Почему Virtual DOM перестал быть главным
- Что изменилось после 2023 года
- HTML снова становится платформой
- Роль браузера в 2026 году

* [📖 Читать главу](./book/chapter-01.md)  
* [📚 Литература](./references/chapter-01.md)  
* [💻 Примеры](./examples/chapter-01.md)  
* [🧪 Практика](./exercises/chapter-01.md)

---

## Глава 2. Baseline и новая веб-платформа

Темы:

- Living Standard
- Baseline
- Interop
- Современные возможности браузеров
- Когда больше не нужны полифилы
- Progressive Enhancement нового поколения

* [📖 Читать главу](./book/chapter-02.md)  
* [📚 Литература](./references/chapter-02.md)  
* [💻 Примеры](./examples/chapter-02.md)  
* [🧪 Практика](./exercises/chapter-02.md)

---

## Глава 3. Архитектура современного фреймворка

Темы:

- Framework vs Library
- Runtime vs Compile-time
- Hydration
- Partial Hydration
- Progressive Hydration
- Islands Architecture
- Resumability
- Fine-Grained Reactivity
- Signals
- Compiler-first архитектуры

* [📖 Читать главу](./book/chapter-03.md)  
* [📚 Литература](./references/chapter-03.md)  
* [💻 Примеры](./examples/chapter-03.md)  
* [🧪 Практика](./exercises/chapter-03.md)

---

# Часть II. Reactivity нового поколения

## Глава 4. Эволюция реактивности

Темы:

- Dirty Checking
- Change Detection
- Observable
- Proxy
- Signals
- Fine-Grained Reactivity
- Dependency Graph
- Automatic Dependency Tracking

* [📖 Читать главу](./book/chapter-04.md)  
* [📚 Литература](./references/chapter-04.md)  
* [💻 Примеры](./examples/chapter-04.md)  
* [🧪 Практика](./exercises/chapter-04.md)

---

## Глава 5. Signals

Темы:

- Почему Signals стали стандартом индустрии
- Angular Signals
- Solid Signals
- Preact Signals
- Qwik Signals
- Signal Graph
- Effects
- Computed
- Resources

* [📖 Читать главу](./book/chapter-05.md)  
* [📚 Литература](./references/chapter-05.md)  
* [💻 Примеры](./examples/chapter-05.md)  
* [🧪 Практика](./exercises/chapter-05.md)

---

## Глава 6. Управление состоянием

Темы:

- Local State
- Global State
- Server State
- URL State
- Cache State
- Event State
- Signals vs Redux
- Signals vs MobX
- Signals vs NgRx
- Zustand
- Jotai
- TanStack Store

* [📖 Читать главу](./book/chapter-06.md)  
* [📚 Литература](./references/chapter-06.md)  
* [💻 Примеры](./examples/chapter-06.md)  
* [🧪 Практика](./exercises/chapter-06.md)

---

# Часть III. Rendering

## Глава 7. Современные модели рендеринга

Темы:

- CSR
- SSR
- SSG
- ISR
- Streaming SSR
- Edge Rendering
- Partial Rendering

* [📖 Читать главу](./book/chapter-07.md)  
* [📚 Литература](./references/chapter-07.md)  
* [💻 Примеры](./examples/chapter-07.md)  
* [🧪 Практика](./exercises/chapter-07.md)

---

## Глава 8. Hydration

Темы:

- Что такое Hydration
- Почему Hydration дорогой
- Partial Hydration
- Progressive Hydration
- Selective Hydration
- Lazy Hydration
- Resumability
- Hydration Mismatch

* [📖 Читать главу](./book/chapter-08.md)  
* [📚 Литература](./references/chapter-08.md)  
* [💻 Примеры](./examples/chapter-08.md)  
* [🧪 Практика](./exercises/chapter-08.md)

---

## Глава 9. Server Components

Темы:

- React Server Components
- Server Functions
- Server Actions
- HTML Streaming
- Flight Protocol
- Server-first архитектура

* [📖 Читать главу](./book/chapter-09.md)  
* [📚 Литература](./references/chapter-09.md)  
* [💻 Примеры](./examples/chapter-09.md)  
* [🧪 Практика](./exercises/chapter-09.md)

---

# Часть IV. Современные архитектуры

## Глава 10. Islands Architecture

Темы:

- Astro
- Fresh
- Enhance
- Partial Islands
- HTML-first подход

* [📖 Читать главу](./book/chapter-10.md)  
* [📚 Литература](./references/chapter-10.md)  
* [💻 Примеры](./examples/chapter-10.md)  
* [🧪 Практика](./exercises/chapter-10.md)

---

## Глава 11. Resumability

Темы:

- Qwik
- Serialization
- Lazy Execution
- Resume вместо Hydrate
- Event Replay
- Performance

* [📖 Читать главу](./book/chapter-11.md)  
* [📚 Литература](./references/chapter-11.md)  
* [💻 Примеры](./examples/chapter-11.md)  
* [🧪 Практика](./exercises/chapter-11.md)

---

## Глава 12. Compiler-first Frameworks

Темы:

- Svelte
- Solid Compiler
- Angular Compiler
- React Compiler
- Build-time оптимизация
- Tree Shaking
- Code Splitting

* [📖 Читать главу](./book/chapter-12.md)  
* [📚 Литература](./references/chapter-12.md)  
* [💻 Примеры](./examples/chapter-12.md)  
* [🧪 Практика](./exercises/chapter-12.md)

---

# Часть V. HTML-first Frameworks

## Глава 13. Когда HTML снова главный

Темы:

- Native Dialog
- Popover API
- View Transition
- Anchor Positioning
- Forms
- Declarative Shadow DOM
- Custom Elements
- HTML как API браузера

* [📖 Читать главу](./book/chapter-13.md)  
* [📚 Литература](./references/chapter-13.md)  
* [💻 Примеры](./examples/chapter-13.md)  
* [🧪 Практика](./exercises/chapter-13.md)

---

## Глава 14. Web Components

Темы:

- Custom Elements
- Shadow DOM
- Slots
- Declarative Shadow DOM
- ElementInternals
- Form Associated Custom Elements
- Scoped Registries

* [📖 Читать главу](./book/chapter-14.md)  
* [📚 Литература](./references/chapter-14.md)  
* [💻 Примеры](./examples/chapter-14.md)  
* [🧪 Практика](./exercises/chapter-14.md)

---

## Глава 15. Progressive Enhancement

Темы:

- Минимум JavaScript
- HTML-first
- CSS-first
- Server-first
- Browser-first

* [📖 Читать главу](./book/chapter-15.md)  
* [📚 Литература](./references/chapter-15.md)  
* [💻 Примеры](./examples/chapter-15.md)  
* [🧪 Практика](./exercises/chapter-15.md)

---

# Часть VI. Современные фреймворки

## Глава 16. Angular 2026

Темы:

- Signals
- Standalone
- Control Flow
- Deferred Loading
- Zoneless
- SSR
- Hydration
- Incremental Hydration
- Angular Material
- Будущее Angular

* [📖 Читать главу](./book/chapter-16.md)  
* [📚 Литература](./references/chapter-16.md)  
* [💻 Примеры](./examples/chapter-16.md)  
* [🧪 Практика](./exercises/chapter-16.md)

---

## Глава 17. React 2026

Темы:

- React Compiler
- React 19+
- Server Components
- Server Actions
- Suspense
- Transitions
- use()
- Streaming
- React DOM

* [📖 Читать главу](./book/chapter-17.md)  
* [📚 Литература](./references/chapter-17.md)  
* [💻 Примеры](./examples/chapter-17.md)  
* [🧪 Практика](./exercises/chapter-17.md)

---

## Глава 18. Vue 3.6+

Темы:

- Composition API
- Reactivity
- Vapor Mode
- Nuxt
- Pinia
- SSR
- Islands

* [📖 Читать главу](./book/chapter-18.md)  
* [📚 Литература](./references/chapter-18.md)  
* [💻 Примеры](./examples/chapter-18.md)  
* [🧪 Практика](./exercises/chapter-18.md)

---

## Глава 19. Svelte 5

Темы:

- Runes
- Compiler
- Reactivity
- SvelteKit
- Server Rendering
- Zero Runtime

* [📖 Читать главу](./book/chapter-19.md)  
* [📚 Литература](./references/chapter-19.md)  
* [💻 Примеры](./examples/chapter-19.md)  
* [🧪 Практика](./exercises/chapter-19.md)

---

## Глава 20. Qwik

Темы:

- Resumability
- QRL
- Lazy Execution
- Optimizer
- City
- Edge

* [📖 Читать главу](./book/chapter-20.md)  
* [📚 Литература](./references/chapter-20.md)  
* [💻 Примеры](./examples/chapter-20.md)  
* [🧪 Практика](./exercises/chapter-20.md)

---

## Глава 21. Astro

Темы:

- Islands
- Content Collections
- Server Islands
- View Transition
- Static-first

* [📖 Читать главу](./book/chapter-21.md)  
* [📚 Литература](./references/chapter-21.md)  
* [💻 Примеры](./examples/chapter-21.md)  
* [🧪 Практика](./exercises/chapter-21.md)

---

## Глава 22. SolidJS

Темы:

- Fine-Grained Reactivity
- Signals
- Resources
- Streaming
- SSR

* [📖 Читать главу](./book/chapter-22.md)  
* [📚 Литература](./references/chapter-22.md)  
* [💻 Примеры](./examples/chapter-22.md)  
* [🧪 Практика](./exercises/chapter-22.md)

---

## Глава 23. Next.js

Темы:

- App Router
- React Server Components
- Server Actions
- Edge Runtime
- Turbopack
- Partial Prerendering

* [📖 Читать главу](./book/chapter-23.md)  
* [📚 Литература](./references/chapter-23.md)  
* [💻 Примеры](./examples/chapter-23.md)  
* [🧪 Практика](./exercises/chapter-23.md)

---

## Глава 24. Nuxt

Темы:

- Nitro
- Islands
- Server Components
- Edge
- Hybrid Rendering

* [📖 Читать главу](./book/chapter-24.md)  
* [📚 Литература](./references/chapter-24.md)  
* [💻 Примеры](./examples/chapter-24.md)  
* [🧪 Практика](./exercises/chapter-24.md)

---

# Часть VII. Производительность

## Глава 25. Производительность современных приложений

Темы:

- INP
- LCP
- CLS
- TTFB
- Interaction Latency
- Streaming
- Lazy Loading
- Code Splitting

* [📖 Читать главу](./book/chapter-25.md)  
* [📚 Литература](./references/chapter-25.md)  
* [💻 Примеры](./examples/chapter-25.md)  
* [🧪 Практика](./exercises/chapter-25.md)

---

## Глава 26. Оптимизация JavaScript

Темы:

- Tree Shaking
- Dead Code Elimination
- Bundling
- ES Modules
- Dynamic Import
- Import Maps
- Module Federation

* [📖 Читать главу](./book/chapter-26.md)  
* [📚 Литература](./references/chapter-26.md)  
* [💻 Примеры](./examples/chapter-26.md)  
* [🧪 Практика](./exercises/chapter-26.md)

---

## Глава 27. Современные сборщики

Темы:

- Vite
- Rolldown
- Rspack
- Turbopack
- esbuild
- SWC
- Parcel
- Bun

* [📖 Читать главу](./book/chapter-27.md)  
* [📚 Литература](./references/chapter-27.md)  
* [💻 Примеры](./examples/chapter-27.md)  
* [🧪 Практика](./exercises/chapter-27.md)

---

# Часть VIII. Full Stack

## Глава 28. Server Functions

Темы:

- RPC
- Actions
- Mutations
- Forms
- Progressive Enhancement

* [📖 Читать главу](./book/chapter-28.md)  
* [📚 Литература](./references/chapter-28.md)  
* [💻 Примеры](./examples/chapter-28.md)  
* [🧪 Практика](./exercises/chapter-28.md)

---

## Глава 29. Edge Computing

Темы:

- Cloudflare
- Deno
- Bun
- Workers
- Edge Functions

* [📖 Читать главу](./book/chapter-29.md)  
* [📚 Литература](./references/chapter-29.md)  
* [💻 Примеры](./examples/chapter-29.md)  
* [🧪 Практика](./exercises/chapter-29.md)

---

## Глава 30. Full Stack Frameworks

Темы:

- Next.js
- Nuxt
- Remix
- SvelteKit
- Qwik City
- Astro
- Redwood
- TanStack Start

* [📖 Читать главу](./book/chapter-30.md)  
* [📚 Литература](./references/chapter-30.md)  
* [💻 Примеры](./examples/chapter-30.md)  
* [🧪 Практика](./exercises/chapter-30.md)

---

# Часть IX. Будущее веб-разработки

## Глава 31. AI и веб-фреймворки

Темы:

- AI Coding
- AI Components
- MCP
- Agentic Development
- LLM-интеграция

* [📖 Читать главу](./book/chapter-31.md)  
* [📚 Литература](./references/chapter-31.md)  
* [💻 Примеры](./examples/chapter-31.md)  
* [🧪 Практика](./exercises/chapter-31.md)

---

## Глава 32. WebAssembly и новые архитектуры

Темы:

- Wasm
- Component Model
- WASI
- Rust
- Go
- C#

* [📖 Читать главу](./book/chapter-32.md)  
* [📚 Литература](./references/chapter-32.md)  
* [💻 Примеры](./examples/chapter-32.md)  
* [🧪 Практика](./exercises/chapter-32.md)

---

## Глава 33. Browser Native UI

Темы:

- HTML
- CSS
- Popover
- Dialog
- Anchor Positioning
- View Transition
- Form API

* [📖 Читать главу](./book/chapter-33.md)  
* [📚 Литература](./references/chapter-33.md)  
* [💻 Примеры](./examples/chapter-33.md)  
* [🧪 Практика](./exercises/chapter-33.md)

---

## Глава 34. Что останется от JavaScript-фреймворков через 10 лет?

Темы:

- HTML-first
- Browser-first
- Less JavaScript
- Compiler-first
- AI-first
- Platform-first
- Будущее React
- Будущее Angular
- Будущее Vue
- Будущее веб-платформы

# 📌 Project Status

🚧 Under development

* [📖 Читать главу](./book/chapter-34.md)  
* [📚 Литература](./references/chapter-34.md)  
* [💻 Примеры](./examples/chapter-34.md)  
* [🧪 Практика](./exercises/chapter-34.md)
