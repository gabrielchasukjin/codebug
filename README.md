# Codebug

Codebug replaces scary error messages with digestible text-explanations of the error. 

## Demo
When pandas encounters an error, it spits out a massive red text. 
1. Hard to discern the error message
2. Bold red text discourages coding beginners

<img width="1254" alt="codebug_error" src="https://user-images.githubusercontent.com/95925660/228628449-4609c584-b60a-4c95-aa40-c275756c723c.png">

## Codebug solution
<img width="1266" alt="codebug_sol" src="https://user-images.githubusercontent.com/95925660/228628468-4ba89df1-4612-4aa2-bfc4-2c005311af6d.png">

**Codebug takes in the error message and returns a simple explanation of it.**
1. Encourages student to understand the error
2. Clears up python misconceptions
3. Offers practical suggestions to fix buggy code

Codebug is powered by GPT-3.5 from OpenAI.



## Table of Contents 

- [Installation](#installation)
- [Usage](#usage)

## Installation

Add this line to your command line:

```python
pip install Codebugger
```

If encounter ModuleNotFoundError:

Run following code in python file:

```python
import sys
print(sys.executable)
```

Copy the path (i.e. it may look like this):

```python
/Library/Frameworks/Python.framework/Versions/3.9/bin/python3
```

Install codebugger using the following path in the terminal:

```python
/Library/Frameworks/Python.framework/Versions/3.9/bin/python3 -m pip install Codebugger
```

## Usage

Add the following to your python file:

```python
from codebugger import Codebug
```
### Instance
Create new instance of Codebug() class:

```python
debug = Codebug()
```

### Error Message
Print Error Message: 

```python
debug.getMessage()
```

When no errors are encountered, Codebug returns: "No errors found!" 

### OpenAI API KEY
To recieve explantions of error, user must get API Key from OpenAI: https://platform.openai.com/account/api-keys

Set API-KEY
```python
debug.setAPI('API-KEY')
```

### Explnation of Error
Requires basic understanding of try/except.

Try and Except:
```python
try:
  block of code
except Exception as e: 
  debug.setError() # Compiles the error
  print(debug.explnation()) #API Call to GPT-3.5 for explnation of error
  
```







