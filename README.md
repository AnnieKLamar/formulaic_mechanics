# Formulaic Mechanics

### Created by Annie K. Lamar, and submitted as part of her dissertation project, "Formulaic Mechanics" (Stanford University, 2024)

## Introduction

The creation of an open-source codebase and the many datasets produced in the above chapters represents a significant component of this project. Some of the functions that this codebase provides are truly novel; they are, to my knowledge, the first computational attempt at a given problem. All the computational work related to mutual expectancy falls into this category. Other functions are novel in their accessibility. 

Notably, the TLG prohibits the copying or downloading of the text results from their database. With this codebase, you can perform almost all the same functions that the TLG provides (although only for Homer, and without lemmatization), and you are free to download and use the results in any manner you wish. Notably, the TLG does not provide a way to filter results by metrical pattern or degree of formulaic language—those abilities are unique to this project.

I want this code to be downloaded and used by any researcher for whom it is helpful. I also strove to make this codebase accessible to researchers with little or no programming experience. First, all the datasets are available as .csv files that can be loaded into an external platform like Excel; there is no need to touch the code at all to use much of this data. Second, I have provided both an interactive Jupyter notebook with many code snippets already written where a Classicist with minimal effort can simply switch out line numbers or text names to obtain results. Third, the codebase is heavily commented and accompanied by a technical documentation website. Beginning programmers can easily work with the code.

## Download & Installation

To download this package directly from GitHub:

`git clone https://github.com/AnnieKLamar/formulaic_mechanics`

You can also install this package using pip:

`pip install formulaic_mechanics`

### Dependencies & Requirements

The following non-native Python packages are required:
- `pandas`
- `scipy`
- `statsmodels`
- `lexical-diversity`

## Quickstart

Almost all the code in this package is built to work with, on, or within a Corpus object. The `Corpus` class is defined in the file formulaic_mechanics.py. To instantiate a `Corpus` object, you can simply run this line of code:

`Corpus = Corpus()`

Instantiating a Corpus object should take less than a minute if you downloaded all the data files (in the /data folder) along with the code. In the case that the data is already available, you will be notified as each dataset is loaded. You will see the following appear in your console or IDE:

`Bigram frequencies loaded.`

`Bigram expectancies loaded.`

` … `

`Proper noun statistics loaded.`

`Repeated line sets loaded.`

If you did not download the data folder, `Corpus` object instantiation will also go through the process of 
recreating most of the datasets described below. This could take hours or days depending on the computational power 
of your machine. Each dataset creation process will also print progress update statements. By default, the data 
folder is included in the pip installation process.