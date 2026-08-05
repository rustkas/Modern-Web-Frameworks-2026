# Modern Web Application 2026

## Architecture, Platform, Execution, Data and Delivery of Modern Web Applications

> **Modern Web Application 2026** — системное руководство по архитектуре современных веб-приложений: от HTML, CSS и Web APIs до JavaScript, WebAssembly, WebGPU, серверных систем, данных, AI и production infrastructure.

---

# 📖 О книге

Веб-приложение 2026 года больше нельзя адекватно описать как:

```text
Browser
   ↓
JavaScript
   ↓
Frontend Framework
   ↓
Backend
   ↓
Database
```

Эта модель слишком сильно привязана к эпохе SPA и JavaScript frameworks.

Современный браузер сам является огромной программной платформой, предоставляющей:

* HTML;
* CSS;
* DOM;
* JavaScript;
* Web APIs;
* Web Components;
* Workers;
* Storage;
* Streams;
* Networking;
* WebAssembly;
* WebGPU;
* Navigation;
* View Transitions;
* Service Workers;
* device capabilities;
* browser security primitives.

В результате современное Web Application представляет собой не один runtime, а **систему взаимодействующих execution environments**.

```text
                         Web Application
                               │
          ┌────────────────────┼────────────────────┐
          │                    │                    │
       Browser UI          Application Logic       Data
          │                    │                    │
      HTML / CSS          JS / WASM / Workers    Fetch / Storage
          │                    │                    │
          └────────────────────┼────────────────────┘
                               │
                         Web Platform
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
          Browser           WebGPU           Network
             │                 │                 │
             └─────────────────┼─────────────────┘
                               │
                         Server / Cloud
```

Главный вопрос книги:

> **Как правильно распределить ответственность между Web Platform, клиентским execution layer, сервером, данными и инфраструктурой?**

---

# 🎯 Главная идея

Современное Web Application следует строить **Platform First**.

Не:

```text
Framework
   ↓
Browser
```

а:

```text
Web Platform
      ↓
Application Architecture
      ↓
Optional Framework / Compiler / Runtime
      ↓
Application
```

Framework является не фундаментом Web Application, а **одним из архитектурных инструментов**.

В зависимости от задачи приложение может использовать:

```text
HTML
CSS
Browser APIs
JavaScript
WebAssembly
Workers
WebGPU
Web Components
Server
Database
Cloud
```

и не обязано использовать всё одновременно.

---

# 🧭 Web Application Architecture 2026

Предлагаемая базовая модель:

```text
┌────────────────────────────────────────────────────┐
│                   APPLICATION                      │
│                                                    │
│  UI • Features • Business Logic • Data • State     │
└───────────────────────┬────────────────────────────┘
                        │
┌───────────────────────▼────────────────────────────┐
│               APPLICATION ARCHITECTURE             │
│                                                    │
│ Components • State • Routing • Data Flow           │
│ Rendering • Execution • Security • Delivery        │
└───────────────┬──────────────────────┬─────────────┘
                │                      │
                ▼                      ▼
       ┌─────────────────┐    ┌─────────────────┐
       │ Browser         │    │ Server / Cloud  │
       │                 │    │                 │
       │ HTML            │    │ HTTP            │
       │ CSS             │    │ API             │
       │ JS              │    │ Auth            │
       │ WASM            │    │ Database        │
       │ Workers         │    │ Cache           │
       │ WebGPU          │    │ Queue           │
       │ Storage         │    │ Compute         │
       └────────┬────────┘    └────────┬────────┘
                │                      │
                └──────────┬───────────┘
                           ▼
                    INTERNET / WEB
```

---

# ⚙️ Multiple Execution Layers

Одно из главных изменений Web Platform — наличие нескольких механизмов выполнения.

## JavaScript

JavaScript прежде всего отвечает за:

* orchestration;
* DOM;
* events;
* browser APIs;
* application coordination;
* navigation;
* UI state;
* data flow.

## WebAssembly

WebAssembly может использоваться для:

