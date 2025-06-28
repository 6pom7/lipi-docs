# Introduction

Lipi lessons are created in `json` format and are comprimised of `problem` / `page` objects. These objects can be used to build a lesson.

## Types of Objects

* [`multi_choice`](./Json%20Objects/multi_choice.md)
* [`match_prob`](./Json%20Objects/match_prob.md)
* [`laga_prob`](./Json%20Objects/laga_prob.md)
* [`word_prob`](./Json%20Objects/word_prob.md)
* [`drag_word`](./Json%20Objects/drag_word.md)
* [`sound_word`](./Json%20Objects/sound_word.md)
* `info_page`
* `final_page`

## Example Lesson
```json
[
  {
    "type": "info_page",
    "content": [
      {
        "size": "title",
        "text": "Example Lesson"
      },
      {
        "style": "nl",
        "times": 2
      },
      {
        "size": "big",
        "text": "This is an example lesson",
        "style": "highlight"
      },
      {
        "style": "nl",
        "times": 2
      },
      {
        "text": " Click next to continue!"
      }
    ]
  },
  {
    "type": "multi_choice",
    "answer": "3",
    "options": [
      "3",
      "6",
      "2",
      "9"
    ],
    "question": "1 + 2",
    "subtitle": "Example Question"
  },
  {
    "type": "multi_choice",
    "answer": "こんにちは",
    "options": [
      "こんにちは",
      "ありがとう",
      "はい",
      "いいえ"
    ],
    "hints": [
      "Hello",
      "Thank You",
      "Yes",
      "No"
    ],
    "question": "Hello",
    "subtitle": "Translate to Japanese"
  },
  {
    "type": "word_prob",
    "word": "Hot",
    "answer": "ਗਰਮ"
  },
]

```