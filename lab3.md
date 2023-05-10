**Lab 3**

**grep**
1. `-i`: This option ignores uppercase and lowercase. This is useful when trying to find instances of a word at the beginning and in the middle of a sentence. (Source: https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

Example 1: 

`grep -i "AuToMoBiLE" */*.txt`

Output: 
```
biomed/1471-2288-3-9.txt:        Automobile fatality totals are typically computed with
biomed/1471-2288-3-9.txt:        Annual U.S. automobile accident fatalities are```
```

Example 2:

`grep -i "AiRPlanE" */*.txt`

Output:
```
911report/chapter-11.txt:            In 1994, a private airplane had crashed onto the south lawn of the White House. In
911report/chapter-11.txt:                Security Group devoted largely to the possibility of a possible airplane hijacking
911report/chapter-12.txt:                airplane. Once inside the country, they may seek another form of identification and
911report/chapter-13.2.txt:                that an act or suspected act of airplane piracy was being committed.
911report/chapter-13.2.txt:                reported aboard an American airplane, went to American's gate area at Logan with his
```

2. `-o': This option prints only the matching parts of the matching line on separate lines. This is useful to find which files have a certain word and estimate how many times a word appears. (Source: https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

Example 1:

`grep -o "crash" */*.txt`

Output:
```
911report/chapter-1.txt:crash
911report/chapter-1.txt:crash
911report/chapter-1.txt:crash
911report/chapter-1.txt:crash
911report/chapter-1.txt:crash
911report/chapter-1.txt:crash
911report/chapter-1.txt:crash
911report/chapter-1.txt:crash
911report/chapter-1.txt:crash
```

Example 2:

`grep -o "explosion" */*.txt`

Output:
```
911report/chapter-1.txt:explosion
911report/chapter-13.2.txt:explosion
911report/chapter-13.4.txt:explosion
911report/chapter-13.5.txt:explosion
911report/chapter-13.5.txt:explosion
911report/chapter-13.5.txt:explosion
911report/chapter-13.5.txt:explosion
911report/chapter-3.txt:explosion
911report/chapter-9.txt:explosion
```

3. `-h`: This option displays the matched lines but not the filename. This is useful when the specific file where a setence comes from does not matter.  (Source: https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

Example 1:

`grep -h "exponential decay" */*.txt`

Output:
```
crucial for the exponential decay of 
expectation. Because an exact exponential decay means that
```

Example 2:

`grep -h "The fact is" */*.txt`

Output:
```
a naive intuition. The fact is that we do not know the
is around 70%. The fact is that
```

4. `-n': This option also prints out the line number as well as the matched line. This is useful to tell where in a file a certain line is. (Source: https://www.geeksforgeeks.org/grep-command-in-unixlinux/)

Example 1:

`grep -n "other word" */*.txt`

Output:
```
911report/chapter-13.1.txt:840:                until the summer-if then. In other words, the new administration- like others before
911report/chapter-3.txt:322:                foreign intelligence information. In other words, the authorities of the FISA law
911report/chapter-6.txt:883:            In other words, the Yemenis provided strong evidence connecting the Cole attack to al
biomed/1471-2105-2-1.txt:449:          replacement mutations. In other words, we sum the chances
biomed/1471-2105-3-12.txt:77:          30 ] . In other words, the complexity of these BLAST
biomed/1471-2105-3-12.txt:142:          will be discarded. In other words, hierarchical matches
biomed/1471-2105-3-12.txt:349:            in other words, only GenBank accession numbers can be
```

Example 2:

`grep -n "cosmo" */*.txt`

Output:
```
biomed/1471-2105-2-9.txt:14:        this approach to show that there is a cosmopolitan marine
biomed/1471-2350-4-6.txt:534:        case-control samples in cosmopolitan US and European
biomed/gb-2001-2-4-research0014.txt:43:        arrays contain a cosmopolitan series of well characterized
plos/journal.pbio.0020262.txt:67:        cosmopolitan family history. More questionable are the bits where he paddles casually
plos/journal.pbio.0020306.txt:128:        cosmopolitan genus of diatoms and its physiology has been well studied. Once the primary
plos/journal.pbio.0020439.txt:17:        by revealing otherwise invisible and previously unsuspected worlds. Western cosmology from
plos/journal.pbio.0020439.txt:23:        challenged the completeness of this cosmology and unequivocally demonstrated the existence
```
