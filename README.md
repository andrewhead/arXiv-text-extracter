# arXiv-text-extracter
Scripts to extract text from the bulk data downloaded from arXiv.

## Requirements.

Note that this requires "progressbar". `https://pypi.python.org/pypi/progressbar`

## Basic file structure.

    Corpus/arXiv-text-extracter-master/Metadata
    Corpus/math  - intended output file
    Corpus/tar   - extracted tex files
    Corpus/arXiv-text-extracter-master/arXivExtractor  - all the py files
    Corpus/arXiv-text-extracter-master/metadata
    Corpus/arXiv-text-extracter-master/res
    Corpus/arXiv-text-extracter-master/TeXcount

## Basic usage.

These scripts are very sensitive to the exact directory structure (as might be expected).

Assume the project is in 

    ~/Documents/corpus/

Put the .tex files in `~/Documents/corpus/in` and expect the results in `~/Documents/corpus/out`.  Make sure both directories exist and are read/writable.  

Files will only be included if they have a `.tex` extension.

    cd ~/Documents/corpus/arXivExtracter
    python extractTextFromTex.py --output ~/Documents/corpus/out  ~/Documents/corpus/in

## Find only within one LaTeX environment

If you would like to only consider text which lies inside a LaTeX environment such as

    \begin{proof}
    The great and wonderful proof...
    \end{proof}

Then use the option `--restrict-class proof`.

## Unit tests.

The unit tests for the scripts are in 
