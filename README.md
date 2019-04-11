# Spelldown
A lightweight markup language.

## Feature
- Don't disturb the plain text.
- There's Only One Way To Do It.
- Easy to read and write.

## Syntax

### Character
| Content          | Spelldown           | Markdown              | Org             | HTML                      |
|------------------|---------------------|-----------------------|-----------------|---------------------------|
| <                | `<`                 | `<`                   | `<`             | `&lt;`                    | 
| >                | `>`                 | `>`                   | `>`             | `&gt;`                    | 
| '                | `'`                 | `'`                   | `'`             | `&#039;`                  | 
| "                | `"`                 | `"`                   | `"`             | `&quot;`                  | 
| &                | `&`                 | `&`                   | `&`             | `&amp;`                   | 


### Inline
| Content          | Spelldown          | Markdown              | Org             | HTML                      |
|------------------|--------------------|-----------------------|-----------------|---------------------------|
| **Strong**       | `**Strong**`       | `**Strong**`          | `**Strong**`    | `<strong>Strong</strong>` |
| *Emphasis*       | `//Emphasis//`     | `*Emphasis*`          | `/Emphasis/`    | `<em>Emphasis</em>`       |
| <u>Underline</u> | `__Underline__`    | `<u>Underline</u>`    | `_Underline_`   | `<u>Underline</u>`        |
| ~~Delete~~       | `~~Delete~~`       | `~~Delete~~`          | `+Delete+`      | `<del>Delete</del>`       |
| `Code`           | ``` ``Code`` ```   | `` `Code` ``          | `~Code~`        | `<code>Code</code>`       |
| SuperScript      | `Super^{2}`        | `Super<sup>2</sup>`   | `Super^{2}`     | `Super<sup>2</sup>`       |
| SubScript        | `Sub_{2}`          | `Sub<sub>2</sub>`     | `Sub_{2}`       | `Sub<sub>2</sub>`         |
| SingleQuote      | `''Single''`       | `&lsquo;Single&rsquo;`| `'Single'`      | `&lsquo;Single&rsquo;`    |
| DoubleQuote      | `""Double""`       | `&ldquo;Double&rdquo;`| `"Double"`      | `&ldquo;Double&rdquo;`    |
| Link             | `[text]@(url)`     | `[text](url)`         | `[[url][text]]` | `<a href="url">text</a>`  |
| Image            | `[alt]!(url)`      | `![alt](url)`         | `[[file:url]]`  | `<img src="url" alt="alt" />`|
| Ruby             | `[漢 字]^{かん じ}`  | N/A                   | N/A             | `<ruby>漢<rb>字<rt>かん<rt>じ</ruby>`|
| TeX              | `$$           $$`  | N/A                   | `$           $` |                           |

### Line

#### Heading
```
= head 1
== head 2
=== head 3
==== head 4
===== head 5
====== head 6
```

```
<h1>head 1</h1>
<h2>head 2</h2>
<h3>head 3</h3>
<h4>head 4</h4>
<h5>head 5</h5>
<h6>head 6</h6>
```

#### Horizontal Rule
```
---
```

```
<hr />
```

#### Comment
```
# comment
```

```
<!-- comment -->
```

### Block

#### BlockQuote
```
"""

"""
```

```
<blockquote>

</blockquote>
```

#### Code
````
```

```
````

```
<code>

</code>
```

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

#### TeX
```
$$$

$$$
```
