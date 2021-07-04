# Jaro-Similarity
LuaU Jaro Similarity Implementation from the following sources:

1. http://rosettacode.org/wiki/Jaro_similarity#Python
2. https://www.geeksforgeeks.org/jaro-and-jaro-winkler-similarity/
3. https://github.com/ogus/jaro-winkler/blob/master/src/jaro-winkler.js

# Methods:

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
