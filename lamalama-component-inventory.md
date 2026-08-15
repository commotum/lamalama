# Lama Lama public component and class inventory

**Audit date:** 2026-08-14 (America/Los_Angeles)

This catalog contains **204 human-friendly component entries**, **35 exact class tokens**, and **6 confirmed full signatures**.

The component inventory is exhaustive at the public template/component level for the pages listed under Page coverage. Exact `class=` values are asserted only where the rendered DOM string was supplied and could be preserved verbatim. The public text crawl normalized away most class attributes, so unseen class names are left blank rather than invented.

## Exact project classes

| Class | Human-friendly name | Role |
|---|---|---|
| `lang-switch-item-nl-toggle` | Dutch language toggle | Locale control for switching to Dutch. |
| `ll-container` | Lama Lama twelve-column container | Site-specific layout and gutter primitive. |
| `js-sticky-bar` | Sticky utility bar hook | JavaScript root hook for the fixed bottom utility bar. |
| `ll-add-tag` | Sticky-bar tag item | Marks an item that is registered as a tag/chip in the sticky bar. |
| `ll-part--lang-switch` | Language-switch slot | Names the sticky-bar part reserved for locale controls. |
| `js-lang-switch` | Language-switch behavior hook | JavaScript hook for locale-switch behavior. |
| `ll-part--buttons-label` | Sticky actions-label slot | Names the sticky-bar part that labels the available actions. |
| `js-buttons-label` | Actions-label behavior hook | JavaScript hook for updating the sticky-bar action label. |
| `ll-add-button` | Sticky-bar button item | Marks an item as a button/action within the sticky bar. |
| `js-menu` | Floating menu root hook | JavaScript root hook for the centered floating navigation menu. |
| `!w-ll-1/12` | Forced one-of-twelve width | Applies the site’s custom one-column width with important priority. |
| `-lg:hidden` | Hide at custom lg variant | Hides the element under the site’s custom -lg responsive rule. |

## Confirmed full signatures

### SIG-01 — Full sticky language-switch DOM path

```text
body > div.fixed.inset-0.flex.items-end.ll-container.pointer-events-none.z-\[6\].js-sticky-bar > div > div.flex.gap-x-1.items-center.uppercase.whitespace-nowrap.ll-add-tag.ll-part--lang-switch.\!w-ll-1\/12.-lg\:hidden.js-lang-switch
```

**Interpretation:** A fixed full-viewport wrapper aligns a compact language-switch slot to the bottom; the wrapper is click-through while the child is a named sticky-bar part.

**Evidence:** Exact — user-supplied selector

### SIG-02 — Fixed sticky-bar wrapper

```text
fixed inset-0 flex items-end ll-container pointer-events-none z-[6] js-sticky-bar
```

**Interpretation:** Viewport-sized bottom-aligned shell for the sticky action system.

**Evidence:** Exact — parsed from user-supplied selector

### SIG-03 — Sticky language-switch slot

```text
flex gap-x-1 items-center uppercase whitespace-nowrap ll-add-tag ll-part--lang-switch !w-ll-1/12 -lg:hidden js-lang-switch
```

**Interpretation:** One-column sticky-bar slot containing the locale controls.

**Evidence:** Exact — parsed from user-supplied selector

### SIG-04 — Sticky actions label

```text
ll-part--buttons-label !w-ll-1/12 -lg:hidden js-buttons-label ll-add-button w-max whitespace-nowrap max-h-max relative
```

**Interpretation:** A compact context/action label registered as a sticky-bar button item.

**Evidence:** Exact — user-supplied class attribute

### SIG-05 — Centered floating menu

```text
fixed left-1/2 -translate-x-1/2 backdrop-blur-sm top-4 rounded z-20 opacity-0 w-[calc(100vw-(32/16*1rem))] max-w-[calc(438/16*1rem)] flex flex-col js-menu
```

**Interpretation:** A horizontally centered, blurred, rounded, responsive menu panel whose base state is transparent.

**Evidence:** Exact — user-supplied class attribute

### SIG-06 — Dutch language toggle token

```text
lang-switch-item-nl-toggle
```

**Interpretation:** Locale-specific control token for the Dutch option.

**Evidence:** Exact — user-supplied rendered DOM token

## Curated component inventory

