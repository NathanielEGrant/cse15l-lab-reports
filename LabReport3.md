# Lab Report 3

## Source

![Image](grepVariations.png)
The main and only source that I used to dive more in depth with the ```grep``` command was ChatGPT. 

### Grep -r variation
Chatgpt had given me the ```grep -r``` variation, which described that this allowed me to search through file directories and find all the specified character patterns within that grouping of files.

```
$ grep -r helo biomed
biomed/1471-2180-3-10.txt:        Mycobacterium chelonae [ 32 ] . These
biomed/1471-2199-3-11.txt:        tumor cells, most of which are of epitheloid origin, become
biomed/1471-2199-3-11.txt:        fibroblasts versus apoptosis in epitheloid cells.
biomed/1471-2334-3-15.txt:          nephelometer flasks on a rotating platform (60 rpm) or
biomed/1471-2350-2-8.txt:          nephelometry [ 14]. Nephropathy was defined as a
biomed/ar328.txt:        nephelometry to disclose autoimmune phenomena and/or
biomed/ar93.txt:          human epidermal tissue. RF was tested by nephelometry.
biomed/ar93.txt:          IgM RF was measured by nephelometry, and a level
biomed/bcr458.txt:        bachelor's degree, which is 220% higher than the national
```

My first use of  ```grep -r``` was a test, to see how the variation actually worked. The command above searched through all the files in the biomed directory and found every instance where the combination ```helo``` appeared. It also specified which file each instance of it appeared, which is helpful if you wanted to do a deep dive of the specified word.

```
$ grep -r " frog " biomed
biomed/1471-2091-3-31.txt:          acids 792-816 of frog Myo1c (SVLDKSWPVPPPSLREASELLREMC;
biomed/1471-213X-1-13.txt:        active form of Notch (Nac) in frog embryos led to an
biomed/1471-213X-1-13.txt:        neurons in frog and zebrafish [ 25, 26, 27, 28]. Each of
biomed/1471-213X-1-13.txt:        of frog [ 24] and chick [ 20] and in the neural plate of
biomed/1471-213X-1-13.txt:        frog [ 25] and zebrafish [ 26, 27, 28], concomitant with
biomed/1471-213X-1-13.txt:          negative form of frog Delta-1 protein into early cleavage
biomed/1471-213X-1-6.txt:        used to fertilize frog eggs in the lab [ 25]. We rinsed the
biomed/1471-213X-3-2.txt:        duplication. Instead, when over-expressed in frog or fish
biomed/1471-2164-2-8.txt:        during early frog development [ 1 ] . Nucleoplasmin forms a
biomed/1471-2202-1-1.txt:        skin of the frog 
biomed/1471-2202-1-1.txt:        frog
biomed/1471-2202-3-4.txt:          to Ca 2+(1.8 mM in frog Ringer's solution) but not to
biomed/1471-2202-3-4.txt:          condition, whole oocytes were bathed in frog Ringer's
biomed/gb-2002-3-2-research0008.txt:        tetraploid frog 
```

One of the uses this variation could have would be the ability to search huge file directories for specific information. I chose to look through all the biomed files for the phrase ```frog```, and from here any researchers interested in frog specific testing can look into each of these files.


### Grep -i variation

ChatGPT's second variation was ```grep -i```, which described that it was a case insensitive variation the original ```grep``` command. 

