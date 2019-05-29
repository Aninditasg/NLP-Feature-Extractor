# NLP-Feature-Extractor
This code filters out 10 most important words from a document matrix.

he following code finds out the list of most important most common words from a list of documents and writes it to a json file in the following format into a json which can be used from other web applications. Table format Keyword | Docs | Sentences

Following steps summarize the tasks: 1) Read the text from the folder into doc _corpus
                                     2) Perform the following steps to clean up the data 
                                       a)Tokenize the sentences into words. 
                                       b)Remove stopwords and irrelevant words like pronouns, as they wouldn't be good hash tag
                                         candidates. 
                                       c) Use lemmatizer to group together different forms of the word to mean the same term like two and
                                          2 should be considered the same in an NLP problem which filters the most important word. 
                                       d) Use Stemmer to reduce reocurring verb forms to the root form like say,saying said gets reduced                                            to say
                                     3) Use Count Vectorizer to get a matrix with word counts across the Corpus and find out relevant
                                        features. 
                                     4) Use TF IDF to find word relevance so that the frequency of the word in a document is compared to
                                        frquency of the word across the documents, this filters out irrelevant words by assigning them a                                           low relevance score. 
                                     5) Combine the output features from count vectorizer and relevance matrix from TF IDF to generate the                                         top 10 keywords 
                                     6) Create a Table to display the documents containing the keywords and filter out the sentences. 
                                     7) Convert output to a dictionary and write it to a JSON file.

