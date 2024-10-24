# 2024-UCSF-DSOS-Python-SQL-Fall-Workshops

Code and Data for the 2024 Fall Python/SQL fall workshop series at the UCSF Library

## Intro to Python and SQL, Part 1 (10/4/24)

In this workshop, we produced two notebooks

### Python_SQL_Day_1.ipynb

We created this notebook using Google Colab, but it should work if you open it with Jupyter Notebook on your laptop or workstation. This notebook contains to read a CSV file containing Covid testing data from Carbon Health into a pandas dataframe. 

Some of the code in this notebook was generated through Colab's AI coding assistant. We will continue to use this tool throughout the workshop series. You can identify code that was AI generated through the prompt, which is added at the start of the code cell with the text "#prompt:" prepended to the instructions issued to the AI asstant. 

For more information on this data set, see: https://covidclinicaldata.org


### Oregon-Sugar-Document

We created this document using Jupyter Notebook running locally. This notebook demonstrates how to load text data in a tab-delimited format into a pandas dataframe. We downloaded the "Oregon Sugar Document" from the UCSF Industry Documents Library. This dataset contains prepared dataset text extracted through OCR from scanned image and pdf files. You may notice that some documents are more accurately transcribed than others, and some documents have a large amount of non-alphanumerical characters that result from attempts to transcribe images, handwriting, or other difficult-to-translate artifacts of a document. Note that this document was produced a few years ago, and more recent (though also more expensive) transcription technologies are now able to transcribe handwriting, cursive, and text within images much more accurately.

To browse the Industry Documents Library, see: https://www.industrydocuments.ucsf.edu

To access the Oregon Sugar Document prepared dataset, see: https://www.industrydocuments.ucsf.edu/research-tools/api/
(follow the link to "data sets" - you may need to scroll to find it. I'll be easier if you sort by file size in ascending order). 


## Intro to Python and SQL, Part 2 (10/11/24)

In this workshop, we produced three notebooks.

### Covid_Mock_Data.ipynb

We created this document to illustrate how to create a mock dataset that is similar in structure to a real dataset. This can be useful when providing sample data for collaborations or testing when the original dataset can't be shared (due to size, security, or other constraints). Specifically, we used Generative AI to generate code for creating a pandas dataframe that closely matches the Covid data from Carbon Health. 

### Covid_Queries.ipynb

In his workbook, we downloaded all Covid testing data from carbon health, created a pandas dataframe, and used SQL to create queries reporting on the frequency of different symptoms with positive or negative covid tests. We created this notebook on google colab, so you will see the AI prompts we used to create queries and describe visualizations.

### Covid_Queries_Local.ipynb

We created this notebook locally with Jupyter Notebook through Anaconda Navigator. It contains code for installing pandasql, reading a csv file into a pandas dataframe through a web url, and creating various analytical queries on the covid testing dataset from Carbon Health. 

## Python and Web APIs, Part 1 (10/18/24)

In this workshop, we created four notebooks to investigate how to work with Python Dictionaries to query and parse JSON data from Web APIs. We used the API from the National Library of Medicine's RXNorm database and the Industry Documents Library SOLR based web service for searching documents.

### Python-Dictionaries.ipynb
We created this notebook to illustrate the drawbacks of using lists or dataframes for storing data based on key/value pairs, and created a dictionary to hold the caffeine content of different beverages in a table from the Mayo Clinic page. 

### Caffeine-Dictionary.ipynb
We created this notbook on google colab to see how the generative AI coding assistant would translate the information on caffeine content into a dictionary. Interestingly, the data was largely but not completely accurate and contained information for beverages not listed on the Mayo Clinic page. 

### Web-API-Python.ipynb
In this workbook, we queried the National Library of Medicine's public API for information on prescription drugs and read the results into a JSON document that we converted into a python dictionary. We created a look to extract the synonyms listed for various drugs. We had the change to look into a deeply nested and fairly complicated JSON document. 

### Industry-Documents-API.ipynb
We created this workbook on google colab. We queried and parsed information from the Industry Documents Library API, and used generative AI to parse and extract data. 

## Image, Audio, and Video to Text Transcription with Python

### Doctr_Ocr.ipynb
Google Colab notebook, demo OCR open source tool doctr_ocr

### Py_Tesseract_OCR.ipynb
Google Colab notebook, demo OCR open source tool py-tesseract

### Whisper_AI_Transcription.ipynb
Google Colab notebook, demo Whisper AI video/audio transcription

### Google Demo API
https://cloud.google.com/use-cases/ocr



