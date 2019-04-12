# Spelldown
A lightweight markup language for ebook.

## Feature
- Obviousness over shortness.

## Syntax

### Escape
```
\**Strong\**
\[[text]]@(http://example.com)
```

```
Strong
[[text]]@(<a href="http://example.com">http://example.com</a>)
```

### UnEscape
```
\\**Strong**
\\[[text]]@(http://example.com)
\\\[[text]]@(http://example.com)
\\\\[[text]]@(http://example.com)
```

```
\<strong>Strong</strong>
\<a href="http://example.com">text</a>
\[[text]]@(<a href="http://example.com">http://example.com</a>)
\\<a href="http://example.com">text</a>
```

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
| SingleQuotationMark | `''Single''`| `&lsquo;Single&rsquo;`| `'Single'`      | `&lsquo;Single&rsquo;`    |
| DoubleQuotationMark | `""Double""`| `&ldquo;Double&rdquo;`| `"Double"`      | `&ldquo;Double&rdquo;`    |
| URL         | `http://example.com`| `http://example.com`  |                 |`<a href="example.com">http://example.com</a>`|
| Link        | `[[text]]@(url)`    | `[text](url)`         | `[[url][text]]` | `<a href="url">text</a>`  |
| Image       | `[[alt]]=(url)`     | `![alt](url)`         | `[[file:url]]`  | `<img src="url" alt="alt" />`       |
| Ruby        | `[[漢 字\|かん じ]]`  | N/A                   | N/A             | `<ruby>漢<rb>字<rt>かん<rt>じ</ruby>` |
| Math(TeX)   | `$$           $$`   | N/A                   | `$           $` |                           |
| Comment     | `##comment##`       | `<!-- comment -->`    |                 | `<!-- comment -->`        |
| Tag         | `[[{span}area]]`    | N/A                   | N/A             | `<span>area</span>`       |
| Attribute   | `[[{attr=foo}area]]`| N/A                   | N/A             | `<span attr="foo">area</span>`      |
| ID          | `[[{#id}area]]`     | N/A                   | N/A             | `<span id="id">area</span>`         |
| Class       | `[[{.class}area]]`  | N/A                   | N/A             | `<span class="class">area</span>`   |
| Shell       | `[[area]]!(cmd foo bar)`   | N/A            |                 |                           |
| Function    | `[[area]]!!(func arg1:foo)`| N/A            |                 |                           |

### Multiline

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

#### Paragraph
```
para1

para2
```

```
<p>para1</p>
<p>para2</p>
```

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

#### Quote
```
"""
Lorem ipsum ...

and so on
"""
```

```
<blockquote>
<p>Lorem ipsum ...</p>
<p>and so on</p>
</blockquote>
```

#### Code
````
```ruby
[1..100].each do |i|
  puts i
end
```
````

```
<code class="highlight highlight-source-ruby">
[1..100].each do |i|
  puts i
end
</code>
```

#### Definition List
```
term1::
  def1
term2::def2
```

```
<dl>
  <dt>term1</dt>
  <dd>def1</dd>
  <dt>term2</dt>
  <dd>def2</dd>
</dl>
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

#### Horizontal Rule
```
---
```

```
<hr />
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

#### Math(TeX)
```
$$$

$$$
```

#### Comment
```
# comment
```

```
<!-- comment -->
```

#### Tag
```
[[[{section}
Lorem ipsum ...
]]]
```

```
<section>
  <p>Lorem ipsum ...</p>
</section>
```

#### Attribute
```
[[[{data-foo=bar }
Lorem ipsum ...
]]]
```

```
<div data-foo="bar">
  <p>Lorem ipsum ...</p>
</div>
```

#### ID
```
[[[{#id}
Lorem ipsum ...
]]]
```

```
<div id="id">
  <p>Lorem ipsum ...</p>
</div>
```

#### Class
```
[[[{.class}
Lorem ipsum ...
]]]
```

```
<div class="class">
  <p>Lorem ipsum ...</p>
</div>
```

#### Shell
```
#!cmd foo bar
```

#### Function
```
#!!func arg1:foo arg2:bar
```