* CPU-intensive computation;
* image processing;
* audio/video processing;
* parsing;
* compression;
* cryptography;
* scientific computing;
* сложных алгоритмов;
* вычислительной бизнес-логики.

Таким образом:

```text
JavaScript
    ↓
Orchestration / UI / Platform

WebAssembly
    ↓
Computation / Data / Algorithms
```

Это не конкурирующие технологии, а два взаимодополняющих execution layers. Именно эта модель является одной из центральных архитектурных идей Emerge.

---

# 🧩 Progressive Application Architecture

Современное приложение не обязано загружать все возможности сразу.

Можно представить его как последовательное усиление:

```text
Level 0
HTML

        ↓

Level 1
HTML + CSS

        ↓

Level 2
HTML + CSS + JavaScript

        ↓

Level 3
HTML + CSS + JS + Web APIs

        ↓

Level 4
+ Components / Signals / Runtime

        ↓

Level 5
+ WebAssembly

        ↓

Level 6
+ Workers

        ↓

Level 7
+ WebGPU
```

Это расширяет классическую идею Progressive Enhancement.

Теперь progressive enhancement относится не только к UI, но и к:

* runtime;
* computation;
* data processing;
* concurrency;
* GPU;
* offline capabilities.

Именно такой **Progressive Runtime / Progressive WebAssembly** подход был формализован в архитектуре Emerge.

---

# 📚 Содержание

# Предисловие

## Что такое Modern Web Application в 2026 году

* От Web Page к Web Application
* От MPA к SPA
* От SPA к Platform-Native Applications
* Почему Browser стал Application Platform
* Почему Framework больше не является центром приложения
* Почему Web Application теперь имеет несколько execution layers
* JavaScript и WebAssembly
* Browser и Server
* Что означает Platform First
* Архитектурная карта книги

---

# Часть I. Web Platform

## Глава 1. Browser как Application Platform

* Browser Process
* Renderer Process
* GPU Process
* Network Process
* Site Isolation
* Browser Security Model
* Event Loop
* Rendering Pipeline
* Scheduler
* Browser Storage
* Permissions
* Browser ↔ Operating System

## Глава 2. HTML как Application Interface

* HTML Living Standard
* Semantic HTML
* DOM
* HTML как declarative API
* Forms
* Validation
* Dialog
* Popover
* Details / Summary
* Declarative Shadow DOM
* Accessibility
* HTML как transport format

## Глава 3. CSS как Application Layer

* Cascade
* Layers
* Scope
* Nesting
* Custom Properties
* Design Tokens
* Container Queries
* Anchor Positioning
* Modern Layout
* View Transitions
* Scroll-driven Animations
* CSS как execution-free UI engine

## Глава 4. JavaScript как Platform Orchestration Layer

* ECMAScript Modules
* Event Loop
* Tasks
* Microtasks
* Rendering
* DOM
* Events
* Fetch
* Streams
* URL
* Navigation
* Web APIs
* JavaScript architecture

## Глава 5. Web APIs

* File System Access
* OPFS
* IndexedDB
* Cache API
* Clipboard
* Notifications
* Permissions
* Geolocation
* Camera
* Microphone
* Bluetooth
* WebSockets
* WebRTC
* Web Workers
* Service Workers
* WebGPU
* WebNN

---

# Часть II. Application Architecture

## Глава 6. Что такое Application Architecture

* Application vs Website
* Application vs Framework
* Application vs Runtime
* Architecture boundaries
* Components
* Features
* Services
* State
* Data
* Execution

## Глава 7. Component Architecture

* Native Components
* Web Components
* Custom Elements
* Shadow DOM
* Slots
* Templates
* ElementInternals
* Form-associated elements
* Component contracts
* Component composition

## Глава 8. State Architecture

* Local state
* UI state
* Server state
* URL state
* Persistent state
* Shared state
* Derived state
* Signals
* Fine-grained reactivity

## Глава 9. Application Data Flow

```text
User
 ↓
UI
 ↓
Event
 ↓
State
 ↓
Application Logic
 ↓
Data Layer
 ↓
Network / Storage
 ↓
Server
```

