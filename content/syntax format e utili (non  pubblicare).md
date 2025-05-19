---
draft: true
---

## Lists
---
You can create an unordered list by adding a `-`, `*`, or `+` before the text.

```md
- First list item
- Second list item
- Third list item
```

- First list item
- Second list item
- Third list item

To create an ordered list, start each line with a number followed by a `.` symbol.

```md
1. First list item
2. Second list item
3. Third list item
```

1. First list item
2. Second list item
3. Third list item

## Task lists
---
To create a task list, start each list item with a hyphen and space followed by `[ ]`.

```md
- [x] This is a completed task.
- [ ] This is an incomplete task.
```

- [x] This is a completed task.
- [ ] This is an incomplete task.

You can toggle a task in Reading view by selecting the checkbox.

<mark style="background: #FFB8EBA6;">Tip</mark>

ou can use any character inside the brackets to mark it as complete.

```md
- [x] Milk
- [?] Eggs
- [-] Eggs
```

- [x] Milk
- [x] Eggs
- [-] Eggs  
## Code blocks
---
To format a block of code, surround the code with triple backticks.


```
test
```

Per settare il code block con delle dimensioni ridotte è necessario andare in impostazioni -- aspetto -- (in fondo) snippet css, aprire la cartella e creare un css con questo code all'interno

```
/* Hide heading and trailing when there is no content in them */
div.HyperMD-codeblock-begin:not(:has( > .cm-formatting-code-block)),
div.HyperMD-codeblock-end:not(:has( > .cm-formatting-code-block)) {
  --code-size: 5px;  /* Size of leading/trailing lines */
}
```

il `--code-size: ` permette di settare gli spazi in verticale. 5/10 px sono ottimali 

` (ALT+96) e ~ (ALT+126)`

## Linkare testate
---

Per linkare le testate nella stessa nota, scrivere `[[#` per avere una lista di tutti i titoli di testa all'interno della nota.

Esempio, `[[#Preview a linked file]]`, questo mostrerà un collegamento diretto alla testata corrispondente

**Linkare la testata di un'altra nota**

Compre prima, sarà necessario inserire `#`, ma in questo caso sarà necessario inserirlo dopo il collegamento a un'altra nota.

Esempio, `[[Obsidian#Links are first-class citizens]]` questo creerà un collegamento a una testata all'interno della nota `Obsidian`.

**Linkare una sottotestata**
 
E' possibile inserire multipli collegamenti alle testate semplicemente aggiungendo `#`tra una testa e l'altra, questo ovviamente vale se la testata è sotto un'altra, in cascata.

Per Esempio, `[[Help and support#Questions and advice#Report bugs and request features]]`, creerà un collegamento alla testata `Report bugs and request features`, che a sua volta sta sotto `Questions and advice` il tutto dentro la nota `Help and support`.

**Cercare una testata in tutto il vault**

Per cercare una testata in tutto il vault basta scrivere`[[## ]]` per avere tutti i risultati. 

Per esempio, `[[##` cercerà in modo generico dentro al vault, mentre `[[## team]]` cercherà tutte le testate con la parola *team*.


## Linkare un blocco
---

A block is a unit of text in your note, such as a paragraph, block quote, or list item.

You can link to a block by adding `#^` at the end of your link destination followed by a unique block identifier. For example, `[[2023-01-01#^37066d]]`.

Fortunately, you don't need to know the identifier. When you type the caret (`^`), you can select the block from a list of suggestions to insert the correct identifier.

**Searching for blocks across the vault**

You can also search for blocks to link to from across your vault using the `[[^^block]]` syntax. However, more items qualify as blocks compared to `heading links`, so this list will be much longer.

## Change the link display text
---
By default, Obsidian will show the link text as it appears, such as `[[Aliases]]` showing [Aliases](https://help.obsidian.md/Linking+notes+and+files/Aliases) and `[[Basic formatting syntax#Code blocks]]` showing [Basic formatting syntax > Code blocks](https://help.obsidian.md/Editing+and+formatting/Basic+formatting+syntax#Code%20blocks).

You have the option to modify the text used for displaying a link by using the `[[Aliases|Nicknames]]` and `[[Basic formatting syntax#Code blocks|Code blocks]]` syntaxes to create the [Nicknames](https://help.obsidian.md/Linking+notes+and+files/Aliases) and [Code blocks](https://help.obsidian.md/Editing+and+formatting/Basic+formatting+syntax#Code%20blocks) links.

## Markdown 
---
##### Callouts

Use callouts to include additional content without breaking the flow of your notes. You can also rename them changing the text after che ]

"> [!note]"

> [!note] prova
> testo prova

##### Nested Callouts

You can nest callouts in multiple levels.

> [!question] Can callouts be nested?
> > [!todo] Yes!, they can.
> > > [!example]  You can even use multiple layers of nesting.

---

>[!tip] Altri Callouts
I Callouts possono avere icone personalizzate o anche colori attraverso il css, ma ci sono già dei preimpostati e la lista è sulla [wiki](https://help.obsidian.md/Editing+and+formatting/Callouts#Supported+types) di obsidian sotto la sezione `Supported types`


## Footnotes
---
 You can add footnotes[^1] to your notes using the following syntax:

```
This is a simple footnote[^1].

[^1]: This is the referenced text.
[^2]: Add 2 spaces at the start of each new line.
  This lets you write footnotes that span multiple lines.
[^note]: Named footnotes still appear as numbers, but can make it easier to identify and link references.
```

You can also inline footnotes in a sentence. Note that the caret goes outside the brackets.

```
You can also use inline footnotes. ^[This is an inline footnote.]
```

>[!note] Note
>Inline footnotes only work in reading view, not in Live Preview.

## Supported Markdown extensions 
---

| Syntax          | Description                                                                                                               |
| --------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `[[Link]]`      | [Internal links](https://help.obsidian.md/Linking+notes+and+files/Internal+links)                                         |
| `![[Link]]`     | [Embed files](https://help.obsidian.md/Linking+notes+and+files/Embed+files)                                               |
| `![[Link#^id]]` | [Block references](https://help.obsidian.md/Linking+notes+and+files/Internal+links#Link%20to%20a%20block%20in%20a%20note) |
| `^id`           | [Defining a block](https://help.obsidian.md/Linking+notes+and+files/Internal+links#Link%20to%20a%20block%20in%20a%20note) |
| `%%Text%%`      | [Comments](https://help.obsidian.md/Editing+and+formatting/Basic+formatting+syntax#Comments)                              |
| `~~Text~~`      | [Strikethroughs](https://help.obsidian.md/Editing+and+formatting/Basic+formatting+syntax#Bold,%20italics,%20highlights)   |
| - ==Text==      | [Highlights](https://help.obsidian.md/Editing+and+formatting/Basic+formatting+syntax#Bold,%20italics,%20highlights)       |
| ` ``` `         | [Code blocks](https://help.obsidian.md/Editing+and+formatting/Basic+formatting+syntax#Code%20blocks)                      |
| `- [ ]`         | [Incomplete task](https://help.obsidian.md/Editing+and+formatting/Basic+formatting+syntax#Task%20lists)                   |
| `- [x]`         | [Completed task](https://help.obsidian.md/Editing+and+formatting/Basic+formatting+syntax#Task%20lists)                    |
| `> [!note]`     | [Callouts](https://help.obsidian.md/Editing+and+formatting/Callouts)                                                      |
| (see link)      | [Tables](https://help.obsidian.md/Editing+and+formatting/Advanced+formatting+syntax#Tables)                               |





[^1]: This is a footnotes
