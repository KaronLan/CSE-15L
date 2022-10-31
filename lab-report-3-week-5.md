**grep**

`grep -l`: it list all the file names of what ever grep finds. 

`$ grep -l "emergency" technical/*/*.txt`<br/>
result:
```
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-3.txt
technical/911report/chapter-6.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
technical/biomed/1471-2334-3-11.txt
technical/biomed/1471-2350-3-7.txt
technical/biomed/1471-2377-3-4.txt
technical/biomed/1471-2458-1-9.txt
technical/biomed/1471-2458-3-20.txt
technical/biomed/1472-684X-2-2.txt
...
technical/biomed/rr37.txt
technical/plos/journal.pbio.0020121.txt
technical/plos/journal.pbio.0020263.txt
technical/plos/pmed.0020034.txt
technical/plos/pmed.0020059.txt
technical/plos/pmed.0020065.txt
technical/plos/pmed.0020140.txt
```
This command is printing all the text file names that contains the word "emergency" in `technical/`.<br/>
It is very helpful because `grep "emergency" technical/*/.txt` prints about five pages of contents and is very hard to read.<br/>
Thus by only printing the file name, it will be easier to find out what files contains our target.<br/>

`$ grep -l "what" plos/*.txt`<br/>
result:
```
plos/journal.pbio.0020001.txt
plos/journal.pbio.0020010.txt
plos/journal.pbio.0020012.txt
plos/journal.pbio.0020028.txt
plos/journal.pbio.0020040.txt
...

plos/pmed.0020226.txt
plos/pmed.0020232.txt
plos/pmed.0020246.txt
plos/pmed.0020249.txt
plos/pmed.0020258.txt
plos/pmed.0020272.txt
```
This command is printing all the text file names that contains the word "what" in `technical/plos`.<br/>
I went into the directory to look for "what" specifically in plos directory.
It is useful because I am only looking for the file names, and do not care about the sentences in the files.<br/>
This command line options eliminate the time it takes for the terminal to print out the content and also my time to read.<br/>

`$ grep -l "emergency" plos/*.txt`<br/>
result:
```
plos/journal.pbio.0020121.txt
plos/journal.pbio.0020263.txt
plos/pmed.0020034.txt
plos/pmed.0020059.txt
plos/pmed.0020065.txt
plos/pmed.0020140.txt
```
This command is printing all the text file names that contains the word "emergency" in `technical/plos`.<br/>
It makes it very easy to save those file names into a file and make use of the information.<br/>


