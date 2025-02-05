---
title: "Basic Web Scraping (2025/02/05)"
description: ""
---

#### [Visit (https://github.com/takehika0129/no3-basic-web-scraping)](https://github.com/takehika0129/no3-basic-web-scraping)

# **Concept**
This focuses on scraping quotes from `quotes.toscrape.com` based on specified tags. The goal is to create a simple way to collect relevant quotes while handling pagination and avoiding duplicate data.

# **Features**
- **🛠️ Robust Web Scraping Tools**: Uses `requests` for fetching web pages and `beautifulsoup` for parsing HTML.
- **📑 Multi-Page Navigation**: Navigates through multiple pages to extract more quotes.
- **🔄 Unique Quote Handling**: Ensures unique quotes by maintaining a global set.

# **Challenges & Solutions**  
- **Handling Pagination**: Initially, the scraper only accessed the front page, but it was modified to dynamically access each tag's dedicated page to retrieve quotes, ensuring comprehensive data extraction.
- **Avoiding Duplicate Quotes**: Some quotes appeared under multiple tags. This was solved by using a global `set` of unique quotes, ensuring each quote is only collected once.

# **⚠️ Ethical Scraping Practices**
When engaging in web scraping, it is important to respect the website’s `robots.txt` file and terms of service. Excessive requests can overload servers, leading to potential bans or legal consequences. Always ensure that scraping is conducted responsibly, with minimal impact on the website being accessed.

# **Future Improvements**
- **Database Integration**: Implementing a database to store and retrieve quotes efficiently.
- **Optimized Performance**: Adding multi-threading to speed up scraping while being mindful of request limits.
- **API Development**: Developing a simple API to access the collected quotes programmatically.

---
[Back to All Prototypes](../index.md)
