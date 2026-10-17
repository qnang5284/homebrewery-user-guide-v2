# Homebrewery User Guide

**Audience:** First-time authors who want D&D-style pages without a layout app  
**Product:** [The Homebrewery](https://homebrewery.naturalcrit.com) (NaturalCrit)  
**Renderer:** V3 (recommended for new documents)  
**Last updated:** 10 October 2026

This basic guide walks you from a blank brew to a printable PDF, and covers the most known and basic snippets you will find in the app, to help you start your journey to creating your very first professional looking 5e module. You do not need to memorize every snippet. Homebrewery injects the hard parts for you; you only need a few Markdown habits and a handful of Homebrewery-specific lines.

---

## Table of contents

1. [What Homebrewery is](#1-what-homebrewery-is)
2. [Start a new document](#2-start-a-new-document)
3. [Core Markdown syntax](#3-core-markdown-syntax)
4. [Text Editor](#4-text-editor)
  - [Column Break](#41-column-break)
  - [New Page](#42-new-page)
  - [Page Numbering](#43-page-numbering)
  - [Footer](#44-footer)
  - [Vertical Spacing](#45-vertical-spacing)
  - [Horizontal Spacing](#46-horizontal-spacing)
  - [Wide Block](#47-wide-block)
  - [QR Code](#48-qr-code)
  - [Link to page](#49-link-to-page)
  - [Add Comment](#410-add-comment)
  - [Homebrewery Credit](#411-homebrewery-credit)
  - [Table of Contents](#412-table-of-contents)
  - [Index](#413-index)
5. [Player's Handbook snippets](#5-players-handbook-snippets)
  - [Spell](#51-spell)
  - [Spell List](#52-spell-list)
  - [Class Feature](#53-class-feature)
  - [Quote](#54-quote)
  - [Note](#55-note)
  - [Descriptive Text Box](#56-descriptive-text-box)
  - [Monster Stat Block (unframed)](#57-monster-stat-block-unframed)
  - [Monster Stat Block](#58-monster-stat-block)
  - [Wide Monster Stat Block](#59-wide-monster-stat-block)
  - [Front Cover Page](#510-front-cover-page)
  - [Inside Cover Page](#511-inside-cover-page)
  - [Part Cover Page](#512-part-cover-page)
  - [Back Cover Page](#513-back-cover-page)
  - [Magic Item](#514-magic-item)
  - [Artist Credit](#515-artist-credit)
6. [Images, tables et al.](#6-images-tables-et-al)
  - [Images](#61-images)
  - [Tables](#62-tables)
  - [Fonts](#63-fonts)
  - [License](#64-license)
7. [Editor tools](#7-editor-tools)
  - [History](#history)
  - [Undo](#undo)
  - [Redo](#redo)
  - [Fold All](#fold-all)
  - [Unfold All](#unfold-all)
  - [Clean your Code](#clean-your-code)
  - [Brew Editor](#brew-editor)
  - [Style Editor](#style-editor)
  - [Snippets](#snippets)
  - [Properties](#properties)
  - [Settings](#settings)
8. [Export to PDF](#8-export-to-pdf)
9. [Quick troubleshooting](#9-quick-troubleshooting)
10. [Where to go next](#10-where-to-go-next)

---

## 1. What Homebrewery is

Homebrewery is a **browser-based editor** that turns Markdown into pages that look like official fifth-edition Dungeons & Dragons books: parchment backgrounds, two-column body text, class tables, notes, and monster stat blocks.

You type on the left. A live preview updates on the right. Snippets in the toolbar insert ready-made PHB-style blocks so you rarely have to build a layout from scratch.

**What it is good at**

- Adventure text, subclasses, spells, magic items, and bestiary pages
- Sharing a live link with playtesters
- Printing a letter-sized PDF that matches the preview

**What it is not**

- A word processor with automatic pagination (you place page breaks yourself)
- An official Wizards of the Coast product (you are responsible for the licenses on any art or text you publish)

If something looks “off,” it is usually a missing page break, overflowing columns, or print settings—not a broken document. The later sections cover those cases.

---

## 2. Start a new document

### 2.1 Open the editor

1. Go to [https://homebrewery.naturalcrit.com](https://homebrewery.naturalcrit.com).
2. Sign in with Google if you want the brew saved to your account (strongly recommended).
3. Start a new brew (Home / **New**, or [https://homebrewery.naturalcrit.com/new](https://homebrewery.naturalcrit.com/new)).
4. Keep the **V3** renderer for new work. Legacy still opens old documents; new snippets and styling live on V3.

### 2.2 Learn the workspace

![Homebrewery layout, showing the brew editor, preview, and snippet bar](./assets/homebrewery-layout.png)


| Area                    | What it does                                     |
| ----------------------- | ------------------------------------------------ |
| **Brew editor** **(1)** | Your Markdown source                             |
| **Preview** **(2)**     | Paginated pages as they will print               |
| **Snippet bar (3)**     | Inserts PHB blocks, tables, images, page numbers |


**Gentle advice:** save early, give the brew a real title, and write one short paragraph first. Confirm the preview updates before you add stat blocks. That single check saves a lot of “did I type in the wrong place?” confusion.

### 2.3 Use snippets instead of memorizing syntax

Place the cursor where the content should appear, then pick a snippet (for example **PHB → Monster Stat Block** or **Tables → …**). Homebrewery pastes a complete, valid example. Replace the placeholder names and numbers. You can always trim extra rows later.

---

## 3. Core Markdown syntax

Homebrewery uses standard Markdown for everyday writing. These four patterns cover most body text.

### Headings

Use `#` through `######`. In PHB-style themes, `#` and `##` look like chapter and section titles; `###` is a common in-column heading.

```markdown
# Chapter 3: The Saltmarsh Heist

## The Docks at Night

### Optional: Talking to the Harbor Master
```

**Tip:** Headings can feed the Table of Contents snippet. Prefer real heading lines over bold-only titles when you want a ToC later.

### Bold and italics

```markdown
The **ancient** door is *slightly ajar*.

You can combine ***bold italics*** for spell names or trait titles.
```

- `**bold**` → **bold**
- `*italics*` → *italics*
- `***both***` → ***both***

In monster traits, Homebrewery convention is italic-bold on the trait name:

```markdown
***Keen Smell.*** The hound has advantage on Wisdom (Perception) checks that rely on smell.
```

### Lists

**Unordered**

```markdown
- Grappling hook
- 50 feet of silk rope
- A very nervous mule
```

**Ordered**

```markdown
1. Approach the gate in disguise.
2. Bribe or bluff the watch.
3. Find the ledger in the counting house.
```

Nested lists indent with two to four spaces. Keep list items short; long paragraphs belong outside the list so columns still balance.

### A few extras you will see immediately

```markdown
> This blockquote becomes a **note** in the PHB theme.

A line with only a colon adds a little vertical space:

:

[Harbor map](https://example.com) and ![alt text](https://example.com/art.png)
```

You can write HTML when you must, but stay in Markdown until a snippet cannot do the job.

---