* Unidirectional data flow
* Reactive data flow
* Event-driven architecture
* Signals
* Commands
* Events
* Resources
* Caching
* Synchronization

## Глава 10. Application Boundaries

* UI boundary
* Runtime boundary
* Data boundary
* Network boundary
* Security boundary
* Server boundary
* Worker boundary
* WASM boundary
* GPU boundary

---

# Часть III. Rendering and Application Delivery

## Глава 11. Browser Rendering Pipeline

* HTML parsing
* DOM
* CSSOM
* Render Tree
* Style
* Layout
* Paint
* Composite
* GPU
* JavaScript execution
* WASM execution
* Rendering bottlenecks

## Глава 12. Rendering Architectures

* MPA
* SPA
* SSR
* CSR
* SSG
* Streaming SSR
* Partial Rendering
* Islands
* Selective Hydration
* Progressive Hydration
* Resumability

## Глава 13. Hydration and Resumability

* Why hydration is expensive
* Hydration boundaries
* Partial hydration
* Lazy hydration
* Resumability
* Serialized state
* Event replay
* Runtime activation

## Глава 14. Navigation Architecture

* URLs
* History API
* Navigation API
* Client navigation
* Server navigation
* MPA navigation
* SPA navigation
* Hybrid navigation
* View Transitions
* Navigation state

## Глава 15. Progressive Delivery

* Code Splitting
* Lazy Loading
* Preloading
* Prefetching
* Speculation Rules
* Resource priorities
* Streaming
* Progressive hydration
* Progressive runtime
* Progressive WebAssembly

---

# Часть IV. JavaScript Application Architecture

## Глава 16. JavaScript Runtime Architecture

* Modules
* Bundling
* Runtime
* Dependencies
* Execution cost
* Main Thread
* Long Tasks
* Scheduling
* Memory

## Глава 17. Reactive Applications

* Signals
* Computed values
* Effects
* Dependency graphs
* Fine-grained reactivity
* State propagation
* Reactive DOM
* Signals vs Virtual DOM

## Глава 18. Framework Architectures

* Angular
* React
* Vue
* Svelte
* Solid
* Qwik
* Astro
* Next.js
* Nuxt
* Server Components
* Islands
* Resumability
* Compiler-first architectures

## Глава 19. Choosing a Framework

* When a framework is useful
* When a framework is unnecessary
* Platform-first architecture
* Framework-first architecture
* Compiler-first architecture
* Server-first architecture
* Hybrid architecture
* Decision matrix

---

# Часть V. WebAssembly Application Architecture

## Глава 20. WebAssembly как второй Execution Layer

* WebAssembly overview
* WASM binary format
* WASM virtual machine
* Modules
* Functions
* Memory
* Imports
* Exports
* JavaScript ↔ WASM

## Глава 21. Когда использовать WASM

* Algorithms
* Image processing
* Audio
* Video
* Cryptography
* Compression
* Parsing
* Data processing
* Simulation
* Scientific computing
* Business logic

## Глава 22. JavaScript ↔ WebAssembly

```text
JavaScript
    │
    ├── call
    ▼
WebAssembly
    │
    ├── memory
    ├── exports
    └── result
    │
    ▼
JavaScript
```

* Imports
* Exports
* Typed Arrays
* Linear Memory
* Serialization
* Zero-copy
* Interop cost
* Ownership
* Error handling

## Глава 23. WASM Memory Architecture

* Linear Memory
* JS Heap
* Typed Arrays
* ArrayBuffer
* SharedArrayBuffer
* Memory ownership
* Allocation
* Deallocation
* Memory growth
* Zero-copy design

## Глава 24. WASM Workers

* Main Thread
* Worker
* WASM
* Message passing
* SharedArrayBuffer
* Atomics
* Worker pools
* Parallel computation
* Multithreading

## Глава 25. WASM + WebGPU

* CPU vs GPU
* WebGPU
* WASM
* GPU buffers
* WGSL
* Compute pipelines
* Image processing
* Scientific visualization
* Simulation
* Browser GPU architecture

