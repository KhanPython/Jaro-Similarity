# Jaro-Similarity:

**LuaU Jaro Similarity Implementation from the following sources:**

###### 1. http://rosettacode.org/wiki/Jaro_similarity#Python
###### 2. https://github.com/ogus/jaro-winkler/blob/master/src/jaro-winkler.js 
###### 3. https://www.geeksforgeeks.org/jaro-and-jaro-winkler-similarity/


>Jaro similarity is the measure of similarity between two string, represented by a range from 0 to 1. Where 1 means the strings are equal and 0 - no similarities

>The Jaro-Winkler similarity is a string metric measuring edit distance between two strings. Jaro – Winkler Similarity is much similar to Jaro Similarity. They both differ when the prefix of two string match. Jaro – Winkler Similarity uses a prefix scale ‘p’ which gives a more accurate answer when the strings have a common prefix up to a defined maximum length l


# Overview of methods:

###### Default input configuration:
```lua
inputConfig = {
    caseSensitive = false,
    scalingFactor = 0.1,
    prefixLength  = 4
}
```

###### Calculate Jaro similarity:
```lua
Jaro:JaroSimilarity(string1: string, string2: string, inputConfig: table)
```
###### Calculate Jaro distance: (inverse of Jaro similarity)
```lua
Jaro:JaroDistance(string1: string, string2: string, inputConfig: table)
```
###### Calculate Jaro Winkler:
```lua
Jaro:JaroWinkler(string1: string, string2: string, inputConfig: table)
```
# Example usage:
```lua
local JaroUtil = require(game.ServerScriptService.JaroUtil)

print(JaroUtil:JaroSimilarity("Hello", "hello", {
    caseSensitive = true,
}))

print(JaroUtil:JaroSimilarity("Hello", "Hello")) 

print(JaroUtil:JaroDistance("Hello", "Bello"))

--//Output 1: 0.8666..
--//Output 2: 1
--//Output 3: 0.1333.. 
```
