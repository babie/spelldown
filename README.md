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
| Content     | Spelldown           | Markdown              | Org             | HTML                      |
|-------------|---------------------|-----------------------|-----------------|---------------------------|
| **Strong**  | `**Strong**`        | `**Strong**`          | `**Strong**`    | `<strong>Strong</strong>` |
| *Emphasis*  | `//Emphasis//`      | `*Emphasis*`          | `/Emphasis/`    | `<em>Emphasis</em>`       |
| Underline   | `__Underline__`     | `<u>Underline</u>`    | `_Underline_`   | `<u>Underline</u>`        |
| ~~Delete~~  | `~~Delete~~`        | `~~Delete~~`          | `+Delete+`      | `<del>Delete</del>`       |
| `Code`      | ``` ``Code`` ```    | `` `Code` ``          | `~Code~`        | `<code>Code</code>`       |
| SuperScript | `Super^{2}`         | `Super<sup>2</sup>`   | `Super^{2}`     | `Super<sup>2</sup>`       |
| SubScript   | `Sub_{2}`           | `Sub<sub>2</sub>`     | `Sub_{2}`       | `Sub<sub>2</sub>`         |
| SingleQuote | `''Single''`        | `&lsquo;Single&rsquo;`| `'Single'`      | `&lsquo;Single&rsquo;`    |
| DoubleQuote | `""Double""`        | `&ldquo;Double&rdquo;`| `"Double"`      | `&ldquo;Double&rdquo;`    |
| Link        | `[[text@url]]`      | `[text](url)`         | `[[url][text]]` | `<a href="url">text</a>`  |
| Image       | `![[alt@url]]`      | `![alt](url)`         | `[[file:url]]`  | `<img src="url" alt="alt" />` |
| Ruby        | `[[漢 字\|かん じ]]`  | N/A                   | N/A             | `<ruby>漢<rb>字<rt>かん<rt>じ</ruby>` |
| ID          | `[[area]]#id`       | N/A                   | N/A             | `<span id="id">area</span>` |
| Class       | `[[area]].class`    | N/A                   | N/A             | `<span class="class">area</span>` |
| TeX         | `$$           $$`   | N/A                   | `$           $` |                           |


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

#### New Line
```
line1
line2
line3
```

```
<p>line1<br/>
line2<br/>
line3</p>
```

#### Paragraph
```
para1

para2
```

```
<p>para1</p>
<p>para2</p>
```

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

#### Table
```
| 1 | 2 | 3 |
|---|---|---|
| a | b | c |
| x | y | z |
```

```
<table>
  <tr>
    <th>1</th>
    <th>2</th>
    <th>3</th>
  </tr>
  <tr>
    <td>a</td>
    <td>b</td>
    <td>c</td>
  </tr>
  <tr>
    <td>x</td>
    <td>y</td>
    <td>z</td>
  </tr>
</table>
```

#### Footnote
```
Lorem ipsum[^1]

[^1]: Dummy text.
```

```
<p>Lorem ipsum<sup><a href="#footnote-1">1</a></sup></p>

<p><span id="footnote-1">1. Dummy text</span></p>
```

#### TeX
```
$$$

$$$
```
