# Natural Language Toolkit (nltk) and Context-Free Grammar (CFG) Project  

This project utilizes the Natural Language Toolkit (nltk) and Context-Free Grammar (CFG) to generate and manipulate sentences based on a defined grammar structure. The script also imports the `random` module, which may be used for generating random selections from the grammar.  

## Prerequisites  

Before running this code, ensure you have the necessary dependencies installed:  

```bash
pip install nltk
Usage
Import the necessary libraries:
python
Copy
Edit
import nltk
from nltk import CFG
import random
Define a grammar using CFG.
Use nltk.ChartParser or nltk.RecursiveDescentParser to parse sentences.
Generate and manipulate sentences based on the grammar.
Example
python
Copy
Edit
# Define a simple grammar
grammar = CFG.fromstring("""
  S -> NP VP
  NP -> 'John' | 'Alice'
  VP -> 'eats' | 'sleeps'
""")

# Generate a parser
parser = nltk.ChartParser(grammar)

# Example sentence
sentence = ['John', 'eats']

# Parse the sentence
for tree in parser.parse(sentence):
    print(tree)
License
This project is open-source and free to use under the MIT License.
