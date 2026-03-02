# CSD Student Assistant — Learning Resources

A curated set of learning resources for CSD Student Assistants.

---

## 🐙 Git, GitHub & GitHub Desktop

Start with GitHub Desktop and build the mental model of commits, branches, pushes, and pull requests. **This is a priority learning area**.

- [GitHub Desktop Documentation](https://docs.github.com/en/desktop) — Official docs. Start with the [Getting Started](https://docs.github.com/en/desktop/overview/getting-started-with-github-desktop) guide.
- [Getting Started with Git and GitHub Desktop](https://www.codecademy.com/article/what-is-git-and-github-desktop) — Codecademy. Quick conceptual overview of version control, repositories, commits, and cloning.
- [An Intro to Git and GitHub for Beginners](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners) — HubSpot. Walks through the core workflow step by step.

**Key concepts to understand:** repository, commit, push, pull, branch, merge, pull request, `.gitignore`, and README files.

### Pull Request Etiquette

When you submit a PR, you're asking someone to review your work. A good PR respects their time.

- [Writing a Great Pull Request Description](https://www.pullrequest.com/blog/writing-a-great-pull-request-description/) — HackerOne / PullRequest. Covers the What / Why / How / Testing framework for PR descriptions with concrete examples.
- [Helping Others Review Your Changes](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/getting-started/helping-others-review-your-changes) — GitHub's official guide on writing descriptions, linking issues, and guiding reviewers through your changes.

**In practice for our team:** Keep PRs focused on one thing. Write a short title that says what changed. If the change is visual, include a screenshot. In the description, add link to the relevant Jira ticket (if available) and explain the "how": why you made certain decisions and why you wrote the code the way you did. For your learning and development, it is crucial to write code while being cognizant of how it performs, when it will fail, what the likelihood of failure is, and how it will scale with more data. Your PR description is the place to show that thinking. 

---

## 📘 R Programming

Start with the foundational text and work through it sequentially. It covers data structures, dplyr transformations, writing functions, iteration with purrr, and more. **This is a priority learning area**.

**Primary Resource:**

- [R for Data Science, 2nd Edition](https://r4ds.hadley.nz/) — Hadley Wickham, Mine Çetinkaya-Rundel & Garrett Grolemund. Free online. This is the single most important resource on this list. Key chapters: Data Transformation (dplyr), Functions, Iteration (purrr), and Tidy Data.

**Supplementary:**

- [R Programming for Data Science](https://bookdown.org/rdpeng/rprogdatascience/) — Roger Peng. Free online. Covers R fundamentals (data types, control structures, functions, scoping) in more depth than R4DS.
- [Hands-On Programming with R](https://rstudio-education.github.io/hopr/) — Garrett Grolemund. Free online. Beginner-friendly introduction to R through small projects. Good if R4DS feels too fast at the start.
- [Advanced R, 2nd Edition](https://adv-r.hadley.nz/) — Hadley Wickham. Free online. For when you're comfortable with R and want to understand how it actually works under the hood (environments, functional programming, metaprogramming). Not required reading immediately, but invaluable long-term.

---

## ✨ R Shiny

Most of CSD's dashboards are built with Shiny. **This is a priority learning area**.

**Primary Resource:**

- [Mastering Shiny](https://mastering-shiny.org/) — Hadley Wickham. Free online. The definitive guide, from first app to production-grade development. Read Part I (Getting Started) and Part II (Shiny in Action) thoroughly. Part III and IV (Best Practices) are valuable as your apps grow in complexity.

**Supplementary:**

- [Shiny Official Tutorial](https://shiny.posit.co/r/getstarted/) — Posit's getting-started tutorial. Quick, hands-on, and good for building your first app before diving into the book.
- [Shiny Gallery](https://shiny.posit.co/r/gallery/) — Browse real Shiny apps for inspiration and to see what's possible.
- [bslib Documentation](https://rstudio.github.io/bslib/) — We use bslib for theming and layout in all our apps. Review this once you're comfortable with basic Shiny.

**Key concepts to understand:** reactive values, observers, `reactive()` vs `observe()` vs `eventReactive()`, UI/server separation, `renderPlot` / `renderDT` / `renderUI`, and how `source()` works for shared code across apps.

### Web Fundamentals for Shiny Styling

Our Shiny apps use custom CSS extensively — things like `tags$div(class = "viz-card", style = "padding: 20px")`, `bs_add_rules()`, and flexbox layouts. You don't need to become a frontend developer, but you do need enough HTML/CSS literacy to read and modify this code confidently.

- [MDN: CSS Styling Basics](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics) — Mozilla's official learning path. Covers selectors, the box model (margin, padding, border), colors, fonts, and how CSS rules cascade. This is the best single resource for building a solid mental model of how CSS works.
- [CSS-Tricks: A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) — Visual reference for flexbox properties. Our apps use `display: flex`, `gap`, `align-items`, and `justify-content` constantly.
- [Chrome DevTools: Inspect and Debug CSS](https://developer.chrome.com/docs/devtools/css) — Learn to right-click → Inspect Element in your browser. This is the single most useful debugging skill for Shiny styling. You can see exactly which CSS rules are being applied, test changes live, and figure out why something looks wrong.

**What you'll encounter in our codebase:** `tags$div()`, `tags$p()`, `tags$h4()` are just R wrappers for HTML elements. The `class` argument maps to CSS classes. The `style` argument is inline CSS. `bs_add_rules()` injects custom CSS into the bslib theme. Once you understand these mappings, the Shiny UI code will make much more sense.

---

## 🎨 Tidyverse Style Guide

Consistent style makes code readable by others (and by future-you). Our team follows the tidyverse style guide.

- [The Tidyverse Style Guide](https://style.tidyverse.org/) — The official reference. Covers naming, syntax, pipes, functions, and documentation.
- [R4DS Chapter 4: Workflow — Code Style](https://r4ds.hadley.nz/workflow-style.html) — A gentler introduction to the same style principles, with examples.
- [styler R package](https://styler.r-lib.org/) — Install this in your IDE. It auto-formats your code to tidyverse style. Run it before every commit.

---

## 🤖 Working with AI-Generated Code


**How to learn effectively while using AI:**

- [KDnuggets: 7 Steps to Mastering Vibe Coding](https://www.kdnuggets.com/7-steps-to-mastering-vibe-coding) — A practical guide on using AI-generated code as a learning tool. The core idea: don't just accept the output; read every line, ask the AI to explain unfamiliar patterns, and use the code it generates to teach yourself. Covers prompt engineering, learning the underlying language, and building toward real code ownership.

**Understanding the risks:**

- [Zencoder: 5 Vibe Coding Risks and Ways to Avoid Them](https://zencoder.ai/blog/vibe-coding-risks) — Practical breakdown of technical debt, security gaps, and dependency sprawl with mitigation strategies.

**Our team's expectations:**

1. **Read every line.** If an AI wrote the code, you are still responsible for understanding it. If you can't explain what a function does, don't commit it.
2. **Test edge cases.** AI-generated code often handles the happy path but breaks on NAs, empty inputs, unexpected types, or large datasets. Think about what could go wrong.
3. **Keep it clean.** AI tends to produce verbose, repetitive code. Refactor it to match our style guide before committing. Remove dead code, unnecessary comments, and redundant logic.
4. **Never trust credentials handling.** AI will happily hardcode API keys, paste secrets into scripts, or skip `.gitignore` entries. Always check for this.
5. **Ask if you're unsure.** It's always better to ask than to commit code you don't fully understand.

---

## 📚 Library Data Basics

Understanding the structure of library metadata is good context to have for the data you'll be working with. **This is NOT a priority learning area**.

- [Understanding MARC Bibliographic](https://www.loc.gov/marc/umb/um01to06.html) — Library of Congress. The definitive beginner introduction to MARC records: what they are, why they exist, and how fields/subfields/indicators work.

**Key concepts to understand:**

- **Title-level (bibliographic) data:** Describes the intellectual work — title, author, publisher, subject headings, ISBN, OCLC number. One bib record can represent a book that exists in many libraries.
- **Holdings-level data:** Describes what a specific library owns — which volumes, which copy, at which location. Links a bib record to a physical or electronic collection.
- **Item-level data:** Describes a specific physical piece — barcode, shelf location, circulation status, condition. One holding can have multiple items (e.g. copy 1 and copy 2).

Think of it as: the **title** is the book itself, the **holding** is "UCSB Library owns this," and the **item** is "this specific copy on the 3rd floor."

---

## 📊 Alma Analytics

Alma Analytics is built on Oracle Business Intelligence (OBI). You don't need to become an expert, but you should be comfortable navigating it and building basic reports. **This is NOT a priority learning area**.

- [Ex Libris: Presentations and Documents — Analytics](https://knowledge.exlibrisgroup.com/Alma/Training/Extended_Training/Presentations_and_Documents_-_Analytics) — The most comprehensive single resource. Contains dozens of how-to guides for specific report types (expenditures, loans, users, etc.), filtering techniques, formulas, and data visualization.

---
