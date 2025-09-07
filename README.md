# Web Scraping and XML Data Integration Engine for Country Information

## Description

This project showcases a robust Java application engineered to perform web scraping from diverse online sources to gather detailed country information. The collected data is then structured and integrated into a unified XML database. This application serves as a practical demonstration of data extraction, web scraping techniques, and advanced XML data management.

The core of the application lies in its "Wrappers," which are custom-built components designed to target specific websites, extract relevant information using regular expressions, and process it. The application is complemented by a Java Swing GUI, allowing users to interact with the collected data, perform complex queries, and generate various outputs.

This project is an excellent portfolio piece for showcasing skills in data integration, web scraping, and backend development to potential employers and recruiters.

## Key Features

* **Web Scraping & Data Extraction**:
    * Utilizes custom wrappers to scrape data from multiple, heterogeneous web sources.
    * Employs regular expressions to parse HTML and extract specific data points such as population, area, capital city, president, and more.
    * Integrates the scraped data into a structured XML format.

* **XML Data Management**:
    * Loads and displays country and factual data from the generated XML files (`paises.xml` and `factos.xml`).
    * Provides functionalities to add, remove, and modify country data directly through the application's interface.
    * Ability to reset the XML database, triggering the web scraping process to rebuild it from scratch.

* **Advanced Querying and Transformation**:
    * **XPath & XQuery**: Enables powerful queries to search and filter the integrated data. Users can find countries based on various criteria like continent, currency, language, or population metrics.
    * **XSLT**: Transforms the XML data into user-friendly formats, including:
        * HTML pages to display country flags and information.
        * TXT files for simple data listings (e.g., countries, capitals).
        * New XML documents based on specific queries (e.g., the top 5 most populous countries).

* **Data Validation**:
    * Ensures data integrity by validating the XML files against DTD and XSD schemas.

## Technologies Used

* **Core Language**: Java
* **Web Scraping**: Custom HTTP request handling and HTML parsing with Regular Expressions.
* **Data Format**: XML
* **XML Processing APIs**: JDOM2, Saxon
* **Query Languages**: XPath, XQuery
* **GUI**: Java Swing
* **Build Tool**: Maven

## How It Works

1.  **Data Scraping**: The application initiates HTTP requests to predefined websites containing country information.
2.  **Wrapping and Parsing**: The HTML content is processed by dedicated "Wrapper" classes. Regular expressions are used to pinpoint and extract the required data fields.
3.  **XML Integration**: The extracted data is then used to construct two main XML files: `paises.xml` (general country information) and `factos.xml` (detailed facts and statistics).
4.  **User Interaction**: The Java Swing GUI provides a menu-driven interface for the user to interact with the XML database, allowing for data manipulation, querying, and transformation.

## Setup and Installation

1.  **Prerequisites**:
    * Java Development Kit (JDK) 21 or newer.
    * Apache Maven.

2.  **Clone the repository**:
    ```bash
    git clone <your-repository-url>
    ```

3.  **Navigate to the project directory**:
    ```bash
    cd <project-directory>
    ```

4.  **Build and run the application**:
    ```bash
    mvn clean install
    mvn exec:java
    ```

## Usage

Once the application is running, use the top menu bar to access its features:

* **Principal**: Reset the database (re-scrape all data) or exit.
* **XML**: View the raw XML files or add/remove/modify country data.
* **XPATH**: Execute powerful searches on the integrated data.
* **Validar**: Validate the XML data against its schemas.
* **XSLT**: Generate different output formats from the XML data.

All results from queries and transformations are displayed in the main text area of the application.
