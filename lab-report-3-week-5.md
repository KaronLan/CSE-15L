**grep**

`grep -l`: it list all the file names of what ever grep finds. 
It is very helpful when we only need to know the files that contains our target instead of browsing through all the instances where the target appears.
It will really save us time. <br/>
`$ grep -l "what" plos/*.txt`
result:
```
plos/journal.pbio.0020001.txt
plos/journal.pbio.0020010.txt
plos/journal.pbio.0020012.txt
plos/journal.pbio.0020028.txt
plos/journal.pbio.0020040.txt
...
plos/pmed.0020146.txt
plos/pmed.0020155.txt
plos/pmed.0020158.txt
plos/pmed.0020162.txt
plos/pmed.0020189.txt
plos/pmed.0020191.txt
plos/pmed.0020200.txt
plos/pmed.0020206.txt
plos/pmed.0020209.txt
plos/pmed.0020210.txt
plos/pmed.0020226.txt
plos/pmed.0020232.txt
plos/pmed.0020246.txt
plos/pmed.0020249.txt
plos/pmed.0020258.txt
plos/pmed.0020272.txt
```
