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


`grep -l`: ignore case <br/>


`$ grep -i "emergency" technical/911report/*9*.txt`<br/>
result:
```
 Emergency response is a product of preparedness. On the morning of September 11,
                local public servants, especially the first responders: fire, police, emergency
                and exposed vulnerabilities in the World Trade Center's and the city's emergency
                to ensure safety, and elevators stopped. The public-address system and emergency
                Twin Towers. The 911 emergency call system was overwhelmed. The general evacuation
...
            Command was established at 9:41. At the same time, the Arlington County Emergency
                both sites will likely recur in any emergency of similar scale. The task looking
            Like the national defense effort described in chapter 1, the emergency response to
                911 operators and FDNY dispatch were not adequately integrated into the emergency
                disasters, it is important to integrate those taking 911 calls into the emergency
                would be "responsible for the management of the City's response to the emergency."
                by clearing emergency lanes to the WTC.
                emergency of this scale contributed to the early lack of units in the South Tower,
                not "responsible for the management of the City's response to the emergency," as the
            In May 2004, New York City adopted an emergency response plan that expressly
```
This command is printing out all the sentences containing "emergency", no matter if it is uppercase or lowercase.<br/>
It can be very helpful when we need any content related to the target. We wouldn't want to miss it because of case. <br/>


`grep -i -l "emergency" technical/*/*.txt`<br/>
result:
```
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
...
technical/biomed/cc300.txt
technical/biomed/cc303.txt
technical/biomed/cc713.txt
technical/biomed/cc973.txt
technical/biomed/cvm-2-1-038.txt
technical/biomed/cvm-2-6-286.txt
technical/biomed/rr37.txt
technical/plos/journal.pbio.0020121.txt
technical/plos/journal.pbio.0020263.txt
technical/plos/pmed.0010010.txt
technical/plos/pmed.0020034.txt
technical/plos/pmed.0020059.txt
technical/plos/pmed.0020065.txt
technical/plos/pmed.0020140.txt
```
This command line prints out the file names of text files that contains "emergency" and "Emergency" in technical.<br/>
It result in more names than the command `$ grep -l "emergency" technical/*/*.txt`.
I think it is useful because I get more related information about emergency without reading all the text containing the word.


`$ grep -i "emergency" technical/biomed/*.txt`<br/>
result:
```
technical/biomed/1471-2334-3-11.txt:        A total of 296 patients were evaluated in the emergency
technical/biomed/1471-2334-3-11.txt:        discharged from the emergency room while 88 (30%) were
technical/biomed/1471-2334-3-11.txt:        emergency departments. Five patients (4%) visited the
technical/biomed/1471-2334-3-11.txt:        status on emergency room services revealed uninsured
technical/biomed/1471-2334-3-11.txt:        emergency patients were less likely to be admitted to the
technical/biomed/1471-2334-3-11.txt:        hospital than insured emergency patients. [ 19 ] Weissman
technical/biomed/1471-2350-3-7.txt:        contrast between the outcomes of elective versus emergency
technical/biomed/1471-2377-3-4.txt:            emergency medical service or in the emergency
technical/biomed/1471-2458-1-9.txt:        hospital emergency rooms in other practice settings. All
technical/biomed/1471-2458-1-9.txt:        diagnostic codes. Emergency room visits were excluded for
technical/biomed/1471-2458-1-9.txt:        another one. We believe the omission of emergency room
technical/biomed/1471-2458-1-9.txt:        emergency rooms is also of great value. We see the system
technical/biomed/1471-2458-1-9.txt:        described here as being complementary to emergency room
technical/biomed/1471-2458-1-9.txt:        earlier signal than will an emergency room based detection
technical/biomed/1471-2458-1-9.txt:        that don't warrant emergency room care.
technical/biomed/1471-2458-3-20.txt:        healthcare workers in emergency departments, intensive care
technical/biomed/1471-2458-3-20.txt:          The population of interest for the survey was emergency
...

technical/biomed/cc1044.txt:        Emergency Department (χ 2= 43.6,
technical/biomed/cc1044.txt:        hypo/hyperglycemia, cardiac disease, emergency admission,
technical/biomed/cc1044.txt:        The prevalence of delirium in the Emergency Department
technical/biomed/cc1044.txt:        18.5% in emergency admissions, similar to Kishi's series
technical/biomed/cc1044.txt:        (16%) [ 29], but emergency admission was not considered a
technical/biomed/cc1477.txt:        admission was after emergency surgery, and the presence of
technical/biomed/cc1477.txt:          admission was more likely to be medical or emergency
technical/biomed/cc1497.txt:        the patient, and whether the surgery was emergency or
technical/biomed/cc1538.txt:        initial emergency life-saving surgery and prompt,
technical/biomed/cc1538.txt:          acute settings such as intensive care units, emergency
technical/biomed/cc1538.txt:          evaluation in an emergency room trauma bay. This might be
technical/biomed/cc1538.txt:          intra-hospital transport for emergency imaging (e.g.
technical/biomed/cc2171.txt:          addition, all patients who died in an emergency
technical/biomed/cc2171.txt:        crowding; for example, emergency rooms or ICUs might have
technical/biomed/cc300.txt:        bone mineral in emergency situations by means of
technical/biomed/cc303.txt:        complicated ventilation, admission source (home, emergency
technical/biomed/cc303.txt:          admitted from the emergency room, 73 (33%) from general
technical/biomed/cc303.txt:        In the rural centers, the emergency room (ER) was the
technical/biomed/cc713.txt:          emergency department he was hypotensive and had pain in
technical/biomed/cc973.txt:        units and emergency prehospital settings. The GCS provides
technical/biomed/cc973.txt:        as possible in emergency situations, and may be repeated at
technical/biomed/cc973.txt:        With the development of emergency medicine, a need arose
technical/biomed/cvm-2-1-038.txt:        well-coordinated center can perform emergency diffusion and
technical/biomed/cvm-2-1-038.txt:        duration comparable with that of emergency head CT. There
technical/biomed/cvm-2-6-286.txt:        including death, MI, emergency bypass surgery, and repeat
technical/biomed/rr37.txt:          subjects who appeared to rely on emergency department
technical/biomed/rr37.txt:          CI, 0-7%). Reliance on emergency department care was
technical/biomed/rr37.txt:        for asthma. Reliance on the emergency department for urgent
technical/biomed/rr37.txt:        reliance on emergency department for urgent asthma care,
```
This command line prints out the file names and the lines that contains "emergency" and "Emergency" in technical/biomed.<br/>
It is very useful when we want to scan through the material realted to emergency and roughly understand what's going without going into the file until we find something that interest us. Then we can follow the path listed on the left to go into the file and read.<br/>


