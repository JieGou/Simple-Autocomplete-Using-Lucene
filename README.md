# Simple Autocomplete Using Lucene

## Introduction

This project consists in a system, developed using C# and Lucene.NET, that indexes single words and their weights (frequency of use), providing very fast and ordered suggestions, based on prefix and similar words and according to their weight, much like the functionality of smartphones' suggestions when typing.
At first, the project was developed in a private version control system, but it was decided afterwards to make it public, that's the reason for a single commit.
This project as it is, is going to be integrated with another project developed by me and a fellow researcher, that can be found [here](https://github.com/vitox761/IC) (lacks proper documentation)

## Features
* Saves words with weights according to their frequencies of use
  * Adds new words to an index
  * Increments the weight of an indexed word when it's inserted again
* Index words from user input or text files (.txt)
* Retrieves, from a set of characters (user input), words that contain such characters as their prefix
* Retrieves, from a set of characters (user input), words that are similar to the one in course of typing
* Enumerates suggestions to a given prefix (retrieved the previously populated index) from the highest weight to the lowest
* Highly efficient
  * No delay in searching and indexing words in a full populated index base (~140000 words) 
  * Lightweight (consumes aprox. 30-50MB RAM and Disk)
  * With an index built by a single user (the most common words written are "heavier"), preliminar tests proved a gain of up to 40% increase in his typing speed.
* The weights are normalized periodically, decreasing all the weights and mantaining the more recently used words always in evidence
* It doesn't need internet connection (autocomplete features can be integrated in apps through online services, this is an internet independant implementation)

## How does it work?

The following items are prerequisites for understand this section:
* Lucene project general idea
* Indexing and Retrieving information with Lucene
* Lucene's File System Directory and RAM Directory

I would recommend [this article](http://www.codeproject.com/Articles/320219/Lucene-Net-ultra-fast-search-for-MVC-or-WebForms) related to [this repository](https://github.com/mikhail-tsennykh/Lucene.Net-search-MVC-sample-site) to clarify the main functionalities of Lucene, noting that I used it myself as a starting point to develop this very project.

Further documentation to be added...







