
(learn-myst)=
## Learn Myst Markdown
This is a list of the minimum specifications required to create useful documention.

- Carriage return / Line Break
- Horizontal Rule
- Multiple size headers
- Codeblocks (copy code button)
- Comments
- Embedded Images
- Admonition
- Note
- Embedded Video (Onedrive)
- Links [Section, Page, External]
- Escape Special Characters
- Theme Variations (dark)

#### Carriage Return / Line Break

In Myst, line breaks can be accomplished by adding two spaces at the end or backslash.

    '  '
    \

This is a line break  
as we typically get in code using \'\n'.  
But here instead we end the line with two spaces.  
Or we can use\
a backslash.

#### Horizontal Rule (line across page)
Consists of three dashes. Sphinx calls these 'transitions'.

    ---
---

--- 

#### Code Blocks
Code Block are created by indenting four spaces.

    Indent (four spaces gives us an code block.
    A space above to separate the block from any preceding text may be required.
---

#### Comments
Comments use the '%' to precede the comment.

    %
    [//]: # (This is a comment.)
    [//]: # (This is a
    multiline comment.
    It can span multiple lines.)
    
```{note} 
:class: warning

Spaces must be included around ': # ('

``` 

% comment
[\\]: # (why all this for
 a comment)
---

#### Embedded Images
Embedded images use:

    ![alt](src "title")
    ![A cute cat](https://example.com/cat.jpg "A cute cat")
    
![cartoon fish](./_static/fun-fish.png "fun fish graphic")

---


Using the HTML tag \'img' we can align and ajust the size of an image.

    <img src="image_file_path" alt="alternate_text">
    <img src="./_static/fun-fish.png" alt="cartoon fish" align="left" width="100">
    XHTML tags should be closed, HTML5 do not.
<p>  
<br>    
<img src="./_static/fun-fish.png" alt="cartoon fish" align="left" width="100">
<br>
</p>

Without using 'div' statements, we have a problem.  

    <div style="display:block; text-align:center;">
    <img src="./_static/fun-fish.png" alt="cartoon fish" align="center" width="100">
    </div>
   
<div style="display:block; text-align:center;">
  <img src="./_static/fun-fish.png" alt="cartoon fish" align="center" width="125">
</div>

Alternately we use margin:auto to center:

    <div style="display:block; text-align:center;">
    <img src="./_static/fun-fish.png" alt="cartoon fish" width="100" style="margin:auto;">
    </div>

<div style="display:block; text-align:center;">
  <img src="./_static/fun-fish.png" alt="cartoon fish" width="125" style="margin:auto;">
</div>

---

Image right align:

    <div style="text-align: right;">
    <img src="./_static/fun-fish.png" alt="alt text" style="float: right; margin-left: 10px; display: block; clear: right;">
    <img src="./_static/fun-fish.png" alt="alt text" style="float: right; margin-left: 10px; display: block; clear: right;">
    </div>

<div style="display:block; text-align: center;">
  <img src="./_static/fun-fish.png" alt="alt text" width="150" style="float: right; margin-left: 10px; display: block; clear: right;">
  <img src="./_static/fun-fish.png" alt="alt text" width="150" style="float: right; margin-left: 10px; display: block; clear: right;">
</div>

<div style="display:block; text-align: right;">
  <img src="./_static/fun-fish.png" alt="cartoon fish" width="150" style="float: right;">
</div>

```
<div style="text-align:right;">
  <img src="./_static/fun-fish.png" alt="alt text" width="150" style="display:block;">
</div>

```
---
We can flop an image using:

    <div style="display:block; text-align:center; transform: scaleX(-1);">
    <img src="./_static/fun-fish.png" alt="cartoon fish" align="right" width="150">
    </div>   

<div style ="display:block">
   <div style="display:block; text-align:center; transform: scaleX(-1);">
     <img src="./_static/fun-fish.png" alt="cartoon fish" width="125" style="margin:auto;">
   </div>
</div>

---

#### Admonition!

Here is how to add Admonition.

    ```{admonition} Here's my title
    :class: warning

    Here's my admonition content
    ```  

```{admonition} Here's my title
:class: warning

Here's my admonition content
```

[Admonition vis Code Fence (Myst)](https://myst-parser.readthedocs.io/en/v0.17.1/syntax/optional.html#syntax-header-anchors)

    ::::{important}
    :::{note}
    This text is **standard** _Markdown_
    :::
    :::: 

::::{important}
:::{note}
This text is **standard** _Markdown_
:::
::::

<div class="admonition note" name="html-admonition" style="background: lightgreen; padding: 10px">
<p class="title">This is the **title**</p>
This is the *content*
</div>


#### Note!

Here is how to add a Note.

    ```{note} Here's my title
    :class: warning

    Here's my note content
    ```    

```{note} Here's my title
:class: warning

Here's note content

```   
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/t9xd0hBC_v8?start=14" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

---

<iframe src="https://onedrive.live.com/embed?cid=63413B86A87DF2B1&resid=63413B86A87DF2B1%218219&authkey=AMRFU0zq7UaCW90" width="320" height="261" frameborder="0" scrolling="no" allowfullscreen></iframe>

---

Here we remove the height tag.

<div style ="display:block">
<iframe src="https://onedrive.live.com/embed?cid=63413B86A87DF2B1&resid=63413B86A87DF2B1%218219&authkey=AMRFU0zq7UaCW90" width="320"frameborder="0" scrolling="no" allowfullscreen></iframe>
</div>
---

Here we remove the height tag.

<div style ="display:block">
<iframe src="https://onedrive.live.com/embed?cid=63413B86A87DF2B1&resid=63413B86A87DF2B1%218219&authkey=AMRFU0zq7UaCW90" width="640" height="522" frameborder="0" scrolling="no" allowfullscreen></iframe>
</div>

---

```{admonition} Horizontal Rule post video embed
:class: warning

Be sure to add a Horizontal Rule after the '/div' for a video embed.

```

```{note} Video Sizing
:class: warning

From Onedrive, the video can be doubled in size and over written by the height and width parameters.

```   
---

#### Links

##### External Url.

    [alt-text](url address)
    [myst-parser](https://myst-parser.readthedocs.io/en/v0.17.1/syntax/optional.html#syntax-header-anchors)
    
We have installed myst-parser via documentation directions 
[myst-parser](https://myst-parser.readthedocs.io/en/v0.17.1/syntax/optional.html#syntax-header-anchors)

This allows us to use:

    [some header](header-label)
    

Clicking on the [link will take us to the Note Header](Note)

 Another page [next page](credit.rst) 
 
 
#### Multiple Size Headings
These are examples of different size headings.

    h1: #, h2: ##, h3: ###, h4: ####, h5: #####, h6: ######

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6