## Глава 26. WebAssembly Component Model

* Module Model
* Component Model
* WIT
* Interfaces
* Canonical ABI
* Composition
* Language-independent components
* WASI
* Component architecture

---

# Часть VI. Progressive Enhancement 2.0

## Глава 27. Progressive Enhancement

* История Progressive Enhancement
* HTML First
* CSS First
* JavaScript Last
* Graceful Degradation
* Accessibility
* Offline
* Network resilience

## Глава 28. Progressive Runtime

* Runtime boundaries
* Runtime islands
* Lazy runtime
* Runtime activation
* Partial runtime
* Zero-runtime architecture
* Client execution budgets

## Глава 29. Progressive WebAssembly

* Lazy WASM
* WASM code splitting
* WASM preloading
* WASM caching
* Progressive activation
* WASM Workers
* Progressive computational capabilities

## Глава 30. Platform-Native Applications

* Native HTML
* Native CSS
* Native Web APIs
* Web Components
* JS orchestration
* WASM computation
* Browser capabilities
* Minimal framework layer

---

# Часть VII. Data Architecture

## Глава 31. Web Application Data

* Server data
* Client data
* Local data
* Remote data
* Derived data
* Cached data
* URL data

## Глава 32. Browser Storage

* Cookies
* localStorage
* sessionStorage
* IndexedDB
* Cache API
* OPFS
* Storage quotas
* Persistence
* Eviction

## Глава 33. Network Data

* Fetch
* HTTP
* HTTP caching
* Streams
* WebSockets
* WebTransport
* WebRTC
* Server-Sent Events
* Network resilience

## Глава 34. Data Synchronization

* Optimistic UI
* Offline-first
* Conflict resolution
* Synchronization
* Cache invalidation
* Local-first architecture
* Event-driven synchronization

---

# Часть VIII. Server Architecture

## Глава 35. Modern Web Server

* HTTP
* Request / Response
* Routing
* Middleware
* Sessions
* Authentication
* Authorization
* Validation

## Глава 36. Backend Application Architecture

* Monolith
* Modular Monolith
* Microservices
* Serverless
* Edge Functions
* Workers
* Event-driven backend

## Глава 37. API Architecture

* REST
* RPC
* GraphQL
* WebSockets
* Webhooks
* Streaming APIs
* API versioning
* API contracts
* Type-safe APIs

## Глава 38. Server Rendering

* SSR
* Streaming
* Server Components
* Server Actions
* HTML generation
* Data loading
* Server/client boundaries

---

# Часть IX. Database and Persistence

## Глава 39. Database Architecture

* Relational databases
* PostgreSQL
* MySQL
* Document databases
* Key-value stores
* Graph databases
* Search engines

## Глава 40. Application Data Model

* Entities
* Relations
* Transactions
* Constraints
* Indexes
* Migrations
* ORM
* Query builders

## Глава 41. Distributed Data

* Replication
* Sharding
* Caching
* Event sourcing
* CQRS
* Message queues
* Event streams
* Consistency

---

# Часть X. Authentication and Security

## Глава 42. Web Security Model

* Origin
* Same-Origin Policy
* Site Isolation
* CORS
* CSP
* Trusted Types
* Permissions
* Secure Contexts

## Глава 43. Application Authentication

* Sessions
* Cookies
* OAuth
* OpenID Connect
* Passkeys
* WebAuthn
* MFA
* Token-based authentication

## Глава 44. Application Authorization

* RBAC
* ABAC
* Permissions
* Capabilities
* Resource ownership
* Multi-tenant authorization

## Глава 45. WebAssembly Security

* WASM sandbox
* Memory isolation
* Unsafe native code
* Buffer vulnerabilities
* Dependency security
* Supply-chain attacks
* WASM capability boundaries

WebAssembly не является автоматически безопасным только потому, что выполняется в sandbox. Ошибки памяти и уязвимости самого WASM-модуля остаются частью модели угроз. Современные исследования отдельно рассматривают buffer overflows, use-after-free и цепочки атак, проходящие через WASM в Web Application.

---

