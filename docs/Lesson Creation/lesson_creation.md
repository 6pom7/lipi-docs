# Formating

Lipi lessons are created in `json` format and are comprimised of `problem` / `page` objects. These objects can be used to build a lesson.

## Types of Objects

* `multi_choice`
* `match_prob`
* `laga_prob`
* `word_prob`
* `drag_word`
* `sound_word`
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