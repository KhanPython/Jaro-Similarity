# Jaro-Similarity
LuaU Jaro Similarity Implementation from:

    http://rosettacode.org/wiki/Jaro_similarity#Python 
    https://www.geeksforgeeks.org/jaro-and-jaro-winkler-similarity/ 
    https://github.com/ogus/jaro-winkler/blob/master/src/jaro-winkler.js

# Methods

1. Get Jaro similarity:
```lua
  Jaro:JaroSimilarity(string1: string, string2: string, inputConfig: table)
```
2. Get Jaro distance (inverse of Jaro similarity)
```lua
  Jaro:JaroDistance(string1: string, string2: string, inputConfig: table)
```
3. Get Jaro Winkler
```lua
  Jaro:JaroWinkler(string1: string, string2: string, inputConfig: table)
```
