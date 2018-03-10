# NLTK
This is a cheatsheet for **nltk** library. I **will not** be including:
1. Basic python function here
2. Methods for academic research

---

## [Text module](http://www.nltk.org/api/nltk.html#module-nltk.text)
This module brings together a variety of NLTK functionality for text analysis

### [Text class](http://www.nltk.org/api/nltk.html#nltk.text.Text)
| Methods | Description | Link |
| --- | --- | --- |
| `text.concordance(WORD, width=INTEGER, lines=(INTEGER or all))` | Shows us every occurrence of a given word, together with some context | [Link](http://www.nltk.org/api/nltk.html#nltk.text.Text.concordance) |
| `test.search(STRING)` | Find all words that share a common context |  |
| `text.common_contexts([WORD1, WORD2])` | Examine just the contexts that are shared by two or more words | [Link](http://www.nltk.org/api/nltk.html#nltk.text.Text.common_contexts) |
| `text.collocations()` | Return words that occur together unusually often | [Link](http://www.nltk.org/api/nltk.html#nltk.text.Text.collocations) |
| `text.dispersion_plot([VARIABLE1, VARIABLE2, ... VARIABLEN])` | Produce a plot showing the distribution of the words through the text | [Link](http://www.nltk.org/api/nltk.html#nltk.text.Text.dispersion_plot) |

---

## [Probability module](http://www.nltk.org/api/nltk.html#module-nltk.probability)
Classes for representing and processing probabilistic information

### [Frequency distribution class](http://www.nltk.org/api/nltk.html#nltk.probability.FreqDist)
| Methods | Description | Link |
| --- | --- | --- |
| `fdist = FreqDist(text)` | Return a dictionary containing frequency distribution | [Link](http://www.nltk.org/api/nltk.html#nltk.probability.FreqDist) |
| `fdist.most_common(INTEGER)` | Return the most common words | |
| `fdist[STRING]` | Return the count of STRING from frequency dictionary | |
| `fdist.freq(WORD)` | Return the percentage of word in entire text | [Link](http://www.nltk.org/api/nltk.html#nltk.probability.FreqDist.freq) |
| `fdist.hapaxes()` | Return list of words that only occur once | [Link](http://www.nltk.org/api/nltk.html#nltk.probability.FreqDist.hapaxes) |
| `fdist.plot(50, cumulative=True)` | Plot samples from the frequency distribution displaying the most frequent sample first | [Link](http://www.nltk.org/api/nltk.html#nltk.probability.FreqDist.plot) |
| `fdist.tabulate()` | Frequency distribution as a table |  |
