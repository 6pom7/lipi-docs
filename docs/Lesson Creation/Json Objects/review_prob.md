---
tags:
  - Object
  - Problem
---
# Review Problem

Name: `"review"`

??? tip "Template"
    ```json
      {
          "type": "review",
          "chapter": // (1)!
      },
    
    ```

    1.  Add an integer value of the chapter you would like to
        pull the review question from here.

    
## About

The review object pulls a random problem from the specified
`"chapter"` property.

## Creation

You create a multi choice problem by setting `"type"` to `"review"`. 

```json
  {
      "type": "review",
      ...
  }
```

## Properties

* [`"chapter"`](#chapter) <code><b>REQUIRED</b></code> <code><b>INTEGER</b></code>

--- 

### Chapter

`"chapter": `

This is the chapter you want to get the problem from.

```json
  "chapter": 3
```
> This would get a random problem from chapter 3
--- 

## Examples
```json
  {
    "type": "review",
    "chapter": 3
  },
```
```json
  {
    "type": "review",
    "chapter": 4
  },
```
