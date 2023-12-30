<h1 align="center"> tgpt2 </h1>

<p align="center">
<a href="https://github.com/Simatwa/tgpt2/actions/workflows/python-test.yml"><img src="https://github.com/Simatwa/tgpt2/actions/workflows/python-test.yml/badge.svg" alt="Python Test"/></a>
<a href="LICENSE"><img alt="License" src="https://img.shields.io/static/v1?logo=GPL&color=Blue&message=GNUv3&label=License"/></a>
<a href="https://pypi.org/project/tgpt2"><img alt="PyPi" src="https://img.shields.io/static/v1?logo=pypi&label=Pypi&message=v0.0.1&color=green"/></a>
<a href="https://github.com/psf/black"><img alt="Black" src="https://img.shields.io/static/v1?logo=Black&label=Code-style&message=Black"/></a>
<a href="#"><img alt="Passing" src="https://img.shields.io/static/v1?logo=Docs&label=Docs&message=Passing&color=green"/></a>
<a href="#"><img alt="coverage" src="https://img.shields.io/static/v1?logo=Coverage&label=Coverage&message=90%&color=yellowgreen"/></a>
<a href="#" alt="progress"><img alt="Progress" src="https://img.shields.io/static/v1?logo=Progress&label=Progress&message=95%&color=green"/></a>
<a href="https://pepy.tech/project/tgpt2"><img src="https://static.pepy.tech/personalized-badge/tgpt2?period=total&units=international_system&left_color=grey&right_color=green&left_text=Downloads" alt="Downloads"></a>
<!--<a href="https://github.com/Simatwa/tgpt2/releases"><img src="https://img.shields.io/github/downloads/Simatwa/tgpt2/total?label=Downloads&color=success" alt="Downloads"></img></a> -->
<a href="https://github.com/Simatwa/tgpt2/releases"><img src="https://img.shields.io/github/v/release/Simatwa/tgpt2?color=success&label=Release&logo=github" alt="Latest release"></img></a>
<a href="https://github.com/Simatwa/tgpt2/releases"><img src="https://img.shields.io/github/release-date/Simatwa/tgpt2?label=Release date&logo=github" alt="release date"></img></a>
<a href="https://wakatime.com/badge/github/Simatwa/tgpt2"><img src="https://wakatime.com/badge/github/Simatwa/tgpt2.svg" alt="wakatime"></a>
</p>

<p align="center">
AI for all
</p> 

```python
from tgpt2 import TGPT
bot = TGPT()
resp = bot.chat('<Your prompt>')
print(resp)
# Output : How may I help you.
```

This project allows you to interact with AI ([LLaMA](https://ai.meta.com/llama/)) without API Key.

The name *tgpt2* is inherited from it's parent project [tgpt](https://github.com/aandrew-me/tgpt) which runs on [golang](https://go.dev/).

## Prerequisite

- [x] [Python>=3.9](https://python.org)

## Installation and usage

### Installation

Pick either of the following ways to get started.

1. From pypi:

```
pip install tgpt2
```

2. Direct from source

```
pip install git+https://github.com/Simatwa/tgpt2.git
```

3. Clone and Install

```
git clone https://github.com/Simatwa/tgpt2.git
cd tgp2
pip install .
```

## Usage

This package features a ready to use commandline interface.

- Quick response
   `python -m tgpt2 generate "<Your prompt>"`

- Interactive mode 
   `python -m tgpt2 interactive`

Instead of `python -m tgpt2`, ypu can as well use just `tgpt2`

<details>

<summary>

### Developer Docs

</summary>

1. Generate a quick response

```python
from tgpt2 import TGPT
bot = TGPT()
resp = bot.chat('<Your prompt>')
print(resp)
# Output : How may I help you.
```

2. Get back whole response

```python
from tgpt2 import TGPT
bot = TGPT()
resp = bot.ask('<Your Prompt')
print(resp)
# Output
"""
{'completion': "I'm so excited to share with you the incredible experiences...", 'stop_reason': None, 'truncated': False, 'stop': None, 'model': 'llama-2-13b-chat', 'log_id': 'cmpl-3NmRt5A5Djqo2jXtXLBwJ2', 'exception': None}
"""
```

#### Stream Response 

Just add parameter `stream` with value  `true`.

1. Text Generated only 

```python
from tgpt2 import TGPT
bot = TGPT()
resp = bot.chat('<Your prompt>', stream=True)
for value in resp:
    print(value)
# output
"""
How may
How may I help 
How may I help you
How may I help you today?
"""
```

2. Whole Response

```python
from tgpt2 import TGPT
bot = TGPT()
resp = bot.ask('<Your Prompt>', stream=True)
for value in resp:
    print(value)
# Output
"""
{'completion': "I'm so", 'stop_reason': None, 'truncated': False, 'stop': None, 'model': 'llama-2-13b-chat', 'log_id': 'cmpl-3NmRt5A5Djqo2jXtXLBwJ2', 'exception': None}

{'completion': "I'm so excited to share with.", 'stop_reason': None, 'truncated': False, 'stop': None, 'model': 'llama-2-13b-chat', 'log_id': 'cmpl-3NmRt5A5Djqo2jXtXLBwJ2', 'exception': None}

{'completion': "I'm so excited to share with you the incredible ", 'stop_reason': None, 'truncated': False, 'stop': None, 'model': 'llama-2-13b-chat', 'log_id': 'cmpl-3NmRt5A5Djqo2jXtXLBwJ2', 'exception': None}

{'completion': "I'm so excited to share with you the incredible experiences...", 'stop_reason': None, 'truncated': False, 'stop': None, 'model': 'llama-2-13b-chat', 'log_id': 'cmpl-3NmRt5A5Djqo2jXtXLBwJ2', 'exception': None}
"""
```


</details>


> **Note** : At the time of wriiting this, Chatting conversational is not supported

## Acknowledgements

1. [x] [tgpt](https://github.com/aandrew-me/tgpt)
2. [x] You

