# is.gd/korrektor

Machine-readable prompt: https://raw.githubusercontent.com/johannesadelstein/textkorrektor/refs/heads/main/korrektor.txt

License: CC BY 4.0 applies to all versions from 28 April 2026 onward.  
Author: Johannes Adelstein, Bielefeld

This document contains a prompt for multilingual text correction.

## How do I use the prompt?

### Option 1: Copy and paste

Copy the entire prompt and paste it into an AI model of your choice. Append the text you want to have checked.

### Option 2: Direct reference

Simply tell the AI (tested with Claude and Grok on 7 May 2026):

    Proceed with my text as described at is.gd/korrektor

## Notes on use

### 1. Link machine

is.gd/korrektor is a link machine (see Option 2 above and Section 6). The prompt provides an output format that makes it easy to copy and paste flagged passages, for example to locate them in the original text or document them.

### 2. Preliminary check with LanguageTool

For optimal results, particularly when checking dates, it can be helpful to run the text through LanguageTool first:

https://languagetool.org/editor/

The free version limits the amount of text you can check at once. Simply delete the section that has already been checked, and LanguageTool will automatically process the next section.

### 3. Running the prompt again

Especially when is.gd/korrektor identifies many errors, it may be worth running the prompt again. However, it is designed to detect the most serious errors on the first pass.

### 4. Multiple texts

is.gd/korrektor can check several shorter texts at once. It can also process texts in other languages, although it is primarily optimized for German.

### 5. Additional information

is.gd/korrektor can take additional information into account, preferably provided before the text to be checked. For example, supplying the current date allows it to assess whether time-sensitive texts, such as event announcements, are up to date.

Separating this information from the text to be checked helps the model interpret it correctly.

Example:

    Important: The publication date is tomorrow, Wednesday, 22 April 2026.
    ========= TEXTS TO BE CHECKED: =========

### 6. Photo or file

Send a photo of a text or a file from your phone to your paid AI service and include the instruction:

    Proceed as described at is.gd/korrektor

### 7. Limitations

is.gd/korrektor isn't human either. Like all of us, it can be convinced that something false is true.

As with LanguageTool, the purpose of this kind of assistance is to help identify errors that might otherwise be overlooked.

The immense advantage of the underlying LLM technology is its ability to examine texts for errors in meaning and context.