### Global & Interaction

| ID | Human-friendly component | Level | Purpose | Exact project class(es) | Exact utility class(es) | Confidence |
|---|---|---|---|---|---|---|
| G01 | Page loading progress counter | Atom / primitive | Shows page-loading progress before the main experience becomes available. | — | — | High — rendered component evidence |
| G02 | Main site shell/root | Organism | Top-level wrapper that composes the template and its global layers. | — | — | High — rendered component evidence |
| G03 | 12-column site grid/container | Molecule | Provides the site-wide width, gutters, and twelve-column alignment system. | `ll-container` | — | High — exact class evidence |
| G04 | Fixed bottom sticky utility bar | Atom / primitive | Keeps contextual labels, language controls, and actions anchored to the viewport. | `js-sticky-bar` | `fixed; inset-0; flex; items-end; pointer-events-none; z-[6]` | High — exact class evidence |
| G05 | Sticky-bar full-screen positioning wrapper | Atom / primitive | Keeps contextual labels, language controls, and actions anchored to the viewport. | — | `fixed; inset-0; flex; items-end; pointer-events-none; z-[6]` | High — exact class evidence |
| G06 | Sticky language-switch group | Molecule | Supports the site’s content hierarchy, navigation, or presentation system. | `ll-add-tag; ll-part--lang-switch; js-lang-switch` | `flex; gap-x-1; items-center; uppercase; whitespace-nowrap; !w-ll-1/12; -lg:hidden` | High — exact class evidence |
| G07 | Dutch language toggle | Atom / primitive | Provides a clear user action, navigation target, or state change. | `lang-switch-item-nl-toggle` | — | High — exact class evidence |
| G08 | English language toggle | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| G09 | Sticky actions label | Atom / primitive | Provides a clear user action, navigation target, or state change. | `ll-part--buttons-label; js-buttons-label` | `!w-ll-1/12; -lg:hidden; w-max; whitespace-nowrap; max-h-max; relative` | High — exact class evidence |
| G10 | Sticky action button item | Atom / primitive | Provides a clear user action, navigation target, or state change. | `ll-add-button` | — | High — exact class evidence |
| G11 | Sticky tag/chip item | Atom / primitive | Displays a compact category, attribute, capability, or status label. | `ll-add-tag` | — | High — exact class evidence |
| G12 | Centered floating navigation menu | Atom / primitive | Provides primary site navigation in a compact floating layer. | `js-menu` | `fixed; left-1/2; -translate-x-1/2; backdrop-blur-sm; top-4; rounded; z-20; opacity-0; w-[calc(100vw-(32/16*1rem))]; max-w-[calc(438/16*1rem)]; flex; flex-col` | High — exact class evidence |
| G13 | Menu open trigger | Atom / primitive | Provides primary site navigation in a compact floating layer. | — | — | High — rendered component evidence |
| G14 | Menu close/minimize control | Atom / primitive | Provides primary site navigation in a compact floating layer. | — | — | High — rendered component evidence |
| G15 | Primary navigation link list | Molecule | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| G16 | Social links cluster | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| G17 | Desktop/mobile language selector | Atom / primitive | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| G18 | Pitchdeck trigger | Atom / primitive | Presents Lama Lama’s capabilities and proof points in a modal presentation. | — | — | High — rendered component evidence |
| G19 | Pitchdeck overlay/panel | Organism | Presents Lama Lama’s capabilities and proof points in a modal presentation. | — | — | High — rendered component evidence |
| G20 | Pitchdeck close/minimize control | Atom / primitive | Presents Lama Lama’s capabilities and proof points in a modal presentation. | — | — | High — rendered component evidence |
| G21 | Pitchdeck split-media layout | Molecule | Presents Lama Lama’s capabilities and proof points in a modal presentation. | — | — | High — rendered component evidence |
| G22 | Pitchdeck multi-list layout | Molecule | Presents Lama Lama’s capabilities and proof points in a modal presentation. | — | — | High — rendered component evidence |
| G23 | Pitchdeck image-grid layout | Molecule | Presents Lama Lama’s capabilities and proof points in a modal presentation. | — | — | High — rendered component evidence |
| G24 | “This is us” video overlay | Organism | Displays the agency introduction video in an interruptive full-screen layer. | — | — | High — rendered component evidence |
| G25 | Video play/pause control | Atom / primitive | Controls or reports playback state for an embedded video. | — | — | High — rendered component evidence |
| G26 | Video elapsed-time readout | Atom / primitive | Controls or reports playback state for an embedded video. | — | — | High — rendered component evidence |
| G27 | Video duration readout | Atom / primitive | Controls or reports playback state for an embedded video. | — | — | High — rendered component evidence |
| G28 | Video mute/unmute control | Atom / primitive | Controls or reports playback state for an embedded video. | — | — | High — rendered component evidence |
| G29 | Video close/minimize control | Atom / primitive | Controls or reports playback state for an embedded video. | — | — | High — rendered component evidence |
| G30 | Project brief modal | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| G31 | Multi-step project brief form | Organism | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| G32 | Project-type selector group | Molecule | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| G33 | Project-type option | Atom / primitive | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| G34 | Name input | Atom / primitive | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| G35 | Email input | Atom / primitive | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| G36 | Optional company input | Atom / primitive | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| G37 | Project-details textarea | Atom / primitive | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| G38 | Cancel action | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| G39 | Next-step action | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| G40 | Form submit / “Get in touch” action | Organism | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| G41 | Form success state | Organism | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| G42 | Form error state | Organism | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| G43 | Start a project CTA | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| G44 | Schedule a call CTA | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| G45 | Get in touch CTA | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| G46 | Contact person / phone chip | Atom / primitive | Displays a compact category, attribute, capability, or status label. | — | — | High — rendered component evidence |
| G47 | Global footer contact CTA | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| G48 | Responsive visibility variant | Atom / primitive | Supports the site’s content hierarchy, navigation, or presentation system. | — | `-lg:hidden` | High — exact class evidence |
| G49 | Animated four-layer button/link label | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| G50 | Plus/minus open-close affordance | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |

### Home

| ID | Human-friendly component | Level | Purpose | Exact project class(es) | Exact utility class(es) | Confidence |
|---|---|---|---|---|---|---|
| H01 | Home hero | Organism | Introduces the page with its primary message, context, and media. | — | — | High — rendered component evidence |
| H02 | Hero eyebrow label | Organism | Introduces the page with its primary message, context, and media. | — | — | High — rendered component evidence |
| H03 | Hero headline | Organism | Introduces the page with its primary message, context, and media. | — | — | High — rendered component evidence |
| H04 | Hero body copy | Organism | Introduces the page with its primary message, context, and media. | — | — | High — rendered component evidence |
| H05 | Hero/brand video media | Organism | Introduces the page with its primary message, context, and media. | — | — | High — rendered component evidence |
| H06 | Featured work section | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| H07 | Section label/eyebrow | Organism | Adds compact context or taxonomy above a larger content block. | — | — | High — rendered component evidence |
| H08 | Featured work list/grid | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| H09 | Work/project card | Molecule | Packages a repeatable content unit with media, text, metadata, and optional navigation. | — | — | High — rendered component evidence |
| H10 | Project title | Atom / primitive | Carries the primary display message for its parent component. | — | — | High — rendered component evidence |
| H11 | Project category/tag group | Molecule | Displays a compact category, attribute, capability, or status label. | — | — | High — rendered component evidence |
| H12 | Project tag/chip | Atom / primitive | Displays a compact category, attribute, capability, or status label. | — | — | High — rendered component evidence |
| H13 | “( View + )” hover affordance | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| H14 | View case link | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| H15 | External project/site link | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| H16 | Project summary | Atom / primitive | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| H17 | Project media gallery/stream | Molecule | Presents visual project, service, or culture content. | — | — | High — rendered component evidence |
| H18 | Image media tile | Molecule | Presents visual project, service, or culture content. | — | — | High — rendered component evidence |
| H19 | Video media tile | Molecule | Presents visual project, service, or culture content. | — | — | High — rendered component evidence |
| H20 | View more work link | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| H21 | What we do section | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| H22 | Service tab strip | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| H23 | Service tab/button | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| H24 | Service detail panel | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| H25 | Service capability list | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| H26 | Capability item | Atom / primitive | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| H27 | Call-us/contact teaser | Molecule | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| H28 | Happy clients section | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| H29 | Client-logo marquee | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| H30 | Client-logo item | Atom / primitive | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| H31 | Awards talk media module | Atom / primitive | Presents visual project, service, or culture content. | — | — | High — rendered component evidence |
| H32 | Culture teaser | Molecule | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| H33 | Culture teaser media | Molecule | Presents visual project, service, or culture content. | — | — | High — rendered component evidence |
| H34 | Our culture link | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| H35 | Brief us CTA | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| H36 | Home footer contact intro | Atom / primitive | Closes the page and routes visitors toward contact or another key destination. | — | — | High — rendered component evidence |
| H37 | Embedded about-section navigator | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| H38 | In-page section thumbnail/nav item | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |

### Work Index

| ID | Human-friendly component | Level | Purpose | Exact project class(es) | Exact utility class(es) | Confidence |
|---|---|---|---|---|---|---|
| W01 | Work archive hero | Organism | Introduces the page with its primary message, context, and media. | — | — | High — rendered component evidence |
| W02 | Work archive eyebrow | Organism | Adds compact context or taxonomy above a larger content block. | — | — | High — rendered component evidence |
| W03 | Work archive heading | Organism | Carries the primary display message for its parent component. | — | — | High — rendered component evidence |
| W04 | Work listing/sequence | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| W05 | Repeated work card | Molecule | Packages a repeatable content unit with media, text, metadata, and optional navigation. | — | — | High — rendered component evidence |
| W06 | Work archive footer CTA | Organism | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |

### Case Study

| ID | Human-friendly component | Level | Purpose | Exact project class(es) | Exact utility class(es) | Confidence |
|---|---|---|---|---|---|---|
| C01 | Case page shell | Organism | Top-level wrapper that composes the template and its global layers. | — | — | High — rendered component evidence |
| C02 | Back to work control | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| C03 | Case title/hero | Organism | Introduces the page with its primary message, context, and media. | — | — | High — rendered component evidence |
| C04 | Case category tag group | Molecule | Displays a compact category, attribute, capability, or status label. | — | — | High — rendered component evidence |
| C05 | Case intro/description | Atom / primitive | Explains the message, service, project, or cultural principle in readable copy. | — | — | High — rendered component evidence |
| C06 | External project/site CTA | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| C07 | Credits block | Molecule | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| C08 | Credit row | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| C09 | Case media stream | Molecule | Presents visual project, service, or culture content. | — | — | High — rendered component evidence |
| C10 | Related work section | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| C11 | Related project card | Molecule | Packages a repeatable content unit with media, text, metadata, and optional navigation. | — | — | High — rendered component evidence |
| C12 | View all work CTA | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| C13 | Case footer CTA | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |

### Services Common