# Часть XI. Performance Architecture

## Глава 46. Performance Model

* Network cost
* CPU cost
* Memory cost
* JavaScript cost
* WASM cost
* Rendering cost
* GPU cost
* Server cost

## Глава 47. Core Web Vitals

* LCP
* INP
* CLS
* Performance budgets
* Real User Monitoring
* Field data
* Lab data

## Глава 48. JavaScript Performance

* Bundle size
* Code splitting
* Tree shaking
* Lazy execution
* Long Tasks
* Main Thread contention
* Garbage Collection

## Глава 49. WebAssembly Performance

* Startup
* Compilation
* Instantiation
* Function calls
* JS/WASM boundary
* Memory copies
* Zero-copy
* Worker execution
* SIMD
* Multithreading

## Глава 50. GPU Performance

* GPU pipelines
* WebGPU
* Compute shaders
* GPU memory
* CPU/GPU synchronization
* Data transfer
* Rendering budgets

---

# Часть XII. AI-Native Web Applications

## Глава 51. AI в Web Application

* AI APIs
* Browser AI
* Server AI
* Local AI
* Hybrid AI
* AI-assisted UI
* AI-powered application logic

## Глава 52. AI Agents как Application Components

* Agent
* Tool
* Context
* Memory
* Planning
* Execution
* Permissions
* Human-in-the-loop

## Глава 53. AI + Web Platform

* Web APIs
* WebGPU
* WebAssembly
* Local inference
* Streaming generation
* Structured output
* Browser privacy

## Глава 54. AI Application Architecture

```text
                 Web Application
                       │
             ┌─────────┴─────────┐
             │                   │
          Human              AI Agent
             │                   │
             └─────────┬─────────┘
                       │
                    Tools
                       │
          ┌────────────┼────────────┐
          │            │            │
        Browser       Server       Data
          │            │            │
       Web APIs       APIs       Database
```

---

# Часть XIII. Offline and Distributed Web Applications

## Глава 55. Service Workers

* Installation
* Activation
* Fetch interception
* Cache
* Update lifecycle
* Background capabilities

## Глава 56. Offline-first Architecture

* Offline UI
* Local persistence
* Synchronization
* Retry
* Conflict resolution
* Network-aware applications

## Глава 57. PWA Architecture

* Manifest
* Installation
* Service Worker
* Storage
* Offline
* Push
* Background processing

---

# Часть XIV. Application Observability

## Глава 58. Errors

* JavaScript errors
* WASM errors
* Network errors
* Server errors
* Error boundaries
* Source maps
* Debugging production applications

## Глава 59. Logging and Tracing

* Structured logs
* Browser telemetry
* Server telemetry
* Distributed tracing
* Correlation IDs

## Глава 60. Performance Observability

* PerformanceObserver
* Resource Timing
* Navigation Timing
* Long Tasks
* User Timing
* Core Web Vitals
* WASM profiling
* GPU profiling

---

# Часть XV. Deployment and Infrastructure

## Глава 61. Build Architecture

```text
Source
   ↓
Compiler
   ↓
Static Analysis
   ↓
Dependency Graph
   ↓
Optimization
   ↓
JS / CSS / HTML / WASM
   ↓
Assets
   ↓
Deployment
```

## Глава 62. Modern Build Systems

* Bundlers
* Compilers
* Transpilers
* Minifiers
* Tree shaking
* Code splitting
* Asset pipelines
* WASM pipelines

## Глава 63. CDN and Edge

* CDN
* Edge caching
* Edge compute
* Geographic distribution
* Cache invalidation
* HTTP caching

## Глава 64. Containers and Cloud

* Containers
* Kubernetes
* Serverless
* Managed services
* Object storage
* Databases
* Queues
* Observability

## Глава 65. CI/CD

* Git
* Build
* Test
* Security scanning
* Artifact generation
* Deployment
* Rollback
* Feature flags

---

# Часть XVI. Testing Modern Web Applications

## Глава 66. Testing Pyramid

* Unit
* Integration
* Component
* Browser
* End-to-end
* Contract
* Load testing

