===================================================
Learning Representations for Time Series Clustering - Retail application
===================================================


.. image:: https://img.shields.io/pypi/v/dtcr.svg
        :target: https://pypi.python.org/pypi/dtcr

.. image:: https://img.shields.io/travis/GabrielFritz/dtcr.svg
        :target: https://travis-ci.com/GabrielFritz/dtcr

.. image:: https://readthedocs.org/projects/dtcr/badge/?version=latest
        :target: https://dtcr.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status




Applying DTCR to retail problems


* Free software: MIT license
* Documentation: https://dtcr.readthedocs.io.

First steps (due to May 15th)
-----------

1. Build a project proposal containing:
    1. **Project title:** Applying DTCR to retail: An unsupervised approach for customer segmentation;
    2. **Project category:** Unsupervised learning;
    3. **What is the problem that you will be investigating? Why is it interesting?** I'm investigating how to leverage from time series data from customers without having to calculate summaries of this data, which often leads to less informative segments. This is interesting because it possibly allows better customer segmentation, and, with that, better marketing strategy, better stock management, better growth strategies.
    4. **What are the challenges of this project?** The challenges of this project is to implement a SOTA paper and, after that, adapt the algorithm to better fit the retail context.
    5. What dataset are you using? How do you plan to collect it? First, to develop the model, I will be using one dataset from http://timeseriesclassification.com/ . After that, I will refine the model using the Instacart retail dataset: https://www.kaggle.com/c/instacart-market-basket-analysis
    6. **What method or algorithm are you proposing? If there are existing implementations,   will you use them and how? How do you plan to improve or modify such implementations?**
    I will be using the DTCR algorithm proposed in the paper inside the `docs/` folder, which doesn't have an available implementation. I plan to improve this algorithm for customer segmentation problem, which might be done by changing the clustering algorithm, the generative strategy, the encoder decoder strategy, or the loss function.
    7. **What reading will you examine to provide context and background? If relevant, what papers do you refer to?** I will do a extensive study of the DTCR paper and study the papers that performed better than DTCR in other datasets.
    8. **How will you evaluate your results? Qualitatively, what kind of results do you expect (e.g. plots or figures)? Quantitatively, what kind of analysis will you use to evaluate and/or compare your results (e.g. what performance metrics or statistical tests)?** Quantitative - Normalized Mutual Information
Qualitative - Time series comparisons, check for detection of anomalous behavior.

Project map (due to May 30th)
------------

1. Identify at least one dataset;
2. Build dataloader for dataset;
3. Build baseline model;
4. Start writing about project (at least 2 pages);
5. Automatic EDA methodology on dataset;
6. Describe the task;
7. Describe how I will apply the paper techinique to retail context

Features
--------

* TODO

Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