`grep -c`: it list all the file names and count of lines matching the target. 

`$ grep -c "emergency" technical/biomed/*.txt`<br/>
result:
```
technical/biomed/1468-6708-3-1.txt:0
technical/biomed/1468-6708-3-10.txt:0
technical/biomed/1468-6708-3-3.txt:0
...
technical/biomed/rr37.txt:4
technical/biomed/rr73.txt:0
technical/biomed/rr74.txt:0
```
This command prints out all the file names in `technical/biomed` with the count of targets in the file. It is a very very long list so I delete most of it, but most files has a count of 0. I think it will be useful if I want to know which files contain more of the related informtaion, but it will be a lot of work to browse through.


`$ grep -c "emergency." technical/biomed/*9.txt`<br/>
result:
```
technical/biomed/1471-2091-2-9.txt:0
technical/biomed/1471-2105-2-9.txt:0
technical/biomed/1471-2121-3-19.txt:0
technical/biomed/1471-213X-1-9.txt:0
technical/biomed/1471-2156-4-9.txt:0
technical/biomed/1471-2164-2-9.txt:0
technical/biomed/1471-2164-3-19.txt:0
technical/biomed/1471-2164-3-29.txt:0
technical/biomed/1471-2164-3-9.txt:0
technical/biomed/1471-2164-4-19.txt:0
technical/biomed/1471-2172-2-9.txt:0
technical/biomed/1471-2172-3-9.txt:0
technical/biomed/1471-2180-1-29.txt:0
technical/biomed/1471-2180-2-29.txt:0
technical/biomed/1471-2180-3-9.txt:0
technical/biomed/1471-2202-2-19.txt:0
technical/biomed/1471-2202-2-9.txt:0
technical/biomed/1471-2202-3-19.txt:0
technical/biomed/1471-2210-2-9.txt:0
technical/biomed/1471-2229-2-9.txt:0
technical/biomed/1471-2288-1-9.txt:0
technical/biomed/1471-2288-3-9.txt:0
technical/biomed/1471-2296-3-19.txt:0
technical/biomed/1471-2334-1-9.txt:0
technical/biomed/1471-2334-2-29.txt:0
technical/biomed/1471-2334-3-9.txt:0
technical/biomed/1471-2350-3-9.txt:0
technical/biomed/1471-2369-3-9.txt:0
technical/biomed/1471-2407-1-19.txt:0
technical/biomed/1471-2407-2-19.txt:0
technical/biomed/1471-2407-2-9.txt:0
technical/biomed/1471-244X-2-9.txt:0
technical/biomed/1471-2458-1-9.txt:6
technical/biomed/1471-2458-3-9.txt:0
technical/biomed/1472-6793-2-19.txt:0
technical/biomed/1472-6807-2-9.txt:0
technical/biomed/1476-069X-2-9.txt:0
technical/biomed/1477-7525-1-9.txt:0
technical/biomed/1477-7827-1-9.txt:0
technical/biomed/ar149.txt:0
technical/biomed/ar309.txt:0
technical/biomed/ar319.txt:0
technical/biomed/ar409.txt:0
technical/biomed/ar429.txt:0
technical/biomed/ar619.txt:0
technical/biomed/ar79.txt:0
technical/biomed/ar799.txt:0
technical/biomed/cc1529.txt:0
technical/biomed/gb-2002-3-11-research0059.txt:0
technical/biomed/gb-2002-3-12-research0079.txt:0
technical/biomed/gb-2002-3-2-research0009.txt:0
technical/biomed/gb-2002-3-4-research0019.txt:0
technical/biomed/gb-2002-3-6-research0029.txt:0
technical/biomed/gb-2002-3-8-research0039.txt:0
technical/biomed/gb-2002-3-9-research0049.txt:0
technical/biomed/gb-2003-4-2-r9.txt:0
technical/biomed/gb-2003-4-6-r39.txt:0
```
This command prints out all the file in `technical/biomed` that takes the form of `*9.txt`.<br/>
It becomes much easier to read when I restricted the files it can search.<br/>
I am still looking for a way to make it only print the file name that contains the target instead of all the files.


