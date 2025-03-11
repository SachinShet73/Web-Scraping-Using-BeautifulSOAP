# Web-Scraping-Using-BeautifulSoup

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.7+-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4.10.0-orange?style=for-the-badge)](https://www.crummy.com/software/BeautifulSoup/)
[![Pandas](https://img.shields.io/badge/Pandas-Latest-150458?style=for-the-badge&logo=pandas)](https://pandas.pydata.org/)
[![Requests](https://img.shields.io/badge/Requests-Latest-black?style=for-the-badge)](https://requests.readthedocs.io/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter)](https://jupyter.org/)

[![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](http://makeapullrequest.com)

</div>

## 📋 Overview

A comprehensive tutorial repository for learning web scraping using Beautiful Soup in Python. This repository contains educational materials and code examples that demonstrate how to extract and manipulate data from HTML and XML files with Beautiful Soup, a popular Python library for web scraping.

## 🎯 Learning Objectives

After working through the materials in this repository, you will be able to:

- Create and manipulate Beautiful Soup objects
- Navigate and search HTML document trees
- Work with HTML tags, attributes, and text content
- Filter HTML content with various methods
- Extract data from web pages using Beautiful Soup
- Parse HTML tables into pandas DataFrames
- Apply web scraping techniques to real-world scenarios

## ✨ Topics Covered

### Beautiful Soup Objects
- Creating Beautiful Soup objects from HTML content
- Understanding the nested data structure of HTML documents
- Rendering HTML structure with the prettify() method

### HTML Navigation
- Working with HTML tags
- Navigating through children, parents, and siblings
- Accessing and manipulating HTML attributes
- Working with NavigableString objects

### Filtering and Searching
- Using `find_all()` to locate elements by tag name
- Filtering elements by attributes
- Searching for string content
- Using the `find()` method for single element retrieval

### Practical Applications
- Downloading web page content with the Requests library
- Scraping links, images, and other content
- Extracting data from HTML tables
- Converting scraped data into pandas DataFrames

## 🛠️ Technology Stack

### Core Libraries
- Python 3.7+
- Beautiful Soup 4.10.0
- Requests
- Pandas
- lxml 4.6.4
- html5lib 1.1

### Features
- Tag navigation and manipulation
- Element filtering by attributes
- String content extraction
- Table data extraction
- DataFrame conversion

## 📘 Usage and Examples

The repository contains a comprehensive Jupyter Notebook (`WebScraping_Review_Lab.ipynb`) with step-by-step examples and exercises. Here's how to make the most of it:

1. Start by understanding the basics of Beautiful Soup objects
2. Learn to navigate through HTML elements
3. Practice filtering and searching for specific content
4. Work through practical examples of web scraping
5. Complete the exercises to test your knowledge

### Example Code Snippets

#### Creating a Beautiful Soup Object
```python
from bs4 import BeautifulSoup
import requests

# Create a Beautiful Soup object from HTML string
html = "<html><body><h1>Hello, Beautiful Soup!</h1></body></html>"
soup = BeautifulSoup(html, "html.parser")
print(soup.prettify())
```

#### Finding Elements
```python
# Find all links on a webpage
url = "http://www.example.com"
response = requests.get(url)
soup = BeautifulSoup(response.text, "html.parser")

for link in soup.find_all('a'):
    print(link.get('href'))
```

#### Extracting Table Data
```python
# Convert HTML table to DataFrame
table_html = """<table>
  <tr><th>Name</th><th>Age</th></tr>
  <tr><td>Alice</td><td>25</td></tr>
  <tr><td>Bob</td><td>30</td></tr>
</table>"""

soup = BeautifulSoup(table_html, "html.parser")
import pandas as pd
df = pd.read_html(str(soup.find('table')))[0]
print(df)
```


## 📝 License

[![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Beautiful Soup documentation and its creators for the excellent library
- IBM Developer Skills Network for the educational content
- Contributors to the Requests and Pandas libraries
- Everyone who contributes examples and improvements to this repository

## 📚 Additional Resources

- [Beautiful Soup Documentation](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
- [Requests Library Documentation](https://requests.readthedocs.io/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Web Scraping Ethics and Legal Considerations](https://www.scrapehero.com/how-to-prevent-getting-blacklisted-while-scraping/)

---

<div align="center">
  <sub>Built with ❤️ for the web scraping community</sub>
</div>