| ID | Human-friendly component | Level | Purpose | Exact project class(es) | Exact utility class(es) | Confidence |
|---|---|---|---|---|---|---|
| S01 | Service page shell | Organism | Top-level wrapper that composes the template and its global layers. | — | — | High — rendered component evidence |
| S02 | Service eyebrow | Molecule | Adds compact context or taxonomy above a larger content block. | — | — | High — rendered component evidence |
| S03 | Service hero title | Organism | Introduces the page with its primary message, context, and media. | — | — | High — rendered component evidence |
| S04 | Service attribute/tag row | Molecule | Displays a compact category, attribute, capability, or status label. | — | — | High — rendered component evidence |
| S05 | Service attribute tag | Atom / primitive | Displays a compact category, attribute, capability, or status label. | — | — | High — rendered component evidence |
| S06 | Service introduction | Atom / primitive | Explains the message, service, project, or cultural principle in readable copy. | — | — | High — rendered component evidence |
| S07 | Service hero video/media | Organism | Introduces the page with its primary message, context, and media. | — | — | High — rendered component evidence |
| S08 | Next service control | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| S09 | Editorial explanation block | Molecule | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| S10 | Staff role label | Atom / primitive | Adds compact context or taxonomy above a larger content block. | — | — | High — rendered component evidence |
| S11 | Staff quote/expert statement | Atom / primitive | Explains the message, service, project, or cultural principle in readable copy. | — | — | High — rendered component evidence |
| S12 | KPI/statistics grid | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| S13 | KPI/stat item | Atom / primitive | Highlights a measurable result or proof point. | — | — | High — rendered component evidence |
| S14 | Client logo strip | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| S15 | Service feature tile/card | Molecule | Packages a repeatable content unit with media, text, metadata, and optional navigation. | — | — | High — rendered component evidence |
| S16 | Service process intro | Atom / primitive | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| S17 | Process steps container | Molecule | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| S18 | Process step | Atom / primitive | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| S19 | Process step number | Atom / primitive | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| S20 | Process step eyebrow | Molecule | Adds compact context or taxonomy above a larger content block. | — | — | High — rendered component evidence |
| S21 | Process step title | Atom / primitive | Carries the primary display message for its parent component. | — | — | High — rendered component evidence |
| S22 | Process capability list | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| S23 | Process step description | Atom / primitive | Explains the message, service, project, or cultural principle in readable copy. | — | — | High — rendered component evidence |
| S24 | Platform/technology statement | Organism | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| S25 | Service-related work section | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| S26 | Service project card | Molecule | Packages a repeatable content unit with media, text, metadata, and optional navigation. | — | — | High — rendered component evidence |
| S27 | View all work CTA | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| S28 | Service footer contact CTA | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| S29 | Branding outcome-metrics variant | Atom / primitive | Highlights a measurable result or proof point. | — | — | High — rendered component evidence |
| S30 | Website performance-metrics variant | Organism | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| S31 | Marketing growth-metrics variant | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| S32 | Ecommerce feature pair (“Award winning”, “Mobile first”) | Atom / primitive | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| S33 | Ecommerce four-stage process | Atom / primitive | Displays a compact category, attribute, capability, or status label. | — | — | High — rendered component evidence |
| S34 | Shopify platform statement | Organism | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |

### About

| ID | Human-friendly component | Level | Purpose | Exact project class(es) | Exact utility class(es) | Confidence |
|---|---|---|---|---|---|---|
| A01 | About page hero | Organism | Introduces the page with its primary message, context, and media. | — | — | High — rendered component evidence |
| A02 | “All in or nothing” headline | Atom / primitive | Carries the primary display message for its parent component. | — | — | High — rendered component evidence |
| A03 | About pitchdeck preview | Molecule | Presents Lama Lama’s capabilities and proof points in a modal presentation. | — | — | High — rendered component evidence |
| A04 | Awwwards talk video | Atom / primitive | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| A05 | Culture attribute row (Team/Culture/Momentum) | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| A06 | Culture narrative | Atom / primitive | Explains the message, service, project, or cultural principle in readable copy. | — | — | High — rendered component evidence |
| A07 | Culture image gallery | Molecule | Presents visual project, service, or culture content. | — | — | High — rendered component evidence |
| A08 | Explore our culture label/link | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| A09 | Core values section | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| A10 | Core value card | Molecule | Packages a repeatable content unit with media, text, metadata, and optional navigation. | — | — | High — rendered component evidence |
| A11 | Core value index label | Atom / primitive | Adds compact context or taxonomy above a larger content block. | — | — | High — rendered component evidence |
| A12 | Core value headline | Atom / primitive | Carries the primary display message for its parent component. | — | — | High — rendered component evidence |
| A13 | Core value description | Atom / primitive | Explains the message, service, project, or cultural principle in readable copy. | — | — | High — rendered component evidence |
| A14 | Belief/manifesto section | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| A15 | Work showcase statement | Atom / primitive | Explains the message, service, project, or cultural principle in readable copy. | — | — | High — rendered component evidence |
| A16 | Awards section | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| A17 | Awards table | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| A18 | Award row | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| A19 | Clients section | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| A20 | Client logo grid/marquee | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | High — rendered component evidence |
| A21 | Let’s talk contact section | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| A22 | In-page section thumbnail rail | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| A23 | Section thumbnail item | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| A24 | Team roster section | Organism | Introduces the people visitors may work with and groups the team-member profiles. | — | — | High — rendered component evidence |
| A25 | Team member card | Molecule | Packages one team member’s media, name, and role into a repeatable profile unit. | — | — | High — rendered component evidence |
| A26 | Team member portrait/video media | Atom / primitive | Presents the visual portrait or motion profile for a team member. | — | — | High — rendered component evidence |
| A27 | Team member name | Atom / primitive | Identifies the person represented by a team-member card. | — | — | High — rendered component evidence |
| A28 | Team member role label | Atom / primitive | Displays the person’s discipline or job role. | — | — | High — rendered component evidence |

