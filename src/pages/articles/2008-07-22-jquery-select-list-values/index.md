---
archived: true
path: 'jquery-select-list-values'
title: 'jQuery Tip - Getting Select List Values'
description: "Get the select list value or selected option's text."
tags:
  - 'JavaScript & jQuery'
  - 'jQuery'
  - 'Tutorial'
date: '2008-07-22T11:34:03.000Z'
draft: false
layout: 'post'
---

![](./logo-jquery-1.jpg)

A friend asked me a simple question today, but it is worth noting because I have asked the same before, "How do you get the current value from a select list?" To get the current value is very simple using `val()` .

```js
$('#selectList').val()
```

But sometimes you may need to get the selected option's text. This is not as straight forward. First, we get the selected option with `:selected` selector. Then once we have the option, we can get the text with the function, `text()`.

```js
$('#selectList :selected').text()
```

> Note on July 23 `9:14AM: **HoyaSaxa93** wrote in to ask how to get values from select multiples.

This would be how to set a select multiple to an array called, "foo":

```js
var foo = []
$('#multiple :selected').each(function(i, selected) {
  foo[i] = $(selected).text()
})
```
