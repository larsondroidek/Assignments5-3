# Assignment 5.3 — Solution: Typography Showcase Page

## Project Structure
```
typography-showcase/
├── index.html
└── style.css
```
**An internet connection is needed** to load the Google Fonts. If you are offline, the fallback fonts (`Georgia`, `Arial`) are shown instead.

## Steps
1. Go to https://fonts.google.com, select **Playfair Display** and **Source Sans 3** and copy the `<link>` tags it gives you (they are already in the HTML below).
2. Put the Google Fonts `<link>` **before** your `style.css` link in `<head>`.
3. Use the fonts in CSS with `font-family`, always with a fallback.
4. Open with Live Server and check the three sections.

## Font Pairing
| Use | Font | Why |
|-----|------|-----|
| Headings | **Playfair Display** (serif) | Elegant, high contrast, strong personality |
| Body text | **Source Sans 3** (sans-serif) | Clean and very readable at small sizes |

A decorative serif for headings plus a simple sans-serif for body text is a classic complementary pairing: the contrast creates hierarchy while both fonts stay readable.

## index.html
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="Typography showcase using Playfair Display and Source Sans 3 from Google Fonts." />
    <title>Typography Showcase</title>

    <!-- Google Fonts: Playfair Display (headings) + Source Sans 3 (body) -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Source+Sans+3:ital,wght@0,300;0,400;0,600;0,700;1,400&display=swap"
      rel="stylesheet"
    />

    <link rel="stylesheet" href="style.css" />
  </head>

  <body>
    <header class="page-header">
      <h1>Typography Showcase</h1>
      <p class="subtitle">Playfair Display for headings &middot; Source Sans 3 for body text</p>
    </header>

    <main>
      <!-- ===== Section 1: Heading Styles ===== -->
      <section id="headings">
        <h2>Heading Styles</h2>

        <h1 class="demo">Heading 1 — Bold and Large</h1>
        <h2 class="demo">Heading 2 — Section Title</h2>
        <h3 class="demo">Heading 3 — Sub-section Title</h3>
        <h4 class="demo">Heading 4 — Small Heading</h4>

        <h3 class="centered">Centered Heading</h3>
        <h3 class="right">Right-aligned Heading</h3>
        <h3 class="spaced">Wide Letter-Spacing Heading</h3>
        <h3 class="underlined">Underlined Heading</h3>
      </section>

      <!-- ===== Section 2: Paragraph Styles ===== -->
      <section id="paragraphs">
        <h2>Paragraph Styles</h2>

        <h3>Default Paragraph</h3>
        <p>
          Good typography makes text easy and pleasant to read. The font,
          size, spacing and alignment all work together to guide the reader's
          eyes across the page.
        </p>

        <h3>Tight vs. Comfortable Line Height</h3>
        <p class="tight">
          This paragraph uses a tight line-height of 1.1. Lines sit close
          together, which can feel crowded when the text runs over several lines
          like this one does.
        </p>
        <p class="comfortable">
          This paragraph uses a comfortable line-height of 1.8. The extra space
          between lines makes longer text easier to read, which is why body text
          usually uses 1.5 to 1.8.
        </p>

        <h3>Text Alignment</h3>
        <p class="align-left">Left-aligned text is the default and the easiest to read for long paragraphs.</p>
        <p class="align-center">Center-aligned text works well for short quotes and titles.</p>
        <p class="align-right">Right-aligned text can be used for dates, signatures and captions.</p>
        <p class="align-justify">
          Justified text stretches each line to the same width, creating clean
          edges on both sides. It looks formal, like a newspaper column or a
          book page.
        </p>

        <h3>Letter-Spacing</h3>
        <p class="letters-wide">Wide letter-spacing for small uppercase labels</p>
        <p class="letters-tight">Tight letter-spacing for large display text</p>
      </section>

      <!-- ===== Section 3: Text Emphasis ===== -->
      <section id="emphasis">
        <h2>Text Emphasis</h2>

        <p>Font weights: <span class="w300">Light 300</span>, <span class="w400">Regular 400</span>, <span class="w600">Semi-bold 600</span>, <span class="w700">Bold 700</span>.</p>

        <p>Font styles: <span class="style-normal">Normal</span>, <span class="style-italic">Italic</span>.</p>

        <p>
          Text decorations:
          <span class="deco-underline">underline</span>,
          <span class="deco-overline">overline</span>,
          <span class="deco-through">line-through</span>,
          <a href="#emphasis" class="deco-none">a link without underline</a>,
          <a href="#emphasis" class="deco-wavy">a link with wavy underline</a>.
        </p>

        <p>Text transform: <span class="upper">uppercase text</span>, <span class="capital">capitalized text</span>.</p>

        <blockquote>
          &ldquo;Design is not just what it looks like and feels like. Design is
          how it works.&rdquo;
        </blockquote>
      </section>
    </main>

    <footer>
      <p><small>Fonts: Playfair Display and Source Sans 3 from Google Fonts</small></p>
    </footer>
  </body>
