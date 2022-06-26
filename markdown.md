# Markdown

1. [Headers](#headers)
1. [Text Formatting](#text-formatting)
1. [Links and Images](#links-and-images)
1. [Lists](#lists)
1. [Tables](#tables)
1. [Code Blocks](#code-blocks)
1. [Blockquotes](#blockquotes)
1. [Tasks or TODOs](#tasks-or-todos)

## Headers

Create headers with \#
>  
> ```md
> # Header 1
> ## Header 2
> ### Header 3
> #### Header 4
> ##### Header 5
> ###### Header 6
> ```
> # Header 1
> ## Header 2
> ### Header 3
> #### Header 4
> ##### Header 5
> ###### Header 6

## Text Formatting

### Italic or Emphasized

Use single \* or single \_ for make text italic or emphasized 

> 
> ```md
> Some parts of this text is *italic* or _emphasized_.
> 
> Some parts of this text is _italic_ or *emphasized*.
> ```
> Some parts of this text is *italic* or _emphasized_.
> 
> Some parts of this text is _italic_ or *emphasized*.

### Bold or Strong

Use double \* or double \_ for make text bold or strong

> 
> ```md
> Some parts of this text is **bold** or __strong__.
> 
> Some parts of this text is __bold__ or **strong**.
> ```
> Some parts of this text is **bold** or __strong__.
> 
> Some parts of this text is __bold__ or **strong**.

### Deleted

Use single or double \~ for deleted text which looks like line drawed abowe it

> 
> ```md
> I like color ~white~ black.
> 
> I like color ~~black~~ white.
> ```
> I like color ~white~ black.
> 
> I like color ~~black~~ white.

### Escaping special characters

Use \\ for escape characters above so you can use them for other things.

> 
> ```md
> Here is simply all characters above \* \** \_ \__ \~ \~~
> ```
> Here is simply all characters above \* \** \_ \__ \~ \~~

### Horizontal Line
Use triple - for drawing a horizontal line 
> 
> ```md
> Here is some text.
> 
> ---
> Here is some other text that needs to be seperate from other.
> ```
> Here is some text.
> 
> ---
> Here is some other text that needs to be seperate from other.

Sometimes, if you put \--- directly under your text it turns your text to header. I dont know why but worth considering.

## Links and Images

For placing links use `[]()` format. 
- Inside brackets place your text to display.
- Inside paranthesis put your link.
- Optionally you can put title to display whe you hover over link. Put it beside link, in double quote.
- links could be absolute URLs, relative URLs or bookmarks in same page

> 
> ```md
> [example site](https://www.example.com)
> 
> [example site](https://www.example.com "completely optional title")
> 
> [does not exists](/not_here.txt "This file probably does not exists so dont click this link")
> 
> [lists](#lists "This link brings you to next content whic is lists")
> ```
> [example site](https://www.example.com)
> 
> [example site](https://www.example.com "completely optional title")
> 
> [does not exists](/not_here.txt "This file probably does not exists so dont click this link")
> 
> [lists](#lists "This link brings you to next content whic is lists")

## Lists

You could create unordered or ordered lists

### Unordered List

Use \* or \- followed by space to create list items

> 
> ```md
> - apple
> - banana
> - lemon
> 
> * red
> * blue
> * magenta
> ```
> - apple
> - banana
> - lemon
> 
> * red
> * blue
> * magenta

### Ordered List

Use number followed by dot then space for ordered list

> ```md
> 1. book
> 2. notebook
> 3. glass
> ```
> 1. book
> 2. notebook
> 3. glass

Well something to mention here. If you started your ordered list with a number (does not matter if is 1 or 2 or others) as long as you put another number in fromt of next item it will keep counting from first number you put. Is this information is valuable? I ll only but example and go next section. Probably you are going to do the same.

> ```md
> 10. book
> 15. notebook
> 1000. glass
> 3. window
> ```
> 10. book
> 15. notebook
> 1000. glass
> 3. window

### Nested Lists

Indentation with 2 spaces you could nest unordered or ordered lists (i used 3 spaces for ordered lists. They worked like that)

> 
> ```md
> - apple
>   - red
>   - blue
>   - magenta
>     - first
>     - second
> - banana
> - lemon
> ```
> - apple
>   - red
>   - blue
>   - magenta
>     - first
>     - second
> - banana
> - lemon
>
> ```md
> 1. i
>    1. am
>    2. really
>       1. out
>       2. of
> 2. words
> 3. today
>```
> 1. i
>    1. am
>    2. really
>       1. out
>       2. of
> 2. words
> 3. today


## Tables

Better show than try to explain this.
- Use at least 3 `-` in second row
- You can allign  text using dot on top of dot (sometimes called colon as well) ( : )

> 
> ```md
> | ID | Name | Price |
> |:--- |:---:| ---:|
> | 1 | Bread | 10 | 
> | 1000 | Some name which is too long | 45000 |
> ```
> | ID | Name | Price |
> |:--- |:---:| ---:|
> | 1 | Bread | 10 | 
> | 1000 | Some name which is too long | 45000 |

## Code blocks

Use single \` for inline code or use three \` for code block. You can specify language for right coloring in block code. I do not know what happens in inline codea.

>
> Define variable like \`my\_var=10\`
>
> Define variable like `my_var=10`

> ```md
> ```python
> def hello():
>     print("Hello World)
> \```   I need to put back slash here to show you closing three ' otherwise it opens new blcok quote.
> ```

> ```python
> def hello():
>     print("Hello World)
> ```

## Blockquotes

Use \> for createing blockquotes

> 
> ```md
> > Here is my long enough text. I hoped to be long but it could not be. so I repeated it. Here is my long enough text. I hoped to be long but it could not be. so I repeated it.  Here is my long enough text. I hoped to be long but it could not be. so I repeated it.
> ```
> > Here is my long enough text. I hoped to be long but it could not be. so I repeated it. Here is my long enough text. I hoped to be long but it could not be. so I repeated it.  Here is my long enough text. I hoped to be long but it could not be. so I repeated it.

## Tasks or TODOs

In some places ( like github ) you can use checkboxes for task and you can check and uncheck them.

Create a list, them place [ ] this before it. If it supports you have checkbox  now.

You can fill inside of brackets  with x to create checked task.

> 
> ```md
> - [x] Task 1
> - [ ] Task 2
>
> 1. [x] Task 3
> 1. [ ] Task 4
> ```
> - [x] Task 1
> - [ ] Task 2
>
> 1. [x] Task 3
> 1. [ ] Task 4

