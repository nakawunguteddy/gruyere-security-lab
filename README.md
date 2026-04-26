# Gruyere: vulnerable python app for security testing

## usage
Clone and run ./gruyere.py

I've added minor changes for Python 3 compatibility (the code is python2/3 compatible). You might need a `pip3 install future`

Tested on Linux/Unix with Python 2.7 to 3.9
## credits
Base code is Copyright 2017 Google Inc. All Rights Reserved.

This code is licensed under the http://creativecommons.org/licenses/by-nd/3.0/us
Creative Commons Attribution-No Derivative Works 3.0 United States license.

# Gruyere Security Lab — Module 4

## Setup
git clone this repo, then:
pip install future
python gruyere.py

## Vulnerability findings & fixes

| Vulnerability | Exploitable | Fix applied | Commit |
|---|---|---|---|
| Stored XSS | Yes | Default HTML-escape in gtl.py | fix: stored XSS |
| Reflected XSS | Yes | :text escaper in search.gtl | fix: reflected XSS |
| DoS – quitserver | Yes | Admin check + protected URL | fix: DoS quitserver |
| SQL Injection | No (no SQL used) | N/A | doc: SQLi |
| Buffer Overflow | No (Python runtime) | N/A | doc: overflow |

## Screenshots
See /screenshots folder for before/after evidence of each attack and fix.