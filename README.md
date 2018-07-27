# slappy-translations
This project contains translations for the Slappy Sports Ladder App. If you would like to contribute, please send an email to abisoft11@gmail.com.

# Folders
There is a folder for each language that is being translated, named based on the 2-digit code for the language. The primary source for the transalations is English, and is found in the `en` folder.

# Different types of files
Each folder contains several files that need to be translated. There are different file types in the repository and each type should be translated appropriately. 
* All files should be edited in a plain text editor.
* Don't change the format or layout of any of the documents, only the text that needs to be translated.
* Try to keep line breaks where they are, if paragraphs are split over multiple lines. Obviously, the order of sentences may change, but make sure to still have a line break at approximately the same position in the translated text.
* After translating the files please check for spelling errors.

Following are the different types of files that need to be translated:
## Text files (.txt)
Text files for store listing text. The headings are underlined and don't need to be translated - just the text underneath them.

## JSON files (.json)
JSON resources for the app and the server. The format is slightly different for app files and server files, as outlined below.

### Common (JSON files)
Each file contains a list of text resources that need to be translated. Each text resource is identified by its name (on the left), and followed by the text in the language of the JSON file. For example,
```
    "RESOURCE_NAME": "Resource text",
    "OK_BUTTON": "OK",
	"SOME_PAGE_TITLE": "Some Page",
    ...
```
Only the text on the right needs to be translated. **Do not change the identifiers on the left or the order of the resources.**

An `en-comments.json` file is provided as a reference, for both the app and the server JSON files, which includes some comments that are there to assist translators with understanding the context of the resources.

Text for titles and button text are Camel Case (all words capitalised). E.g., "Edit Competitor"
Text for labels are captitalised for the first word. E.g., "Ladder type"
Text for input placeholders are all lower case.  E.g., "search"

### App JSON file
Ignore the following special words or characters in the resource text:
* **Translation variables (values set in the code)** - anything in double parentheses (`{{...}}`) (E.g., `{{appName}}`, `{{value}}`)
* **HTML resources** - anything in angle braces (`<...>`) (E.g., `<br/>`, `<p>`, `<ul>`)

### Server JSON file
Ignore the following special words or characters in the resource text (slightly different to the app's JSON files):
* **Translation variables (values set in the code)** - any word starting with a '$' symbol (E.g., `$days`, `$value`)
* **HTML resources** - anything in angle braces (`<...>`) (E.g., `<br/>`, `<p>`, `<ul>`)

## Web files (.html)
Ignore all html tags (enclosed in angle braces), for example, `<body>`, `<h1>`, `<p>`, etc.  Attributes inside the tags should also be ignored, for example, `<img class="screenshot-3" src="img/select-ladder.png">`.  If you open the files in a web browser, you will be able to see the text only, without the tags, which will be useful to make sure that everything has been translated. 

Ignore any variables in the text.  Variables are single words starting with a '$' symbol.  E.g., `$code`.

Quoted text in html files must be translated. It usually refers to text as it appears in the app, and should be translated to match (including the capitalisation) what it has been translated to in the app/server JSON files.

Text in the files is usually split across lines at logical breaking points in sentences or paragraphs. When translating, please keep the translated text on the same line as the original text, as far as possible.

# General concepts
## Players vs. Competitors
Players are individual users of the app. Competitors are either individuals (for singles ladders) or teams of players (currently only for doubles ladders). Each competitor can be linked to one (for singles ladders) or two (for doubles ladders) players.