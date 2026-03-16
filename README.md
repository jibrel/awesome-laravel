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
