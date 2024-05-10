## GaTech-SEC EDGAR - Project by K.Satwik

### EDGAR

The US Securities and Exchange Commission (SEC) is responsible for maintaining the Electronic Data Gathering, Analysis, and Retrieval system (EDGAR), an online repository that was initially built in 1993. Its purpose is to automate the process of gathering, validating, and accepting submissions and announcements by companies that are legally required to do so. A compilation of data that was scraped from this repository is called the Edgar Schema. The tables in this database schema are made up of several main tables that contain the most basic data from EDGAR as well as several dependent tables that are typically created by scraping and cleaning data from filings and documents that are linked from the main tables, like the set of tables that list the information contained in the Form 3, Form 4, and Form 5 filings. 

### What is 10k fillings?
10-K is short for Form 10-K, which is a document the SEC requires all public companies to file each year. The form presents a financial picture of the company, detailing its revenues, assets, and liabilities for the previous year.

### TLDR Implementation
The following shows a high-level implementation that extracts and summarizes Item 1A, Risk Factors from Tesla’s 10-K filing filed in 2020, in 15 sentences.
<img width="767" alt="image" src="https://github.com/KSatwik/GaTech-SEC/assets/76058437/e20cab36-745a-4a58-a2ee-22ad17ea0d5a">

### Why 2 files parse_10K.py and GaTech_Sec.ipynb? 
The two files, `parse_10K.py` and `GaTech_Sec.ipynb`, serve different purposes and are used in distinct contexts, highlighting different aspects of working with SEC EDGAR 10-K filings.

#### 1. `parse_10K.py`

**Overview:**
- `parse_10K.py` is a Python script designed for parsing specific sections of SEC 10-K filings from provided links. It includes functions to extract text from these filings, particularly focusing on the Business Description, Business Risk, and Management Discussion & Analysis (MD&A) sections.

**Key Features:**
- **Functionality:** The script allows you to specify a link to a 10-K filing and a section identifier (0 for all sections, 1 for Business Description, 2 for Business Risk, 3 for MD&A).
- **Text Extraction:** It uses regular expressions (`re`) and BeautifulSoup (`bs4`) to scrape and extract relevant sections of the 10-K filings.
- **Error Handling:** The script includes error handling to manage unexpected issues during the extraction process.
- **Modularity:** Functions are encapsulated within the script, providing a modular approach to parsing 10-K filings programmatically.

**Insights and Use Cases:**
- **Automation:** `parse_10K.py` enables automation of the process of extracting specific sections of 10-K filings, which is valuable for researchers, analysts, and developers working with financial data.
- **Data Extraction:** It provides insights into the structure and content of 10-K filings, facilitating further analysis and processing of extracted text data.
- **Integration:** The parsed data can be integrated into broader applications or workflows for financial analysis, risk assessment, or natural language processing tasks.

#### 2. `GaTech_Sec.ipynb`

**Overview:**
- `GaTech_Sec.ipynb` is a Jupyter Notebook (`.ipynb`) file that demonstrates a comprehensive workflow using various tools and APIs to analyze SEC 10-K filings interactively.

**Key Features:**
- **API Integration:** The notebook showcases integration with external APIs such as OpenAI and sec-api for text summarization and data retrieval, respectively.
- **Text Processing:** It demonstrates text processing techniques using libraries like `spacy` for sentence tokenization and analysis.
- **Interactive Analysis:** The notebook provides an interactive environment for experimenting with different techniques and models (e.g., GPT-3 for text summarization).
- **Documentation and Visualization:** It includes documentation in Markdown cells, code explanations, and potentially visualizations to enhance understanding.

