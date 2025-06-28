---
tags:
  - Object
  - Problem
---
# Multiple Choice

Name: `"multi_choice"`

??? tip "Template"
    ```json
      {
          "type": "multi_choice",
          "subtitle": "",
          "question": "",
          "options": ["", "", "", ""],
          "hints": ["", "", "", ""],
          "answer": ""
      },
    ```

## Creation

You create a multi choice problem by setting `"type"` to `"multi_choice"`. 

```json
  {
      "type": "multi_choice",
      ...
  }
```

## Properties

* [`"question"`](#question) <code><b>REQUIRED</b></code>
* [`"subtitle"`](#subtitle) <code><b>REQUIRED</b></code>
* [`"options"`](#options) <code><b>REQUIRED</b></code> <code><b>LIST</b></code>
* [`"hints"`](#hints) <code><b>OPTIONAL</b></code> <code><b>LIST</b></code>
* [`"answer"`](#answer) <code><b>REQUIRED</b></code> 
* `"answerText"` <code><b>OPTIONAL</b></code>

--- 

### Question 

`"question": ""`

This is what will be shown to the user. 

```json
  "question": "ਚ",
```
> This will usally be a character or word in which the user has to translate. 

--- 

### Subtitle

`"subtitle": ""`

This is a subtitle shown under the question to let the user know what kind of problem it is. Example: `"Translate"` or `"Sound"`. 

```json
  "subtitle": "Sound",
```

--- 

### Options

`"options": []`

This is a list of multiple options from which the user may pick to answer the question.

```json
  "options": ["Cha", "Ma", "Ra", "La"],
```
!!! warning

    One of the `"options"` must must be **EXACTLY** the same as the
    [`"answer"`](#answer) property, in order for it to function correctly.

--- 

### Hints

`"hints": []`

This is a list of hints that show up directly below the options.
These hints are used to guide the user to the right answer when it's something hard,
or somthing they might not know yet.

```json
  "hints": ["ਚ", "ਮ", "ਰ", "ਲ"]
```
!!! note

    The `"hints"` list must be in **EXACTLY** the same order as their
    corresponding option in the [`"options"`](#options) list.
    ??? example
        ```json
          "options": ["Cha", "Ma", "Ra", "La"],
          "hints": ["ਚ", "ਮ", "ਰ", "ਲ"],
        ```

        * ਚ is the hint for Cha
        * ਮ is the hint for Ma
        * Etc...

--- 

### Answer

`"answer": ""`

This is the answer of the question.

```json
  "answer": "Cha",
```
> The correct answer from the [`"options"`](#options) list.

## Example
```json
  {
    "type": "multi_choice",
    "subtitle": "Sound",
    "question": "ਚ",
    "options": ["Cha", "Ma", "Ra", "La"],
    "answer": "Cha",
    "answerText": "Cha (ਚ)"
  },
```

??? example "Example With Hints"
    ```json
      {
        "type": "multi_choice",
        "subtitle": "Sound",
        "question": "ਚ",
        "options": ["Cha", "Ma", "Ra", "La"],
        "hints": ["ਚ", "ਮ", "ਰ", "ਲ"],
        "answer": "Cha",
        "answerText": "Cha (ਚ)"
      },
    ```
