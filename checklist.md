# Web Tactic Code Review Checklist

## HTML
- Indented with tabs as opposed to spaces
- Nested tags are indented consistently
- White space is used meaningfully
- No commented-out code
- Code includes appropriate comments
- Passes HTMLhint tests
- Document language is specified
- Character encoding is specified and immediately after `<head>` tag
- Unaccessible viewport attributes are avoided
- All form elements are labeled
- `<form>` element has an `id` and `name` attribute
- All `<a>` and `<button>` elements are not empty
- Deprecated `type` attribute is not included on `<script>` and `<link>` elements
- Void elements are not closed
- Linked JS files do not unnecessarily block parsing the rest of the page. `asyc` and `defer` attributes are used
- HTML files are minified in the final build

## CSS/Sass
- CSS is built from SASS files (SCSS syntax)
- Indented with tabs as opposed to spaces
- Indentation is consistent
- Lines are mostly 80-characters wide or less
- Code includes appropriate comments
- CSS rules are written in proper format
- Rules are properly written, multi-line
- No commented-out code
- Passes CSSLint (see config file)
- Declarations are generally sorted by type
- Normalize.css is used (not a global reset)
- Box-sizing is universally set to `border-box`
- Inline styles are generally not used
- Shorthand properties are not used
- Line-heights are unitless
- Images linked in CSS files are scoped to appropriate media queries
- Transitions are used on hover and focus of links and buttons
- Transition `all` is not used
- "Code Smells" are not detected
  - Undoing Styles
  - Magic Numbers
  - Qualified Selectors
  - Absolute Values
  - Brute Forcing
  - Dangerous Selectors
  - Reactive !important
  - IDs
  - Loose Class Names
  - @extend
  - String Concatenation for Classes
  - Background Shorthand
  - Duplicated Key Selectors
  - Classes in Wrong Components
  - `@import`
- CSS files are combined and minified in the final build

## JS
- Indented with tabs as opposed to spaces and indentation is consistent
- no commented-out code
- Lines are mostly 80-characters wide or less
- Code includes appropriate comments
- JS files are combined and minified in the final build

## Images
- CSS to handle design elements (icons, arrows, carets) as opposed to images
- SVGs have been optimized with SVGOMG
- PNGs and JPEGs have been optimized outside of Photoshop with ImageOptim or something else
- No orphans
