# Builder stack handbook

156 entries · last verified 2026-09-21 · 156 links checked · 0 dead

One founder's handbook for building websites, apps, dashboards, visuals and outbound with AI agents: where I get design references, the component libraries and prompt packs I start from, how I ship and check what the agent built, the image and video stack, which scraper for which data, and the skills I hand Claude Code. It merges my private Notion notes with the public link directory at [agentmatik.ai/links](https://agentmatik.ai/links). It is not a directory of everything that exists - if something is here, it earned its place in real work. The longer notes live in [FIELD-NOTES.md](FIELD-NOTES.md). Suggest a link by opening an issue (see [CONTRIBUTING.md](CONTRIBUTING.md)).

Descriptions are my own notes where I wrote one. Where I only saved a link, the description is the repository's, the page's or the post's own summary. A suffix like `(free, no account)`, `(free account)` or `(paid)` is the access label from the agentmatik.ai directory, and a `Why:` that says "we" or "our" is that directory's reason, written for Agentmatik's clients. Ratings like `(Matt: 8/10)` are my personal scores.

## Contents

- [Start here](#start-here)
- [Web design and inspiration](#web-design-and-inspiration)
  - [Website inspiration databases](#website-inspiration-databases)
  - [Design sources and MCPs](#design-sources-and-mcps)
  - [Website prompts](#website-prompts)
  - [Google Stitch](#google-stitch)
- [Dashboards and UI components](#dashboards-and-ui-components)
  - [Dashboard elements](#dashboard-elements)
  - [UI components](#ui-components)
- [Build and ship](#build-and-ship)
  - [RAG](#rag)
  - [Mobile app dev](#mobile-app-dev)
- [Photos, video and design](#photos-video-and-design)
  - [Model aggregators and API providers](#model-aggregators-and-api-providers)
  - [Higgsfield](#higgsfield)
  - [Video generation](#video-generation)
  - [Video editing](#video-editing)
  - [Claude Design for video](#claude-design-for-video)
  - [Tool-specific tutorials](#tool-specific-tutorials)
  - [Upscaling](#upscaling)
- [Scraping and social data](#scraping-and-social-data)
  - [ScrapeCreators](#scrapecreators)
  - [Firecrawl](#firecrawl)
  - [Apify](#apify)
- [GTM and sales](#gtm-and-sales)
  - [Agents](#agents)
- [Skills for builders](#skills-for-builders)
  - [Development skills](#development-skills)
  - [GTM skills](#gtm-skills)
  - [Skill collections and registries](#skill-collections-and-registries)
- [Learning](#learning)
  - [Websites and apps](#websites-and-apps)
  - [Photos, video and design](#photos-video-and-design-1)
  - [GTM and sales](#gtm-and-sales-1)
  - [Videos](#videos)
  - [Creators](#creators)
  - [Podcasts and newsletters](#podcasts-and-newsletters)
- [Field notes](#field-notes)
- [How this list is built](#how-this-list-is-built)
- [License](#license)

## Start here

What I would send a founder who has one evening: my highest-rated picks and the first entries I wrote a reason for. The full list follows.

- [AI Templates](https://www.aitmpl.com) - 1,000+ Claude Code components: 842 skills, 421 agents, 281 commands, 86 MCPs, and 57 hooks (free, no account) Why: Huge surface area - useful for discovering what categories of components even exist. · Skills for builders / Skill collections and registries
- [AI UX Playground](https://aiuxplayground.com/prompts) - Copy-ready AI prompts for designers and PMs - landing-page copy, workflows, and multi-step design processes (free, no account) Why: Rare prompt set aimed at the design/PM workflow, not just code generation. · Web design and inspiration / Website prompts
- [AI Website Prompt Generator](https://aiwebsitepromptgenerator.com) - A generator that writes high-quality website prompts to clone a layout, rebrand a page, match a style, or build from scratch (free, no account) Why: Turns a reference or an idea into a builder-ready prompt in one step. · Web design and inspiration / Website prompts
- [AI with Remy](https://www.youtube.com/@aiwithremy) - Hands-on AI tutorials with a practical, non-hype angle (free, no account) Why: Consistently useful walkthroughs - rated Great in our creator database. · Learning / Creators
- [anthropics/skills](https://github.com/anthropics/skills) - Anthropic's official open-source skill collection. Why: First stop for official, maintained skills - frontend design, skill creator, canvas, themes. · 177k stars · updated 2026-09 · Skills for builders / Skill collections and registries
- [Awesome Claude Code](https://github.com/hesreallyhim/awesome-claude-code) - Selectively curated list of the best skills, hooks, slash commands, orchestrators, and plugins for Claude Code (free, no account) Why: Stricter curation than most awesome-lists - things here tend to actually work. · 54k stars · updated 2026-09 · Skills for builders / Skill collections and registries
- [Awesome Claude Design](https://github.com/rohitg00/awesome-claude-design) - A curated repo of Claude design prompts and recipes - including a 20-minute landing-page recipe (free, no account) Why: Open, versioned, and diff-able - the engineering approach to design prompts (843 stars). · 1.1k stars · MIT · updated 2026-04 · Web design and inspiration / Website prompts
- [Awesome Claude Skills](https://github.com/ComposioHQ/awesome-claude-skills) - Composio's curated list of Claude skills, resources, and tools (free, no account) Why: The best-maintained general directory when you want breadth. · 75k stars · updated 2026-09 · Skills for builders / Skill collections and registries
- [Behance](https://www.behance.net) - Adobe's creative network - vast galleries of branding, product, and web design projects (free, no account) Why: Broader and more art-directed than the dev-focused galleries - great for visual direction before you design. · Web design and inspiration / Website inspiration databases
- [Behind the Craft](https://www.youtube.com/@peteryang) - Peter Yang's show on how the best builders actually work with AI - hands-on interviews, not punditry (free, no account) Why: One of the few AI shows where guests share real workflows you can copy the same day. · Learning / Podcasts and newsletters
- [Claire Vo](https://www.youtube.com/@howiaipodcast) - The How I AI podcast - practitioners showing exactly how they use AI at work (free, no account) Why: Real screen-share workflows instead of talking heads. · Learning / Creators
- [Claude Code UI Agents](https://github.com/mustafakendiguzel/claude-code-ui-agents) - A collection of Claude prompts and agent definitions built for UI/UX design and frontend tasks (free, no account) Why: Purpose-built for front-end work in Claude Code (560 stars). · 636 stars · MIT · updated 2025-08 · Web design and inspiration / Website prompts

## Web design and inspiration

Where I look before I let an agent touch a layout: the galleries I harvest references from, the copy-paste component libraries and MCPs that return clean markup, prompt libraries for the first draft, Google Stitch for interactive mockups, and my notes on making Claude Design earn its quota.

### Website inspiration databases

- [Awwwards](https://www.awwwards.com/directory) - Award-winning websites - the high end of what the web can look like (free, no account)
- [Behance](https://www.behance.net) - Adobe's creative network - vast galleries of branding, product, and web design projects (free, no account) Why: Broader and more art-directed than the dev-focused galleries - great for visual direction before you design.
- [Dribbble](https://dribbble.com/shots/popular) - The classic design showcase - what designers are shipping right now (free, no account)
- [Framer Marketplace](https://www.framer.com/marketplace) - Production-ready Framer templates - useful as structure references even off-Framer (free, no account)
- [Land Book](https://land-book.com) - Curated gallery of real landing pages, searchable by industry and style - free.
- [SiteInspire](https://www.siteinspire.com) - Clean, filterable showcase of web design - strong on typography-led sites (free, no account)
- [Trickle](https://trickle.so) - 50 prompts organized by visual style, mood, and interaction type (free, no account)
- [Vibe Code Components](https://vibecodecomponents.com) - Premium React component prompts that generate design-ready UI (free, no account)

### Design sources and MCPs

- [21st.dev](https://21st.dev) - shadcn block and component marketplace with a large community registry plus the Magic AI MCP - quality varies (community-submitted), so vet each component; copy the prompt from there.
- [Aceternity UI](https://ui.aceternity.com) - Stunning animated hero, 3D and spotlight components, but heavy and weak on accessibility - cherry-pick for marketing pages, skip for app screens and forms. Freemium.
- [AstroWind](https://github.com/arthelokyo/astrowind) - Top Astro+Tailwind landing theme - Free. · 6k stars · MIT · updated 2026-09
- [Cruip free templates](https://cruip.com/free-templates) - Free SaaS landing templates (Simple Light, Open) - lightweight Tailwind CSS starting points, GPL.
- [daisyUI](https://daisyui.com) - Semantic Tailwind components as a plugin; works on any stack (Vue, Svelte, Astro, plain HTML), no JS lock-in. 41k stars, MIT.
- [Flowbite](https://flowbite.com) - 400+ Tailwind components with the widest framework parity (official React, Vue, Svelte and Angular packages). 9k stars, free core plus paid Pro.
- [Flowrift](https://flowrift.com) - 80+ beautifully designed vanilla HTML Tailwind CSS UI blocks - free.
- [HyperUI](https://hyperui.dev) - Largest free copy-paste HTML plus Tailwind set, zero dependencies, actively maintained. 12k stars, MIT, no pro tier.
- [Lapa Ninja](https://lapa.ninja) - 7,300+ landing pages, tightly categorized - the fastest way to see 20 takes on one pattern. Free.
- [Magic UI](https://magicui.design) - 150+ animated, shadcn-compatible components - the best-balanced animated companion to shadcn (marquees, beams, text effects). 21k stars, MIT, shadcn-MCP installable.
- [Mamba UI](https://mambaui.com) - 150+ free Tailwind CSS components and templates, copy as HTML, Vue or JSX.
- [Meraki UI](https://merakiui.com) - 144 clean copy-paste components with first-class RTL support and dark mode - narrower catalog and quiet since mid-2025. Free.
- [Mobbin](https://mobbin.com) - 400k+ real app screenshots, fully searchable - how the best products actually solve each screen. Freemium.
- [One Page Love](https://onepagelove.com) - One-page website gallery showcasing the best single-page sites, templates and resources - free.
- [Paste a URL, get a DESIGN.md (Tran Mau Tri Tam on X)](https://x.com/tranmautritam/status/2047744367549612456) - Drop in a website and get its exact design written as a markdown file; feed that file to Claude Code to replicate the design language on whatever you are building.
- [React Bits](https://reactbits.dev) - 110+ animated, interactive and fully customizable open-source React components - free.
- [Recent (ex-Godly)](https://recent.design) - High-end curated web design gallery - godly.website now redirects to recent.design.
- [SaaS Landing Page](https://saaslandingpage.com) - The best SaaS landing pages since 2020, organized by section and element - free.
- [Tailblocks](https://tailblocks.cc) - 60+ ready-to-use Tailwind CSS blocks - free, but stale (my table flags it).
- [TailGrids](https://tailgrids.com) - 100+ free blocks (HTML, React, Vue) from a polished React plus Figma plus CLI system - thin free tier, only worth it if you will pay for Pro.

### Website prompts

- [AI UX Playground](https://aiuxplayground.com/prompts) - Copy-ready AI prompts for designers and PMs - landing-page copy, workflows, and multi-step design processes (free, no account) Why: Rare prompt set aimed at the design/PM workflow, not just code generation.
- [AI Website Prompt Generator](https://aiwebsitepromptgenerator.com) - A generator that writes high-quality website prompts to clone a layout, rebrand a page, match a style, or build from scratch (free, no account) Why: Turns a reference or an idea into a builder-ready prompt in one step.
- [Awesome Claude Design](https://github.com/rohitg00/awesome-claude-design) - A curated repo of Claude design prompts and recipes - including a 20-minute landing-page recipe (free, no account) Why: Open, versioned, and diff-able - the engineering approach to design prompts (843 stars). · 1.1k stars · MIT · updated 2026-04
- [Claude Code UI Agents](https://github.com/mustafakendiguzel/claude-code-ui-agents) - A collection of Claude prompts and agent definitions built for UI/UX design and frontend tasks (free, no account) Why: Purpose-built for front-end work in Claude Code (560 stars). · 636 stars · MIT · updated 2025-08
- [Design Prompts](https://designprompts.dev) - 31+ design styles rendered from the same data, each with an AI-ready prompt to recreate the aesthetic (free, no account) Why: Fastest way to calibrate a style: compare identical content across 31 aesthetics, then copy the winner.
- [Eversince.ai](https://eversince.ai) - Prompts for hyperrealistic motion on websites - the site now pitches itself as media infrastructure for AI agents.
- [InstaLanding.ai](https://instalanding.ai) - One-shot prompts for cinematic, scroll-based, and interactive landing page components (free, no account) Why: The one-shot components actually look premium out of v0 or Lovable - no ten-round prompt surgery.
- [Jiro](https://jiro.build) - A design prompt library to vibe-code better websites - premium templates and components by niche (travel, e-commerce, SaaS) (free, no account) Why: The strongest art direction per niche - pick the vertical, get a coherent visual language.
- [Lovable Prompts](https://lovable-prompts.com) - 101+ ready-to-use prompts for Lovable - SaaS apps, landing pages, UI/UX components, and backend logic (free, no account) Why: The deepest Lovable-specific set - useful even as a checklist of what to specify.
- [Motionsites.ai](https://motionsites.ai) - Premium prompts built specifically for animated, motion-based hero sections.
- [Prompt Library for UI](https://prompt-library-ui.lovable.app) - UI prompts organized by design style - Expressive, Premium, and more - to steer the look of AI-generated interfaces (free, no account) Why: Style-first: pick the aesthetic, get the prompt that produces it.
- [Promtable](https://promtable.com/prompts/bolt) - Free copy-ready prompts for Bolt.new and other AI builders - copy and adapt without a signup. Why: Genuinely free and frictionless - no gate, no account.
- [shadcn space](https://shadcnspace.com) - Shadcn UI blocks, templates, and components with a one-click Copy Prompt feature for v0, Lovable, and Bolt (free, no account) Why: Pairs perfectly with our shadcn-first workflow - the prompts are pre-optimized for AI builders.
- [StyleKit](https://www.stylekit.top/en/tailwind-ui-prompts) - Tailwind UI prompts - copy a prompt per component to generate Tailwind CSS designs (free, no account) Why: Prompt-per-component granularity for Tailwind-native builds.
- [Superdesign](https://superdesign.dev) - A free, open library of hundreds of UI and design prompts - dashboards, landing pages, components, animations - each with a live preview. Why: The biggest free prompt library we know: search the grid, preview the result, copy the prompt.
- [TurnConcepts](https://turnconcepts.com) - Copy-ready prompts and UI concepts for ChatGPT, Claude, and Cursor - prompt plus rendered UI proof in every card (free, no account) Why: You see the rendered result before you copy - no prompt roulette.
- [ui-prompts (GitHub)](https://github.com/arhamkhnz/ui-prompts) - An open-source collection of reusable prompts for consistent UI generation, including versioned dashboard prompts. Why: Versioned prompts you can diff, fork, and adapt - the engineering approach to prompt libraries. · 39 stars · updated 2026-03
- [WebsitePrompts](https://websiteprompts.com) - A free library of website prompts for ChatGPT, Claude, v0, Cursor, and Bolt - landing pages, SaaS sites, portfolios. Why: Tool-agnostic base library - a solid starting prompt for almost any site type.

### Google Stitch

- [Google Stitch](https://blog.google/innovation-and-ai/models-and-research/google-labs/stitch-ai-ui-design) - Google Labs' AI UI design tool: describe the vibe, audience and aesthetic, or give it a screenshot or URL, and it generates real, interactive UI components. Exports a design.md file Claude Code can follow. My notes on it are in the field notes.

My notes on this section: [Web design and inspiration](FIELD-NOTES.md#web-design-and-inspiration) (32 notes).

## Dashboards and UI components

The admin templates, chart libraries and component systems I benchmark dashboards against - the shadcn stack first, then what to add for charts, tables and animation. Where a link is a GitHub repository, star counts and licenses come from GitHub and are refreshed weekly.

### Dashboard elements

- [AdminLTE](https://adminlte.io) - The most popular open-source Bootstrap admin dashboard template (45,000+ GitHub stars) - free and premium versions.
- [AG Grid](https://www.ag-grid.com/react-data-grid) - Component library. Exceptional performance (free, no account)
- [Ant Design](https://ant.design) - Dense enterprise tables and forms - the standard for ops-heavy admin UIs. Free.
- [Ant Design Pro](https://github.com/ant-design/ant-design-pro) - Full template. Enterprise-ready architecture (free, no account) · 38k stars · MIT · updated 2026-09
- [Apache ECharts](https://github.com/apache/echarts) - Component library. Extensive chart types (20+) (free, no account) · 67k stars · Apache-2.0 · updated 2026-09
- [ApexCharts](https://apexcharts.com) - Modern JavaScript charting library for interactive charts with a simple API - 100+ ready samples to copy, free.
- [Chakra UI](https://www.chakra-ui.com) - Solid, themeable, 40k★ - but the v3 Panda/Ark rewrite adds migration friction. Great on a fresh start.
- [CoreUI](https://coreui.io) - Admin templates and UI components for Bootstrap, React, Angular and Vue - MIT-licensed free core, paid Pro.
- [coss ui (ex-Origin UI)](https://coss.com/ui) - Origin UI was acquired by Cal.com and rebranded to coss ui, a modern component library built on Base UI. Adopt the new coss ui, not the frozen Origin snapshot.
- [Cruip Mosaic](https://github.com/cruip/tailwind-dashboard-template) - Mosaic Lite - free analytics dashboard template built on Tailwind CSS and fully coded in React with Chart.js (GPL). · 2.8k stars · updated 2025-03
- [Cult UI](https://www.cult-ui.com) - Highest visual craft for animated/marketing components. 5k★, MIT, shadcn-MCP installable (free, no account)
- [Efferd](https://efferd.com) - The dashboard look I benchmark against - take the elements from here and paste them into Claude Code.
- [Eldora UI](https://www.eldoraui.site) - Nice free animated effects, shadcn companion. 1.9k★ but single-maintainer - treat as a grab-bag, not a foundation.
- [Float UI](https://floatui.com) - Good-looking multi-framework copy-paste. Effectively unmaintained (~Mar 2025) - cherry-pick, don't standardize.
- [Flowbite Admin](https://github.com/themesberg/flowbite-admin-dashboard) - Free and open-source admin dashboard template with Tailwind dashboard widgets, built with Tailwind CSS and Flowbite. · 2.9k stars · MIT · updated 2025-03
- [HeroUI (ex-NextUI)](https://www.heroui.com) - Gorgeous out of the box, built on React Aria for strong accessibility. 29k stars, MIT - just time the v2 to v3 migration carefully.
- [Horizon AI Boilerplate](https://github.com/horizon-ui/shadcn-nextjs-boilerplate) - Full template. Pre-built AI chat and dashboard layouts (free, no account) · 649 stars · MIT · updated 2025-01
- [Kokonut UI](https://kokonutui.com) - Large free pool of modern animated components, easy shadcn add install. 1.9k★, MIT.
- [Mantine](https://mantine.dev) - Broadest batteries-included system (~100 components plus hooks, dates and charts), ideal for data-heavy admin apps. Imported dependency, 31k stars, MIT.
- [Motion Primitives](https://motion-primitives.com) - Reusable, tasteful animation building blocks rather than full sections. 5.6k★, MIT (commit cadence slowing slightly) (free, no account)
- [MUI X](https://mui.com) - Enterprise data grid and pickers on top of MUI's React component library - freemium.
- [next-shadcn-admin-dashboard](https://github.com/arhamkhnz/next-shadcn-admin-dashboard) - Full template. Modern Next.js 16 and Tailwind v4 stack (free, no account) · 3.1k stars · MIT · updated 2026-09
- [next-shadcn-dashboard-starter](https://github.com/Kiranism/next-shadcn-dashboard-starter) - Full template. Explicit AGENTS.md file for AI workflows (free, no account) · 7k stars · MIT · updated 2026-09
- [Nivo](https://nivo.rocks) - 50+ React chart types - supercharged React dataviz components, free. · also: [github.com](https://github.com/plouc/nivo)
- [Nuxt Dashboard Template](https://github.com/nuxt-ui-templates/dashboard) - Full template. Clean and modern design (free, no account) · 1.1k stars · MIT · updated 2026-09
- [Park UI](https://park-ui.com) - shadcn-style ownership across multiple frameworks (Panda CSS + Ark). 2.3k★ but cadence has stalled; watch what the Chakra org does with it.
- [Preline](https://preline.co) - Best-looking free copy-paste library (needs a small JS plugin for interactivity). 6k★, free core + paid Pro.
- [Radix UI](https://www.radix-ui.com) - Headless, unstyled, gold-standard accessible primitives - the engine under shadcn. 19k★, MIT; use when building a custom design system (free, no account)
- [React Admin](https://marmelab.com/react-admin) - Platform. Backend agnostic (REST/GraphQL) (free, no account)
- [Recharts](https://recharts.github.io) - React charts - free. The recharts.org site has moved to recharts.github.io, the link follows it.
- [Refine](https://refine.dev) - Platform. Headless architecture (free, no account)
- [shadcn dashboard example](https://ui.shadcn.com/examples/dashboard) - The official shadcn/ui dashboard example - the closest thing to the Efferd look, free; start there and make it your own.
- [shadcn-admin](https://github.com/satnaing/shadcn-admin) - Full template. Built on shadcn/ui and Tailwind CSS (free, no account) · 14k stars · MIT · updated 2026-09
- [shadcn-dashboard-landing-template](https://github.com/shadcnstore/shadcn-dashboard-landing-template) - Full template. Dual framework support (Next.js and Vite) (free, no account) · 1.2k stars · MIT · updated 2026-02
- [shadcn-ui-sidebar](https://github.com/salimi-my/shadcn-ui-sidebar) - Specialist. Custom shadcn/ui registry support for easy CLI installation (free, no account) · 1.8k stars · MIT · updated 2025-04
- [shadcn/ui](https://ui.shadcn.com) - The foundation: copy-in primitives you own, accessible, the standard everything else builds on. 117k stars, MIT, reachable through the shadcn MCP.
- [shadcn/ui blocks](https://ui.shadcn.com/blocks) - The official shadcn/ui blocks - dashboards, sidebars, charts, and full page sections you copy straight in (free, no account) Why: The dashboard blocks and charts are the fastest way to a clean operator UI on the shadcn stack - same components we assemble from.
- [shadcnblocks](https://www.shadcnblocks.com) - 1,600+ ready page sections purpose-built for shadcn. Paid ($149+ once) - pays for itself on one client project.
- [ShadcnSpace Admin Dashboard](https://shadcnspace.com/admin-dashboard) - Full template. Built-in Agents.md for AI context (free account)
- [Skiper UI](https://skiper-ui.com) - Distinctive premium interactions, shadcn-installable. Closed-source + solo-maintained + mostly paid ($129+) - accept the lock-in knowingly.
- [Tabler](https://tabler.io) - Premium-quality free Bootstrap admin template with well-designed components and 6k icons.
- [TailAdmin](https://tailadmin.com) - Free and open-source Tailwind CSS admin dashboard template in seven verticals, with HTML, React, Vue and Next versions - free core, paid Pro.
- [Tailwind Plus](https://tailwindcss.com/plus) - Best-in-class marketing/app/ecommerce layout blocks from the Tailwind team. Paid ($299 once) but the highest-ROI paid asset here.
- [TanStack Start Dashboard](https://github.com/Kiranism/tanstack-start-dashboard) - Full template. Uses modern stack (TanStack Start, React 19, Vite 7, Tailwind CSS v4) (free, no account) · 749 stars · MIT · updated 2026-08
- [TanStack Table](https://github.com/TanStack/table) - Component library. Headless architecture allows 100% custom UI (free, no account) · 28k stars · MIT · updated 2026-09
- [Tremor](https://tremor.so) - 35+ dashboard blocks, KPI cards and charts for React - the best free option for dashboards and charts, copy-in code you own. Use the current tremorlabs/tremor repo, not the frozen npm package.
- [Tremor OSS template](https://github.com/tremorlabs/template-dashboard-oss) - Free open-source SaaS dashboard template by Tremor, built on Next.js. · 518 stars · Apache-2.0 · updated 2025-10
- [v0](https://v0.app) - Vercel's prompt-to-UI generator on a shadcn/Next stack; own and review the output. Freemium (~$20/mo) - a generator, not a component "source."
- [Windmill](https://github.com/estevanmaito/windmill-dashboard) - React plus Tailwind dashboard with dark mode - a multi-theme, completely accessible, production-ready dashboard template. Free. · 3k stars · MIT · updated 2024-02

### UI components

- [Design Spells](https://designspells.com) - A catalog of delightful UI details - the little touches that make products feel alive (free, no account)
- [shadcn.io](https://www.shadcn.io) - Platform. Native MCP server integration eliminates AI hallucination of props (free, no account)
- [shadcn/studio](https://shadcnstudio.com/blocks) - Component library. 800+ blocks across marketing, dashboard, and ecommerce (free account)
- [ShaderGradient](https://shadergradient.co) - Animated gradient shaders you can configure visually and drop into a site (free, no account)
- [Untitled UI React](https://www.untitledui.com/react) - Component library. Built with modern stack (React 19.2, Tailwind v4.3, React Aria) (paid)

## Build and ship

Getting a vibe-coded site from localhost to a real domain and keeping it honest. The deploy loop I use: Claude Code edits locally, nothing is pushed until I say so, GitHub receives the commit, Vercel deploys it and serves the custom domain. Then screenshot-based self-checks, RAG and knowledge-store rules, paywalls for mobile, analytics.

### RAG

- [RAG explained: reranking for better answers (Towards Data Science)](https://towardsdatascience.com/rag-explained-reranking-for-better-answers) - Explains why RAG agents do not always return the best results and what reranking does about it.

### Mobile app dev

- [Superwall](https://superwall.com) - Paywall testing for mobile apps - their pitch: monetization and experimentation tools, paywalls, entitlements and SDKs for iOS, Android and web. On my list for testing paywalls before committing to one.

My notes on this section: [Build and ship](FIELD-NOTES.md#build-and-ship) (6 notes).

## Photos, video and design

The image and video stack: a five-phase production pipeline, the model aggregators and API providers I run generations through, Higgsfield's MCP, Seedance and Kling for video, Hyperframes for editing inside Claude Code, and what SwiftCut really is under the hood. Prompting rules for Nano Banana Pro and Kling 3.0 live in the field notes.

### Model aggregators and API providers

- [fal.ai](https://fal.ai) - Generative media API platform - image, video, 3D and audio models (FLUX, Kling, Hailuo and 1000+ more) behind one API. Also the API SwiftCut runs on.
- [Higgsfield](https://higgsfield.ai) - AI-native creative suite: images, video and voice from text prompts or references, editing and upscaling, with an MCP server to drive it from Claude Code.
- [Kie.ai](https://kie.ai) - One API for chat, video, image and music models - used by Nate Herk, good for API use.

### Higgsfield

- [Higgsfield MCP server](https://higgsfield.ai/mcp) - Connect Higgsfield's MCP server to Claude Code (or another agent) and generate images and video from there - the video walkthrough is linked as well. · also: [youtube.com](https://www.youtube.com/watch?v=20BDYk-CU_o)

### Video generation

- [Seedance 2.0 best practices (Amir D on X)](https://x.com/starks_arq/status/2037928570257903983) - Amir D's Seedance 2.0 best-practices post - the post is an image with a link, my label is the only text there is.

### Video editing

- [Hyperframes](https://github.com/nateherkai/hyperframes-student-kit) - add-on to edit videos in Claude Code. · 890 stars · updated 2026-09

### Claude Design for video

- [Create videos, web and apps with Claude Design - tutorial (Peter Yang on LinkedIn)](https://www.linkedin.com/posts/petergyang_heres-my-new-tutorial-with-a-live-demo-of-share-7451288623817342976-0DHY) - Peter Yang's tutorial post with a live demo of Claude Design. The text I kept from it compares Claude Design (upload a video and a transcript, get an animated version, export HTML for Claude Code to render) with Hyperframes plus Claude Code (more setup, more control).

### Tool-specific tutorials

- [Kling 2.5 Turbo image-to-video on fal.ai](https://fal.ai/models/fal-ai/kling-video/v2.5-turbo/standard/image-to-video) - The model behind SwiftCut's transitions: call fal-ai/kling-video-v2.5-turbo directly with start and end frame inputs and a similar prompt to replicate the exact same results.
- [SwiftCut](https://swiftcut.ai) - Cinematic transitions between two frames in minutes. Under the hood it is Kling 2.5 Turbo via the fal.ai API with a crafted transition prompt, hosted on the Vost.ai white-label platform - see the notes.

### Upscaling

- [When an upscaler is so good it feels illegal (r/comfyui)](https://www.reddit.com/r/comfyui/comments/1pi2i67/when_an_upscaler_is_so_good_it_feels_illegal) - The r/comfyui thread on an upscaler that felt too good - the one upscaling link I kept. Reddit shows crawlers nothing, so the title comes from the post slug.

My notes on this section: [Photos, video and design](FIELD-NOTES.md#photos-video-and-design) (11 notes).

## Scraping and social data

Which scraper for which job: ScrapeCreators for social platforms, Firecrawl for regular websites, Apify's store when you want a pre-built actor - plus per-platform notes on Twitter, Reddit and LinkedIn, including where native scraping beats an API and where it gets your account banned.

### ScrapeCreators

- [ScrapeCreators](https://scrapecreators.com) - Social media scraping API built for real-time data from 28+ platforms (Instagram, TikTok, YouTube, LinkedIn, X, Reddit and more) - the full social data stack, pay-as-you-go pricing. The notes cover where it wins (Reddit) and where it falls short (Twitter).

### Firecrawl

- [Firecrawl](https://www.firecrawl.dev) - General web scraping API for AI agents: any website into clean, LLM-ready Markdown or structured JSON; open source, self-hostable, integrates with n8n, LangChain and LlamaIndex. Not built for social media - the notes cover the pricing and structured-extraction complaints.

### Apify

- [Apify](https://apify.com) - The app store of scrapers: a pre-built actor for Amazon, Google Maps, Instagram and most other targets when you do not want to build one. Reliable at medium volume; pricing is hard to forecast (subscription plus compute units plus proxies plus actor rental) - see the notes.

My notes on this section: [Scraping and social data](FIELD-NOTES.md#scraping-and-social-data) (40 notes).

## GTM and sales

Short on purpose - most of my GTM material is course content or other people's pitches, and that stays private. What is here: agents doing sales work, and my notes on speed-to-lead systems. Swan's GTM skills are listed under Skills for builders.

### Agents

- [Agency Agents](https://github.com/msitarzewski/agency-agents) - A complete AI agency at your fingertips - From frontend wizards to Reddit community ninjas, from whimsy injectors to reality checkers. · 153k stars · MIT · updated 2026-09
- [OpenClaw turned into an outbound sales team - ClawGTM (Jaynit Makwana on X)](https://x.com/jaynitmakwana/status/2038530995465695628) - The post that introduced ClawGTM: paste your website and get a ready-to-launch outbound pipeline from an OpenClaw setup acting as a full outbound sales team.

My notes on this section: [GTM and sales](FIELD-NOTES.md#gtm-and-sales) (2 notes).

## Skills for builders

Skills I point Claude Code at when building products: the development skills from jeffallan's guide and friends (one link each - the guide explains them better than I would), Swan's GTM skill library, and the registries and collections I browse when I need one more.

### Development skills

- [Code Reviewer](https://jeffallan.github.io/claude-skills/skills/quality/code-reviewer) - Reviews diffs and files for bugs, security vulnerabilities, code smells, N+1 queries and architecture problems, then produces a prioritized review report - run it before opening a pull request (jeffallan/claude-skills).
- [debug-skill (AlmogBaku)](https://github.com/AlmogBaku/debug-skill) - Let your coding agent debug like a human developer: set breakpoints, step through code, evaluate expressions - the way you actually debug. · 323 stars · MIT · updated 2026-04
- [Feature Forge](https://jeffallan.github.io/claude-skills/skills/workflow/feature-forge) - Structured requirements workshops before you write code: feature specs, user stories, EARS-format requirements, acceptance criteria and implementation checklists (jeffallan/claude-skills).
- [Git worktrees skill (obra/superpowers)](https://github.com/obra/superpowers/tree/main/skills/using-git-worktrees) - Use when feature work needs isolation from the current workspace or before executing an implementation plan - ensures an isolated workspace via native tools or a git worktree fallback (the skill's own description). · 289k stars · MIT · updated 2026-09
- [Playwright Skill](https://github.com/testdino-hq/playwright-skill) - TestDino Playwright Skill: AI-powered guides for Playwright best practices, made by testdino.com. · 369 stars · MIT · updated 2026-09
- [RAG Architect](https://jeffallan.github.io/claude-skills/skills/data-ml/rag-architect) - Designs production-grade RAG systems: chunking, embeddings, vector stores, hybrid search, reranking and retrieval evaluation (jeffallan/claude-skills).
- [Secure Code Guardian](https://jeffallan.github.io/claude-skills/skills/security/secure-code-guardian) - Secure code by default when you build authentication, handle user input or want to prevent the OWASP Top 10 - password hashing, parameterized queries, CORS and CSP headers, input validation, JWT setup (jeffallan/claude-skills).
- [Spec Miner](https://jeffallan.github.io/claude-skills/skills/workflow/spec-miner) - Reverse-engineers specifications from existing codebases - legacy, undocumented or inherited systems: maps dependencies, documents business logic, generates API and architecture docs (jeffallan/claude-skills).
- [The Fool](https://jeffallan.github.io/claude-skills/skills/workflow/the-fool) - Challenges ideas, plans and decisions with structured critical reasoning - devil's advocate, pre-mortem, red team, evidence audit - before a big architecture decision (jeffallan/claude-skills).

### GTM skills

- [GTM skills by Swan (swan-gtm/gtm-skills)](https://github.com/swan-gtm/gtm-skills) - Open, production-grade go-to-market skills for AI agents - prospecting, research, outreach, signals, pipeline, RevOps - as plain SKILL.md files any agent can read. Built and curated by Swan, authored by the GTM community. · 158 stars · MIT · updated 2026-09

### Skill collections and registries

- [AI Templates](https://www.aitmpl.com) - 1,000+ Claude Code components: 842 skills, 421 agents, 281 commands, 86 MCPs, and 57 hooks (free, no account) Why: Huge surface area - useful for discovering what categories of components even exist.
- [anthropics/skills](https://github.com/anthropics/skills) - Anthropic's official open-source skill collection. Why: First stop for official, maintained skills - frontend design, skill creator, canvas, themes. · 177k stars · updated 2026-09
- [Awesome Claude Code](https://github.com/hesreallyhim/awesome-claude-code) - Selectively curated list of the best skills, hooks, slash commands, orchestrators, and plugins for Claude Code (free, no account) Why: Stricter curation than most awesome-lists - things here tend to actually work. · 54k stars · updated 2026-09
- [Awesome Claude Skills](https://github.com/ComposioHQ/awesome-claude-skills) - Composio's curated list of Claude skills, resources, and tools (free, no account) Why: The best-maintained general directory when you want breadth. · 75k stars · updated 2026-09
- [Claude Skills Guide (jeffallan)](https://jeffallan.github.io/claude-skills/skills-guide) - A hand-written guide and catalog of practical Claude Code skills by category (free, no account) Why: Where several of our development skills (Feature Forge, Code Reviewer, The Fool) come from.
- [gstack](https://github.com/garrytan/gstack) - Garry Tan's exact Claude Code setup - 23 opinionated tools acting as CEO, designer, engineering manager, release manager, and QA (free, no account) Why: A complete, working process for shipping with Claude Code - not a toolbox but a sprint: think, plan, build, review, test, ship. · 133k stars · MIT · updated 2026-09
- [Marketing Skills](https://github.com/coreyhaines31/marketingskills) - CRO, copywriting, SEO, analytics, and growth engineering skills for Claude Code (free, no account) Why: The copywriting, seo-audit, and content-strategy skills are the standouts. · 51k stars · MIT · updated 2026-09
- [skills.sh](https://www.skills.sh) - The leaderboard and registry for agent skills - installs, stars, and security audits per skill (free, no account) Why: Our primary source for vetting skills before they touch a client machine.

## Learning

Videos, creators and newsletters that shaped how I build - my own saves per topic, plus the learning material from the agentmatik.ai link directory.

### Websites and apps

- [Building Beautiful Websites with Claude Code Is Too Easy (Nate Herk)](https://www.youtube.com/watch?v=86HM0RUWhCk) - Five simple hacks for building and designing better websites in Claude Code - the video the screenshot loop comes from: let the agent screenshot its own output and iterate (Puppeteer); the resources are linked from the video.
- [Claude Design Builds Beautiful 3D Websites Instantly (full tutorial)](https://www.youtube.com/watch?v=TcFeSjwTo7g&t=215s) - YouTube video by Nate Herk | AI Automation.
- [Once You Know This, Building RAG Agents Becomes Easy in n8n](https://www.youtube.com/watch?v=kOKavHnlPik) - YouTube video by Nate Herk | AI Automation.
- [The NEW Nano Banana 2 + Claude Code = $10k Websites](https://www.youtube.com/watch?v=q0TgUtj6vIs) - YouTube video by Nate Herk | AI Automation.

### Photos, video and design

- [Claude Video Editing Just Became Unrecognizable](https://www.youtube.com/watch?v=Aw3BkmhYu4I) - YouTube video by Nate Herk | AI Automation.

### GTM and sales

- [How a College Student Made $500k with Cold Email (Exact Framework)](https://www.youtube.com/watch?v=XB2xmX3USUI) - YouTube video by Nate Herk | AI Automation.

### Videos

- [NVIDIA GTC keynote: the agentic era](https://www.youtube.com/watch?v=jw_o0xr8MWU) - The keynote where NVIDIA's CEO declared agentic systems the new computer - the context behind this whole category (free, no account)
- [OpenClaw on a Hostinger VPS](https://www.youtube.com/watch?v=BhjK2Gr0Ryc) - Step-by-step: deploy OpenClaw on a cheap VPS (KVM2, Ubuntu 24.04) - the exact path we use for cloud installs (free, no account) Why: The tutorial we point clients to when they ask what hosting an AI assistant actually looks like.
- [OpenClaw on Amazon EC2](https://www.youtube.com/watch?v=04wh2Hlgbds) - Deploying OpenClaw on an EC2 Ubuntu instance, end to end (free, no account) Why: The AWS alternative to the VPS route, for teams already on Amazon.
- [Running local models with Claude Code](https://www.youtube.com/watch?v=O2k_qwZA8HU) - How to run local models alongside Claude Code - when privacy or cost pushes you off the cloud APIs (free, no account) Why: The practical walkthrough for the on-your-own-hardware question we get most.

### Creators

- [AI with Remy](https://www.youtube.com/@aiwithremy) - Hands-on AI tutorials with a practical, non-hype angle (free, no account) Why: Consistently useful walkthroughs - rated Great in our creator database.
- [Claire Vo](https://www.youtube.com/@howiaipodcast) - The How I AI podcast - practitioners showing exactly how they use AI at work (free, no account) Why: Real screen-share workflows instead of talking heads.
- [Greg Isenberg](https://www.youtube.com/@GregIsenberg) - Startup ideas and AI playbooks, episode after episode - the channel behind The Startup Ideas Podcast (free, no account) Why: Essential-tier: a steady source of automation ideas worth stealing.
- [Matthew Berman](https://www.youtube.com/@matthew_berman) - AI news and tutorials covering OpenClaw, LLMs, and open-source AI. Why: The fastest way to stay current on the OpenClaw ecosystem.
- [Nate Herk](https://www.youtube.com/@nateherk) - AI automation tutorials on n8n and Claude Code - 528K subscribers and the AI Automation Society community (free, no account) Why: Essential-tier in our book: the closest channel to how we actually build for clients.
- [Noe Varner](https://www.youtube.com/@noeautomates) - Automation tutorials and the NoeAI community - strong on competitor research and ads workflows (free, no account) Why: Several of our marketing skills trace back to his classroom material.
- [Roman Knox](https://www.instagram.com/roman.knox) - AI content and design workflows, with a strong Gumroad library (free, no account) Why: Rated Great in our database - especially for creative AI workflows.

### Podcasts and newsletters

- [Behind the Craft](https://www.youtube.com/@peteryang) - Peter Yang's show on how the best builders actually work with AI - hands-on interviews, not punditry (free, no account) Why: One of the few AI shows where guests share real workflows you can copy the same day.
- [Lenny's Newsletter & Podcast](https://www.lennysnewsletter.com) - The product and growth newsletter - plus the interview podcast behind it (free, no account) Why: The single best source on product, growth, and how real teams work.
- [The Startup Ideas Podcast](https://www.gregisenberg.com) - Greg Isenberg's podcast - concrete startup ideas and AI playbooks, episode after episode (free, no account) Why: Where a lot of our automation experiments start as someone's throwaway idea.

## Field notes

Working rules I keep in Notion: the checklist I run after vibe-coding an app so it does not get hacked, prompting rules for Nano Banana Pro and Kling 3.0, and a few reminders on building websites and on GTM.

Everything I wrote down, grouped by section, lives in [FIELD-NOTES.md](FIELD-NOTES.md):

- [Web design and inspiration](FIELD-NOTES.md#web-design-and-inspiration) - 32 notes
- [Build and ship](FIELD-NOTES.md#build-and-ship) - 6 notes
- [Photos, video and design](FIELD-NOTES.md#photos-video-and-design) - 11 notes
- [Scraping and social data](FIELD-NOTES.md#scraping-and-social-data) - 40 notes
- [GTM and sales](FIELD-NOTES.md#gtm-and-sales) - 2 notes
- [Field notes](FIELD-NOTES.md#field-notes) - 51 notes

## How this list is built

The sources are four private Notion pages where I keep notes while I work (websites and apps, photos and video, scraping, GTM) and the public link directory at agentmatik.ai/links. A sync script in my workspace (`awesome-sync.py`, not in this repo) reads the pages through the Notion API and keeps only the sections that are explicitly mapped as public - everything else stays private by default. It canonicalizes every URL (https only, tracking parameters dropped, `youtu.be` and `twitter.com` rewritten), drops links to private places (Notion, Google Drive, course platforms, local addresses), scans every string for secrets and private names, merges the directory by canonical URL (my notes win on names and descriptions; the directory fills in a missing "why" and its access label), and writes three files: `data/links.csv` (one row per link), `data/notes.json` (the field notes) and `data/_report.md` (what was excluded and why).

From there everything is automated and reproducible from this repo alone:

- `tools/enrich.py` checks every link and writes `data/enrichment.json`: stars, license, last push and archive state from the GitHub API (renamed repositories are followed), titles from YouTube and X oEmbed, and a plain HTTP check with a browser user agent for everything else.
- `tools/build.py` renders this README and `FIELD-NOTES.md` from `data/` + `config/sections.json` + `templates/`. Links stay here, every note goes to the notes file, grouped by the same sections. Entries are sorted by name inside each section; the build is deterministic, so running it twice produces the same files.
- `tools/lint.py` fails on dead links, descriptions under 30 characters, duplicate names or URLs, non-https links, tracking parameters, links to private hosts, long dashes, placeholders, thin sections and broken table-of-contents anchors - in both files. Whatever it cannot fix on its own is listed under "Open decisions" in `data/_report.md`.
- A weekly GitHub Action (`.github/workflows/links.yml`) re-runs the checks and opens a pull request when either file changes. `data/_dead.md` lists what needs a human look.

Nothing in this README or in `FIELD-NOTES.md` is edited by hand. Fixes go to `data/overrides.json` (keyed by the entry id in `data/links.csv`, or by block id under `_notes` for a note) and the next build picks them up.

Current build: 156 entries in 9 sections, 142 field notes. Links checked: 156, dead: 0, last check: 2026-09-21. What the sync excluded and why is in `data/_report.md`. The field notes are rendered into `FIELD-NOTES.md` by the same build.

## License

The content of this list (README, FIELD-NOTES and the files in `data/`) is licensed under [CC BY 4.0](LICENSE) - share and adapt it with attribution. The scripts in `tools/` are MIT licensed ([LICENSE-CODE](LICENSE-CODE)).
