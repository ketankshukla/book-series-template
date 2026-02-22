# Setup Checklist -- New Book Series Project

A step-by-step guide to setting up a new book series project from this template.

---

## Phase 1: Repository Setup

- [ ] Clone this repo and rename the folder to your series name (kebab-case, e.g., `my-awesome-series`)
- [ ] Run `npm install` to install all dependencies
- [ ] Update `package.json` -- change `"name"` to your series slug
- [ ] Verify the dev server works: `npm run dev`

## Phase 2: Series Planning

- [ ] Fill in `book-series-template.md` with your complete series vision
  - Series name, genre, tone, target audience
  - Book count, chapter count, word count targets
  - Characters (protagonist team, antagonist team, mentors)
  - Romance arcs, death strategy, narration style
  - Cover requirements, Amazon strategy
- [ ] Fill in `book-series-plan.md` with your series structure
  - Book breakdown (titles, themes, chapter counts)
  - Content strategy and cross-book continuity
  - Tone and voice guidelines
  - Distribution and release strategy
- [ ] Fill in `amazon-publishing-template.md` with KDP metadata
  - Keywords, categories, pricing per book
  - Description HTML template
  - Launch sequence

## Phase 3: Content Creation (Per Book)

- [ ] Create book directory: `book-series/Book [NN] - [Title] - [Subtitle]/`
- [ ] Create subdirectories: `chapters/`, `chapter-summaries/`, `front_matter/`, `back_matter/`, `book-summary/`, `book_descriptions/`, `image-prompts/`
- [ ] Write front matter files using templates in `book-series/front-matter-templates/`
  - `copyright.md`, `dedication.md`, `epigraph.md`
  - `dramatis_personae.md` (fiction only)
  - `preface.md`, `introduction.md`, `prologue.md` (non-fiction only)
- [ ] Write all chapters as individual markdown files: `chapter_[NN]_[slug].md`
- [ ] Write chapter summaries: `chapter_[NN]_summary.md`
- [ ] Write book summary: `book_[NN]_summary.md`
- [ ] Write book description: `book_descriptions/description.md`
- [ ] Write back matter using templates in `book-series/back-matter-templates/`
  - `about_the_author.md`, `also_by.md`, `authors_note.md`, `connect.md`, `review_request.md`
  - `epilogue.md` (non-fiction only)
- [ ] Create image prompts: `image-prompts/book_[NN]_cover_prompts.md`
- [ ] Create book blurb: `book-blurbs/book_[NN]_blurb.md`

## Phase 4: Image Generation

- [ ] Generate ebook cover images using prompts in `book-prompts/ebook-covers/`
- [ ] Generate paperback wrap images using prompts in `book-prompts/paperback-wraps/`
- [ ] Generate series logo using prompts in `book-prompts/branding/`
- [ ] Generate box set covers using prompts in `book-prompts/box-sets/`
- [ ] Generate social media images using prompts in `book-prompts/social-media/`
- [ ] Generate character portraits (fiction only) using prompts in `book-prompts/character-portraits/`
- [ ] Place final images in `book-images/` and `public/images/`
- [ ] Copy author photo to `public/images/ketan-shukla.jpeg`

## Phase 5: Website Customization

- [ ] Update `src/app/layout.tsx` -- replace `{{SERIES_NAME}}` and metadata
- [ ] Update `src/app/globals.css` -- set your color scheme in CSS variables
- [ ] Update `src/data/books.ts` -- replace sample data with your actual book data
- [ ] Update `src/data/characters.ts` -- add characters (fiction only; delete file for non-fiction)
- [ ] Update `src/components/Header.tsx` -- replace `{{SERIES_NAME}}`
- [ ] Update `src/components/Hero.tsx` -- replace logo and cover image paths
- [ ] Update `src/components/AuthorSection.tsx` -- replace author bio, stats, series structure
- [ ] Update `src/components/Footer.tsx` -- replace series name, tagline, Amazon URL
- [ ] Update `src/components/BooksSection.tsx` -- update tagline, Amazon complete series URL
- [ ] Verify the site builds: `npm run build`
- [ ] Preview the site: `npm run dev`

## Phase 6: Publishing

- [ ] Generate DOCX files using PowerShell scripts in `book-series/word-docs/`
  - `.\make_book_docx.ps1 -BookFolder "Book 01 - Title - Subtitle"`
  - `.\make_complete_docx.ps1 -BookFolder "Book 01 - Title - Subtitle"`
- [ ] Verify DOCX files for formatting issues (blank pages, missing chapters)
- [ ] Prepare Amazon production files in `amazon-production/`
  - epub files, PDF books, PDF covers
  - Blurbs, descriptions, titles, categories/keywords
- [ ] Fill in `book-series/kdp-categories-and-keywords.md`
- [ ] Fill in `book-series/series-description.md`

## Phase 7: Deployment

- [ ] Push to GitHub
- [ ] Connect GitHub repo to Vercel for automatic deployment
- [ ] Set custom domain (if applicable)
- [ ] Publish books on Amazon KDP
- [ ] Update Amazon URLs in `src/data/books.ts`
- [ ] Rebuild and redeploy

---

**Tip:** Complete each phase fully before moving to the next. The planning phase is the most important -- a thorough plan prevents rework later.
