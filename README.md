# thesisChecker
A python tool for checking the copy ratio of a manuscript. 
- Before running the tool, two inputs are required, one is your PDF manuscript and the other is the folder where the reference paper to be compared is located.

Dependency
--------

MSearcher's code is written use python3.6 on Ubuntu(16.04) system.
* Python > 3.6:
	* PyPDF2
	* sklearn
* Support systems:
	* Linux
	* Windows
	
Usage
-----
The main script in this tool is `calculate_sentences_distance.py`. 
```
usage: calculate_sentences_distance.py [-h] [--dbdir DBDIR] [--cutoff CUTOFF] [--maxnum MAXNUM] [--minlen MINLEN] [--prefix PREFIX] [--output OUTPUT] query_papers [query_papers ...]

Give a PDF paper as input

positional arguments:
  query_papers

optional arguments:
  -h, --help            show this help message and exit
  --dbdir DBDIR, -d DBDIR
                        database paper directory
  --cutoff CUTOFF, -c CUTOFF
                        cutoff value of similarity (default: 0.20)
  --maxnum MAXNUM, -m MAXNUM
                        max number of the highest sentences (default: 5)
  --minlen MINLEN, -l MINLEN
                        min length of the sentence (default: 10)
  --prefix PREFIX, -p PREFIX
                        prefix name of the output file (default: similar_ratio)
  --output OUTPUT, -o OUTPUT
                        output directory (default: ./) 
                                                                                                                                                                                                             
```

Example
------

```
python calculate_sentences_distance.py --dbdir=.\example\Paper .\example\query_paper.pdf

```
