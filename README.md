# Spelldown
A lightweight markup language.

## Feature
- Don't disturb the plain text.
- There's Only One Way To Do It.
- Easy to read and write.

## Syntax

### Inline
| Content          | Spelldown           | Markdown              | Org             | HTML                      |
|------------------|---------------------|-----------------------|-----------------|---------------------------|
| **Strong**       | `**Strong**`        | `**Strong**`          | `**Strong**`    | `<strong>Strong</strong>` |
| *Emphasis*       | `//Emphasis//`      | `*Emphasis*`          | `/Emphasis/`    | `<em>Emphasis</em>`       |
| <u>Underline</u> | `__Underline__`     | `<u>Underline</u>`    | `_Underline_`   | `<u>Underline</u>`        |
| ~~Delete~~       | `~~Delete~~`        | `~~Delete~~`          | `+Delete+`      | `<del>Delete</del>`       |
| `Code`           | ``` ``Code`` ```    | `` `Code` ``          | `~Code~`        | `<code>Code</code>`       |
| Super            | `Super^{2}`         | `Super<sup>2</sup>`   | `Super^{2}`     | `Super<sup>2</sup>`       |
| Sub              | `Sub_{2}`           | `Sub<sub>2</sub>`     | `Sub_{2}`       | `Sub<sub>2</sub>`         |
| Quote            | `''Quote''`         | -                     |                 | `‘Quote’`                 |
| DoubleQuote      | `""DoubleQuote""`   | -                     |                 | `“DoubleQuote”`           |
| Link             | `[[text@url]]`      | `[text](url)`         | `[[url][text]]` | `<a href="url">text</a>`  |
| Ruby             | `[[漢字|かん じ]]`    | -                     | -               | `<ruby>漢<rb>字<rt>かん<rt>じ</ruby>` |
| Image            | `[[alt!title!url]]` | `![alt](url "title")` | `[[file:url]]`  | `<img src="url" alt="alt" title="title" />`|
| LaTeX            | `$$             $$` | -                     | `$           $` |                           |

### Line

#### Comment
```
# comment
```


#### Heading
```
= h1
== h2
=== h3
==== h4
===== h5
====== h6
```

#### Horizontal Rule
```
---
```

### Block

#### blockquote
```
>>>

<<<
```

#### code
````
```

```
````

#### dl,dt,dd
```
term1::
  def1 ...
term2::
  def2 ...
```

#### ul,ol,li
```
- ol1
- ol2
  1. ul1
  2. ul2
  3. ul3
- ol3
```

## Optional

### MathML(TeX)

`$hoge$`

```
$$$
hoge
$$$
```
