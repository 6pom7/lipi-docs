---
tags:
  - Object
  - Problem
---
# Drag Word Problem

Name: `"drag_word"`

??? tip "Template"
    ```json
      {
          "type": "drag_word",
          "targets": [],
          "answer": []
      },
    ```
    ??? tip "Template With Label"
        ```json
          {
              "type": "drag_word",
              "label": "",
              "targets": [],
              "answer": []
          },
        ```

## About

This is a problem in which you drag diffrent Punjabi characters to the [`"targets"`](#targets)
in order to create a word.

## Creation

You create a multi choice problem by setting `"type"` to `"drag_word"`. 

```json
  {
      "type": "drag_word",
      ...
  }
```

## Properties

* [`"label"`](#label) <code><b>OPTIONAL</b></code>
* [`"targets"`](#targets) <code><b>REQUIRED</b></code> <code><b>LIST</b></code>
* [`"answer"`](#answer) <code><b>REQUIRED</b></code> <code><b>LIST</b></code>

--- 

### Label

`"label": ""`

This is the label/instruction that shows up at the top of the problem.
By default it is set to "Transliterate", but this can be overridden if need be.

```json
  "label": "Translate",
```

!!! info

    This property is optional and not required.

---

### Targets 

`"targets": []`

This is a list of targets, to which the user will drag their answers.

```json
  "targets": ["Soo", "Ra", "J"],
```
> This will usally be the sounds of the corresponding options in the [`"answer"`](#answer)
  list.

--- 

### Answer

`"answer": []`

This is a list of characters, which when put together will make a
word. It is split into a list because the user will drag each item sepreatly and
attempt to match them to the corresponding sounds from the [`"targets"`](#targets)
list.

```json
  "answer": ["ਸੂ", "ਰ", "ਜ"]
```

!!! warning

    The answer list must correspond with the [`"targets"`](#targets) in the same exact order to work correctly.

    ??? example

        ```json
          "targets": ["Soo", "Ra", "J"],
          "answer": ["ਸੂ", "ਰ", "ਜ"]
        ```

        In this case the answer for:
        
        * "Soo" is "ਸੂ"
        * "Ra" is "ਰ"
        * "J" is "ਜ"



## Examples
```json
  {
    "type": "drag_word",
    "targets": ["Soo", "Ra", "J"],
    "answer": ["ਸੂ", "ਰ", "ਜ"]
  },
```

??? example "Example With Label"
    ```json
      {
        "type": "drag_word",
        "label": "Sound",
        "targets": ["Soo", "Ra", "J"],
        "answer": ["ਸੂ", "ਰ", "ਜ"]
      },
    ```
