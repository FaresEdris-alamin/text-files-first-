#IR
### **We use skip pointers in optimization **
Why -> to skip posting that won't figure in the search results
How-> by checking if the skip pointer is less than the second pointer 
src->in the 3 slide 
Where-> 
#### Trade off:
- more skips->shorter skip span->more likely to skip. Alot of comparison 
- fewer skips->fewer Pointer comparison ->fewer successful skip. Long skip span

#### Placing skips:
- Used in static list	
- for posting of size L -> root L
- Used to be helpful unless memory based 
- only useful with AND operations not OR&NOT 

#### Pharse queries 
**Ex:"Cairo University "**
##### First attempt
- Biword indexes:
For longer phrases we break them term containing 2 words and then Adding the terms. 
**Issues**: false positives, index blowup due to the size of the dictionary
____
>The concept got extended for longer sequence of words with limited success 

#### Solution 1: Phase index
	Variable sequence length
#### Solution 2: Positional indexes
	Store for each term it's list of positions 
____
#### Processing phrase queries
#### Proximity queries 
	Could be done using Positional indexing 

>**Positional index size**
>>large size due to the need to store every occurrence in the decoument 

#### Rules of thumb 
- A positional index is 2–4 as large as a non-positional index
- Positional index size 35–50% of volume of original text
- Caveat: all of this holds for “English-like” languages
#### Combination schemes 
	- We usually use multiple and different IR system for different types of queries 
	- EX: using Biword for celebrity names, and terms that individually  repeat alot but together rarely 














