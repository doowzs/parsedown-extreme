# ParsedownExtreme
![Release](	https://img.shields.io/github/release/BenjaminHoegh/ParsedownExtreme.svg?style=flat-square) ![GitHub (pre-)release](https://img.shields.io/github/release/BenjaminHoegh/ParsedownExtreme/all.svg?style=flat-square&label=pre-release) ![Github All Releases](https://img.shields.io/github/downloads/BenjaminHoegh/ParsedownExtreme/total.svg?style=flat-square)

ParsedownExtreme is a extension to ParsedownExtra to add even more functions to the library.

### Installation

* Download the "Source code" from the [latest release](https://github.com/BenjaminHoegh/ParsedownExtreme/releases/latest)
* Include `ParsedownExtreme.php`
* You must include `parsedown.php` and `parsedownExtra.php` too.


### Example

```php
$ParsedownExtreme = new ParsedownExtreme();

echo $ParsedownExtreme->text('Hello _Parsedown_!'); # prints: <p>Hello <em>Parsedown</em>!</p>
// you can also parse inline markdown only
echo $ParsedownExtreme->line('Hello _Parsedown_!'); # prints: Hello <em>Parsedown</em>!
```

## New Features

See all new features below

#### Task list

Default `enabled`

**Example**

```markdown
- [ ] ToDos
  - [x] Buy some salad
  - [ ] Brush teeth
  - [x] Drink some water
```

- [ ] ToDos
  - [x] Buy some salad
  - [ ] Brush teeth
  - [x] Drink some water

#### Superscript & Subscript

To toggle Superscript & Subscript you most call `$ParsedownExtreme->superscript('true'|'false')`

**Default:** `disabled`

**Example**

```markdown
Superscript: 19^th^

Subscript: H~2~O
```
<img src='https://github.com/BenjaminHoegh/ParsedownExtreme/blob/master/docs/img/supandsub.png' height='100px'>


#### Insert and mark

To toggle insert you most call `$ParsedownExtreme->insert('true'|'false')`
and `$ParsedownExtreme->mark('true'|'false')` for mark

**Default:** `enabled`

**Example**

### Styles

> *NOTE:* `~~Remove~~` use `<del>` to match CommenMark specs and parsedown default. The new `--` there use `<s>` is just a more correct tag to use for text there isn't about a document change

| Type                | Or           | To get                 |
| ------------------- | ------------ | ---------------------- |
| \_italics\_         | \*Italics\*  | \<i>Italics_\</i>.     |
| \*\*Bold\*\*        | \_\_Bold\_\_ | \<b>Bold\</b>.         |
| \--Strikethrough\-- |              | \<s>Strikethrough\</s> |
| \~\~removed\~\~     |              | \<del>removed\</del>   |
| \==Mark\==          |              | \<mark>Mark\</mark>.   |
| \++Insert\++        |              | \<ins>Insert\</ins>    |



### Typograpic Shortcuts

| Type        | Or    | Get      |
| ----------- | ----- | -------- |
| \(c)        | \(C)  | &copy;   |
| \(r)        | \(R)  | &reg;    |
| \(tm)       | \(TM) | &trade;  |
| \(degree)   |       | &deg;    |
| \(paragraph)|       | &sect;   |
| \...        |       | &hellip; |
| \--         |       | &ndash;  |
| \-\--       |       | &mdash;  |
| \>>         |       | &raquo;  |
| \<<         |       | &laquo;  |



#### Media Embeding

To toggle media embeding you most call `$ParsedownExtreme->media('true'|'false')`

**Default:** `true`

**Example**

```markdown
<!-- Also works with normal URL -->
![Video Example](myVideo.mp4)

![Audio Example](SampleAudio.mp3)

![Image Example](myImage.jpg)

```

<img src='https://github.com/BenjaminHoegh/ParsedownExtreme/blob/master/docs/img/videoembeding.png' height='300px'>





#### (La)KaTeX

To enable (La)KaTeX you must [download katex](https://katex.org)

To toggle KaTeX you most call `$ParsedownExtreme->katex('true'|'false')`

**Default:** `disabled`

**Example**

```Latex
$$
    x = {-b \pm \sqrt{b^2-4ac} \over 2a}.
$$
```
<img src='https://github.com/BenjaminHoegh/ParsedownExtreme/blob/master/docs/img/katex.png' height='100px'>


#### Mermaid

To enable Mermaid [download Mermaid](https://mermaidjs.github.io) and then set `$ParsedownExtreme->enableMermaid()` to enable it.

To toggle Mermaid you most call `$ParsedownExtreme->mermaid('true'|'false')`


**Default:** `disabled`

**Example**

```Mermaid
%%
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts<br/>prevail...
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
%%
```
<img src='https://github.com/BenjaminHoegh/ParsedownExtreme/blob/master/docs/img/mermaid.png' height='250px'>
