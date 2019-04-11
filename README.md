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
| LeftSingleQuote  | `''LSQ''`           | `&lsquo;LSQ&rsquo;`   | `'LSQ'`         | `&lsquo;LSQ&rsquo;`       |
| LeftDoubleQuote  | `""LDQ""`           | `&ldquo;LDQ&rdquo;`   | `"LDQ"`         | `&ldquo;LDQ&rdquo;`       |
| Link             | `[[text@url]]`      | `[text](url)`         | `[[url][text]]` | `<a href="url">text</a>`  |
| Image            | `[[alt!title!url]]` | `![alt](url "title")` | `[[file:url]]`  | `<img src="url" alt="alt" title="title" />`|
| Ruby             | `[[漢 字\|かん じ]]`  | -                     | -               | `<ruby>漢<rb>字<rt>かん<rt>じ</ruby>` |
| TeX              | `$$             $$` | -                     | `$           $` |                           |

### Line

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

#### Comment
```
# comment
```

### Block

#### BlockQuote
```
"""

"""
```

#### Code
````
```

```
````

#### Definition List
```
term1::
  def1 ...
term2::
  def2 ...
```

```
<dl>
  <dt>term1</dt>
  <dd>def1 ...</dd>
  <dt>term2</dt>
  <dd>def2 ...</dd>
</dl>
term1
```

#### List
```
- 1
- 2
  + 2-1
  + 2-2
    - 2-2-1
    - 2-2-2
    - 2-2-3
  + 2-3
- 3
```

```
<ul>
  <li>1</li>
  <li><ol>
    <li>2-1</li>
    <li>2-2</li>
    <li><ul>
      <li>2-2-1</li>
      <li>2-2-2</li>
      <li>2-2-3</li>
    </ul></li>
    <li>2-3</li>
  </ol></li>
  <li>3</li>
</ul>
```

### TeX
```
$$$

$$$
```
