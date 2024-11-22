# 2024-UCSF-DSOS-Python-SQL-Fall-Workshops

Code and Data for the 2024 Fall Python/SQL fall workshop series at the UCSF Library

- [Intro to Python and SQL Part 1](#intro-to-python-and-sql-part-1)
- [Intro to Python and SQL Part 2](#intro-to-python-and-sql-part-2)
- [Python and Web APIs](#python-and-web-apis)
- [Image Audio and Video to Text Transcription with Python](#image-audio-and-video-to-text-transcription-with-python)
- [Python Background for Text Analysis and Natural Language Processing](#python-background-for-text-analysis-and-natural-language-processing)
- [Document Classification with Scikit-Learn](#document-classification-with-scikit-learn)
- [Document Topic Modeling with Python](#document-topic-modeling-with-python)
- [Classification Sentiment Analysis and Topic Modeling using Cloud Based APIs](#classification-sentiment-analysis-and-topic-modeling-using-cloud-based-apis)


## Intro to Python and SQL Part 1 
(10/4/24)

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


## Intro to Python and SQL Part 2 
(10/11/24)

In this workshop, we produced three notebooks.

### Covid_Mock_Data.ipynb

We created this document to illustrate how to create a mock dataset that is similar in structure to a real dataset. This can be useful when providing sample data for collaborations or testing when the original dataset can't be shared (due to size, security, or other constraints). Specifically, we used Generative AI to generate code for creating a pandas dataframe that closely matches the Covid data from Carbon Health. 

### Covid_Queries.ipynb

In his workbook, we downloaded all Covid testing data from carbon health, created a pandas dataframe, and used SQL to create queries reporting on the frequency of different symptoms with positive or negative covid tests. We created this notebook on google colab, so you will see the AI prompts we used to create queries and describe visualizations.

### Covid_Queries_Local.ipynb

We created this notebook locally with Jupyter Notebook through Anaconda Navigator. It contains code for installing pandasql, reading a csv file into a pandas dataframe through a web url, and creating various analytical queries on the covid testing dataset from Carbon Health. 

## Python and Web APIs
(10/18/24)

In this workshop, we created four notebooks to investigate how to work with Python Dictionaries to query and parse JSON data from Web APIs. We used the API from the National Library of Medicine's RXNorm database and the Industry Documents Library SOLR based web service for searching documents.

### Python-Dictionaries.ipynb
We created this notebook to illustrate the drawbacks of using lists or dataframes for storing data based on key/value pairs, and created a dictionary to hold the caffeine content of different beverages in a table from the Mayo Clinic page. 

### Caffeine-Dictionary.ipynb
We created this notbook on google colab to see how the generative AI coding assistant would translate the information on caffeine content into a dictionary. Interestingly, the data was largely but not completely accurate and contained information for beverages not listed on the Mayo Clinic page. 

### Web-API-Python.ipynb
In this workbook, we queried the National Library of Medicine's public API for information on prescription drugs and read the results into a JSON document that we converted into a python dictionary. We created a look to extract the synonyms listed for various drugs. We had the change to look into a deeply nested and fairly complicated JSON document. 

### Industry-Documents-API.ipynb
We created this workbook on google colab. We queried and parsed information from the Industry Documents Library API, and used generative AI to parse and extract data. 

## Image Audio and Video to Text Transcription with Python
(10/25/24)

In this workshop, we wrote Python Code using Google Colab to extract transcripts from image and video files on the Industry Archives.

### Py_Tesseract_OCR.ipynb
We used this notebook to use py-tesseract to extract code from a PDF file hosted on the industry archives. We tried out a few different files.

First, we searched on "avocado" and used some pdf scands of printed material that led to high quality, high accuracy transcriptions using tesseract.
If you'd like to try this, go to https://www.industrydocuments.ucsf.edu and search on "avocado" (the IDL team told me they often use this to test search, as avocados have some chemical properties in common with tobacco). 

Note: 11/5/24 - I had it wrong about avocado, it's eggplant! Rachael Taketa who works with the IDL archive did a metadata presentation yesterday and talked about this - evidently eggplants also contain niccotine. 

For a test file, we used "Henry Avocado Recalls Whole Avocados Because Of Possible Health Risk" 
https://www.industrydocuments.ucsf.edu/tobacco/docs/#id=sgfv0291
This file transcribed with high accuracy using tesseract. This is what we expected, as tesseract is widely used for transcribing printed, typeset material in images.

Next, we tried some other handwritten files and people in the class tried searchign the archives and proposing handwritten messages to test. This one posed a particularly difficult challenge for tesseract (cursive, and rotated sideways!)
https://www.industrydocuments.ucsf.edu/tobacco/docs/#id=jjvy0083

Unfortunately, we weren't able to get a good transcription from this using tesseract, but we were able to get a partial transcript using Google Document AI (below). 

### Doctr_Ocr.ipynb
We didn't use this specific OCR tool during the workshop, but you might be interested in trying it or other OCR Tools. I found that it is similar to Tesseract in that it is effective with printed text but doesn't perform very well with handwriting. 

### Google Demo API

Google offers a cloud based API for video and image transcription, but you need a paid account to use the programming API. However, there is a demo form available that will accept single image or pdf file uploads available at: 
https://cloud.google.com/use-cases/ocr

We tried the cursive, lined, sideways rotated image from https://www.industrydocuments.ucsf.edu/tobacco/docs/#id=jjvy0083 (where we couldn't get a good transcription using tesseract). The reults were good enough to be useable - and remember, this is an unusually difficult transcription. Here's the result - feel free to compare to the original on the IDL site. 

*Janise 1996
m. Pa
Clay Live
Dear Sivi
This
is an I owe you letter
because if you can take time
to read my complaining letter
and do something about it, this
letter is then pristified
Deeling my stadiving
blanket a few wicke
curate ales received that lame
week the "after" for the solem
Lighter" which I also promptly
filled gut and sent.
very next.
The blanket is ver
it's grew into my case, t
hope I never need it but if I ds
it's there. Thank you, now
Сан
at imagine other also
recured my lighter Ipent my
offer in inden 10-96 and*

(note - this was only the first page of the file)

A big challenge at the Library is knowing when to use the more expensive, computationally expensive transcription technology for OCR. An additional challenge is that many documents have a combination of printed and cursive or handwritten text, making it difficult to know when we are losing data. Although we can tell the difference between pure handwriting and pure typeset, documents that mix the two remain more difficult to identify. 

### Whisper_AI_Transcription.ipynb
After image based OCR, we moved on to video-to-text transcription. For this, we used Whisper, an open source product from OpenAI. Whisper is also available as a web based API (paid service), but the open source version delivers high quality high accuracy transcription for video and audio files.

For a test transcription demo, we used a file from the Industry Archives, a collection of industry-produced "anti-smoking" ads from the late 1990s and early 2000s. Because video-to-text transcription can be computationally expensive, we also reviewed how to change the run environment in google colab to use GPU processors. This did substantially reduce the processing time. We also investigated the difference between large, small, tiny pre-trained language models to transcribe speech.

One interesting result is that some of the larger language models repeated phrases that weren't evidently present in the video. Hard to know why - it could be hallucination from the AI system, though one participant raised the possibility that larger models might pick up on background music. I listened carefully to the video again and didn't hear any of these phrases, but it's still possible that the larger more powerful models are attempting to transcribe musical notes into words while smaller models just ignore it (this is a guess, I don't really know). 

## Python Background for Text Analysis and Natural Language Processing 
(11/1/24)

This workshop covered programming techiques for cleaning and preparing text data for machine learning and natural language processing projects.
Much of the material for this week's workshop is available in:

* https://github.com/geoffswc/Document-Classification
* https://github.com/geoffswc/Machine-Learning-NLP-Prep

In this workshop, we produced two notebooks.

### Single-Text-Document.ipynb

For the first part of the workshop, we worked with a single string, a short bit of text we copied from the economics entry on wikipedia:
* https://en.wikipedia.org/wiki/Economics

We removed all non-alphabetical characters, removed stop words, enforced lower case capitalization, then stemmed and lemmatized the word collection.
We also reviewed techniques for creating new lists in a loop python methods for breaking a string into words (tokenization) and reassembling a list of words back into a passage of text (joining). 

We also emphasized that cleaning text isn't a standard process. While there are common techniques and procedures, the decision of what to keep and what to remove from a dataset (text or otherwise) and how to do this is a decision for the researcher/analyst working with a dataset. You can introduce bias into your dataset through cleaning, so it's always important to consider how you are cleaning text and what decisions you're making as you do this.

### Multiple-Document.ipynb

For the second part of the workshop, we applied the same techniques we used for a single string to clean a column of text data in a pandas dataframe.

For data, we used a collection of opiod documents from the washington post, hosted in the Industry Documents Library.
* https://ucsf.app.box.com/v/IDL-DataSets/file/780928732201

## Document Classification With Scikit Learn

In this workshop, we created/reviewed three workbooks to investigate the use of machine learning to classify documents.

### Example-Classification-Set-DefaultDict.ipynb

This workbook introduced a new (for this series) data structure called a *set*. A set is an unordered collection of unique objects (in this case, unique words). We used this to create a "bag-of-words" model, a collection of the unique words in an entire dataset. Although we won't be mangually creating a set because scikit-learn will handle this for us, it's a useful concept and a data structure you'll want to be familiar with as a programmer. 

### Simple-Classification-Scikit-Learn.ipynb

In this workbook, created two very short movie reviews by hand, then created and applied a random forest classifier to train a machine learning model to 1) evaluate the impact of different words on why a model might predict a positive or negative movie review, and 2) predict the positive or negative sentiment of a new movie review not used in the training of the model.

### Sentiment-Pipeline-Example.ipynb

Eventually, code gets too verbose and complicated for us to type everthing, so we downloaded a code base from github, loaded it into jupyter notebook through anaconda, and ran/reviewed code. This workbook uses a larger movie review dataset to train and evaluate a machine learning model designed to assess the language and sentiment of movie reviews. To access this workbook and the data required to run it, see the github repot at:

https://github.com/geoffswc/Document-Classification

## Document Topic Modeling with Python

In this workshop, we continued to investigate document classification. Last week, we explored supervised machine learning, this week, we explore unsupervised machine learning and topic modeling through hands-on programming with scikit-learn.

As with supervised machine learning, there are a number of different algorithms for document classification. Although the scikit-learn api makes it relatively simple to swap them out, the underlying mathematics are very different, and different algorithms produce different artifacts that may be useful to analyse how the machine learning model classifies documents. For this workshopm, we'll use Latent Dirichlet allocation (the github repository also contains code for using kmeans clustering, but we will stick with LDA for this workshop). 

## Workbooks

Most of the documentation and workbooks for this workshop are available in:

https://github.com/geoffswc/YouTube-Transcript-Python

### Algorithms and Math

These workshops emphasize hands on programming rather than theory or algorithms, so our discussion of the mathematics behind LDA will be minimal. I encourage you to read about this (and other algorithms). The scikit-learn documentation itself is very thorough and readable. For a high level overview, I found this summary of LDA to be useful.

https://www.tidytextmining.com/topicmodeling

You may notice this link is from a topic tutorial using R, which is widely used along with Python for data science. For now, you can stick to reading the overview for how LDA works, the implementation in different programming languages will be similar (though not necessarily identical!) 

## Classification Sentiment Analysis and Topic Modeling using Cloud Based APIs

In this workshop, we reviewed a few different methods for accessing pre-trained classification and sentiment analysis models. The first technology, Google Cloud API, was presented as a demo as it requires a paid account. The next two, VADER and HuggingFace, involved hands-on coding in Google Colab, though these workbooks should run locally through Jupyter Notebook on your local machine as well.

### HuggingFaceClassifier.ipynb

In this colab workbook, we used HuggingFace to classify legal and advertising documents form the Industry Documents Library. This workbook uses a "Zero Shot Classifier", an approach that allows a model to assess classification probabilities for categories that were not part of the training set:

https://huggingface.co/tasks/zero-shot-classification

### VaderTest.ipynb

In this colab notebook, we use VADER to estimate the sentiment and magnitude for movie reviews (the same dataset we used last week when we trained a custom model). 

https://github.com/cjhutto/vaderSentiment

We discussed that VADER was trained on social media data, and that this may not provide the best model for assessing whether a movie review is positive or negative. Here's a link for how to customize HuggingFace to assess the sentiment for movie reviews based on the imdb dataset (I haven't looked into this yet, it might be a good topic for a future group coding meetup). 

https://huggingface.co/docs/transformers/en/tasks/sequence_classification

### Predict_Text_Sentiment_And_Category.ipynb

This workbook was presented as a demo, as it relies on a paid service. This workbook calls Google's Cloud based language API to assess the sentiment and magnitude of a passage of text, and identify the probability that it is associated with different topics. This workbook is available in a different repo:

https://github.com/geoffswc/GCP-Auto-AI-Workshop/blob/main/Predict_Text_Sentiment_And_Category.ipynb


















