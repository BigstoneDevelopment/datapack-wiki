
# Style Guide

## Per File Organization

1. All headers must be exactly 1 level down from their parent's level.

## Corrections and Supplemental Information

1. Tempory user-facing comments—such as noting the Datapack is in development—must be bolded and italicized blockquotes. Ie. `> _**Comment Content**_`.

1. Prefer paragraph footers to inline parentheses for corrections and supplements longer than one sentence.

## Meta

### Per File Formatting

1. Front matter must be ordered as follows:
    1. `title`
    1. `layout`
    1. `permalink` (optional)

1. Headers must not be bolded. Prefer `# Header` to `# **Header**`.

1. Headers—including titles—must have a blank line above and below. Prefer `\n# Header\n\nContent` to `# Header\nContent`.

1. Use underscores for italicizing. Prefer `_Italic Content_` to `*Italic Content*`.

1. Numbered lists must use lazy numbering. Prefer `1. One Content\n1. Two Content` to `1. One Content\n2. Two Content`.

1. Italicizing and bolding must be per excerpt, not per word. Prefer `_Italic Content_` to `_Italic_ _Content_`. Prefer `**Bold Content**` to `**Bold** **Content**`.

1. In bold italics, if then bolded and italicized excerpts are the same, the italics must precede the bold. Prefer `_**Bold Italic Content**_` to `**_Bold Italic Content_**`. Prefer `**Bold _Italic Content_ Content**` to `**Bold** _**Italic Content**_ **Content**`.

### File Structure

1. All user-facing pages must be inside the `pages` folder.