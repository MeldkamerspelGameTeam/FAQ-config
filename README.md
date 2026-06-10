FAQ config examples:

The FAQ cache is loaded from data/support_faq.json.
Each FAQ entry should contain an answer string.
Use keywords as one list of match options.
A plain string matches if that word appears in the message.
A nested list matches only if all words in that group appear in the message.
The FAQ fires when any one top-level item in keywords matches.
```
[
  {
    "keywords": ["mail", ["verificatie", "forum"]],
    "answer": "Controleer of je spamfolder leeg is en probeer het later opnieuw."
  },
  {
    "keywords": [["verificatie", "forum"]],
    "answer": "Voor forumtoegang moet je eerst je account verifiëren in Mail en daarna opnieuw inloggen."
  }
]

```
In the first example, the FAQ matches when the message contains mail, or when it contains both verificatie and forum.