## Глава 67. Testing Web Platform Features

* Browser automation
* Web APIs
* Workers
* Service Workers
* Storage
* Navigation
* View Transitions

## Глава 68. Testing WASM

* WASM unit tests
* JS/WASM integration
* Memory tests
* Worker tests
* Performance tests
* Cross-browser testing

## Глава 69. Testing Real Application Flows

* Authentication
* Navigation
* Forms
* Network failures
* Offline
* Slow devices
* Mobile browsers
* Production-like environments

---

# Часть XVII. Architecture Patterns

## Глава 70. SPA Architecture

* Advantages
* Costs
* When appropriate
* When inappropriate

## Глава 71. MPA Architecture

* HTML navigation
* Server rendering
* Forms
* Progressive Enhancement

## Глава 72. Islands Architecture

* Islands
* Partial hydration
* Server-first UI
* Runtime boundaries

## Глава 73. Resumable Architecture

* Serialization
* Resumability
* Lazy execution
* Event recovery

## Глава 74. Platform-Native Architecture

```text
HTML
 +
CSS
 +
Web APIs
 +
Web Components
 +
JavaScript
 +
WASM
 +
Workers
 +
WebGPU
```

* Zero replacement
* Native capabilities
* Minimal runtime
* Progressive execution

## Глава 75. Hybrid Architecture

```text
HTML
   +
CSS
   +
Native Browser APIs
   +
JavaScript
   +
Optional Framework
   +
Optional WASM
   +
Server
```

* When to combine approaches
* Architecture boundaries
* Migration from legacy applications

---

# Часть XVIII. Emerge as a Case Study

## Глава 76. Why Build Another Framework?

* Framework saturation
* Platform evolution
* Abstraction costs
* HTML-first architecture
* Compiler-first architecture
* Progressive runtime

## Глава 77. Emerge Architecture

```text
                         APPLICATION
                              │
                              ▼
                    ┌─────────────────┐
                    │     Emerge      │
                    │                 │
                    │ Components      │
                    │ Signals         │
                    │ Compiler        │
                    │ Router          │
                    │ Data            │
                    │ Runtime         │
                    │ WASM            │
                    └────────┬────────┘
                             │
                 ┌───────────┴───────────┐
                 ▼                       ▼
        JavaScript Execution     WebAssembly Execution
                 │                       │
                 └───────────┬───────────┘
                             ▼
                       Web Platform
```

## Глава 78. Emerge Compiler

* AST
* Static analysis
* Dependency graph
* Signals
* Code generation
* Tree shaking
* JS target
* WASM target
* Execution-layer selection

## Глава 79. Emerge Runtime

* Progressive runtime
* Runtime boundaries
* Components
* Signals
* Router
* Data
* Hydration
* Lazy activation

## Глава 80. Emerge WASM Architecture

* WASM loader
* Bindings
* Memory
* JS ↔ WASM
* Lazy WASM
* WASM Workers
* WASM Components
* WebGPU integration

## Глава 81. Emerge Repository Architecture

```text
emerge/
│
├── packages/
│   ├── core/
│   ├── signals/
│   ├── compiler/
│   ├── runtime/
│   ├── router/
│   ├── data/
│   ├── wasm/
│   ├── wasm-bindings/
│   ├── wasm-components/
│   ├── client/
│   ├── server/
│   └── cli/
│
├── internal/
├── integrations/
├── examples/
├── benchmarks/
├── tests/
└── docs/
```

Эта архитектура уже формализована в отдельной спецификации Emerge Framework.

---

# Часть XIX. Choosing an Architecture

## Глава 82. Architecture Decision Framework

Перед выбором технологии необходимо определить:

```text
1. What is the UI?
2. What is the state?
3. Where does data live?
4. Where does computation happen?
5. Where does rendering happen?
6. What must work without JavaScript?
7. What requires JavaScript?
8. What requires WASM?
9. What requires Workers?
10. What requires GPU?
11. What belongs on the server?
```

## Глава 83. Architecture Decision Matrix

Сравнение:

