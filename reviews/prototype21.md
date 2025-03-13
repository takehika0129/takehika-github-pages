---
title: "Web Scraping + Database Storage (2025/03/13)"
description: ""
---

#### [Visit (https://github.com/takehika0129/no21-web-scraping-storage)](https://github.com/takehika0129/no21-web-scraping-storage)


# **Concept**
This project focuses on scraping book details from `books.toscrape.com` across multiple pages asynchronously. The goal is to create a fast and scalable scraper that extracts structured data and stores them in a database for later analysis.


# **Features**
- **🕵️‍♂️ Asynchronous Scraping for High Speed**: Uses `aiohttp` and `asyncio` to scrape multiple pages simultaneously, reducing wait time.
- **✅ Data Validation with Pydantic**: Ensures clean and structured data with `pydantic` to prevent incomplete or malformed records from being stored in the database.
- **📊 Database Storage with SQLAlchemy**: Scraped data is stored in SQLite or PostgreSQL using `SQLAlchemy`. This makes it easy to query and analyze books later.


# **Challenges & Solutions**
- **Switching from Synchronous to Asynchronous Scraping**: Initially, `requests` caused slow, sequential page fetching but replaced it with `aiohttp` and `asyncio.gather()` for parallel scraping, improving efficiency.
- **Data Validation & Choosing the Right Data Types**: There is uncertainty about the most suitable data type (`float`, `str`, `bool`). I think the optimal data type depends on how the database is managed and the purpose of data analysis, Although "price" is defined as a string.


# ⚠️ Ethical Scraping Practices
When scraping a website, it’s crucial to:
- Respect `robots.txt`: Some websites explicitly disallow scraping.
- Limit requests: Avoid sending too many requests in a short period to prevent overloading the server.
- Use the data responsibly: Ensure that scraped data is used for legal and ethical purposes.

This project scrapes a test website (books.toscrape.com), which is explicitly designed for scraping practice. However, when scraping real websites, always check their Terms of Service.


# **Future Improvements**
- **Dynamic Scraping**: Integrate `selenium` or `playwright` for javaScript-heavy websites while using aiohttp for static scraping.
- **Database Deployment**: Migrate to a cloud-based PostgreSQL database, optimize queries, and implement data cleanup for large-scale scraping.
- **Docker Support**: Package the scraper as a Docker container for easy deployment.

  
---
[Back to All Prototypes](../index.md)
