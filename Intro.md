# Extraction of facial features by using Gabor filter #

This is a school project. No cool people allowed. :D

We have used Gabors filter for extracting facial features for use in face recognition task. An achived accuracy on used data set is 94.7%. We have used SVM as a classifier and commercial data set with about 4000 images and 500 classes (different human faces) (data set was given to us (already normalized, in `.nrm` format), we do not know its origin).

Mean problem of using Gabor filters is selection of good parameters. For quick overview of Gabor filters and parameter selection (Gabor filter design) problem we suggest visiting the site:
http://matlabserver.cs.rug.nl/edgedetectionweb/web/edgedetection_params.html

Documentation for the project is in the directory `doc`. It is written in Croatian language.

Used data set is not available for public. Images in data set are in `.nrm` format and they were normalized before use.

We have used LibSVM as a classifier. It is available from: http://www.csie.ntu.edu.tw/~cjlin/libsvm/

## HOWTO install ##
Project is implemented in Python language, therefore source code can be executed with Python interpreter.

## Dependency ##
You need to install:
  * Python (version 2.5 or newer) - http://python.org/
  * Module scipy - http://www.scipy.org/
  * Module numpy - http://numpy.scipy.org/
  * Module PIL - http://www.pythonware.com/products/pil/
  * LibSVM for Python - http://www.csie.ntu.edu.tw/~cjlin/libsvm/

## HOWTO run training ##
Training is done by `train.py` script.

**Example:**
```
bash-4.0$ python train.py -m ../lica.model ../data/*
Skipping non-nrm file ../data/readme.txt
Ukupno zadano 295 razreda uzoraka.
Ukupno zadano 2360 uzoraka.

Training libsvmclassifier classifier.
Done!
Model for libsvmclassifier classifier saved to: ../lica.model
```

Text output is partialy in Croatian language :).

## HOWTO run classification ##
Classification is done by `classify.py` script.

**Example:**
```
bash-4.0$ python classify.py -m ../lica.model ../data/006_4_2.nrm ../data/007_4_2.nrm ../data/008_4_2.nrm
Ukupno zadano 3 uzoraka.

Classifying by libsvmclassifier classifier.
../data/006_4_2.nrm is classified as 006
../data/007_4_2.nrm is classified as 007
../data/008_4_2.nrm is classified as 008
```

## HOWTO run evaluation ##
Evaluation is done by script `test.py`.

**Example:**
```
bash-4.0$ python test.py ../data/*
```

## Authors ##
  * Tomislav Reicher (project leader)
  * Krešimir Antolić
  * Igor Belša
  * Marko Ivanković
  * Ivan Krišto
  * Maja Legac
  * Tomislav Novak