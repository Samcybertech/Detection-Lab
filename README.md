# AI-Fuzzer: ML-Powered Intelligent Web Fuzzer

[![Python](https://img.shields.io/badge/Python-3.10+-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An advanced web application fuzzer that uses machine learning to learn from responses, intelligently mutate payloads, and prioritize inputs likely to trigger vulnerabilities (SQLi, XSS, command injection, etc.).

Unlike traditional fuzzers, this tool adapts its mutation strategy over time using feedback from previous requests.

### Features
- Adaptive payload mutation based on response feedback
- Integration with wordlists + generative suggestions
- Customizable mutation strategies (random, context-aware)
- Request logging and filtering (Burp-style)
- Basic anomaly detection for potential vulnerabilities

It works well with Burpsuitepro

## Installation
```bash
https://github.com › cyberark › FuzzyAI
cd ai-fuzzer
pip install -r requirements.txt


## Quick Start

python fuzzer.py --url "http://target.com/login" --method POST \
  --data "username=FUZZ&password=test" --wordlist payloads.txt \
  --strategy adaptive
