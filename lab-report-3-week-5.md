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

`$ grep -i "emergency" technical/911report/*9*.txt`
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

`grep -i -l "emergency" technical/*/*.txt`
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

`$ grep -i "emergency" technical/biomed/*.txt`
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

