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


## Intro to Python and SQL, Part 2 (10/4/24)

In this workshop, we produced three notebooks.

### Covid-Mock-Data.ipynb

We created this document to illustrate how to create a mock dataset that is similar in structure to a real dataset. This can be useful when providing sample data for collaborations or testing when the original dataset can't be shared (due to size, security, or other constraints). Specifically, we used Generative AI to generate code for creating a pandas dataframe that closely matches the Covid data from Carbon Health. 

### Covid-Queries.ipynb

In his workbook, we downloaded all Covid testing data from carbon health, created a pandas dataframe, and used SQL to create queries reporting on the frequency of different symptoms with positive or negative covid tests. 




