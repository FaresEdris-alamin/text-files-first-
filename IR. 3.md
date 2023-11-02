#IR
Lecture
Boolean retrieval model 
Term document incidence matrix,
	it's attribute: row=M=distinct term, 
	    column=N=documents 
	it's problem : waste of space 
Inverted index 
	1. Dictionary 
		docID: sorted alphabetically, 
		stored in the RAM in a fixed array , 
	2. Posting list
		sorted ascending,  
		in memory using linked list or variable length array, diff. In size/insertion ease, 
		on disk continuously stored passing after passing, 
Indexing pipeline 
	- determine the document 
	- tokenizer: turn the document to token stream
	- linguistic module: turn the token to it's base form 
	- indexer: 
		input: sequence of token
		we sort the term alphabetically, 
		same term in the document are merged, 
		then split into dictionary and posting list, 
		document frequency is added:for Query optimization, 
Merge algorithm 
	query processing: AND
	O(size of array 1&2)
	pseudocode 
Boolean queries 
	give exact match, 
	uses AND, OR, Not to join query terms, 
	Views each document as a set of words, 
	is precise and simple to implement, 
	used: Email, library catalog, Mac OS X Spotlight, 
	westlaw
Query optimization 
	start with smallest set
