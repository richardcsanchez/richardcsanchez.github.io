---
layout: post
title:      "Code Challenge 1"
date:       2019-08-17 14:56:28 -0400
permalink:  code_challenge_1
---

As I move into a new phase of coding, I've been trying to hone my skills and do more logic based coding. One of the more stressful aspects of interviewing is the anticipation of being asked to perform a code challenge on the spot. In this blogpost, I'll go though one of the more basic but tricky challenges I've encountered. 

### The Challenge: 
### "Given a sentence, output the frequency of each letter in the sentence, removing whitespaces."
 
The first step I tackled here is to remove the white space in the string. My initial thought was to call ```.trim()```, but I quickly remembered that would only remove white space from the front and end of a string, not inbetween words.
 
 I was trying to avoid using regex and I was looking at some more unconventional "hacky" methods. I found that if I ```.split(" ")``` the string, then called ```.join("")```, I would get a string without whitespaces. I could then call ```.split("")``` again on that new string and get an array of individual letters.

```
var string = "this is a string"

var newString = string.split(" ").join("")
var letterArray = newString.split("")

console.log(newString): "thisisastring"
console.log(letterArray): ["t", "h", "i", "s", "i", "s", "a", "s", "t", "r", "i", "n", "g"
]
```

While this gave me the desired result, calling ```.split()``` on two different lines while manipulating the same string didn't look very elegant. So I went with the regex option, which gave me the result in one line of clean code.

```
var letterArray = string.replace(/\s+/g, '').split("")
```

From there, I looped over the the `letterArray` with a `for...` loop, incrementing the count for each letter as it was iterated over, and created an object ,`result`, to store the incrementing counts. 

```
var result = {}

for (var i = 0; i < letterArray.length; i++) {
  letter = letterArray[i]
```

	
While iterating, if we have seen this letter, increase the count by one
	
    ```
		if (result[letter]) {
    result[letter]++
		```
			
Otherwise set count to 1
	
   ``` 
	 } else {
     result[letter] = 1
    }
}
```

The `result` object gives us pairs of letters and their individual counts: 

```
Object {
  a: 1,
  g: 1,
  h: 1,
  i: 3,
  n: 1,
  r: 1,
  s: 3,
  t: 2
}
```

Full Code:
```
var string = "this is a string"

var letterArray = string.replace(/\s+/g, '').split("")

var letter = ""
var result = {}

for (var i = 0; i < letterArray.length; i++) {
  letter = letterArray[i]
  
    if (result[letter]) {
      result[letter]++
    } else {
      result[letter] = 1
    }
}

console.log(result)
```

