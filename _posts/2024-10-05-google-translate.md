---
layout: post
title:  "Using Google Translate in Python"
author: Will Knisley
description: A blog post on how to use google translate in python
image: "/path/to/image"
---

Google translate is a great and easy way to quickly read something in a different language, and implementing it in python opens lots of doors when it comes to datasets and other data sources in other languages. 

Installing the google translate python module is fairly straightforward. If you have pip installed, it's as easy as inputting 
```python
pip install googletrans==4.0.0-rc1
```
into your terminal, and pip will take care of the rest. 

This translator can be used in many different ways, but the easiest way is to simply use it on a phrase or sentence. You'll need to import the translator using, and  
```python
from googletrans import Translator
and initialize an instance using
translator = Translator()
```

From there, you can input any string you want to use in another lanugage. If you don't want to input the source or destination language, Google will try to autodetect the language and then translate the string into English.
For example,
```python
from googletrans import Translator
translator = Translator()
result = translator.translate("Wir wollen trinken")
print(result.text)
```
outputs "We want to drink."

You can also input a source/destination language if you want to specify the language you're inputting, or if you want Google to output the translated string in a language besides english.
For example,
```python
result = translator.translate("Wir wollen trinken", dest="es")
print(result.text)
```
would output "Queremos beber."

If you're looking for a specific language code to use, you can check in googletrans.LANGUAGES.

You can also use googletrans to detect the language of a string. For example
```python
result = translator.detect("Wir wollen trinken")
print(result)
would output 
Detected(lang=de, confidence=None)
```

One of the more useful ways to use the google translate module for data science is translating data from a dataset. You can use the module to translate data from any language to another with a simple for loop like below:

```python
english_words = []
words = pd.read_csv("words.csv")
german_words = words["german_words"]


for i in range(5):
    result = translator.translate(german_words[i])
    english_words.append(result.text)
```

There are many different applications for google translate in data science, but these are just some of the basics of how to get started with it. Being able to work with data from all around the world in any language available through Google Translate is exciting and can only mean better research in the future. This module could be especially helpful with using data that's in another language. With translation, we're able to access and use data from all over the world.