`$ grep -v -c "emergency" technical/biomed/*9.txt`<br/>
result:
```
technical/biomed/1471-2091-2-9.txt:481
technical/biomed/1471-2105-2-9.txt:455
technical/biomed/1471-2121-3-19.txt:823
technical/biomed/1471-213X-1-9.txt:736
technical/biomed/1471-2156-4-9.txt:836
technical/biomed/1471-2164-2-9.txt:857
technical/biomed/1471-2164-3-19.txt:594
technical/biomed/1471-2164-3-29.txt:408
technical/biomed/1471-2164-3-9.txt:514
technical/biomed/1471-2164-4-19.txt:553
technical/biomed/1471-2172-2-9.txt:337
technical/biomed/1471-2172-3-9.txt:396
technical/biomed/1471-2180-1-29.txt:677
technical/biomed/1471-2180-2-29.txt:273
technical/biomed/1471-2180-3-9.txt:620
technical/biomed/1471-2202-2-19.txt:562
technical/biomed/1471-2202-2-9.txt:729
technical/biomed/1471-2202-3-19.txt:542
technical/biomed/1471-2210-2-9.txt:393
technical/biomed/1471-2229-2-9.txt:799
technical/biomed/1471-2288-1-9.txt:450
technical/biomed/1471-2288-3-9.txt:793
technical/biomed/1471-2296-3-19.txt:409
technical/biomed/1471-2334-1-9.txt:372
technical/biomed/1471-2334-2-29.txt:450
technical/biomed/1471-2334-3-9.txt:437
technical/biomed/1471-2350-3-9.txt:494
technical/biomed/1471-2369-3-9.txt:401
technical/biomed/1471-2407-1-19.txt:477
technical/biomed/1471-2407-2-19.txt:563
technical/biomed/1471-2407-2-9.txt:270
technical/biomed/1471-244X-2-9.txt:540
technical/biomed/1471-2458-1-9.txt:538
technical/biomed/1471-2458-3-9.txt:394
technical/biomed/1472-6793-2-19.txt:522
technical/biomed/1472-6807-2-9.txt:364
technical/biomed/1476-069X-2-9.txt:1263
technical/biomed/1477-7525-1-9.txt:480
technical/biomed/1477-7827-1-9.txt:778
technical/biomed/ar149.txt:468
technical/biomed/ar309.txt:352
technical/biomed/ar319.txt:541
technical/biomed/ar409.txt:527
technical/biomed/ar429.txt:352
technical/biomed/ar619.txt:358
technical/biomed/ar79.txt:639
technical/biomed/ar799.txt:467
technical/biomed/cc1529.txt:462
technical/biomed/gb-2002-3-11-research0059.txt:1336       
technical/biomed/gb-2002-3-12-research0079.txt:1073       
technical/biomed/gb-2002-3-2-research0009.txt:524
technical/biomed/gb-2002-3-4-research0019.txt:692
technical/biomed/gb-2002-3-6-research0029.txt:466
technical/biomed/gb-2002-3-8-research0039.txt:357
technical/biomed/gb-2002-3-9-research0049.txt:572
technical/biomed/gb-2003-4-2-r9.txt:983
technical/biomed/gb-2003-4-6-r39.txt:1008
```
This command prints out the file name and line count in `technical/biomed/*9.txt` that does not contain "emergency". <br/>
It will be very useful when we want to find the file that does not have anything to do with the target, and have the biggest number of lines.

