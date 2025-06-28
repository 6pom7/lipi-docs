---
tags:
  - Object
  - Problem
---
# Word Problem

Name: `"word_prob"`

??? tip "Template"
    ```json
      {
        "type": "word_prob",
        "word": "",
        "answer": ""
      },
    ```

## About

This is a typing word problem in which the user is usally
tasked with translating the given [`"word"`](#word) into a 
Punjabi word.

## Creation

You create a multi choice problem by setting `"type"` to `"word_prob"`. 

```json
  {
      "type": "word_prob",
      ...
  }
```

## Properties

* [`"word"`](#word) <code><b>REQUIRED</b></code>
* [`"answer"`](#answer) <code><b>REQUIRED</b></code>

---

### Word

`"word": ""`

This is the English verion of the word. This is the word that
the user needs to translate.

```json
  "word": "King",
```

--- 

### Answer

`"answer": ""`

This is the translated version of the [`"word"`](#word).

```json
  "answer": "ਰਾਜਾ",
```

!!! info 

    Lipi automatically creates a keyboard the user can use
    to type out the answer, which is why this problem only
    reqiures the [`"word"`](#word) and [`"answer"`](#answer).

---

## Examples

```json
  {
    "type": "word_prob",
    "word": "King",
    "answer": "ਰਾਜਾ"
  },
```