</html>
```

## style.css
```css
/* ===== Base: body font (Source Sans 3) ===== */
body {
  font-family: "Source Sans 3", Arial, sans-serif; /* fallback fonts if Google Fonts fails */
  font-size: 18px;
  font-weight: 400;
  line-height: 1.6;
  color: #2d2a32;
  background-color: #faf8f5;
  max-width: 820px;
  margin: 0 auto;
  padding: 24px;
}

/* ===== Headings font (Playfair Display) ===== */
h1,
h2,
h3,
h4 {
  font-family: "Playfair Display", Georgia, serif;
  color: #3b1f2b;
  line-height: 1.25;
}

h1 {
  font-size: 2.6rem;
  font-weight: 900;
}

h2 {
  font-size: 2rem;
  font-weight: 700;
  border-bottom: 2px solid #c9a227;
  padding-bottom: 6px;
  margin-top: 40px;
}

h3 {
  font-size: 1.5rem;
  font-weight: 700;
  margin-top: 24px;
}

h4 {
  font-size: 1.2rem;
  font-weight: 400;
  font-style: italic;
}

/* ===== Page header ===== */
.page-header {
  text-align: center;
  padding: 16px 0;
}

.page-header h1 {
  letter-spacing: 2px;
  margin-bottom: 4px;
}

.subtitle {
  font-size: 1.1rem;
  font-weight: 300;
  letter-spacing: 1px;
  text-transform: uppercase;
  color: #7a6a72;
}

/* ===== Section 1: Heading Styles ===== */
.demo {
  margin: 12px 0;
}

.centered {
  text-align: center;
}

.right {
  text-align: right;
}

.spaced {
  letter-spacing: 6px;
  text-transform: uppercase;
  font-size: 1.2rem;
}

.underlined {
  text-decoration: underline;
  text-decoration-color: #c9a227;
  text-decoration-thickness: 3px;
  text-underline-offset: 6px;
}

/* ===== Section 2: Paragraph Styles ===== */
.tight {
  line-height: 1.1;
}

.comfortable {
  line-height: 1.8;
}

.align-left {
  text-align: left;
}

.align-center {
  text-align: center;
}

.align-right {
  text-align: right;
}

.align-justify {
  text-align: justify;
}

.letters-wide {
  letter-spacing: 4px;
  text-transform: uppercase;
  font-size: 0.9rem;
  font-weight: 600;
}

.letters-tight {
  letter-spacing: -1px;
  font-size: 1.8rem;
  font-weight: 700;
}

/* ===== Section 3: Text Emphasis ===== */
.w300 { font-weight: 300; }
.w400 { font-weight: 400; }
.w600 { font-weight: 600; }
.w700 { font-weight: 700; }

.style-normal { font-style: normal; }
.style-italic { font-style: italic; }

.deco-underline { text-decoration: underline; }
.deco-overline { text-decoration: overline; }
.deco-through { text-decoration: line-through; }

a {
  color: #8b1e3f;
}

.deco-none {
  text-decoration: none;
}

.deco-wavy {
  text-decoration: underline wavy #c9a227;
}

.upper { text-transform: uppercase; letter-spacing: 1px; }
.capital { text-transform: capitalize; }

blockquote {
  font-family: "Playfair Display", Georgia, serif;
  font-size: 1.4rem;
  font-style: italic;
  line-height: 1.5;
  text-align: center;
  color: #5a3a47;
  margin: 28px 20px;
  padding: 12px 20px;
  border-left: 4px solid #c9a227;
}

/* ===== Footer ===== */
footer {
  text-align: center;
  color: #7a6a72;
  margin-top: 40px;
}
```

## Requirements Checklist
| Requirement | Where it is met |
|-------------|-----------------|
| 2 Google Fonts | Playfair Display and Source Sans 3 (`<link>` in `<head>`) |
| Different fonts for headings and body | `h1–h4 { font-family: "Playfair Display" }`, `body { font-family: "Source Sans 3" }` |
| Different sizes and weights | `h1` 2.6rem/900, `h2` 2rem/700, body 18px/400, `.w300` to `.w700`, `.letters-wide` 0.9rem |
| `text-align` | `.centered`, `.right`, `.align-left/center/right/justify` |
| `text-decoration` | `underline`, `overline`, `line-through`, `none`, wavy underline |
| `font-style` | `italic` on `h4`, `blockquote`, `.style-italic`; `normal` |
| `letter-spacing` | `.spaced` 6px, `.letters-wide` 4px, `.letters-tight` -1px |
| `line-height` | `.tight` 1.1, body 1.6, `.comfortable` 1.8 |
| 3 sections | **Heading Styles**, **Paragraph Styles**, **Text Emphasis** |

## Submission
- ✅ `index.html` and `style.css` (attached)
- 📸 Optional screenshot of the page (with the fonts loaded)
