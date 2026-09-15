# Resume Builder

A single-file resume builder that runs entirely in the browser. No server, no account, no
dependencies at runtime. One HTML file you can open from a USB stick and still print from.

**Live:** https://xaviermcguire.github.io/builder.html

## Why

As I started to rebuild my resume I realized the formatting was the part that was equally hard as it was easy to replicate. 

Career-office advice is consistent and mostly unwritten down in a usable form: one page, action verb plus result, no tables because applicant tracking systems choke on them

Instead of just giving you a blank template, I wanted a tool that actually encodes those best practices right into the workflow.
## What it does

- **Eight formats**, split into three standard ones taught by career offices (Harvard, ATS Plain,
  Business School) and five design variants.
- **Full Customization** on top of any format - fonts, accent color, sizes, spacing,
  margins, borders, section heading treatment, bullet characters.
- **Flexible Sections** Dated entries, label-and-list, or multi-column layouts for coursework.
  Convert between formats without losing content. Thirteen common sections ready to add.
- **A live check panel** that flags mechanical problems: bullets that open with "Responsible for",
  entries with no quantified result, mixed date formats, content spilling past one page.
- **Save and reopen.** Your resume exports as a small JSON file and autosaves to localStorage between visits.
- **Real hyperlinks** that survive print-to-PDF, so an employer reading the PDF can click through
  to a repo or LinkedIn.
- **A responsive web export** - the same content as a phone-readable page, for hosting.

## Decisions worth explaining

**Everything is packed into one file**: Usually bad practice, super helpful here. Instead of spreading things out across multiple folders and stylesheets, everything lives in a single HTML file. This means there's no complex setup or server required—you can literally download the file, put it on a thumb drive, open it on any computer, and it just works.

**Print-driven layout, not screen-driven.** Sizes are in points and inches rather than pixels,
because the artifact is a printed page. The screen is the preview, not the target.

**Clean format switching**: You can jump between different layout styles (like a strict Harvard style or a modern design) instantly without rewriting your content. If a style doesn't look right, you can reset it easily without your data getting messy or lost in the background.
## What I would change next

- The check panel is regex over text. Catching a weak bullet properly needs to understand the
  claim, not the first word.
- Making formats easier to add in the future: Right now, every layout style was built and tweaked individually by hand. If I want to add brand new designs later on, it takes a bit of custom work. Creating a standardized "type scale" (a consistent system for font sizes and spacing) would make it much faster and easier to roll out new templates.
- Multi-page support: Leaving it restricted to one page was a deliberate choice for resumes, but it makes the tool useless if someone needs a full academic CV.

## Credits

Built with Claude. The formatting conventions come from standard career-office guidance,
adapted from *The Damn Good Resume Guide* (Yana Parker).