* MPA
* SPA
* SSR
* SSG
* Islands
* Resumability
* Server Components
* Platform-Native
* Hybrid

По критериям:

* startup;
* runtime;
* complexity;
* SEO;
* accessibility;
* offline;
* performance;
* developer experience;
* scalability;
* WASM integration;
* Web Platform alignment.

## Глава 84. Migration Architecture

* Legacy MPA → modern Web
* jQuery → Web Platform
* SPA → SSR
* SPA → Islands
* Framework → Web Components
* JavaScript → CSS / HTML
* JavaScript → WASM
* Monolith → modular architecture
* Legacy backend → modern API

---

# Часть XX. Building a Modern Web Application

## Глава 85. Project Architecture

Создание приложения с нуля:

```text
application/
├── ui/
├── components/
├── state/
├── data/
├── services/
├── workers/
├── wasm/
├── server/
└── infrastructure/
```

## Глава 86. HTML and CSS Foundation

* Semantic HTML
* Forms
* Responsive UI
* Container Queries
* Design Tokens
* Accessibility

## Глава 87. JavaScript Layer

* Modules
* Events
* State
* Data fetching
* Navigation
* Browser APIs

## Глава 88. WASM Layer

* Identify computational boundaries
* Select language
* Build module
* Define interface
* JS/WASM interop
* Lazy loading
* Worker execution

## Глава 89. Server Layer

* HTTP
* API
* Authentication
* Database
* Cache
* Server rendering

## Глава 90. Production

* Build
* Tests
* Security
* Performance
* Observability
* CDN
* Deployment
* Monitoring

---

# Часть XXI. Final Architecture

## Глава 91. The Modern Web Application Model

Финальная модель:

```text
                         USER
                           │
                           ▼
                  ┌─────────────────┐
                  │  WEB APPLICATION│
                  └────────┬────────┘
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
      Presentation      Application       Data
          │                │                │
      HTML / CSS       JS / WASM        Fetch / Storage
          │                │                │
          └────────────────┼────────────────┘
                           │
                    ┌──────▼──────┐
                    │ Web Platform│
                    └──────┬──────┘
                           │
            ┌──────────────┼──────────────┐
            │              │              │
         Browser        Workers         WebGPU
            │              │              │
            └──────────────┼──────────────┘
                           │
                       Network
                           │
                           ▼
                    ┌──────────────┐
                    │Server / Cloud│
                    └──────┬───────┘
                           │
                  ┌────────┼────────┐
                  │        │        │
               Database   Cache    Queue
```

## Глава 92. The Execution-Layer Model

```text
                         Application
                              │
                              ▼
                    Architecture Layer
                              │
               ┌──────────────┼──────────────┐
               ▼              ▼              ▼
             HTML            JS             WASM
               │              │              │
          Structure       Orchestration   Computation
               │              │              │
               └──────────────┼──────────────┘
                              ▼
                       Web Platform
                              │
                  ┌───────────┼───────────┐
                  ▼           ▼           ▼
               Browser     Workers     WebGPU
```

## Глава 93. The Platform-Native Web Application

Современное приложение должно:

* использовать HTML вместо JavaScript там, где это возможно;
* использовать CSS вместо JS для presentation behavior;
* использовать Web APIs вместо framework abstractions;
* использовать Web Components для native component boundaries;
* использовать JavaScript для orchestration;
* использовать WebAssembly для подходящих вычислительных задач;
* использовать Workers для background execution;
* использовать WebGPU для GPU workloads;
* использовать сервер для server-side responsibilities;
* использовать database для persistence;
* использовать compiler для уменьшения runtime work;
* использовать Progressive Enhancement для постепенного расширения возможностей.

---

# 🧠 Главный архитектурный принцип книги

Современное Web Application — это **не JavaScript application, запущенное внутри браузера**.

Это:

> **Application, построенное поверх Web Platform и распределяющее работу между несколькими execution environments.**

```text
HTML
   → structure

CSS
   → presentation

JavaScript
   → orchestration

WebAssembly
   → computation

Workers
   → concurrency

WebGPU
   → GPU computation

Web APIs
   → native capabilities

Server
   → network-side application logic

Database
   → persistence
```

