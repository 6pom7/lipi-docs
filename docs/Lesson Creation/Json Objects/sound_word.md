---
tags:
  - Object
  - Problem
---
# Sound Word Problem

Name: `"sound_word"`

??? tip "Template"
    ```json
      {
        "type": "sound_word",
        "word": ""
      },
    ```
    ??? tip "Template With Options"
        ```json
          {
            "type": "sound_word",
            "word": "",
            "options": ["", "", "", ""]
          },
        ```

## Creation

You create a multi choice problem by setting `"type"` to `"sound_word"`. 

```json
  {
      "type": "sound_word",
      ...
  }
```

## Properties

* [`"word"`](#word) <code><b>REQUIRED</b></code>
* [`"options"`](#options) <code><b>OPTIONAL</b></code> <code><b>LIST</b></code>

--- 

### Word 

`"word": ""`

This is the Punjabi word who's sound will be used for this problem. The sound of this word will
be played to the user and the user will have find the right word from the [`"options"`](#options)
list.

```json
  "word": "ਸਚ",
```
> In this case Lipi will fetch the sound for the word "ਸਚ" and play it 
  to the user.

!!! warning

    In order for Lipi to be able to play the sound of the word,
    the word needs to be in the Lipi **online** storage! (1)
    { .annotate }

    1. In otherwords it needs to be in the Supabase storage.

--- 

### Options

`"options": []`

This is a list of multiple options from which the user may pick to answer the question.
Make sure to add the word from the [`"word"`](#word) property as one of the options!

```json
  "options": ["ਸਚ", "ਮਿਰਚ", "ਖਾਲੀ", "ਕੇਲਾ"],
```
!!! warning

    One of the `"options"` must must be **EXACTLY** the same as the
    [`"word"`](#word) property, in order for it to function correctly.

??? info "Not Reqired"

    The `"options"` property is not required. Lipi will automatically generate a list of random
    words if the `"options"` property is not given!
---

## Example
```json
  {
    "type": "sound_word",
    "word": "ਸਚ"
  },
```

??? example "Example With Options"
    ```json
      {
        "type": "sound_word",
        "options": ["ਸਚ", "ਮਿਰਚ", "ਖਾਲੀ", "ਕੇਲਾ"],
        "word": "ਸਚ"
      },
    ```