### Contact

| ID | Human-friendly component | Level | Purpose | Exact project class(es) | Exact utility class(es) | Confidence |
|---|---|---|---|---|---|---|
| T01 | Contact page hero | Organism | Introduces the page with its primary message, context, and media. | — | — | High — rendered component evidence |
| T02 | Postal address block | Molecule | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| T03 | Phone link | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| T04 | Email link | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| T05 | Contact action group | Molecule | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| T06 | Social follow section | Organism | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | High — rendered component evidence |
| T07 | Instagram link | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| T08 | LinkedIn link | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| T09 | Project brief form trigger | Organism | Collects or structures project-brief/contact information. | — | — | High — rendered component evidence |
| T10 | Contact footer/closing line | Atom / primitive | Closes the page and routes visitors toward contact or another key destination. | — | — | High — rendered component evidence |
| T11 | “Join in our DNA” interactive module | Organism | Provides an experimental camera-based contact-page experience. | — | — | High — rendered component evidence |
| T12 | Activate camera control | Atom / primitive | Requests activation of the camera experience. | — | — | High — rendered component evidence |
| T13 | Camera preview/video surface | Molecule | Displays the camera-based visual experience after activation. | — | — | High — rendered component evidence |
| T14 | Back to contact control | Atom / primitive | Returns from the camera/DNA experience to the standard contact content. | — | — | High — rendered component evidence |
| T15 | Grid settings panel | Molecule | Groups controls that alter the camera/DNA grid presentation. | — | — | High — rendered component evidence |
| T16 | Grid settings input/control | Atom / primitive | Adjusts a parameter of the camera/DNA grid. | — | — | High — rendered component evidence |
| T17 | Dark/light appearance toggle | Molecule | Switches the experimental contact module between dark and light presentation modes. | — | — | High — rendered component evidence |

### Language

| ID | Human-friendly component | Level | Purpose | Exact project class(es) | Exact utility class(es) | Confidence |
|---|---|---|---|---|---|---|
| L01 | English locale variant | Atom / primitive | Provides the language-specific version of the same content architecture. | — | — | High — rendered component evidence |
| L02 | Dutch locale variant | Atom / primitive | Provides the language-specific version of the same content architecture. | — | — | High — rendered component evidence |
| L03 | Language-toggle active state | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | High — rendered component evidence |
| L04 | Translated content variant | Atom / primitive | Provides the language-specific version of the same content architecture. | — | — | High — rendered component evidence |

### Media & Layout Primitives

| ID | Human-friendly component | Level | Purpose | Exact project class(es) | Exact utility class(es) | Confidence |
|---|---|---|---|---|---|---|
| P01 | Responsive image | Atom / primitive | Presents visual project, service, or culture content. | — | — | Medium–High — repeated visual/template evidence |
| P02 | Inline/autoplay video | Atom / primitive | Supports the site’s content hierarchy, navigation, or presentation system. | — | — | Medium–High — repeated visual/template evidence |
| P03 | Media grid | Molecule | Presents visual project, service, or culture content. | — | — | Medium–High — repeated visual/template evidence |
| P04 | Split media/text layout | Molecule | Presents visual project, service, or culture content. | — | — | Medium–High — repeated visual/template evidence |
| P05 | Multi-column list | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | Medium–High — repeated visual/template evidence |
| P06 | Horizontal logo marquee | Molecule | Organizes repeated content into a consistent scannable structure. | — | — | Medium–High — repeated visual/template evidence |
| P07 | Repeating card list | Molecule | Packages a repeatable content unit with media, text, metadata, and optional navigation. | — | — | Medium–High — repeated visual/template evidence |
| P08 | Eyebrow/bracket label | Molecule | Adds compact context or taxonomy above a larger content block. | — | — | Medium–High — repeated visual/template evidence |
| P09 | Animated layered text link/button | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | Medium–High — repeated visual/template evidence |
| P10 | Plus/minus disclosure affordance | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | Medium–High — repeated visual/template evidence |
| P11 | Parenthesized plus view affordance | Atom / primitive | Provides a clear user action, navigation target, or state change. | — | — | Medium–High — repeated visual/template evidence |
| P12 | Tag/chip | Atom / primitive | Displays a compact category, attribute, capability, or status label. | — | — | Medium–High — repeated visual/template evidence |
| P13 | KPI numeric value | Atom / primitive | Highlights a measurable result or proof point. | — | — | Medium–High — repeated visual/template evidence |
| P14 | Section divider/anchor label | Organism | Adds compact context or taxonomy above a larger content block. | — | — | Medium–High — repeated visual/template evidence |

