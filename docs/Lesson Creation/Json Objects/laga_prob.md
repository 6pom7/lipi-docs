---
tags:
  - Object
  - Problem
---
# Laga Problem

Name: `"multi_choice"`

??? tip "Template"
    ```json
      {
        "type": "laga_prob",
        "prompt": "",
        "start_text": "",
        "answer": ""
      }
    ```

## Creation

You create a laga problem by setting `"type"` to `"laga_prob"`. 

```json
  {
      "type": "laga_prob",
      ...
  }
```

## Properties

* [`"prompt"`](#prompt) <code><b>REQUIRED</b></code>
* [`"start_text"`](#start-text) <code><b>REQUIRED</b></code>
* [`"options"`](#options) <code><b>OPTIONAL</b></code> <code><b>LIST</b></code>
* [`"hints"`](#hints) <code><b>OPTIONAL</b></code> <code><b>BOOLEAN</b></code>
* [`"answer"`](#answer) <code><b>REQUIRED</b></code> 

--- 

### Prompt

`"prompt": ""`

This is the instruction that will be shown to the user.

```json
  "prompt": "Make the Chaa sound",
```
> Tipically a prompt will just ask the user to make a certian sound.
--- 

### Start Text

`"start_text": ""`

This is the text that the preview starts off as. This is typically a character in which the user will
add a laga from one of the [`"options"`](#options) in order to make the 
sound given in the [`"prompt"`](#prompt).

```json
  "start_text": "ਚ",
```

In this case the user will add a laga from the [`"options"`](#options) to the ਚ character to make the sound given in the prompt.

--- 

### Options

`"options": [6]`

This is a list of laga that the user can add onto the [`"start_text"`](#start-text) in order to make the sound in 
the [`"prompt"`](#prompt). The list of options must contain at least and at most 6 laga.
This is property is **OPTIONAL** and is not required in order for the problem to work.

```json
  "options": ["ਾ", "ਿ", "ੀ", "ੁ", "ੂ", "ੈ"],
```
!!! warning
    The laga used in the [`"answer"`](#answer) must be provided in the list of options!
??? note "Not Required"

    Lipi has updated and no longer **REQUIRES** a list of options. Lipi can now genarate a random list of options
    given the [`"answer"`](#answer) property. You can still provide a list of options, Lipi will use the provided
    `"options"` if they are given. If not Lipi will randomly generate new options.


--- 

### Hints
`"hints": false`

Weather or not to show hints under the laga. The hints would show what sound the laga (or that option)
makes. For example the laga ਾ would have the hint `Aa` as it makes the Aa sound.

```json
  "hints": true,
```

??? info 

    Used to be a list full of hints for the options much like in the multi choice problem,
    but since the option auto generation update it has been changed to a boolean.

---

### Answer

`"answer": ""`

This is the answer of the question. It should contain the [`"start_text"`](#start-text) along with the 
laga attached, so that makes the sound specified in the [`"prompt"`](#prompt).

```json
  "answer": "ਚਾ"
```
This makes the Chaa sound so this is the answer. The user would essentially create this using the givin options. If the user chooses the "ਾ" option they can get the correct answer.

## Example
```json
  {
    "type": "laga_prob",
    "prompt": "Make the Chaa sound",
    "start_text": "ਚ",
    "answer": "ਚਾ"
  },
```

??? example "Example With Options"
    ```json
    {
      "type": "laga_prob",
      "prompt": "Make the Chaa sound",
      "start_text": "ਚ",
      "options": ["ਾ", "ਿ", "ੀ", "ੁ", "ੂ", "ੈ"],
      "answer": "ਚਾ"
    },
    ```

??? example "Example With Hints"
    ```json
    {
      "type": "laga_prob",
      "prompt": "Make the Chaa sound",
      "start_text": "ਚ",
      "hints": true,
      "answer": "ਚਾ"
    },
    ```