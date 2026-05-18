.. image:: https://img.shields.io/badge/tstn--063-lsst.io-brightgreen.svg
   :target: https://tstn-063.lsst.io
.. image:: https://github.com/lsst-tstn/tstn-063/workflows/CI/badge.svg
   :target: https://github.com/lsst-tstn/tstn-063/actions/

#####################################################################################################################
The Nightly Digest: an integrated dashboard for monitoring and contextualizing the progress of observatory operations
#####################################################################################################################

TSTN-063
========

As the Vera C Rubin Observatory moves towards starting the Legacy Survey of Space and Time (LSST), it is imperative to provide an integrated logging platform to serve Rubin staff and the scientific community so they may monitor daily operations. We have developed a solution to fulfill this need: the Nightly Digest. The Nightly Digest displays a dashboard of high-level performance metrics to understand how we spent observation time and our progress in the survey. Supporting pages integrate monitoring data including observer remarks, exposure metadata, and telemetric data to enable a wide view of nightly operations. The Nightly Digest is deployed in Phalanx to leverage authentication, authorization, and data services for secure operations. Its FastAPI backend supports asynchronous ingestion of heterogeneous data sources while reducing and caching metrics for efficient retrieval. The Nightly Digest has been developed and deployed and continues to be improved as we add features with stakeholder feedback. We present our current modern web application to enable efficient nightly operations.

Links
=====

- Live drafts: https://tstn-063.lsst.io
- GitHub: https://github.com/lsst-tstn/tstn-063

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-tstn/tstn-063

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the `acronyms.tex` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