---

# 🔗 Связь с другими книгами

`Modern Web Application 2026` является **системообразующей книгой** серии.

Она использует результаты:

* **Modern HTML 2026** — HTML как декларативный API Web Platform;
* **Modern CSS 2026** — CSS как полноценный UI/layout engine;
* **Modern JavaScript 2026** — JavaScript как язык orchestration;
* **Modern Web Browsers 2026** — Browser как application platform;
* **Modern Web Frameworks 2026** — архитектуры современных frameworks;
* **WebAssembly as a Modern Web Platform 2026** — второй execution layer;
* **Create Your Own Progressive Enhancement Framework 2026** — Emerge как практическая реализация Platform-Native Architecture.

Таким образом:

```text
Modern HTML
      │
Modern CSS
      │
Modern JavaScript
      │
Modern Web Browsers
      │
WebAssembly
      │
Modern Web Frameworks
      │
      ▼
Modern Web Application
      │
      ▼
Create Your Own Progressive Enhancement Framework
      │
      ▼
Emerge
```

При этом Emerge не является обязательным ответом на каждую архитектурную задачу. Он используется здесь как **case study**, показывающий, как описанные принципы можно превратить в конкретный framework architecture. Это важное различие между этой книгой и книгой про создание Emerge.

---

# 🎯 После прочтения книги

Читатель должен уметь:

* проектировать Web Application как целостную систему;
* понимать границы Browser и Server;
* использовать Web Platform непосредственно;
* выбирать между MPA, SPA, SSR, SSG, Islands и Resumability;
* проектировать component architecture;
* проектировать state и data flow;
* понимать JavaScript runtime;
* использовать Signals;
* определять, когда нужен WebAssembly;
* проектировать JS ↔ WASM interop;
* использовать WASM Workers;
* понимать WASM Component Model;
* применять WebGPU;
* проектировать offline-first приложения;
* строить security model;
* проектировать database и backend architecture;
* измерять performance;
* строить observability;
* организовывать CI/CD;
* проектировать AI-enabled applications;
* выбирать framework только после понимания Web Platform;
* проектировать Platform-Native Applications.

---

# 🧭 Главная формула

```text
Modern Web Application
=
Web Platform
+
Application Architecture
+
Execution Architecture
+
Data Architecture
+
Server Architecture
+
Security
+
Performance
+
Delivery
+
Observability
```

А execution architecture всё чаще выглядит так:

```text
                    Application
                         │
             ┌───────────┼───────────┐
             ▼           ▼           ▼
            HTML         JS         WASM
             │           │           │
        structure    orchestration computation
             │           │           │
             └───────────┼───────────┘
                         ▼
                  Web Platform
                         │
              ┌──────────┼──────────┐
              ▼          ▼          ▼
           Browser    Workers     WebGPU
```

---

# 🚀 Final Thesis

> **The modern Web application is not a framework application running on a browser.**
>
> **It is a platform-native system built on top of the Web Platform.**

В этом смысле будущее Web Application определяется не ростом количества framework abstractions, а способностью архитектуры **правильно использовать возможности самой платформы**.

```text
HTML
+
CSS
+
Web APIs
+
JavaScript
+
WebAssembly
+
Workers
+
WebGPU
+
Server
+
Data
```

Именно это и является предметом **Modern Web Application 2026**.

---

# 📄 License

The book is distributed under Creative Commons Attribution 4.0 International.

Code examples are distributed under the MIT License.

---

# 🤝 Contributing

Contributions are welcome.

You can contribute through:

* Issues
* Discussions
* Pull Requests
* Architecture proposals
* Examples
* Experiments
* Benchmarks
* Web Platform research
* WebAssembly experiments
* Security research
* Performance research

---

# 🚧 Project Status

**Status:** Research / Architecture / Writing

**Target:** 2026+

**Core thesis:**

> **The Web Platform is no longer merely the environment in which a Web Application runs. It is the foundation on which the application should be architected.**
