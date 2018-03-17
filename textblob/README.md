# Textblob

| Methods | Description |
| --- | --- |
| `TextBlob(TEXT)` | Create a textblob |
| `TextBlob(TEXT).tags` | Part-of-speech (POS) tag |
| `TextBlob(TEXT).noun_phrases` | Noun phrase (NP) extraction |
| `TextBlob(TEXT).sentiment` | Sentiment analysis |
| `TextBlob(TEXT).words` | Word tokenization |
| `TextBlob(TEXT).sentences` | Sentence tokenization |
| `TextBlob(TEXT).words[INDEX].singularize()` | Convert word to singular form |
| `TextBlob(TEXT).words[INDEX].pluralize()` | Convert word to plural form |
| `Word(TEXT).lemmatize()` | Show the text in inflected form |
| `Word(TEXT).synsets` | Show the synsets property of text |
| `Word(TEXT).get_synsets(pos=VERB)` | Method to get text synsets |
| `Word(TEXT).definitions` | Get definition for text |
| `TextBlob(TEXT).correct()` | Return correct spelling |
| `Word(TEXT).spellcheck()` | Return a list of suggested spellings |
| `TextBlob(TEXT).word_counts[WORD]` | Return word count |
| `TextBlob(TEXT).words.count[WORD, case_sensitive=True]` | Return word count, default not case sensitive |
| `TextBlob(TEXT).noun_phrases.count(WORD)` | Noun phrase (NP) extraction count |
| `TextBlob(TEXT).translate(from_lang, to)` | Text translation |
| `TextBlob(TEXT).detect_language()` | Detect text language |
| `TextBlob(TEXT).parse()` | Parse text |
| `TextBlob(TEXT).ngrams(n=INTEGER)` | Return n-grams |