## Class-family interpretation

| Pattern | Family | Meaning | Confirmed examples |
|---|---|---|---|
| `js-*` | Behavior-hook family | JavaScript selectors or mount points; not primarily styling contracts. | `js-sticky-bar; js-lang-switch; js-buttons-label; js-menu` |
| `ll-part--*` | Named component-part family | Semantic slots within a larger Lama Lama component. | `ll-part--lang-switch; ll-part--buttons-label` |
| `ll-add-*` | Sticky-item registration family | Marks items that are registered into a larger interactive shell. | `ll-add-tag; ll-add-button` |
| `ll-container` | Layout primitive | Site-specific container and twelve-column grid alignment. | `ll-container` |
| `lang-switch-item-*-toggle` | Locale-control family | Per-locale toggle naming convention. | `lang-switch-item-nl-toggle` |
| `w-ll-* / !w-ll-*` | Custom grid-width utility family | Project Tailwind utilities for Lama Lama grid fractions. | `!w-ll-1/12` |
| `-lg:*` | Custom responsive-variant family | Project-defined responsive variant. | `-lg:hidden` |
| `[...]` | Arbitrary-value utility family | Tailwind values embedded directly in a class token. | `z-[6]; w-[calc(...)]; max-w-[calc(...)]` |
| `!utility` | Important modifier | Raises a utility’s priority with Tailwind’s important modifier. | `!w-ll-1/12` |
| `Standard Tailwind utilities` | Atomic layout/style family | Generic positioning, flexbox, spacing, typography, visibility, and effects. | `fixed; flex; rounded; opacity-0; whitespace-nowrap` |
| `State-bearing utilities` | Visual state family | Utilities whose presence represents an interaction state. | `opacity-0; hidden` |
| `Escaped CSS selectors` | Selector serialization rule | Special characters are escaped in CSS paths but remain unescaped in class attributes. | `\!w-ll-1\/12; z-\[6\]; -lg\:hidden` |

## Page coverage

| Template | Locale | Page type | URL |
|---|---|---|---|
| Homepage | EN | Core landing page | https://lamalama.com/ |
| Homepage | NL | Localized landing page | https://lamalama.com/nl/ |
| Work archive | EN | Archive/index | https://lamalama.com/work/ |
| About | EN | Editorial/about page | https://lamalama.com/about-us/ |
| Contact | EN | Contact page | https://lamalama.com/contact/ |
| Contact | NL | Localized contact page | https://lamalama.com/nl/contact/ |
| Branding | EN | Service template | https://lamalama.com/services/branding/ |
| Websites | EN | Service template | https://lamalama.com/services/websites/ |
| Marketing | EN | Service template | https://lamalama.com/services/marketing/ |
| Ecommerce | EN | Service template | https://lamalama.com/services/ecommerce/ |
| Jack & AI | EN | Case study | https://lamalama.com/cases/jack-ai/ |
| Moov | EN | Case study | https://lamalama.com/cases/moov/ |
| Gardeners | EN | Case study | https://lamalama.com/cases/gardeners/ |
| Neurons Lab | EN | Case study | https://lamalama.com/cases/neurons-lab/ |
| Prazeres United | EN | Case study | https://lamalama.com/cases/prazeres-united/ |
| Home Agency | EN | Case study | https://lamalama.com/cases/home-agency/ |
| Ajax | EN | Case study | https://lamalama.com/cases/ajax/ |

## Exact-crawl deliverables

Run `crawl-lamalama-components.mjs` using the accompanying README to generate the authoritative rendered-DOM class token, class combination, element, mutation, resource, and snapshot files. The crawler is read-only, does not submit forms, does not enter admin/authenticated paths, and excludes third-party iframe contents.