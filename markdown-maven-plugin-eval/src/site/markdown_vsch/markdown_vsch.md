`vsch/markdown-page-generator-plugin`
=====================================

[GitHub: vsch/markdown-page-generator-plugin 🌐](https://github.com/vsch/markdown-page-generator-plugin)

[H1 Markdown Syntax][title]  [⇈](up.md)
====================
[title]:http://daringfireball.net/projects/markdown/syntax

<DIV STYLE="font-family:'DejaVu Sans Mono','Andale Mono',Courier,Monaco,'Courier New',monospace; 
color: red; font-size: 12pt;">
0123 Plain <i>Italic</i> <u>Underline</u> <b>Bold</b> 
</DIV>

<a id="toc"></a>
[Heading](#Heading) |
[Code](#Code) |
[Monospace](#Monospace) |
[Lists](#Lists) |
[Tables](#Tables) |
[Links](#Links) |
[Images](#Images) |

Heading H2: three or more hyphens [▴](#toc)
---------------------------------
### H3
#### H4
##### H5
###### H6

_____

Horizontal Rule: at least three asterisks `***` or hyphens `---`.

*****

Italics emphasis brackets with *single asterisks* `*` or _single underscores_ `_`. Strong bold emphasis brackets with **double asterisks** `**` or __double underscores__ `__`. Mixed emphasis can be **can be _nested_**. ~~Strikethrough~~ is bracketed with two tildes.

<mailto:someone@example.com> (Someone Example)

> Blockquotes use `>` similar to email reply text.
> > This line is nested in the same quote.  
>
> * Lists
> * [Some link][arbitrary_id]
> * Etc.
>

[arbitrary_id]:http://www.wikipedia.com

N0-BREAK SPACE : U+00A0 `&nbsp;`. Directly type char into code segments.

<a id="Code"></a>
Code [▴](#toc)
----

Inline `code` has `single back-ticks around` it.

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

```
Triple tilde `~` or back-ticks ```` creates a <pre><code> block.
No language indicated. No syntax highlighting.
```  

If ``inline code with `backticks` `` use double backticks:  
```` ``inline code with `backticks` `` ````  (spaces must preceed the final set of backticks)

```c
print('tildes can also be used!')
```

```bash
$ macdown file_to_open.md
```

actionscript apacheconf applescript bash (sh) c coffeescript cpp (c++) css fortran git go groovy handlebars html http ini java javascript (js) json latex less markdown matlab objectivec (objc) pascal perl php python ruby sql swift xml

<a id="Monospace"></a>
Monospace [▴](#toc)
---------

Monospace 120

``` swift
123456789*123456789*123456789*123456789*123456789*123456789*123456789*123456789*123456789*123456789*123456789*123456789*
```
Portrait 64

``` swift
123456789*123456789*123456789*123456789*123456789*123456789*1234
```
Landscape 85  

``` swift
123456789*123456789*123456789*123456789*123456789*123456789*123456789*123456789*12345
```

<a id="Lists"></a>
Lists [▴](#toc)
-----
1. First ordered list item
2. Another item
  * Unordered sub-list.
1. Actual numbers don't matter, just that it's a number
  1. Ordered sub-list  
    1. Sub-sub-list
4. And another item.

   Properly indented paragraph. Blank line above. At least one leading space.

   Two trailing spaces creates a linebreak. ..  
   Note that this line is separate, but within the same paragraph.

* Unordered list can use asterisks
- Or '-' minuses
+ Or '+' pluses

<a id="Tables"></a>
Tables _(extension)_  [▴](#toc)
--------------------
Colons can be used to align columns. The outer pipes (|) are optional.  Needs at least 3 dashes per column `---`.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| zebra stripes | alternate     |   120 |
| column 2      | centered      |  1230 |
| column 3      | ✓             |     1 |

```markdown
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| zebra stripes | alternate     |   120 |
| column 2      | centered      |  1230 |
| column 3      | ✓             |     1 |
```

|Option name         | Markup           | Result if enabled     |
|------------------|-----------------|------------------|
|Autolink          | http://t.co     | <http://t.co>    |

If intra_letter_emphasis is not enabled, then `_` and `*` are are unmodified in a name or equation a=b*c.

| Option name       | &lt;html&gt; | Result if enabled  |
| ----------------- |:--------:| ---------------------- |
| <em>Emphasis</em> | `<em>`   | So <em>italic</em>     |
| Highlight         | `<mark>` | <mark>look here</mark> |
| Quote             | `<q>`    | <q>As I was ...</q>    |
| Strikethrough     | `<del>`  | <del>strike that</del> |
| Superscript       | `<sup>`  | foot<sup>note</sup>    |
| Underline         | `<u>`    | <u>ancient book</u>    |

<table style="width:100%; font-family: monospace;">
<tr>
  <th>Firstname</th>
  <th>Lastname</th>
  <th><pre>Points</pre></th>
</tr> 
<tr>
  <td>Jill</td>
  <td>Smith</td>
  <td>50</td>
</tr>
<tr>
  <td>Eve</td>
  <td>Jackson</td>
  <td>94</td>
</tr>
</table> 

***

<a id="Links"></a>
Links [▴](#toc)
-----

###### inline link
[Markdown Syntax &neArr;](http://www.site.org/ "Daring Fireball Markdown: Syntax")

```markdown
 [Link Description](http://site "title")
```

###### reference link
[see Note 1][Note1]  
[see MDN:Hover][MDN:Hover]

[Note1]: http://mozilla.org
[MDN:Hover]: https://developer.mozilla.org/en-US/docs/Web/CSS/:hover

```markdown
 [see Note 1][Note1]  
 [see MDN:Hover][MDN:Hover]

 [Note1]: http://mozilla.org
 [MDN:Hover]: https://developer.mozilla.org/en-US/docs/Web/CSS/:hover
```

```markdown
 [url_id]: http://example.com "Optional Title"
 [url_id]: http://example.com 'Optional Title'
 [url_id]: http://example.com (Optional Title)
 [url_id]: <http://example.com/> "Angle Brackets OK"
```

```markdown
 [url_id]: http://example.com/some/long/url
     "Title With White Space Padding"
```

[Link via id=""](#anchor21)  
[Link via name=""](#anchor22)

<a id="anchor21"></a>Link to here via `id`. HTML5 creates a JavaScript global for each `id`. `name` is obsolete in HTML5, but may work and also not create globals. `id` must be unique in the whole document. `id` can contain `azAZ_-.`

```markdown
 [Link via id=""](#anchor21)
 <a id="anchor21"></a>Link to here via `id`.
 <p id="anchor21">Link to here via <code>id</code>.</p>
```

<a name="anchor22"></a>Link to here via a *fragment* `<a>` tag `name` attribute.

```markdown
 [Link text via name=""](#anchor22)
 <a name="anchor22"></a>Link to here via name.
```

Markdown `<http://example.com/>` expands to HTML `<a href="http://example.com/">http://example.com/</a>`

Browser looks for absolute "server" path `file:///Markdown_files/figure1.png`

<a id="Images"></a>
Images [▴](#toc)
------
Inline-style (HTTP)  
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

`![alt text](https://github.com/…/images/icon48.png "Title Text")`

Inline-style (relative)  
[![alt text]( markdown_vsch_files/figure1.png "Title 1")]( markdown_vsch_files/figure1.png)  
`![alt text]( markdown_vsch_files/figure1.png "Title 1")`

(relative, clickable)

```markdown
[![alt text]( markdown_vsch_files/figure1.png "Title 1")]
(04.55_Markdown__QREF_files/figure1.png)
```

Reference-style (HTTP)  
![alt text][logo]  

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Title 48"

`![alt text][logo]`
`[logo]: https://github.com/…/images/icon48.png "Title 2"`


Reference-style (relative)  
![alt text][logo2]

[logo2]: markdown_vsch_files/figure2.png "Title 2"

```markdown
 ![alt text][logo2]
 [logo2]: markdown_vsch_files/figure2.png "Title 2"
```

--
Reference-style (relative, description=reference implicit)  
![logo3]

[logo3]: markdown_vsch_files/figure3.png "Title 3"

```markdown
 ![logo3]
 [logo3]: markdown_vsch_files/figure3.png "Title 3"
```

HTML Style (Relative) _note: figures 1, 2 & 3 have 120px height._
<p><img src="markdown_vsch_files/figure4.png"
         alt="figure4"
       title="Figure 4"
       height=120></p> 

```html
<p><img src="markdown_vsch_files/figure4.png"
         alt="figure4"
       title="Figure 4"
       width=407
       height=120></p>
```

Browser looks for relative "server" path `file:///Users/~/…/markdown_vsch_files/figure3.png`

Limitations
-----------

* Doxia class decorations are not automatically generated.

    `<a class="externalLink" href="…">…</a>`

Resources
---------
[GitHub: vsch/markdown-page-generator-plugin 🌐](https://github.com/vsch/markdown-page-generator-plugin)
