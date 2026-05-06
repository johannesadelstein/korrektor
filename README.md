# [is.gd/korrektor](https://is.gd/korrektor)

**machine-readable prompt:** https://raw.githubusercontent.com/johannesadelstein/textkorrektor/refs/heads/main/korrektor.txt  
**License:** CC BY 4.0  applies to all versions from 28 April 2026 onward.  
**Author:** Johannes Adelstein, Bielefeld

---

This document contains a prompt for text correction.

## How do I use the prompt?

### Option 1: Copy and paste

1. Copy the prompt text through to the end and paste it into an AI of your
   choice.  
   The prompt has been tested on ChatGPT.com.
2. Append the text to be corrected at the end.

### Option 2: Direct reference

Tell the AI directly:

> Proceed with my text as described at is.gd/korrektor

---

## Notes on use

### 1. Link machine

**is.gd/korrektor** is a link machine; see Option 2 above and point 6.
The prompt it contains provides a helpful format for copying and pasting
incorrect expressions, for example when searching the original text or for
documentation purposes.

### 2. Preliminary check with LanguageTool

For optimal results, for example with automatical date checking, it can be helpful to check the
text with LanguageTool beforehand:

<https://languagetool.org/editor/>

In the free version, the amount of text is limited. You can simply delete
the part of the text that has already been read; the correction then
automatically covers the next section.

### 3. Reactivation when there are many errors

Especially when **is.gd/korrektor** finds many errors, it may be worth
activating the program again. However, **is.gd/korrektor** is designed to
find the most serious errors in the first pass.

### 4. Multiple texts

**is.gd/korrektor** can check several shorter texts at the same time. It can also process texts in other languages, but it is specialized in German texts.

### 5. Additional information

**is.gd/korrektor** can take additional information from the user,
preferably before the text to be corrected. With a current date,
**is.gd/korrektor** can check whether texts, such as announcements, are
up to date. Separating this information from the text to be corrected makes
it easier for the program to classify the information. Example:

```text
Important: The publication date of the texts is tomorrow, Wednesday, 22 April 2026.
========= TEXTS TO BE CORRECTED: =========
```

### 6. Photo or file

Send a photo of a text or a file from your phone to your subscription AI and
add the following instruction:

> proceed as described at is.gd/korrektor

### 7. Limitations

**is.gd/korrektor** is not human either and can, like all of us, be convinced
that something false is true. The purpose of this kind of assistance, as
with LanguageTool, is to help find overlooked errors. The immense advantage
of the underlying LLM technology is that it can search for errors in terms
of content.
