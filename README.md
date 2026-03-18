# 🟣 Laravel Packages Directory — Comprehensive Reference

> **A deep-dive reference of Laravel & PHP packages across 43 categories.**
> Maintained for PurplePractice and the broader Laravel ecosystem.
> Last updated: March 2026 · Compiled with live web research.

---

## Table of Contents

1. [ORM, Migrations, Seeding & Databases (SQL & NoSQL)](#1-orm-migrations-seeding--databases-sql--nosql)
2. [Authentication](#2-authentication)
3. [Authorization — RBAC & ABAC](#3-authorization--rbac--abac)
4. [Multi-Tenancy](#4-multi-tenancy)
5. [UI & Frontend](#5-ui--frontend)
6. [AI & Laravel](#6-ai--laravel)
7. [Testing & Debugging](#7-testing--debugging)
8. [PDF Generation](#8-pdf-generation)
9. [DOCX Generation](#9-docx-generation)
10. [Excel Generation](#10-excel-generation)
11. [JSON Exporting](#11-json-exporting)
12. [ZIP File Export](#12-zip-file-export)
13. [Payments & Payment Gateways](#13-payments--payment-gateways)
14. [Activity Logs](#14-activity-logs)
15. [Audit Trail](#15-audit-trail)
16. [Event Sourcing](#16-event-sourcing)
17. [FHIR API & FHIR Tools](#17-fhir-api--fhir-tools)
18. [WYSIWYG Editors](#18-wysiwyg-editors)
19. [Markdown Editors](#19-markdown-editors)
20. [Email — IMAP & POP (Reading Mailboxes)](#20-email--imap--pop-reading-mailboxes)
21. [Email Sending & SMTP](#21-email-sending--smtp)
22. [S3 & File Storage](#22-s3--file-storage)
23. [Caching](#23-caching)
24. [Queue, Tasks, Commands & Scheduling](#24-queue-tasks-commands--scheduling)
25. [Media & Image Manipulation/Management](#25-media--image-manipulationmanagement)
26. [REST API](#26-rest-api)
27. [Webhooks](#27-webhooks)
28. [GraphQL](#28-graphql)
29. [Search Engines](#29-search-engines)
30. [Optimizing](#30-optimizing)
31. [Monetization](#31-monetization)
32. [Localization](#32-localization)
33. [3rd Party Services Integration](#33-3rd-party-services-integration)
34. [Hosting](#34-hosting)
35. [Forms](#35-forms)
36. [Charts](#36-charts)
37. [AI Integration](#37-ai-integration)
38. [Official Laravel Packages](#38-official-laravel-packages)
39. [Medical PHP & Laravel Packages](#39-medical-php--laravel-packages)
40. [IoT & Hardware](#40-iot--hardware)
41. [eCommerce](#41-ecommerce)
42. [Barcode Generation](#42-barcode-generation)
43. [Signature Collection](#43-signature-collection)

---

## 1. ORM, Migrations, Seeding & Databases (SQL & NoSQL)

### Core (Built-in Laravel)

| Package | Composer | Notes |
|---------|----------|-------|
| **Eloquent ORM** | `illuminate/database` | Built-in; ActiveRecord ORM with relationships, scopes, observers |
| **Laravel Migrations** | built-in | Schema version control via `php artisan migrate` |
| **Laravel Seeding** | built-in | `DatabaseSeeder` + Model Factories |
| **Laravel Query Builder** | built-in | Fluent chainable SQL builder |
| **Database Factories** | built-in | Fake data via Faker |

### SQL Drivers & Extensions

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel MySQL** | built-in | Full MySQL 5.7+ / MariaDB support |
| **Laravel PostgreSQL** | built-in | Full PostgreSQL 13+ support including JSONB |
| **Laravel SQLite** | built-in | Lightweight; great for testing |
| **Laravel SQL Server** | built-in | MSSQL via `sqlsrv` driver |
| **Doctrine DBAL** | `doctrine/dbal` | Column renaming in migrations; schema introspection |
| **Laragear/Rawsql** | `laragear/rawsql` | Safely inject raw SQL fragments |
| **staudenmeir/eloquent-has-many-deep** | `staudenmeir/eloquent-has-many-deep` | Multi-level Eloquent relationships |
| **staudenmeir/eloquent-json-relations** | `staudenmeir/eloquent-json-relations` | Eloquent relationships via JSON columns |
| **calebporzio/sushi** | `calebporzio/sushi` | Eloquent models backed by in-memory arrays |
| **Kirschbaum-Development/eloquent-uuid** | `laravel/concerns` | UUID primary keys trait |
| **laravel/eloquent-sluggable** | `cviebrock/eloquent-sluggable` | Auto slug generation for models |
| **Kirschbaum/eloquent-sortable** | `spatie/eloquent-sortable` | Sortable Eloquent models |

### NoSQL Drivers

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel MongoDB** | `mongodb/laravel-mongodb` | Official MongoDB Eloquent driver (v5+); replaces jenssegers |
| **jenssegers/mongodb** | `jenssegers/mongodb` | Legacy; superseded by official `mongodb/laravel-mongodb` |
| **Laravel Redis** | built-in | Redis via `predis/predis` or `phpredis` |
| **Predis** | `predis/predis` | Pure PHP Redis client |
| **Laravel Elasticsearch** | `elasticsearch/elasticsearch` | Official Elasticsearch PHP client |
| **laravel-scout-elastic** | `babenkoivan/elastic-scout-driver` | Laravel Scout driver for Elasticsearch |
| **jenssegers/laravel-cassandra** | `dukenst2006/cassandra` | Cassandra driver for Laravel |
| **awobaz/compoships** | `awobaz/compoships` | Composite key Eloquent relationships |
| **FirebaseServiceProvider** | `kreait/laravel-firebase` | Google Firebase / Firestore in Laravel |
| **tightenco/parental** | `tightenco/parental` | Single Table Inheritance for Eloquent |

### Migration Tooling

| Package | Composer | Notes |
|---------|----------|-------|
| **ibers/laravel-migrations-generator** | `kitloong/laravel-migrations-generator` | Reverse-engineer existing DB to migrations |
| **spatie/laravel-db-snapshots** | `spatie/laravel-db-snapshots` | Create and restore DB snapshots |
| **brianium/paratest** | `brianium/paratest` | Parallel DB seeding for tests |
| **orangehill/iseed** | `orangehill/iseed` | Reverse seed generator from DB data |
| **dg/bypass-finals** | `dg/bypass-finals` | Bypass final class restrictions in tests |

---

## 2. Authentication

### Official Laravel Starter Kits

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Breeze** | `laravel/breeze` | Minimal auth scaffolding; Blade, Inertia/React, Inertia/Vue or API |
| **Laravel Jetstream** | `laravel/jetstream` | Full-featured; teams, 2FA, sessions; Livewire or Inertia |
| **Laravel Fortify** | `laravel/fortify` | Headless auth backend; used by Jetstream under the hood |
| **Laravel Sanctum** | `laravel/sanctum` | SPA & mobile token auth; built-in since Laravel 8 |
| **Laravel Passport** | `laravel/passport` | Full OAuth2 server implementation |
| **Laravel Socialite** | `laravel/socialite` | OAuth login via GitHub, Google, Facebook, Twitter, etc. |

### JWT & Token Auth

| Package | Composer | Notes |
|---------|----------|-------|
| **tymon/jwt-auth** | `tymon/jwt-auth` | JWT authentication for APIs |
| **firebase/php-jwt** | `firebase/php-jwt` | Low-level JWT library |
| **lcobucci/jwt** | `lcobucci/jwt` | Standards-compliant JWT (RS256/ES256 support) |

### SSO & Enterprise Auth

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel SAML2** | `aacotroneo/laravel-saml2` | SAML2 SP integration |
| **socialiteproviders/** | `socialiteproviders/*` | 100+ OAuth providers (Azure AD, Keycloak, LDAP, etc.) |
| **LdapRecord-Laravel** | `directorytree/ldaprecord-laravel` | Full Active Directory / LDAP authentication |
| **Keycloak Web Guard** | `robsontenorio/laravel-keycloak-web-guard` | Keycloak SSO for web |
| **Keycloak Bearer** | `robsontenorio/laravel-keycloak-bearer-user-provider` | Keycloak JWT bearer tokens for APIs |

### 2FA & Security

| Package | Composer | Notes |
|---------|----------|-------|
| **pragmarx/google2fa-laravel** | `pragmarx/google2fa-laravel` | TOTP 2-factor authentication |
| **spatie/laravel-login-link** | `spatie/laravel-login-link` | Magic link login (dev/testing) |
| **yadahan/laravel-authentication-log** | `yadahan/laravel-authentication-log` | Log all login attempts with device/IP |

---

## 3. Authorization — RBAC & ABAC

### RBAC Packages

| Package | Composer | Notes |
|---------|----------|-------|
| **spatie/laravel-permission** | `spatie/laravel-permission` | De facto standard; roles + permissions; DB-driven; cacheable |
| **silber/bouncer** | `silber/bouncer` | Fluent RBAC with scopes; code-first ability definitions |
| **Filament Shield** | `bezhansalleh/filament-shield` | Auto-generates Filament permissions from policies |
| **binary-cats/laravel-rbac** | `binary-cats/laravel-rbac` | Opinionated RBAC extension on top of Spatie Permission |
| **laratrust/laratrust** | `santigarcor/laratrust` | Roles & permissions with team support |

### ABAC & Policy-Based

| Package | Composer | Notes |
|---------|----------|-------|
| **php-casbin/laravel-authz** | `php-casbin/laravel-authz` | Casbin-based ACL / RBAC / ABAC for Laravel |
| **casbin/laravel-rbac** | `casbin/laravel-rbac` | ACL, RBAC, ABAC via Casbin policy language |
| **Laravel Gates & Policies** | built-in | Closure-based gates; class-based Policies |
| **laravel/telescope** | `laravel/telescope` | Inspect gate/policy decisions in dev |

---

## 4. Multi-Tenancy

| Package | Composer | Notes |
|---------|----------|-------|
| **stancl/tenancy** | `stancl/tenancy` | ⭐ Most feature-rich; schema-per-tenant or DB-per-tenant; auto-bootstraps connections, cache, filesystem, queues, Redis |
| **spatie/laravel-multitenancy** | `spatie/laravel-multitenancy` | Lightweight; bare essentials; single or multi DB; tenant-aware jobs and artisan |
| **tenancy/tenancy** | `tenancy/tenancy` | Highly customizable; event-driven hooks; good for non-standard setups |
| **gecche/laravel-multidomain** | `gecche/laravel-multidomain` | Domain-based tenancy with separate env files per domain |
| **romegadigital/multitenancy** | `romegadigital/multitenancy` | Subdomain-based tenancy; simpler feature set |
| **archtechx/tenancy** | `archtechx/tenancy` | SaaS boilerplate template (commercial) built on stancl/tenancy |

---

## 5. UI & Frontend

### Admin Panels & CRUD

| Package | Composer / NPM | Notes |
|---------|----------------|-------|
| **Filament** | `filament/filament` | ⭐ Best-in-class admin panel; v3 with panels, forms, tables, widgets |
| **Laravel Nova** | `laravel/nova` (commercial) | Official; polished admin panel; $299/project |
| **Backpack for Laravel** | `backpack/crud` | CRUD admin with many add-ons (commercial options) |
| **Orchid Platform** | `orchid/platform` | Admin/CMS panel with screens API |
| **Laravel Voyager** | `tcg/voyager` | Simple admin with media manager |
| **Laravel Boilerplate** | `rappasoft/laravel-boilerplate` | Starter with roles, permissions, admin |

### Full-Stack UI Frameworks

| Package | Composer / NPM | Notes |
|---------|----------------|-------|
| **Inertia.js** | `inertiajs/inertia-laravel` + `@inertiajs/react` | SPA-like apps without separate API; React, Vue, Svelte |
| **Laravel Livewire** | `livewire/livewire` | Reactive server-driven components; no JS required |
| **Laravel Blade** | built-in | Blade templating engine |
| **Alpine.js** | `alpinejs` (npm) | Lightweight JS for Blade/Livewire |

### UI Component Libraries

| Package | NPM | Notes |
|---------|-----|-------|
| **IBM Carbon Design** | `@carbon/react` | Clinical-grade; accessible; used for PurplePractice clinical modules |
| **shadcn/ui** | via CLI | Radix primitives + Tailwind; excellent for portals |
| **Tailwind CSS** | `tailwindcss` | Utility-first CSS; standard in modern Laravel |
| **Headless UI** | `@headlessui/react` | Unstyled accessible components for React/Vue |
| **Flowbite** | `flowbite` | Tailwind component library with Blade support |
| **Preline UI** | `preline` | Tailwind component library |
| **daisyUI** | `daisyui` | Tailwind plugin with component classes |

### Asset Bundling

| Package | Composer / NPM | Notes |
|---------|----------------|-------|
| **Vite** | `laravel/vite-plugin` (npm) | Official; fast HMR; replaces Mix in Laravel 9+ |
| **Laravel Mix** | `laravel-mix` (npm) | Legacy webpack wrapper; still maintained |

---

## 6. AI & Laravel

> See also [Section 37 — AI Integration](#37-ai-integration) for client packages.

| Package | Composer | Notes |
|---------|----------|-------|
| **openai-php/laravel** | `openai-php/laravel` | Official OpenAI PHP client with Laravel facade |
| **prism-php/prism** | `prism-php/prism` | Multi-provider AI (OpenAI, Claude, Gemini) with tool calling |
| **echolabs/prism** | `echolabs/prism` | Structured AI output, streaming, embeddings |
| **anthropics/anthropic-sdk-php** | `anthropic/sdk` | Official Anthropic Claude PHP SDK |
| **cloudstudio/ollama-laravel** | `cloudstudio/ollama-laravel` | Run local models via Ollama |
| **laravel-ai/laravel-ai** | `laravel-ai/laravel-ai` | Abstraction layer for multiple AI providers |
| **spatie/laravel-ai-translator** | `spatie/laravel-ai-translator` | AI-powered translation strings |
| **gehrisandro/laravel-chatgpt** | `gehrisandro/laravel-chatgpt` | ChatGPT chat interface for Laravel |

---

## 7. Testing & Debugging

### Testing Frameworks

| Package | Composer | Notes |
|---------|----------|-------|
| **Pest PHP** | `pestphp/pest` | ⭐ Modern testing framework; expressive, fast; Laravel plugin available |
| **PHPUnit** | `phpunit/phpunit` | Built-in with Laravel; unit and feature tests |
| **Laravel Dusk** | `laravel/dusk` | Browser automation testing (ChromeDriver) |
| **Mockery** | `mockery/mockery` | Mocking library; built-in with Laravel test suite |

### API & HTTP Testing

| Package | Composer | Notes |
|---------|----------|-------|
| **Saloon** | `saloonphp/saloon` | HTTP client with built-in testing/mocking for APIs |
| **pestphp/pest-plugin-laravel** | `pestphp/pest-plugin-laravel` | Laravel-specific Pest helpers |
| **pestphp/pest-plugin-livewire** | `pestphp/pest-plugin-livewire` | Pest helpers for Livewire |
| **nunomaduro/collision** | `nunomaduro/collision` | Beautiful error reporting in terminal |

### Debugging & Profiling

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Telescope** | `laravel/telescope` | ⭐ Debug assistant; requests, queries, jobs, mail, cache |
| **Laravel Debugbar** | `barryvdh/laravel-debugbar` | Debug toolbar in browser |
| **Laravel Ray** | `spatie/laravel-ray` | Desktop debug tool; dump, log, queries |
| **Clockwork** | `itsgoingd/clockwork` | Browser DevTools extension for Laravel profiling |
| **Laravel Log Viewer** | `opcodesio/log-viewer` | Beautiful log viewer in the browser |
| **beyondcode/laravel-query-detector** | `beyondcode/laravel-query-detector` | N+1 query detection |
| **nunomaduro/larastan** | `nunomaduro/larastan` | PHPStan static analysis for Laravel |
| **Enlightn** | `enlightn/enlightn` | Performance & security audit tool |

### Code Quality

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Pint** | `laravel/pint` | Official PHP CS Fixer config for Laravel |
| **phpstan/phpstan** | `phpstan/phpstan` | Static analysis |
| **rector/rector** | `rector/rector` | Automated PHP refactoring |

---

## 8. PDF Generation

| Package | Composer | Notes |
|---------|----------|-------|
| **barryvdh/laravel-dompdf** | `barryvdh/laravel-dompdf` | ⭐ HTML to PDF via DomPDF; most popular |
| **barryvdh/laravel-snappy** | `barryvdh/laravel-snappy` | HTML to PDF/image via wkhtmltopdf/wkhtmltoimage |
| **spatie/laravel-pdf** | `spatie/laravel-pdf` | Modern wrapper around Chromium headless (puppeteer-style); excellent CSS support |
| **niklasravnsborg/laravel-pdf** | `niklasravnsborg/laravel-pdf` | mPDF wrapper for Laravel |
| **Laravel FPDF** | `codedge/laravel-fpdf` | FPDF wrapper |
| **mpdf/mpdf** | `mpdf/mpdf` | Direct mPDF library; RTL/Arabic support |
| **tcpdf/tcpdf** | `tecnickcom/tcpdf` | TCPDF; barcode + image support in PDF |
| **Gotenberg** | `gotenberg/gotenberg-php` | Docker-based PDF service; best fidelity |

---

## 9. DOCX Generation

| Package | Composer | Notes |
|---------|----------|-------|
| **phpoffice/phpword** | `phpoffice/phpword` | ⭐ Full Word document generation; tables, images, headers |
| **openspout/openspout** | `openspout/openspout` | XLSX + DOCX streaming writer |
| **laravel-docx** | `alhaji/laravel-docx` | Blade/template-based DOCX generation |
| **docx-converter** | `dompdf` + `libreoffice` | Convert HTML → DOCX via LibreOffice CLI |
| **PHPDocX** | `phpdocx/phpdocx` (commercial) | Advanced DOCX/ODT generation |

---

## 10. Excel Generation

| Package | Composer | Notes |
|---------|----------|-------|
| **Maatwebsite/Laravel-Excel** | `maatwebsite/excel` | ⭐ Most popular; import/export XLSX, XLS, CSV; Eloquent integration |
| **openspout/openspout** | `openspout/openspout` | Low-memory streaming XLSX/ODS/CSV writer |
| **rap2hpoutre/fast-excel** | `rap2hpoutre/fast-excel` | Fast XLSX export using OpenSpout; minimal memory |
| **phpoffice/phpspreadsheet** | `phpoffice/phpspreadsheet` | Full spreadsheet library; charts, formulae, cell styles |
| **spatie/simple-excel** | `spatie/simple-excel` | Simple, elegant wrapper around OpenSpout |

---

## 11. JSON Exporting

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel API Resources** | built-in | `JsonResource` and `ResourceCollection` for JSON API responses |
| **fractal/fractal** | `league/fractal` | Transformers for JSON output |
| **spatie/laravel-fractal** | `spatie/laravel-fractal` | Laravel wrapper for Fractal |
| **Laravel JSON:API** | `laravel-json-api/laravel` | Full JSON:API spec-compliant responses |
| **JSON:API Resources** | `timacdonald/json-api` | Lightweight JSON:API resource layer |
| **spatie/laravel-data** | `spatie/laravel-data` | Typed DTOs with JSON serialization and validation |

---

## 12. ZIP File Export

| Package | Composer | Notes |
|---------|----------|-------|
| **PHP ZipArchive** | built-in (PHP) | Native PHP ZipArchive; no Composer needed |
| **spatie/laravel-backup** | `spatie/laravel-backup` | Creates ZIP backups of DB + files |
| **chumper/zipper** | `madnest/madzipper` | Simple Zipper for creating/extracting ZIPs |
| **ZipStream-PHP** | `maennchen/zipstream-php` | Stream large ZIPs without writing to disk |
| **stechstudio/laravel-zipstream** | `stechstudio/laravel-zipstream` | ZIP streaming in Laravel responses |

---

## 13. Payments & Payment Gateways

### Stripe

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Cashier (Stripe)** | `laravel/cashier` | ⭐ Official Stripe subscription billing; Stripe Checkout |
| **stripe/stripe-php** | `stripe/stripe-php` | Official Stripe PHP SDK |

### PayPal

| Package | Composer | Notes |
|---------|----------|-------|
| **srmklive/paypal** | `srmklive/paypal` | PayPal Express Checkout & REST API |
| **laravel-paypal** | `victorybiz/laravel-paypal` | Laravel wrapper for PayPal SDK |

### Multi-Gateway

| Package | Composer | Notes |
|---------|----------|-------|
| **League Omnipay** | `league/omnipay` | Multi-gateway abstraction layer (40+ gateways) |
| **Laravel Cashier (Paddle)** | `laravel/cashier-paddle` | Official Paddle billing |
| **spatie/laravel-stripe-payments** | `spatie/laravel-stripe-payments` | Simple Stripe payment processing |

### GCC / Regional

| Package | Composer | Notes |
|---------|----------|-------|
| **Tap Payments** | `mytaxi/tap-payment` | Tap Payments (Gulf) integration |
| **PayTabs** | community packages | PayTabs GCC gateway |
| **Telr** | community packages | Telr payment gateway (UAE) |
| **2checkout** | `verifone/2checkout-php` | 2Checkout/Verifone |

---

## 14. Activity Logs

| Package | Composer | Notes |
|---------|----------|-------|
| **spatie/laravel-activitylog** | `spatie/laravel-activitylog` | ⭐ Log model changes; cause tracking; custom events; subject/causer polymorphism |
| **haruncpi/laravel-user-activity** | `haruncpi/laravel-user-activity` | Simple user-level activity log |
| **yadahan/laravel-authentication-log** | `yadahan/laravel-authentication-log` | Login/logout/failed login log |
| **antonrom1/laravel-model-changes-history** | `antonrom1/laravel-model-changes-history` | Model field-level change history |

---

## 15. Audit Trail

| Package | Composer | Notes |
|---------|----------|-------|
| **owen-it/laravel-auditing** | `owen-it/laravel-auditing` | ⭐ Detailed field-level audit; drivers (DB, file, Redis); custom resolvers |
| **spatie/laravel-activitylog** | `spatie/laravel-activitylog` | Dual-use; audit + activity log |
| **VentureCraft/revisionable** | `venturecraft/revisionable` | Model revision history; simple approach |
| **infyomlabs/laravel-generator** | `infyomlabs/laravel-generator` | CRUD generator with audit scaffold |

---

## 16. Event Sourcing

| Package | Composer | Notes |
|---------|----------|-------|
| **spatie/laravel-event-sourcing** | `spatie/laravel-event-sourcing` | ⭐ Aggregates, projectors, reactors; event store in DB |
| **EventSauce** | `eventosauce/eventsauce` | Framework-agnostic; used as inspiration for Spatie's package |
| **broadway/broadway** | `broadway/broadway` | CQRS + ES framework for PHP |
| **prooph/event-store** | `prooph/event-store` | Prooph event store with multiple adapters |
| **hirevoice/laravel-event-store** | `hirevoice/laravel-event-store` | Simple event store for Laravel |

---

## 17. FHIR API & FHIR Tools

### PHP FHIR Libraries

| Package | Composer | Notes |
|---------|----------|-------|
| **dcarbone/php-fhir** | `dcarbone/php-fhir` | ⭐ FHIR R4/STU3/R5 PHP model generator; DCarbone's widely used generator |
| **luscii/php-fhir-model** | `luscii/php-fhir-model` | Pre-generated FHIR STU3 model classes from dcarbone |
| **smalot/php-fhir** | community | FHIR R4 PHP models |
| **LibreEHR FHIR API** | `libreehr/fhir` | Laravel FHIR API for LibreEHR database |

### FHIR Server / Middleware (Not PHP, but integrates via API)

| Tool | Notes |
|------|-------|
| **HAPI FHIR** | Gold-standard Java FHIR server; expose via REST from Laravel via `Saloon` |
| **Medplum** | Node-based FHIR R4 server; REST API |
| **Azure Health Data Services** | Managed FHIR service (R4/STU3) |
| **Google Cloud Healthcare API** | FHIR + HL7v2 + DICOM managed service |

### Laravel Integration Patterns

| Package | Composer | Notes |
|---------|----------|-------|
| **saloonphp/saloon** | `saloonphp/saloon` | Best PHP HTTP client for FHIR server integration; mock-friendly |
| **spatie/laravel-data** | `spatie/laravel-data` | Map FHIR resources to typed DTOs |
| **opis/json-schema** | `opis/json-schema` | Validate openEHR archetypes & FHIR profiles |

---

## 18. WYSIWYG Editors

> These are frontend (npm) packages, typically integrated via Inertia/Livewire.

| Package | NPM / Composer | Notes |
|---------|----------------|-------|
| **TipTap** | `@tiptap/react` | ⭐ ProseMirror-based; extensible; headless; best-in-class 2024 |
| **Quill.js** | `quill` | Popular; ReactQuill for React |
| **CKEditor 5** | `@ckeditor/ckeditor5-react` | Feature-rich; commercial license for advanced features |
| **TinyMCE** | `@tinymce/tinymce-react` | Mature; many plugins; commercial for some features |
| **Froala** | `froala-editor` (commercial) | Very polished; fast |
| **Jodit** | `jodit-react` | Open-source; fast; good RTL support |
| **rich-textarea** | community | Lightweight alternative |
| **mohamedsabil83/filament-forms-tiptap-editor** | `mohamedsabil83/filament-forms-tiptap-editor` | TipTap for Filament forms |

---

## 19. Markdown Editors

| Package | NPM / Composer | Notes |
|---------|----------------|-------|
| **EasyMDE** | `easymde` | Simple markdown editor; codemirror-based |
| **Toast UI Editor** | `@toast-ui/react-editor` | Full-featured; WYSIWYG + Markdown modes |
| **@uiw/react-md-editor** | `@uiw/react-md-editor` | React markdown editor with preview |
| **Milkdown** | `@milkdown/core` | Plugin-based WYSIWYG markdown editor |
| **Markdownit** | `markdown-it` | Markdown renderer (not editor) |
| **awesomize/filament-markdown-editor** | `awesomize/filament-markdown-editor` | Markdown editor for Filament |
| **spatie/laravel-markdown** | `spatie/laravel-markdown` | Render markdown in Blade with code highlighting |

---

## 20. Email — IMAP & POP (Reading Mailboxes)

| Package | Composer | Notes |
|---------|----------|-------|
| **webklex/laravel-imap** | `webklex/laravel-imap` | ⭐ IMAP/POP3 email reading; attachments; flags; search |
| **webklex/php-imap** | `webklex/php-imap` | Base library used by laravel-imap |
| **ddeboer/imap** | `ddeboer/imap` | IMAP library with OOP interface |
| **phpmailer/phpmailer** | `phpmailer/phpmailer` | Legacy; includes IMAP/POP helpers |
| **fetchmail** | system-level | Fetchmail daemon via shell_exec integration |

---

## 21. Email Sending & SMTP

### Mail Drivers & Services

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Mail** | built-in | `Mail::send()`, Mailables, `markdown` templates |
| **Mailgun** | `symfony/mailgun-mailer` | Mailgun via Symfony mailer (built-in driver) |
| **Postmark** | `symfony/postmark-mailer` | Postmark driver |
| **SES** | `aws/aws-sdk-php` | Amazon SES driver |
| **Resend** | `resend/resend-php` | Resend email API driver |
| **SendGrid** | `sichikawa/laravel-sendgrid-driver` | SendGrid SMTP or API |
| **MailerSend** | `mailersend/laravel-driver` | MailerSend API driver for Laravel |
| **SMTP2GO** | community | SMTP2GO driver |

### Email Templates & Testing

| Package | Composer | Notes |
|---------|----------|-------|
| **Mailable Livewire** | `wire-elements/livewire-mail` | Interactive email templates |
| **spatie/laravel-mail-preview** | `spatie/laravel-mail-preview` | Preview emails in browser during dev |
| **mailthief** | `tightenco/mailthief` | Intercept and test sent mail |
| **Laravel Mail Manager** | `spatie/laravel-failed-job-monitor` | Monitor failed email delivery |

---

## 22. S3 & File Storage

### Storage Drivers

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Filesystem** | built-in | Local, S3, FTP, SFTP drivers via `Storage` facade |
| **aws/aws-sdk-php** | `aws/aws-sdk-php` | AWS S3 SDK |
| **league/flysystem-aws-s3-v3** | `league/flysystem-aws-s3-v3` | Flysystem S3 adapter (used internally by Laravel) |
| **league/flysystem-sftp-v3** | `league/flysystem-sftp-v3` | SFTP via SSH2 |
| **Google Cloud Storage** | `league/flysystem-google-cloud-storage` | GCS driver |
| **Azure Blob Storage** | `matthewbdaly/laravel-azure-storage` | Azure Blob Storage driver |
| **Cloudinary** | `cloudinary-labs/cloudinary-laravel` | Cloudinary image/video CDN |
| **DigitalOcean Spaces** | `s3` compatible | Use standard S3 driver with Spaces endpoint |

### Media Management

| Package | Composer | Notes |
|---------|----------|-------|
| **spatie/laravel-medialibrary** | `spatie/laravel-medialibrary` | ⭐ Associate media with Eloquent models; conversions; S3-aware |
| **rutorika/sortable** | companion | Sortable media collections |

---

## 23. Caching

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Cache** | built-in | File, DB, Redis, Memcached, DynamoDB drivers |
| **predis/predis** | `predis/predis` | Pure PHP Redis client |
| **phpredis** | `ext-redis` (PECL) | Fast C extension for Redis |
| **spatie/laravel-responsecache** | `spatie/laravel-responsecache` | Full HTTP response caching |
| **archtechx/laravel-defer** | `archtechx/laravel-defer` | Defer slow computations via deferred calls |
| **spatie/laravel-query-builder** | `spatie/laravel-query-builder` | Cache-aware query building from HTTP params |
| **laravel/octane** | `laravel/octane` | Keep app in memory between requests (Swoole/RoadRunner) |
| **rennokki/laravel-eloquent-cache** | `rennokki/laravel-eloquent-cache` | Automatic Eloquent model caching |

---

## 24. Queue, Tasks, Commands & Scheduling

### Queue Drivers

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Queues** | built-in | Database, Redis, SQS, Beanstalkd drivers |
| **Laravel Horizon** | `laravel/horizon` | Redis queue dashboard; supervisor; metrics |
| **Laravel Worker** | built-in | `php artisan queue:work` |
| **Laravel Reverb** | `laravel/reverb` | Official WebSocket server for broadcasting |
| **Supervisor** | system-level | Process manager for queue workers |

### Job Processing

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Bus** | built-in | Job chaining; batching; pipelines |
| **spatie/laravel-failed-job-monitor** | `spatie/laravel-failed-job-monitor` | Notify on failed jobs |
| **laravel/pulse** | `laravel/pulse` | Real-time app performance monitoring incl. queue stats |
| **imdhemy/laravel-queue-rabbitmq** | `vladimir-yuldashev/laravel-queue-rabbitmq` | RabbitMQ driver |
| **aws/aws-sdk-php` (SQS)** | `aws/aws-sdk-php` | Amazon SQS driver (built-in) |

### Scheduling

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Scheduler** | built-in | `Schedule` facade; cron-based task scheduling |
| **spatie/laravel-schedule-monitor** | `spatie/laravel-schedule-monitor` | Monitor scheduled tasks; Oh Dear integration |
| **tightenco/tasker** | `tightenco/tasker` | GUI task runner |

---

## 25. Media & Image Manipulation/Management

### Image Manipulation

| Package | Composer | Notes |
|---------|----------|-------|
| **Intervention Image** | `intervention/image` | ⭐ Resize, crop, watermark, filter images; GD or Imagick |
| **spatie/image** | `spatie/image` | Image manipulation with optimization; built on Glide |
| **league/glide** | `league/glide` | On-the-fly image manipulation via URL params |
| **PHP Image Resize** | `gumlet/php-image-resize` | Simple resize library |
| **Imagick** | `ext-imagick` (PECL) | PHP wrapper for ImageMagick |

### Media Management

| Package | Composer | Notes |
|---------|----------|-------|
| **spatie/laravel-medialibrary** | `spatie/laravel-medialibrary` | ⭐ Media attached to models; conversions; S3; responsive images |
| **awcodes/filament-curator** | `awcodes/filament-curator` | Filament-based media manager |
| **tightenco/laravel-imageup** | `qcod/imageup` | Auto upload and resize images on model save |
| **unisharp/laravel-filemanager** | `unisharp/laravel-filemanager` | File manager UI (Blade/jQuery) |
| **spatie/laravel-image-optimizer** | `spatie/laravel-image-optimizer` | Optimize PNG/JPG/SVG using OptiPNG, jpegtran, etc. |

---

## 26. REST API

### API Building

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel API Resources** | built-in | `JsonResource`; clean JSON API output |
| **spatie/laravel-query-builder** | `spatie/laravel-query-builder` | Filter, sort, include relationships from URL params; API-style |
| **Laravel JSON:API** | `laravel-json-api/laravel` | Full JSON:API 1.1 compliant |
| **timacdonald/json-api** | `timacdonald/json-api` | Lightweight JSON:API resources |
| **saloonphp/saloon** | `saloonphp/saloon` | Consume external REST APIs; mock-friendly |

### API Documentation

| Package | Composer | Notes |
|---------|----------|-------|
| **knuckleswtf/scribe** | `knuckleswtf/scribe` | ⭐ Auto-generate API docs from code + annotations |
| **dedoc/scramble** | `dedoc/scramble` | OpenAPI 3 docs auto-generated; zero annotations |
| **darkaonline/l5-swagger** | `darkaonline/l5-swagger` | Swagger/OpenAPI 3 UI |

### Rate Limiting & Security

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Rate Limiting** | built-in | `throttle` middleware |
| **spatie/laravel-cors** | `fruitcake/laravel-cors` | CORS headers; now `laravel/framework` handles CORS natively |

---

## 27. Webhooks

| Package | Composer | Notes |
|---------|----------|-------|
| **spatie/laravel-webhook-client** | `spatie/laravel-webhook-client` | ⭐ Receive & process incoming webhooks; signature verification; queuing |
| **spatie/laravel-webhook-server** | `spatie/laravel-webhook-server` | Send outgoing webhooks with retry, signing, backoff |
| **ohseesoftware/laravel-server-analytics** | companion | Webhook analytics |
| **DarkaOnLine/laravel-guzzle** | companion | Guzzle HTTP for sending webhooks manually |

---

## 28. GraphQL

| Package | Composer | Notes |
|---------|----------|-------|
| **nuwave/lighthouse** | `nuwave/lighthouse` | ⭐ Schema-first GraphQL server; Eloquent-integrated; subscriptions |
| **rebing/graphql-laravel** | `rebing/graphql-laravel` | Code-first GraphQL server |
| **api-platform/graphql** | companion | GraphQL via API Platform |
| **graphql-php/graphql-php** | `webonyx/graphql-php` | Low-level GraphQL base library (Lighthouse uses this) |
| **mll-lab/laravel-graphiql** | `mll-lab/laravel-graphiql` | GraphiQL IDE in Laravel |

---

## 29. Search Engines

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Scout** | `laravel/scout` | ⭐ Full-text search abstraction; Algolia, Meilisearch, Typesense, DB drivers |
| **Laravel Scout Algolia** | `algolia/algoliasearch-client-php` | Algolia driver for Scout |
| **Meilisearch** | `meilisearch/meilisearch-php` | Meilisearch driver for Scout |
| **Typesense** | `typesense/typesense-php` | Typesense driver for Scout |
| **babenkoivan/elastic-scout-driver** | `babenkoivan/elastic-scout-driver` | Elasticsearch driver for Scout |
| **Laravel Full Text Search** | `spatie/laravel-search-string` | Search string to Eloquent query parser |
| **tntsearch/tntsearch** | `teamtnt/tntsearch` | Fast SQLite full-text search; no external service |
| **teamtnt/laravel-scout-tntsearch-driver** | `teamtnt/laravel-scout-tntsearch-driver` | TNTSearch as Scout driver |

---

## 30. Optimizing

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Octane** | `laravel/octane` | ⭐ Keep app booted in memory; Swoole or RoadRunner; massive performance gains |
| **spatie/laravel-responsecache** | `spatie/laravel-responsecache` | Cache full HTTP responses |
| **spatie/laravel-image-optimizer** | `spatie/laravel-image-optimizer` | Optimize assets |
| **Laravel Pulse** | `laravel/pulse` | Real-time monitoring dashboard |
| **Enlightn** | `enlightn/enlightn` | Automated performance audits |
| **beyondcode/laravel-query-detector** | `beyondcode/laravel-query-detector` | Detect N+1 queries automatically |
| **genealabs/laravel-model-caching** | `genealabs/laravel-model-caching` | Automatic Eloquent model caching |
| **renoki-co/laravel-eloquent-cache** | `rennokki/laravel-eloquent-cache` | Cache model retrievals |
| **tightenco/paradeiser** | companion | Optimize Eloquent eager loading |
| **Horizon** | `laravel/horizon` | Redis queue tuning and monitoring |

---

## 31. Monetization

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Cashier (Stripe)** | `laravel/cashier` | Subscriptions, trials, invoices via Stripe |
| **Laravel Cashier (Paddle)** | `laravel/cashier-paddle` | Paddle Billing (VAT-aware) |
| **spatie/laravel-stripe-terminal** | community | Stripe Terminal integration |
| **imdhemy/laravel-purchases** | `imdhemy/laravel-purchases` | In-app purchase verification (iOS/Android) |
| **laravel/cashier-mollie** | `laravel/cashier-mollie` | Mollie billing (EU-focused) |
| **Laravel Spark** | `laravel/spark` (commercial) | SaaS billing boilerplate with Cashier |

---

## 32. Localization

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Localization** | built-in | `Lang` facade; `resources/lang`; plural forms |
| **mcamara/laravel-localization** | `mcamara/laravel-localization` | ⭐ URL-based locale detection; language prefix routing |
| **astrotomic/laravel-translatable** | `astrotomic/laravel-translatable` | Translate Eloquent model attributes |
| **spatie/laravel-translatable** | `spatie/laravel-translatable` | Store translations as JSON in model columns |
| **Tightenco/Babel** | `tightenco/babel` | Frontend localization using Laravel translations |
| **laravel-lang/lang** | `laravel-lang/lang` | Community translations for all Laravel packages |
| **Laravel Translation** | `laravel/translation` | Built-in |
| **kargnas/laravel-ai-translator** | `spatie/laravel-ai-translator` | AI-powered translation of lang files |

---

## 33. 3rd Party Services Integration

| Service | Package | Notes |
|---------|---------|-------|
| **Google APIs** | `google/apiclient` | GMaps, Calendar, Drive, Sheets |
| **Firebase** | `kreait/laravel-firebase` | Firestore, Auth, Messaging, Storage |
| **Twilio** | `twilio/sdk` | SMS, Voice, WhatsApp |
| **Vonage/Nexmo** | `vonage/laravel` | SMS via Vonage (formerly Nexmo) |
| **Slack** | `laravel/slack-notification-channel` | Slack notifications |
| **Pusher** | `pusher/pusher-php-server` | Pusher WebSocket broadcasting |
| **AWS** | `aws/aws-sdk-php` | S3, SES, SQS, SNS, DynamoDB, Rekognition, etc. |
| **Stripe** | `stripe/stripe-php` | Payments |
| **HubSpot** | `hubspot/api-client` | CRM integration |
| **Salesforce** | `omniphx/forrest` | Salesforce REST API |
| **SendGrid** | `sichikawa/laravel-sendgrid-driver` | Email |
| **Mailchimp** | `spatie/laravel-newsletter` | Newsletter subscription management |
| **GitHub** | `graham-campbell/github` | GitHub API wrapper |
| **Zoom** | `jubaer/zoom-laravel` | Zoom meetings API |
| **DocuSign** | `docusign/esign-client` | eSignature API |

---

## 34. Hosting

### PaaS / Laravel-Native

| Platform | Package/Tool | Notes |
|----------|-------------|-------|
| **Laravel Forge** | forge.laravel.com | ⭐ Official server provisioning; Nginx, PHP, MySQL/PostgreSQL, SSL |
| **Laravel Vapor** | `laravel/vapor-cli` | Serverless Laravel on AWS Lambda |
| **Laravel Envoyer** | envoyer.io | Zero-downtime deployment |
| **Ploi** | ploi.io | Similar to Forge; cheaper |
| **Cloudways** | cloudways.com | Managed cloud hosting |

### Docker / Container

| Package | Notes |
|---------|-------|
| **Laravel Sail** | `laravel/sail` — Official Docker dev environment |
| **Laradock** | Full Docker environment with all services |
| **Docker + Nginx + PHP-FPM** | Production container stack |

### CDN & Performance

| Package | Notes |
|---------|-------|
| **CloudFlare** | CDN + DDoS protection + workers |
| **AWS CloudFront** | CDN for static assets |
| **BunnyCDN** | Cost-effective CDN |

---

## 35. Forms

| Package | Composer | Notes |
|---------|----------|-------|
| **Filament Forms** | `filament/forms` | ⭐ Standalone form builder (also part of Filament panel) |
| **Laravel Precognition** | `laravel/precognition` | Live validation before form submission |
| **livewire/livewire** | `livewire/livewire` | Reactive forms with server-side validation |
| **Laravel Form Requests** | built-in | Validated request classes |
| **spatie/laravel-html** | `spatie/laravel-html` | HTML form builder with type-safe API |
| **collective/html** | `laravelcollective/html` | Legacy HTML/Form helpers |
| **cviebrock/eloquent-sluggable** | companion | Slug field generation |

---

## 36. Charts

| Package | Composer / NPM | Notes |
|---------|----------------|-------|
| **Laravel Charts** | `consoletvs/charts` | Blade + multiple JS chart libraries |
| **Filament Charts** | `filament/charts` | Chart widgets for Filament panels |
| **Chart.js** | `chart.js` (npm) | Most popular JS charting library |
| **Recharts** | `recharts` (npm) | React-based Chart.js alternative; used with Inertia |
| **ApexCharts** | `apexcharts` (npm) | Feature-rich; React/Vue wrappers |
| **Highcharts** | `highcharts` (npm) | Commercial; enterprise features |
| **D3.js** | `d3` (npm) | Low-level; maximum customization |
| **spatie/laravel-analytics** | `spatie/laravel-analytics` | Google Analytics data in Laravel |
| **Laravel Pulse** | `laravel/pulse` | Built-in performance charts dashboard |

---

## 37. AI Integration

> See also [Section 6 — AI & Laravel](#6-ai--laravel)

| Package | Composer | Notes |
|---------|----------|-------|
| **openai-php/laravel** | `openai-php/laravel` | ⭐ OpenAI GPT-4, Embeddings, Whisper, DALL-E |
| **prism-php/prism** | `prism-php/prism` | Multi-provider (Claude, GPT, Gemini, Ollama) unified API |
| **anthropic/sdk** | `anthropic/sdk` | Official Claude PHP SDK |
| **cloudstudio/ollama-laravel** | `cloudstudio/ollama-laravel` | Local models via Ollama |
| **gehrisandro/laravel-chatgpt** | `gehrisandro/laravel-chatgpt` | Chat completions wrapper |
| **spatie/laravel-ai-translator** | `spatie/laravel-ai-translator` | AI-translate Laravel lang files |
| **laravel-ai/laravel-ai** | `laravel-ai/laravel-ai` | Unified AI provider abstraction |
| **usebruno/bruno** | companion | API testing for AI endpoints |
| **LangChain PHP** | `kambo/langchain` | LangChain-style chains in PHP |
| **Vector Embeddings** | `pgvector` (PostgreSQL extension) | Store + search vectors for semantic search |

---

## 38. Official Laravel Packages

| Package | Composer | Notes |
|---------|----------|-------|
| **Laravel Breeze** | `laravel/breeze` | Auth scaffolding |
| **Laravel Cashier** | `laravel/cashier` | Stripe billing |
| **Laravel Cashier Paddle** | `laravel/cashier-paddle` | Paddle billing |
| **Laravel Dusk** | `laravel/dusk` | Browser testing |
| **Laravel Echo** | `laravel/echo` (npm) | Real-time broadcasting |
| **Laravel Envoy** | `laravel/envoy` | Remote task runner |
| **Laravel Folio** | `laravel/folio` | File-based page routing |
| **Laravel Fortify** | `laravel/fortify` | Headless auth backend |
| **Laravel Horizon** | `laravel/horizon` | Redis queue dashboard |
| **Laravel Jetstream** | `laravel/jetstream` | Full-stack starter kit |
| **Laravel MCP** | `laravel/mcp` | Model Context Protocol server |
| **Laravel Mix** | `laravel-mix` | Legacy webpack wrapper |
| **Laravel Octane** | `laravel/octane` | High-performance app server |
| **Laravel Passport** | `laravel/passport` | OAuth2 server |
| **Laravel Pennant** | `laravel/pennant` | Feature flags |
| **Laravel Pint** | `laravel/pint` | PHP CS Fixer config |
| **Laravel Precognition** | `laravel/precognition` | Live validation |
| **Laravel Prompts** | `laravel/prompts` | Beautiful CLI prompts |
| **Laravel Pulse** | `laravel/pulse` | App monitoring |
| **Laravel Reverb** | `laravel/reverb` | WebSocket server |
| **Laravel Sail** | `laravel/sail` | Docker dev environment |
| **Laravel Sanctum** | `laravel/sanctum` | SPA/API token auth |
| **Laravel Scout** | `laravel/scout` | Full-text search |
| **Laravel Socialite** | `laravel/socialite` | OAuth social login |
| **Laravel Telescope** | `laravel/telescope` | Debug assistant |
| **Laravel Valet** | `laravel/valet` | macOS dev environment |
| **Laravel Vapor CLI** | `laravel/vapor-cli` | Serverless deployment |
| **Laravel Nova** | `laravel/nova` (commercial) | Admin panel |

---

## 39. Medical PHP & Laravel Packages

### FHIR & HL7

| Package | Composer | Notes |
|---------|----------|-------|
| **dcarbone/php-fhir** | `dcarbone/php-fhir` | FHIR R4/R5 PHP model generator |
| **luscii/php-fhir-model** | `luscii/php-fhir-model` | Pre-built FHIR STU3 models |
| **LibreEHR FHIR** | `libreehr/fhir` | FHIR R4 API for LibreEHR |
| **Medplum Laravel adapter** | community | Medplum FHIR server integration |

### openEHR

| Package | Composer | Notes |
|---------|----------|-------|
| **opis/json-schema** | `opis/json-schema` | Archetype validation |
| **Custom AQL Builder** | PurplePractice internal | AQL-inspired Eloquent query builder for openEHR archetypes |
| **EHRbase REST client** | via `saloonphp/saloon` | EHRbase CDR REST/openEHR API integration |

### Clinical / DICOM

| Package / Tool | Notes |
|----------------|-------|
| **Orthanc** | DICOM PACS server (Docker sidecar); REST API |
| **Cornerstone.js** | `@cornerstonejs/core` — Browser-based DICOM viewer |
| **dcmjs** | `dcmjs/dcmjs` (npm) — DICOM in JavaScript |
| **php-dicom** | `dcm4php/dcm4php` — PHP DICOM parsing |

### Pharmacy / Drug

| Package / Source | Notes |
|-----------------|-------|
| **FDA Drug API** | Public API for drug lookups (via Saloon) |
| **openFDA** | `openfda-php` — Drug adverse events |
| **RxNorm API** | NLM drug normalization REST API |

### ICD / SNOMED / LOINC

| Package / Source | Notes |
|-----------------|-------|
| **WHO ICD-10/11 API** | Public REST API; integrate via Saloon |
| **SNOMED CT** | Use SNOWSTORM server; query via REST |
| **LOINC API** | Clinical terminology REST API |

---

## 40. IoT & Hardware

### MQTT / Messaging

| Package | Composer | Notes |
|---------|----------|-------|
| **php-mqtt/client** | `php-mqtt/client` | ⭐ MQTT client for PHP; subscribe/publish |
| **bluerhinos/phpmqtt** | `bluerhinos/phpmqtt` | Lightweight MQTT client |
| **Laravel Reverb** | `laravel/reverb` | WebSocket server; bridges MQTT data to browser |
| **Mosquitto** | system-level | MQTT broker (Eclipse Mosquitto Docker) |

### Hardware & Peripherals

| Package | Composer | Notes |
|---------|----------|-------|
| **thermal ESC/POS** | `mike42/escpos-php` | Thermal printer control |
| **PrintNode** | `printnode/printnode-php` | Cloud print service API |
| **QZ Tray** | JavaScript bridge | Local desktop print without browser dialogs |
| **CUPS** | `nesk/puphpeteer` / shell | Server-side printing via CUPS |
| **Barcode Scanner (USB HID)** | via WebHID API or USB event stream | Browser WebHID or serial port |

### CGM & Wearables

| Package | Notes |
|---------|-------|
| **Terra API** | `tryterra/terra-php` — CGM data aggregator (Dexcom, Libre, Garmin, Apple Health) |
| **Vital/Junction** | REST API; FHIR R4 output; connect via Saloon |
| **Thryve** | Health data platform API |

---

## 41. eCommerce

| Package | Composer | Notes |
|---------|----------|-------|
| **Bagisto** | `bagisto/bagisto` | ⭐ Full Laravel eCommerce platform; multi-store; RBAC |
| **Shopper** | `shopperlabs/shopper` | Headless eCommerce for Laravel + Livewire |
| **aimeos/aimeos-laravel** | `aimeos/aimeos-laravel` | Enterprise eCommerce; very feature-rich |
| **Mage2** | `magento/magento2` (not Laravel) | Magento 2; integrate via REST API |
| **WooCommerce** | API integration | Use `automattic/woocommerce` PHP client |
| **Laravel Cart** | `darryldecode/cart` | Simple shopping cart |
| **Cart for Laravel** | `bumbummen99/shoppingcart` | Session/DB shopping cart |
| **Laravel Cashier** | `laravel/cashier` | Subscription billing component |
| **PayPal Checkout** | `srmklive/paypal` | PayPal for eCommerce |

---

## 42. Barcode Generation

### Barcode Generation

| Package | Composer | Notes |
|---------|----------|-------|
| **milon/barcode** | `milon/barcode` | ⭐ 1D/2D barcodes as SVG, PNG, HTML; QR codes; integrates with dompdf |
| **picqer/php-barcode-generator** | `picqer/php-barcode-generator` | Generate 1D barcodes (Code128, EAN, ITF, etc.) as SVG/PNG |
| **endroid/qr-code** | `endroid/qr-code` | ⭐ QR code generation; Laravel bundle available; SVG/PNG/GIF/PDF |
| **endroid/qr-code-bundle** | `endroid/qr-code-bundle` | Symfony/Laravel integration |
| **tecnickcom/tcpdf** | `tecnickcom/tcpdf` | Built-in 1D/2D barcode into PDF |
| **Zxing** | `zxing/zxing-php` | ZXing barcode reading/writing |
| **chillerlan/php-qrcode** | `chillerlan/php-qrcode` | QR code generator with styling support |
| **simple-qrcode** | `simplesoftwareio/simple-qrcode` | Simple QR code facade for Laravel |

---

## 43. Signature Collection

### Digital Signature Pads (Frontend)

| Package | NPM | Notes |
|---------|-----|-------|
| **signature_pad** | `signature_pad` | ⭐ Most popular; smooth HTML5 canvas signatures; exports PNG/SVG |
| **react-signature-canvas** | `react-signature-canvas` | React wrapper for signature_pad |
| **vue-signature-pad** | `vue-signature-pad` | Vue wrapper |

### Laravel Backend / PDF Integration

| Package | Composer | Notes |
|---------|----------|-------|
| **spatie/laravel-signature** | community | Store base64 signature images |
| **Store as base64** | built-in | Save `data:image/png;base64,...` to storage |
| **Inject into PDF** | `barryvdh/laravel-dompdf` | Embed signature image into PDF via `<img>` tag |
| **spatie/laravel-pdf** | `spatie/laravel-pdf` | Render HTML with embedded signature into PDF |

### Electronic / Legal eSignature

| Package | Composer / API | Notes |
|---------|----------------|-------|
| **DocuSign** | `docusign/esign-client` | Legal eSignature API |
| **HelloSign / Dropbox Sign** | `hellosign/hellosign-php-sdk` | Legal eSignature; embedded signing |
| **Adobe Sign** | REST API via Saloon | Adobe Acrobat Sign |
| **SignWell** | REST API | Affordable eSignature API |
| **PandaDoc** | `pandadoc/php-sdk` | Document + eSignature workflow |

---

## Appendix: Spatie Package Reference

Spatie produces an exceptional suite of Laravel packages. Key packages by category:

| Package | Category |
|---------|----------|
| `spatie/laravel-permission` | Authorization |
| `spatie/laravel-activitylog` | Activity / Audit |
| `spatie/laravel-event-sourcing` | Event Sourcing |
| `spatie/laravel-medialibrary` | Media |
| `spatie/laravel-multitenancy` | Multi-tenancy |
| `spatie/laravel-backup` | Backup |
| `spatie/laravel-responsecache` | Caching |
| `spatie/laravel-query-builder` | API / REST |
| `spatie/laravel-data` | DTOs / Serialization |
| `spatie/laravel-webhook-client` | Webhooks (receive) |
| `spatie/laravel-webhook-server` | Webhooks (send) |
| `spatie/laravel-translatable` | Localization |
| `spatie/laravel-schedule-monitor` | Scheduling |
| `spatie/laravel-health` | Monitoring |
| `spatie/laravel-pdf` | PDF |
| `spatie/image` | Images |
| `spatie/laravel-image-optimizer` | Image optimization |
| `spatie/laravel-ray` | Debugging |
| `spatie/laravel-login-link` | Auth (dev) |
| `spatie/laravel-mail-preview` | Email |
| `spatie/laravel-ai-translator` | AI / Localization |

---

> **Legend:** ⭐ = Recommended / most widely adopted in its category.
> Packages listed reflect community adoption, maintenance status, and compatibility with Laravel 11/12 as of early 2026.

# 🟪 Top 100 Laravel-Based Projects

> A curated list of the most notable open-source projects, packages, and production platforms built with the [Laravel](https://laravel.com) PHP framework.

---

## 📑 Table of Contents

- [🏆 Tier 1 — Mega Projects (20k+ Stars)](#tier-1-mega-projects-20k-stars)
- [🥇 Tier 2 — Major Open-Source Applications (10k–20k Stars)](#tier-2-major-open-source-applications-10k–20k-stars)
- [🥈 Tier 3 — Established Projects & Ecosystem (5k–10k Stars)](#tier-3-established-projects-&-ecosystem-5k–10k-stars)
- [🥉 Tier 4 — Notable Applications & Packages (2k–5k Stars)](#tier-4-notable-applications-&-packages-2k–5k-stars)
- [📦 Essential Laravel Packages & Frameworks](#essential-laravel-packages-&-frameworks)
- [🔧 Specialized Tools & Packages](#specialized-tools-&-packages)
- [🧩 Core Ecosystem & Infrastructure](#core-ecosystem-&-infrastructure)
- [🏗️ Architecture & Developer Experience](#architecture-&-developer-experience)
- [🚀 Production SaaS & Commercial Platforms](#production-saas-&-commercial-platforms)
- [⚡ Community Favorites & Utilities](#community-favorites-&-utilities)
- [🌐 Platforms, Services & Emerging Tools](#platforms,-services-&-emerging-tools)


---

## 🏆 Tier 1 — Mega Projects (20k+ Stars)

| # | Project | Category | Description | Links |
|--:|---------|----------|-------------|-------|
| 1 | **Coolify** | `DevOps / PaaS` | Self-hostable PaaS alternative to Vercel, Heroku & Netlify. Deploy apps, databases, and 280+ services. | [GitHub](https://github.com/coollabsio/coolify) · [Website](https://coolify.io) |
| 2 | **Filament** | `Admin Panel / UI Framework` | Powerful open-source UI framework for Laravel. Build admin panels fast with Livewire. | [GitHub](https://github.com/filamentphp/filament) · [Website](https://filamentphp.com) |
| 3 | **Monica** | `CRM / Personal` | Personal CRM to manage friends, family, and business relationships. Uses DDD architecture. | [GitHub](https://github.com/monicahq/monica) · [Website](https://www.monicahq.com) |
| 4 | **Firefly III** | `Finance` | Personal finances manager. Track transactions, budgets, and financial goals. | [GitHub](https://github.com/firefly-iii/firefly-iii) · [Website](https://www.firefly-iii.org) |
| 5 | **Koel** | `Media / Music` | Personal music streaming server. Built with Laravel + Vue.js. | [GitHub](https://github.com/koel/koel) · [Website](https://koel.dev) |

---

## 🥇 Tier 2 — Major Open-Source Applications (10k–20k Stars)

| # | Project | Category | Description | Links |
|--:|---------|----------|-------------|-------|
| 6 | **BookStack** | `Documentation / Wiki` | Platform for creating documentation/wiki content. Used across 7k+ sites. | [GitHub](https://github.com/BookStackApp/BookStack) · [Website](https://www.bookstackapp.com) |
| 7 | **Invoice Ninja** | `Invoicing / Billing` | Invoicing and billing platform for freelancers and small businesses. | [GitHub](https://github.com/invoiceninja/invoiceninja) · [Website](https://www.invoiceninja.com) |
| 8 | **Cachet** | `Status Pages` | Beautiful open-source status page system for monitoring service uptime. | [GitHub](https://github.com/cachethq/cachet) · [Website](https://cachethq.io) |
| 9 | **Flarum** | `Forum` | Next-generation forum software. Modern, fast, and extensible. | [GitHub](https://github.com/flarum/flarum) · [Website](https://flarum.org) |
| 10 | **Bagisto** | `E-Commerce` | Open-source Laravel eCommerce platform with multi-vendor support. | [GitHub](https://github.com/bagisto/bagisto) · [Website](https://bagisto.com) |

---

## 🥈 Tier 3 — Established Projects & Ecosystem (5k–10k Stars)

| # | Project | Category | Description | Links |
|--:|---------|----------|-------------|-------|
| 11 | **Snipe-IT** | `Asset Management` | Free open-source IT asset/license management system. | [GitHub](https://github.com/snipe/snipe-it) · [Website](https://snipeitapp.com) |
| 12 | **Akaunting** | `Accounting` | Free online accounting software for small businesses and freelancers. | [GitHub](https://github.com/akaunting/akaunting) · [Website](https://akaunting.com) |
| 13 | **October CMS** | `CMS` | Self-hosted CMS platform based on Laravel. Focus on simplicity. | [GitHub](https://github.com/octobercms/october) · [Website](https://octobercms.com) |
| 14 | **Pterodactyl Panel** | `Game Server Management` | Game server management panel. Uses Docker for server instances. | [GitHub](https://github.com/pterodactyl/panel) · [Website](https://pterodactyl.io) |
| 15 | **Voyager** | `Admin Panel` | The Missing Laravel Admin. Adds a full admin panel with BREAD CRUD. | [GitHub](https://github.com/thedevdojo/voyager) · [Website](https://voyager.devdojo.com) |
| 16 | **Statamic** | `CMS` | Flat-first, Laravel + Git powered CMS with beautiful control panel. | [GitHub](https://github.com/statamic/cms) · [Website](https://statamic.com) |
| 17 | **Laravel Debugbar** | `Developer Tools` | Profiling and debugging tool embedding PHP Debug Bar into Laravel. | [GitHub](https://github.com/barryvdh/laravel-debugbar) |
| 18 | **Krayin CRM** | `CRM / Business` | Free & open-source Laravel CRM for SMEs. Complete customer lifecycle management. | [GitHub](https://github.com/krayin/laravel-crm) · [Website](https://krayincrm.com) |
| 19 | **FreeScout** | `Helpdesk` | Super lightweight free open-source help desk and shared inbox. HelpScout clone. | [GitHub](https://github.com/freescout-helpdesk/freescout) · [Website](https://freescout.net) |
| 20 | **Aimeos** | `E-Commerce` | Ultra-fast professional eCommerce components for Laravel. | [GitHub](https://github.com/aimeos/aimeos-laravel) · [Website](https://aimeos.org) |

---

## 🥉 Tier 4 — Notable Applications & Packages (2k–5k Stars)

| # | Project | Category | Description | Links |
|--:|---------|----------|-------------|-------|
| 21 | **NexoPOS** | `POS System` | Web-based Point of Sale system with Laravel, TailwindCSS, and Vue.js. | [GitHub](https://github.com/Blair2004/NexoPOS) · [Website](https://nexopos.com) |
| 22 | **InvoiceShelf** | `Invoicing` | Fork of Crater. Self-hosted invoicing and expense tracking. | [GitHub](https://github.com/InvoiceShelf/InvoiceShelf) · [Website](https://invoiceshelf.com) |
| 23 | **Canvas** | `Blogging / CMS` | A publishing platform for bloggers built on Laravel. | [GitHub](https://github.com/austintoddj/canvas) |
| 24 | **Attendize** | `Event Management` | Self-hosted ticket sales and event management platform. | [GitHub](https://github.com/attendize/attendize) · [Website](https://www.attendize.com) |
| 25 | **PyroCMS** | `CMS` | Modular CMS and development platform built with Laravel. | [GitHub](https://github.com/pyrocms/pyrocms) · [Website](https://pyrocms.com) |
| 26 | **Jigsaw** | `Static Site Generator` | Static site generator using Blade templates and Markdown. | [GitHub](https://github.com/tighten/jigsaw) · [Website](https://jigsaw.tighten.com) |
| 27 | **Spatie Laravel Backup** | `DevOps / Backup` | Automated backup of databases and file systems. Multi-destination support. | [GitHub](https://github.com/spatie/laravel-backup) · [Website](https://spatie.be/docs/laravel-backup) |
| 28 | **Laravel IDE Helper** | `Developer Tools` | Generates helper files for IDE auto-completion. | [GitHub](https://github.com/barryvdh/laravel-ide-helper) |
| 29 | **Spatie Laravel Permission** | `Auth / RBAC` | Role and permission management for Laravel. | [GitHub](https://github.com/spatie/laravel-permission) · [Website](https://spatie.be/docs/laravel-permission) |
| 30 | **Laravel Excel** | `Data Import/Export` | Import and export Excel/CSV with Laravel using PhpSpreadsheet. | [GitHub](https://github.com/SpartnerNL/Laravel-Excel) · [Website](https://laravel-excel.com) |

---

## 📦 Essential Laravel Packages & Frameworks

| # | Project | Category | Description | Links |
|--:|---------|----------|-------------|-------|
| 31 | **Twill** | `CMS` | CMS toolkit for Laravel by AREA 17. Intuitive and powerful admin panel. | [GitHub](https://github.com/area17/twill) · [Website](https://twillcms.com) |
| 32 | **Orchid** | `Admin Panel` | Laravel platform for building back-office applications and admin panels. | [GitHub](https://github.com/orchidsoftware/platform) · [Website](https://orchid.software) |
| 33 | **Laravel Horizon** | `Queue Management` | Dashboard and code-driven configuration for Redis queues. | [GitHub](https://github.com/laravel/horizon) · [Website](https://laravel.com/docs/horizon) |
| 34 | **Laravel Nova** | `Admin Panel` | Beautifully designed administration panel for Laravel (commercial). | [GitHub](https://github.com/laravel/nova-issues) · [Website](https://nova.laravel.com) |
| 35 | **Pinkary** | `Social Media` | Social platform built with PHP 8.3, Laravel, Livewire, Alpine. | [GitHub](https://github.com/pinkary-project/pinkary.com) · [Website](https://pinkary.com) |
| 36 | **Laravel Socialite** | `Authentication` | OAuth authentication with Facebook, Google, Twitter, etc. | [GitHub](https://github.com/laravel/socialite) · [Website](https://laravel.com/docs/socialite) |
| 37 | **Laravel Sanctum** | `Authentication` | Featherweight authentication system for SPAs and APIs. | [GitHub](https://github.com/laravel/sanctum) · [Website](https://laravel.com/docs/sanctum) |
| 38 | **Laravel Scout** | `Search` | Driver-based full-text search for Eloquent models. | [GitHub](https://github.com/laravel/scout) · [Website](https://laravel.com/docs/scout) |
| 39 | **Laravel Echo** | `Real-time` | JavaScript library for subscribing to channels and listening to events. | [GitHub](https://github.com/laravel/echo) · [Website](https://laravel.com/docs/broadcasting) |
| 40 | **Laravel Telescope** | `Developer Tools` | Debug assistant for Laravel. Monitors requests, exceptions, queries. | [GitHub](https://github.com/laravel/telescope) · [Website](https://laravel.com/docs/telescope) |

---

## 🔧 Specialized Tools & Packages

| # | Project | Category | Description | Links |
|--:|---------|----------|-------------|-------|
| 41 | **Apiato** | `API Framework` | Framework for building scalable and testable API-centric applications. | [GitHub](https://github.com/apiato/apiato) · [Website](https://apiato.io) |
| 42 | **AvoRed** | `E-Commerce` | Modular open-source eCommerce platform built on Laravel. | [GitHub](https://github.com/avored/laravel-ecommerce) · [Website](https://www.avored.com) |
| 43 | **Botman** | `Chatbot` | Framework-agnostic PHP library for building chatbots. | [GitHub](https://github.com/botman/botman) · [Website](https://botman.io) |
| 44 | **LaraAdmin** | `Admin Panel / CRM` | Open-source CRM platform with CRUD generation and module management. | [GitHub](https://github.com/dwijitsolutions/laraadmin) · [Website](https://laraadmin.com) |
| 45 | **Asgard CMS** | `CMS` | Modular, multi-language CMS built with Laravel. | [GitHub](https://github.com/AsgardCms/Platform) · [Website](https://asgardcms.com) |
| 46 | **Laravel.io** | `Community / Forum` | The Laravel community portal source code. | [GitHub](https://github.com/laravelio/laravel.io) · [Website](https://laravel.io) |
| 47 | **Lemon Squeezy** | `Payments / SaaS` | Payment provider built with Laravel + Vue (acquired by Stripe). | [Website](https://www.lemonsqueezy.com) |
| 48 | **Geocodio** | `Geocoding / API` | Low-cost geocoding web service built with Laravel + Nova. | [Website](https://www.geocod.io) |
| 49 | **Podscan** | `Podcast Analytics` | Podcast scanning and monitoring SaaS. 5-6 TB raw storage. | [Website](https://podscan.fm) |
| 50 | **Fathom Analytics** | `Analytics` | Privacy-focused analytics. Handles 157B+ requests/month on Laravel infra. | [Website](https://usefathom.com) |

---

## 🧩 Core Ecosystem & Infrastructure

| # | Project | Category | Description | Links |
|--:|---------|----------|-------------|-------|
| 51 | **Spatie Media Library** | `File Management` | Associate files with Eloquent models. Conversions and optimizations. | [GitHub](https://github.com/spatie/laravel-medialibrary) · [Website](https://spatie.be/docs/laravel-medialibrary) |
| 52 | **Spatie Activitylog** | `Logging / Audit` | Log activity inside your Laravel app. | [GitHub](https://github.com/spatie/laravel-activitylog) · [Website](https://spatie.be/docs/laravel-activitylog) |
| 53 | **Laravel Passport** | `Authentication` | Full OAuth2 server implementation for Laravel. | [GitHub](https://github.com/laravel/passport) · [Website](https://laravel.com/docs/passport) |
| 54 | **Laravel Cashier** | `Payments` | Expressive interface to Stripe's subscription billing services. | [GitHub](https://github.com/laravel/cashier-stripe) · [Website](https://laravel.com/docs/billing) |
| 55 | **Laravel Breeze** | `Starter Kit` | Minimal authentication scaffolding with Blade, Vue, or React. | [GitHub](https://github.com/laravel/breeze) · [Website](https://laravel.com/docs/starter-kits) |
| 56 | **Laravel Jetstream** | `Starter Kit` | Full-featured auth scaffolding with Livewire or Inertia. | [GitHub](https://github.com/laravel/jetstream) · [Website](https://jetstream.laravel.com) |
| 57 | **Livewire** | `Frontend / Reactivity` | Full-stack framework for building dynamic UIs without leaving PHP. | [GitHub](https://github.com/livewire/livewire) · [Website](https://livewire.laravel.com) |
| 58 | **Inertia.js** | `Frontend / SPA` | Build SPAs without building an API. Server-driven routing. | [GitHub](https://github.com/inertiajs/inertia-laravel) · [Website](https://inertiajs.com) |
| 59 | **Stancl Tenancy** | `Multi-Tenancy` | Automatic multi-tenancy for Laravel. Schema or DB per tenant. | [GitHub](https://github.com/stancl/tenancy) · [Website](https://tenancyforlaravel.com) |
| 60 | **Laravel Pennant** | `Feature Flags` | Feature flag management for Laravel applications. | [GitHub](https://github.com/laravel/pennant) · [Website](https://laravel.com/docs/pennant) |

---

## 🏗️ Architecture & Developer Experience

| # | Project | Category | Description | Links |
|--:|---------|----------|-------------|-------|
| 61 | **Corcel** | `WordPress Integration` | Use WordPress backend with Laravel models. Read from WP database. | [GitHub](https://github.com/corcel/corcel) |
| 62 | **Spatie Query Builder** | `API / Query` | Build Eloquent queries from API requests with filtering and sorting. | [GitHub](https://github.com/spatie/laravel-query-builder) · [Website](https://spatie.be/docs/laravel-query-builder) |
| 63 | **Laravel Pint** | `Code Style` | Opinionated PHP code style fixer built on PHP-CS-Fixer. | [GitHub](https://github.com/laravel/pint) · [Website](https://laravel.com/docs/pint) |
| 64 | **Pest PHP** | `Testing` | Elegant PHP testing framework with a focus on simplicity. | [GitHub](https://github.com/pestphp/pest) · [Website](https://pestphp.com) |
| 65 | **Laravel Dusk** | `Testing / Browser` | Browser automation and testing tool for Laravel. | [GitHub](https://github.com/laravel/dusk) · [Website](https://laravel.com/docs/dusk) |
| 66 | **Laravel Reverb** | `WebSocket` | First-party WebSocket server for Laravel. Real-time broadcasting. | [GitHub](https://github.com/laravel/reverb) · [Website](https://laravel.com/docs/reverb) |
| 67 | **Lighthouse** | `GraphQL` | Framework for serving GraphQL from Laravel applications. | [GitHub](https://github.com/nuwave/lighthouse) · [Website](https://lighthouse-php.com) |
| 68 | **Larastan** | `Static Analysis` | PHPStan extension for Laravel. Finds bugs without running code. | [GitHub](https://github.com/larastan/larastan) |
| 69 | **Spatie Laravel Data** | `Data Objects` | Powerful data objects for Laravel applications. | [GitHub](https://github.com/spatie/laravel-data) · [Website](https://spatie.be/docs/laravel-data) |
| 70 | **Laravel Octane** | `Performance` | Supercharge Laravel with Swoole and RoadRunner. | [GitHub](https://github.com/laravel/octane) · [Website](https://laravel.com/docs/octane) |

---

## 🚀 Production SaaS & Commercial Platforms

| # | Project | Category | Description | Links |
|--:|---------|----------|-------------|-------|
| 71 | **Mumsnet** | `Community / Publishing` | UK's largest parenting platform, fully rebuilt on Laravel. | [Website](https://www.mumsnet.com) |
| 72 | **SaaSykit** | `SaaS Boilerplate` | Laravel-based boilerplate for building SaaS products. | [GitHub](https://github.com/saasykit/saasykit) · [Website](https://saasykit.com) |
| 73 | **Laracasts** | `Education` | Definitive educational resource for Laravel developers. Laravel + Vue backend. | [Website](https://laracasts.com) |
| 74 | **Directify** | `Directory / SaaS` | Directory builder SaaS. $50K revenue, $1.5K MRR. Laravel + Filament. | [Website](https://directify.app) |
| 75 | **Klasio** | `LMS / Education` | Modern LMS for creators, educators, and online academies. | [Website](https://klasio.com) |
| 76 | **Ghost Explorer** | `Publishing` | Powers explore.ghost.org. ~12M req/mo on Laravel Cloud. | [Website](https://ghost.org) |
| 77 | **SplitMyExpenses** | `Finance / Personal` | Expense splitting app built with Laravel. | [Website](https://splitmyexpenses.com) |
| 78 | **LINQ Me Up** | `AI / SaaS` | AI-empowered SaaS platform built with Laravel. | — |
| 79 | **StyleCI** | `CI/CD` | PHP coding style continuous integration service. Fixes GitHub repos. | [Website](https://styleci.io) |
| 80 | **Handesk** | `Helpdesk` | Help desk ticketing and lead management tool. | [GitHub](https://github.com/BadChoice/handesk) |

---

## ⚡ Community Favorites & Utilities

| # | Project | Category | Description | Links |
|--:|---------|----------|-------------|-------|
| 81 | **Laravel Datatables** | `UI / Tables` | jQuery DataTables API for Laravel. Server-side processing. | [GitHub](https://github.com/yajra/laravel-datatables) · [Website](https://yajrabox.com/docs/laravel-datatables) |
| 82 | **Laravel Websockets** | `WebSocket` | WebSocket server implemented in PHP for Laravel. | [GitHub](https://github.com/beyondcode/laravel-websockets) · [Website](https://beyondco.de/docs/laravel-websockets) |
| 83 | **Spatie Laravel Sitemap** | `SEO` | Generate sitemaps for Laravel applications. | [GitHub](https://github.com/spatie/laravel-sitemap) · [Website](https://spatie.be/docs/laravel-sitemap) |
| 84 | **Laravel DomPDF** | `PDF Generation` | HTML to PDF conversion wrapper for Laravel using DomPDF. | [GitHub](https://github.com/barryvdh/laravel-dompdf) |
| 85 | **Laravel Envoy** | `Deployment` | Task runner for executing common tasks on remote servers. | [GitHub](https://github.com/laravel/envoy) · [Website](https://laravel.com/docs/envoy) |
| 86 | **Timegrid** | `Booking / Scheduling` | Online reservation platform for businesses. | [GitHub](https://github.com/timegridio/timegrid) |
| 87 | **GitScrum** | `Project Management` | Git + Scrum task management for developer teams. | [GitHub](https://github.com/renatomarinho/laravel-gitscrum) · [Website](https://gitscrum.com) |
| 88 | **Laravel Pulse** | `Monitoring` | Real-time application performance monitoring dashboard. | [GitHub](https://github.com/laravel/pulse) · [Website](https://laravel.com/docs/pulse) |
| 89 | **Spatie Translatable** | `Localization` | Make Eloquent models translatable. | [GitHub](https://github.com/spatie/laravel-translatable) · [Website](https://spatie.be/docs/laravel-translatable) |
| 90 | **Laravel Folio** | `Routing` | Page-based routing for Laravel applications. | [GitHub](https://github.com/laravel/folio) · [Website](https://laravel.com/docs/folio) |

---

## 🌐 Platforms, Services & Emerging Tools

| # | Project | Category | Description | Links |
|--:|---------|----------|-------------|-------|
| 91 | **Voten** | `Social Media` | Real-time community platform. Slack + Reddit hybrid. | [GitHub](https://github.com/voten-co/voten) |
| 92 | **Laravel Envoyer** | `Deployment` | Zero downtime deployment tool for PHP/Laravel. | [Website](https://envoyer.io) |
| 93 | **Laravel Forge** | `Server Management` | Server management and deployment. Powers thousands of Laravel apps. | [Website](https://forge.laravel.com) |
| 94 | **Laravel Vapor** | `Serverless` | Serverless deployment platform for Laravel powered by AWS Lambda. | [Website](https://vapor.laravel.com) |
| 95 | **Laravel Cloud** | `Cloud Platform` | Official Laravel cloud hosting platform. | [Website](https://cloud.laravel.com) |
| 96 | **Snappy** | `PDF Generation` | Wrapper for wkhtmltopdf/wkhtmltoimage in Laravel. | [GitHub](https://github.com/KnpLabs/snappy) |
| 97 | **Spatie Newsletter** | `Email Marketing` | Manage email newsletters with Mailchimp integration. | [GitHub](https://github.com/spatie/laravel-newsletter) |
| 98 | **Notification Channels** | `Notifications` | Community-driven notification channels (Slack, Telegram, etc.). | [GitHub](https://github.com/laravel-notification-channels) · [Website](https://laravel-notification-channels.com) |
| 99 | **NativePHP** | `Desktop / Mobile` | Build native desktop and mobile apps with PHP and Laravel. | [GitHub](https://github.com/nativephp/laravel) · [Website](https://nativephp.com) |
| 100 | **Laravel Prompts** | `CLI / UX` | Beautiful and user-friendly forms for command-line applications. | [GitHub](https://github.com/laravel/prompts) · [Website](https://laravel.com/docs/prompts) |

---

## 📊 Category Breakdown

| Category | Count |
|----------|------:|
| Admin Panel | 5 |
| CMS | 5 |
| E-Commerce | 3 |
| Developer Tools | 3 |
| Authentication | 3 |
| DevOps | 2 |
| CRM | 2 |
| Finance | 2 |
| Invoicing | 2 |
| Helpdesk | 2 |
| Social Media | 2 |
| Community | 2 |
| Payments | 2 |
| Starter Kit | 2 |
| Frontend | 2 |
| Testing | 2 |
| WebSocket | 2 |
| PDF Generation | 2 |
| Deployment | 2 |
| Media | 1 |
| Documentation | 1 |
| Status Pages | 1 |
| Forum | 1 |
| Asset Management | 1 |
| Accounting | 1 |
| Game Server Management | 1 |
| POS System | 1 |
| Blogging | 1 |
| Event Management | 1 |
| Static Site Generator | 1 |
| Auth | 1 |
| Data Import/Export | 1 |
| Queue Management | 1 |
| Search | 1 |
| Real-time | 1 |
| API Framework | 1 |
| Chatbot | 1 |
| Geocoding | 1 |
| Podcast Analytics | 1 |
| Analytics | 1 |
| File Management | 1 |
| Logging | 1 |
| Multi-Tenancy | 1 |
| Feature Flags | 1 |
| WordPress Integration | 1 |
| API | 1 |
| Code Style | 1 |
| GraphQL | 1 |
| Static Analysis | 1 |
| Data Objects | 1 |
| Performance | 1 |
| SaaS Boilerplate | 1 |
| Education | 1 |
| Directory | 1 |
| LMS | 1 |
| Publishing | 1 |
| AI | 1 |
| CI/CD | 1 |
| UI | 1 |
| SEO | 1 |
| Booking | 1 |
| Project Management | 1 |
| Monitoring | 1 |
| Localization | 1 |
| Routing | 1 |
| Server Management | 1 |
| Serverless | 1 |
| Cloud Platform | 1 |
| Email Marketing | 1 |
| Notifications | 1 |
| Desktop | 1 |
| CLI | 1 |

---

## 🔗 Key Resources

- [Laravel Framework](https://github.com/laravel/laravel) — The framework itself (79k+ stars)
- [Awesome Laravel](https://github.com/chiraggude/awesome-laravel) — Curated list of packages, tutorials, and resources
- [Laravel Open-Source Projects](https://github.com/goodnesskay/Laravel-Open-Source-Projects) — Categorized list of open-source Laravel apps
- [Large Laravel Project Examples](https://github.com/LaravelDaily/Large-Laravel-PHP-Project-Examples) — Real production projects with traffic/revenue data
- [Laravel Daily Packages](https://laraveldaily.com/packages) — 239+ curated packages with 100+ GitHub stars
- [Laravel Daily Open-Source Projects](https://laraveldaily.com/code-examples/projects) — Sortable list with code examples

---

*Last updated: March 2026. Star counts are approximate and change frequently.*

