---
tags:
  - Object
  - Problem
---
# Matching Problem

Name: `"match_prob"`

??? tip "Template"
    ```json
      {
        "type": "match_prob",
        "answer_key": {
            "": "",
            "": "",
            "": "",
            "": ""
        }
      }
    ```

## Creation

You create a match problem by setting `"type"` to `"match_prob"`. 

```json
  {
      "type": "match_prob",
      ...
  }
```

## Properties

* [`"answer_key"`](#answer-key) <code><b>REQUIRED</b></code> <code><b>DICTIONARY</b></code>

--- 

### Answer Key 

`"answer_key": {}`

The `"answer_key"` property is a dictionary which contains `key` `value` pairs that **match**.

```json
  "answer_key": {
      "One": "1",
      "Two": "2",
      "Four": "4",
      "Three": "3"
  }
```
  In this case we can see that `"One"` matches `"1"` so if the user clicked on `"One"` and matched it with `"1"`, Then that would be correct!
  On the other hand if they tried to match `"One"` with `"3"` that would be wrong!
!!! note
    You do not have to worry about scrambling just make sure the `key` `value` pairs match, and Lipi will do the scrambling for you.

--- 

## Example
```json
  {
    "type": "match_prob",
    "answer_key": {
      "One": "1",
      "Two": "2",
      "Four": "4",
      "Three": "3"
    }
  }
```