**Insights and Use Cases:**
- **Hands-on Exploration:** `GaTech_Sec.ipynb` allows users to explore and experiment with real-world data (SEC filings) using Python libraries and external APIs.
- **Educational Resource:** It serves as an educational resource for learning about data extraction, natural language processing (NLP), and financial analysis within a practical context.
- **Demonstration of Tools:** The notebook showcases the capabilities of specific tools (e.g., OpenAI's GPT-3) and APIs for text processing and analysis tasks.
- **Workflow Integration:** It illustrates how different components (text extraction, summarization, visualization) can be integrated into a cohesive analytical workflow.

#### Differentiation and Insights:

- **Functional Focus:** `parse_10K.py` is primarily focused on data extraction and parsing of 10-K filings, providing essential tools for working with financial text data programmatically. In contrast, `GaTech_Sec.ipynb` offers a broader exploration of data analysis techniques, leveraging APIs and libraries for interactive exploration and experimentation.
  
- **Practical Applications:** While `parse_10K.py` emphasizes modular functionality for specific tasks (e.g., text extraction), `GaTech_Sec.ipynb` demonstrates a more comprehensive and interactive approach to analyzing SEC filings, incorporating external APIs and showcasing real-world applications of NLP techniques.

- **Educational Value:** Both files contribute to understanding financial data analysis, but `GaTech_Sec.ipynb` particularly serves as a valuable educational resource, illustrating practical implementations and workflows for data-driven tasks in finance and NLP.

`parse_10K.py` and `GaTech_Sec.ipynb` complement each other by providing distinct perspectives and functionalities within the realm of SEC 10-K filings analysis, catering to different user needs and objectives in the field of financial data processing and exploration.

### What is your code about?
Incorporating Streamlit with financial analysis tools can provide several actionable insights for users in finance. Below are key insights that can be drawn and their practical applications, along with code snippets to showcase the implementation within a Streamlit app.

1. **Text Summarization for Efficient Analysis** Efficiently summarizes complex financial disclosures for quick analysis and decision-making and saves time and effort by focusing on critical points without reading entire documents.
2. **Section-specific Text Extraction for Targeted Analysis** Facilitates focused analysis on critical sections of financial disclosures relevant to investment decision-making and extracts key information related to business operations, risks, and management insights.
3. **Natural Language Processing (NLP) Insights for Enhanced Analysis** Gains insights into trends, sentiments, and relationships within financial text data for informed decision-making and identifies important entities (e.g., companies, financial metrics) and their contextual significance.

### Where is your frontend or app deployed?
I chose to use Streamlit to streamline my project and present it professionally, focusing on simplifying the user experience by allowing selection of company tickers via a web interface. However, unexpected personal challenges such as family issues and power outages due to rain hindered my progress. Despite these obstacles, I prioritized completing the backend tasks with thorough documentation. I apologize and appreciate your understanding.

### Why colab and what is the frontend? ( Task 2 )
Utilizing Google Colab provides a convenient environment for running Python code with access to GPU resources, making it suitable for machine learning and data analysis tasks. 

Streamlit offers an accessible approach to building interactive web applications directly from Python scripts, ideal for showcasing and sharing project outputs without requiring extensive frontend development knowledge. 

( I couldn't complete the same even with the extra time due to few family reasons and power cuts due to rains proof attached as a link (https://timesofindia.indiatimes.com/city/hyderabad/hyderabad-power-outage-after-heavy-rain-and-storm-damage/articleshow/109961474.cms); 

I know it sounds as an excuse but I tried my best to submit whatever I have done. Sorry and thank you for the opportunity )

### What could be added to improve the UI/UX and usability?
**1. Interactive Data Visualization:**

Graphs and Charts: Integrate plotting libraries like matplotlib or plotly to visualize key metrics extracted from SEC filings (e.g., financial performance over time, sentiment analysis results).

Word Clouds: Display word clouds to highlight frequently occurring terms in specific sections (e.g., Business Description, Risk Factors) for intuitive understanding.

**2. User-Defined Analysis Parameters:**

Dropdowns and Sliders: Implement interactive dropdown menus and sliders to allow users to customize analysis parameters (e.g., number of sentences for text summarization, sentiment analysis thresholds).

Filtering and Sorting: Enable users to filter and sort extracted data based on specific criteria (e.g., financial metrics, keywords).

**3. Integration with External APIs:**

Financial Data APIs: Integrate with external financial data APIs (e.g., stock market data) to enrich analysis and provide real-time insights.

Natural Language Understanding APIs: Utilize NLU APIs (e.g., Google Cloud NLP, IBM Watson) for advanced text processing and analysis.
