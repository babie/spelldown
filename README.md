# Spelldown
A lightweight markup language.

## Feature
- Don't disturb the plain text.
- There's Only One Way To Do It.
- Easy to read and write.

## Syntax

### Inline

| Content          | Spelldown          | Markdown            | Org             | HTML                      |
|------------------|--------------------|---------------------|-----------------|---------------------------|
| Heading          | `= Heading`        | `# Heading`         | `* Heading`     | `<h1>Heading</h1>`        |
| Comment          | `# Comment`        | `<!- Comment ->`    | `# Comment`     |	`<!– Comment –>`          |
| **Strong**       | `**Strong**`       | `**Strong**`        | `**Strong**`    | `<strong>Strong</strong>` |
| *Emphasis*       | `//Emphasis//`     | `*Emphasis*`        | `/Emphasis/`    | `<em>Emphasis</em>`       |
| <u>Underline</u> | `__Underline__`    | `<u>Underline</u>`  | `_Underline_`   | `<u>Underline</u>`        |
| ~~Delete~~       | `~~Delete~~`       | `~~Delete~~`        | `+Delete+`      | `<del>Delete</del>`       |
| `Code`           | `` `Code` ``       | `` `Code` ``        | `~Code~`        | `<code>Code</code>`       |
| Super            | `Super^{2}`        | `Super<sup>2</sup>` | `Super^{2}`     | `Super<sup>2</sup>`       |
| Sub              | `Sub_{2}`          | `Sub<sub>2</sub>`   | `Sub_{2}`       | `Sub<sub>2</sub>`         |
| Link             | `[text](url)`      | `[text](url)`       | `[[url][text]]` | `<a href="url">text</a>`  |
| Ruby             | `[漢字]<かん,じ>`    | -                   | -               | `<ruby>漢<rt>かん</rt>字<rt>じ</rt></ruby>` |


### Block

#### quote
#### code
#### dl,dt,dd
#### ul,ol,li
#### Math(TeX)
