<p>
    <center><h1> Advanced NLP with spaCy </h1> </center>
</p>

![](https://i.imgur.com/JC00pHW.jpg)
<!-- ![](https://i.imgur.com/5RXLtrr.jpg) -->

> Course material from the course ADVANCED NLP with spaCy & Other NLP material from Kaggle
<!-- using htmlpreview -->
<!-- link to render static html -->
<!-- https://htmlpreview.github.io/ -->

## NLP Data Collection Tips and Tricks

### Capturing Data 

1. Plain Text using python os module
```python
import os 
with open('demo.txt') , 'r') as f :
    text = f.read()
    print(text)
```
2. Tabular Data Using pandas
```python
import pandas as pd
df = pd.read_csv('demo.csv')
```
3. Fetching data from online Resources 
```python
import requests
r = requests.get('https://demo.rest/demo.json')
res = r.json()

data = res['key_1']['key_2'][0] # 0 or any index
```

### Cleaning data 
1. Using Regex
```python
import re
pattern = re.compile(r'<.*?.')
print(pattern.sub('',text))
```

2. BeautifulSoap
```python
from bs4 import BeautifulSoap
soup = BeautifulSoap(html_text, 'html5lib')
print(soup.get_text())

soup.find_all('div',class='classname')
soup.select_one('css selector')
```


### Normalization
1. Case Normalization
```python
text = text.lower()
```
2.Punctuation Removal
```python
import re
text = re.sub(r"[^a-zA-Z0-9]","",text)
```
### Tokenization

```
list = text.split(' ')
```
## spaCy 
- [Chapter 1](https://htmlpreview.github.io/?https://github.com/pawarashish564/ADVANCED-NLP-with-spaCy/blob/master/Chapter-1.html) 
- [Chapter 2](https://htmlpreview.github.io/?https://github.com/pawarashish564/ADVANCED-NLP-with-spaCy/blob/master/Chapter-2.html) 
- [Chapter 3](https://htmlpreview.github.io/?https://github.com/pawarashish564/ADVANCED-NLP-with-spaCy/blob/master/Chapter-3.html)

## NLP - Notebooks

- [Text Classification](https://htmlpreview.github.io/?https://github.com/pawarashish564/ADVANCED-NLP-with-spaCy/blob/master/Text-Classification.html)

