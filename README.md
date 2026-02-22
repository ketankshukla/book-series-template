# Book Series Template

A reusable template repository for creating book series projects -- fiction or non-fiction. Clone this repo for any new book series and follow the setup instructions to customize it for your project.

This template captures the best patterns from three completed series projects and provides a complete starting point for planning, writing, publishing, and marketing a book series.

---

## What This Template Includes

- **Next.js 16 website** with React 19, Tailwind CSS 4, TypeScript, and Lucide React -- fully functional with parameterized components
- **Book series planning documents** with fill-in-the-blank placeholders
- **Amazon KDP publishing templates** with metadata, pricing, and launch strategy
- **AI image prompt templates** for ebook covers, paperback wraps, branding, box sets, social media, character portraits, and YouTube thumbnails
- **Front and back matter templates** for both fiction and non-fiction
- **PowerShell DOCX generation scripts** using Pandoc for manuscript assembly
- **Video script and prompt templates** for HeyGen trailers and marketing videos
- **Complete directory structure** for organizing all book content, images, and production files

---

## Directory Structure

```
book-series-template/
|-- README.md                          # This file
|-- SETUP.md                           # Step-by-step setup checklist
|-- book-series-plan.md                # Series planning document (fill-in-the-blanks)
|-- book-series-template.md            # Master series vision document
|-- amazon-publishing-template.md      # KDP metadata, pricing, launch strategy
|-- .gitignore
|-- package.json                       # Pre-configured dependencies
|-- tsconfig.json / next.config.ts     # TypeScript and Next.js config
|-- postcss.config.mjs / eslint.config.mjs / vercel.json
|
|-- book-series/                       # ALL BOOK CONTENT
|   |-- series-description.md          # HTML-formatted KDP series description
|   |-- kdp-categories-and-keywords.md # Categories and keywords per book
|   |-- ai-image-tools.md              # Guide to AI image generation tools
|   |-- word-docs/                     # DOCX generation scripts and output
|   |   |-- chapters-only/             # Chapter-only DOCX files
|   |   |-- complete/                  # Complete book DOCX files (front+chapters+back)
|   |   |-- make_book_docx.ps1         # PowerShell: chapters -> DOCX
|   |   |-- make_complete_docx.ps1     # PowerShell: full book -> DOCX
|   |-- front-matter-templates/        # Front matter templates
|   |-- back-matter-templates/         # Back matter templates
|   +-- [BOOK DIRECTORIES CREATED PER BOOK]
|
|-- book-blurbs/                       # Short marketing blurbs per book
|-- book-prompts/                      # AI image generation prompts
|   |-- ebook-covers/                  # Per-book ebook cover prompts
|   |-- paperback-wraps/               # Per-book paperback cover prompts
|   |-- branding/                      # Series logo and branding prompts
|   |-- box-sets/                      # Box set / collection cover prompts
|   |-- social-media/                  # Social media image prompts
|   |-- character-portraits/           # [FICTION ONLY] Character portraits
|   +-- youtube-thumbnails/            # YouTube thumbnail prompts
|
|-- book-images/                       # Generated images (from AI tools)
|-- amazon-production/                 # Production-ready publishing files
|-- video-prompts/                     # Video generation specifications
|-- video-scripts/                     # Marketing video scripts
|-- archived-prompts/                  # Previous prompt iterations
|-- archived-images/                   # Previous image iterations
|
+-- src/                               # NEXT.JS WEBSITE
    |-- app/
    |   |-- layout.tsx                 # Root layout (parameterized)
    |   |-- page.tsx                   # Main single-page app
    |   +-- globals.css                # Global styles with CSS variables
    |-- components/
    |   |-- Header.tsx / Hero.tsx / BooksSection.tsx
    |   |-- BookCard.tsx / BookModal.tsx
    |   |-- AuthorSection.tsx / Footer.tsx
    |   |-- YouTubePlayer.tsx / ImageProtection.tsx
    |-- context/
    |   +-- BookContext.tsx             # Book state management
    +-- data/
        |-- books.ts                   # Book and Chapter interfaces + data
        +-- characters.ts             # [FICTION ONLY] Character data
```

---

## Tech Stack

- **Framework:** Next.js 16 with React Compiler
- **UI:** React 19
- **Styling:** Tailwind CSS 4
- **Icons:** Lucide React
- **Language:** TypeScript 5 (strict mode)
- **Deployment:** Vercel (via GitHub)
- **Manuscript:** Pandoc + PowerShell for DOCX generation

---

## File Naming Conventions

- **Directories:** kebab-case (`book-series`, `front-matter`, `ebook-covers`)
- **Book folders:** `Book [NN] - [Title] - [Subtitle]`
- **Chapter files:** `chapter_[NN]_[slug_with_underscores].md`
- **Chapter summaries:** `chapter_[NN]_summary.md`
- **Book summaries:** `book_[NN]_summary.md`
- **Image prompts:** `book_[NN]_cover_prompts.md`
- **Generated images:** `book_[N]_cover_v[version]_[tool].png`

---

## Workflow

1. **Planning** -- Fill in `book-series-template.md` and `book-series-plan.md`
2. **Content Creation** -- Write chapters, front matter, back matter per book
3. **Image Generation** -- Use prompts in `book-prompts/` with AI tools
4. **Website** -- Update `src/data/books.ts` and customize components
5. **Publishing** -- Generate DOCX files, prepare Amazon production assets
6. **Launch** -- Deploy website to Vercel, publish on KDP

---

## Quick Start

```bash
# 1. Clone this template
git clone https://github.com/ketankshukla/book-series-template.git my-series-name
cd my-series-name

# 2. Install dependencies
npm install

# 3. Start development server
npm run dev

# 4. Build for production
npm run build
```

See `SETUP.md` for the complete step-by-step setup checklist.

---

**Author:** Ketan Shukla | **Publisher:** Metronagon | **Website:** metronagon.com
