# BYGB-7990-Assignment-1
## Overview
This project uses NLTK in Python to analyze and obtain a fashion trend from fashion reviews. NLTK is a library for Nature Language Processing. 
This project used stop word removing, Porter Stemmer, Lancaster Stemmer, and POS tags.  
***
## Installation
Install nltk by executing `pip install nltk` in Terminal   
After installation, import nltk in Python:  
`import nltk`  
`nltk.downloan()`  
***
## Usage
1. Import packages from nltk:  
`from nltk.corpus import stopwords`  
` from nltk import FreqDist`  

2. Initial process: tokenize content and eliminate numbers:   
` review_token=nltk.word_tokenize(review)`  
` review_word=[w.lower() for w in review_token if w.isalpha()]`  

3. Sort based on frequency:  
` review_freq=FreqDist(review_word)`  
` review_sorted=sorted(review_freq.items(), key=lambda k:k[1], reverse=True)`  

4. Removing stop word based on English standard:  
` stopwords=stopwords.words('english')`  
` review_nostop=[w for w in review_word if w not in stopwords]`  

5. Apply Porter Stemmer approach:   
` ps=nltk.PorterStemmer()`  
`review_stem=[ps.stem(w) for w in review_nostop]`

6. Apply Lancanster Stemmer:  
`ls=nltk.LancasterStemmer()`  
`review_ls=[ls.stem(w) for w in review_nostop]`

7. Apply POS tag:   
` review_POS=nltk.pos_tag(review_token)`
***

