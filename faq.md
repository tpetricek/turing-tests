---
layout: page
title: FAQ
permalink: /faq/
---

## How do I submit a new challenge?

1. Clone <https://github.com/alan-turing-institute/turing-tests>. 
2. Switch to the `gh-pages` branch.
3. Add a new post in the `_posts` directory (see any existing post for an
   example).
4. Place your data somewhere publicly accessible (or get in touch with us if you
   would like us to host it). Make sure the data is organised as described below.
4. Submit a pull request.


## What is the format of the dataset submission?

Please submit your data as a single `zip` file with the following directory
structure:

    .
    |-- data/
    |   |-- raw/
    |   |-- clean/
    |   |-- gold/
    |-- doc/
    |-- README
    |-- LICENCE
    |-- CHANGELOG

The file `LICENCE` should contain the license under which the data is made
available (or a link to it) together with any copyright notices. The file
`README` should contain at least a description of the source of the
data. `CHANGELOG` is a a reverse-chronological description of changes to the
dataset.

`data/raw` is for the data in its “rawest“ form. It may be that this is the only
form in which data is provided. Otherwise, `data/clean` is for data that has
been processed to make it easily readable by standard software (eg, `R`).
Finally, `data/gold` is for a comparison dataset that does not contain “errors”:
for example, if the challenge is to identify the same record in different files,
then this directory should contain correctly matched records.

`doc` is for explanations.

Empty directories do not need to exist. All other structure is up to you. In
later versions, we may adjust this format to allow greater automation of the
analytical process.


## What information is required?

There are two questions your description should answer:

1. What is this data?

   Please explain your dataset.

   We want to make it as easy as possible for researchers to get to grips with
   the data -- even when the challenge is itself to make sense of the data. It
   will help enormously if you describe as much as possible of the background
   and context to the data: How was it obtained? How was it generated? What does
   it mean?

2. What do you want to do with it?

   Please say, as precisely as possible, how to measure “success” for your
   particular challenge.

   These challenges are rather like “unit tests” for machine learning. That is,
   we want to test and compare our ideas by applying them to real-world
   challenges. To do so it’s important to be able to evalulate any given answer
   by comparing it to a known answer or, at the least, to other possible
   answers.
   
   
## Can I share my confidential / top secret data?

   Well, that is up to you. However, at the moment, we do not have a mechanism
   for securely making data from this website available only to our researchers.
   We would prefer that all Turing Test submissions contain only data that has
   been made public.
   
   As an alternative, we would be happy to accept synthetic datasets.
   
   Please feel free to contact us if you would like to discuss making
   condidential data available to our researchers.
   
   
