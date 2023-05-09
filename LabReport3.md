# Lab Report 3

## Source

![Image](grepVariations.png)
![Image](grepVariations3.png)
The main and only source that I used to dive more in depth with the ```grep``` command was ChatGPT. 

### grep -r variation
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


### grep -i variation

ChatGPT's second variation was ```grep -i```, which described that it was a case insensitive variation the original ```grep``` command.
![Image](grepVariations2.png)
Working back off of the previous search using ```$ grep -r " frog " biomed```, I realized that that search was not finding all cases of frog, because it was case sensitive. I was curious if I was able to use multiple of these variations in the same command, and by asking chatgpt I found out I was able to.

```
$ grep -ir " frog " biomed
biomed/1471-2091-3-31.txt:          acids 792-816 of frog Myo1c (SVLDKSWPVPPPSLREASELLREMC;
biomed/1471-213X-1-13.txt:        active form of Notch (Nac) in frog embryos led to an
biomed/1471-213X-1-13.txt:        the overexpressed Notch protein fell. Frog retinal cells
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
While this search only brought up one extra instance of frog that was capitalized, this could help a ton when searching for phrases that can or cannot be capitalized, i.e. when frog is at the beginning of a sentence.

```
$ grep -ir " acl " biomed
biomed/1471-2474-3-3.txt:        strengths of the ACL at the strain rates of 40, and 140
biomed/1471-2474-3-3.txt:        ACL in humans and rhesus monkeys to analyze age and species
biomed/1471-2474-3-3.txt:        ACL and PCL hyperextension. In the PCL, ligament tearing
biomed/1471-2474-3-3.txt:        the ACL failure mode of Rhesus monkeys. The first study
biomed/1471-2474-3-3.txt:        et al in 1976 studied ACL failure in
biomed/1471-2474-3-3.txt:        PCL and ACL were reverse from those of the previous
biomed/gb-2003-4-2-r14.txt:          acl ) surely belong to an operon,
biomed/gb-2003-4-2-r14.txt:          start and stop codons (Figure 4). Acl exhibits strong
biomed/gb-2003-4-2-r14.txt:          the function of Acl is likely to be closer to
biomed/gb-2003-4-2-r14.txt:          acl is tightly organized with
biomed/gb-2003-4-2-r14.txt:          acl . An anthranilate-CoA ligase
biomed/gb-2003-4-2-r14.txt:          Xylella Acl exhibited greater
biomed/gb-2003-4-2-r14.txt:          If anthranilate is indeed the substrate of Acl in
biomed/gb-2003-4-2-r14.txt:          acl are problematic at the present
```

My second use of the ```grep -i``` variation was based upon the idea of non-uniformal abbreviations. This search brought up a few different variations of the abbreviation acl, which showed both different meanings of the grouping acl and the idea that sometimes these abbreviations are not uniform among the scientific community.

### grep -l variation
The 3rd variation I am using that ChatGPT referred to me is ```grep -l```. The chatbot says that this search returns only the name of files that contains the specified variations.

```
$ grep -li " frog " *
1471-2091-3-31.txt
1471-213X-1-13.txt
1471-213X-1-6.txt
1471-213X-3-2.txt
1471-2164-2-8.txt
1471-2202-1-1.txt
1471-2202-3-4.txt
gb-2002-3-2-research0008.txt
```

This use of ```grep -l``` returns to us all the files that contain the word "frog"(case-insensitive). Again, this could be a quick way to get the files that do mention frog research, and from there we can grep specific keywords such as specific organs or proteins that may be involved with these frogs.

```
$ grep -li cycloheximide *
1471-2091-3-14.txt
1471-2121-3-11.txt
1471-2121-3-22.txt
1471-2121-3-8.txt
1471-213X-2-8.txt
1471-213X-3-3.txt
1471-2156-3-4.txt
1471-2180-3-5.txt
1471-2202-4-5.txt
1475-2867-3-12.txt
1475-2867-3-2.txt
1475-4924-1-10.txt
1476-9433-1-2.txt
ar331.txt
```
Again, this variation of grep is very useful when it comes to traversing large directories. This use of ```grep -l``` looks for all instances of cycloheximide and returns every file that contains it.

### grep -v variation

The final variation that ChatGPT gave me is ```grep -v```. This looks at the specified character pattern, and looks for lines in the file that do not contain that pattern.

```
$ grep -vi muscl 1471-2156-2-8.txt




        Background
        Dystrophin and its associated proteins are thought to be
        the extracellular matrix [ 1], and the absence of many of
        these proteins can lead to the phenotype of muscular
        dystrophy [ 2]. The dystrophin-associated protein complex
        (DAPC) consists of several subgroups of protein complexes,
        each associated either directly or indirectly with
        dystrophin. The sarcoglycans are four transmembrane
        proteins [ 3] that are organized by a fifth protein called
        sarcospan [ 4]. This complex is thought to be involved in
        signalling at the cell membrane [ 5]. A second subcomplex,
        known as the dystroglycan complex [ 6], interacts directly
        with dystrophin in the cytoplasm and laminin in the
        extracellular matrix, thus providing a structural link
        between the inside and the outside of the cell. A third
        subcomplex involves the dystrobrevins [ 7, 8] and
        syntrophins [ 9] which form a complex at the C-terminal
        region of dystrophin [ 10, 11, 12] and have an as yet
        unidentified function.
        Desmuslin (DMN) was recently identified as an
        α-dystrobrevin-interacting protein via the yeast two-hybrid
        method [ 13]. Both desmuslin mRNA and protein are expressed
        encodes a novel intermediate filament (IF) protein of 1253
        amino acids. Electron microscopic analysis shows that
        protein. Co-immunopreciptation experiments revealed that
        the desmuslin and α-dystrobrevin interaction involves the
        region of protein encoded by exons 8-16 of α-dystrobrevin
        and domains 1A through 2A of the desmuslin rod domain.
        Desmuslin is hypothesized to function as a mechanical
        unrecognized linkage between the extracellular matrix via
        the DAPC and the Z-discs through desmin and plectin [
        14].
        As several IF proteins, including desmin, have been
        implicated in human genetic disorders such as dominant and
        recessive congenital and adult onset myopathies [ 15, 16,
        17, 18], desmuslin becomes a candidate to be involved in
        myopathies as well. Supporting this is the exclusive
        expression of
        The
        DMN gene was analyzed for mutations
        in 71 patients with various forms of muscular dystrophy and
        myopathy. In addition to 9 single-nucleotide polymorphisms
        (SNPs) that do not change the protein sequence, we
        identified 12 SNPs that do alter the residue they encode.
        Although examination of controls has shown that none of
        them is likely to cause the phenotype, our results are
        useful for future disequilibrium studies of this region of
        chromosome 15q26.3 and for mutation analysis and
        association studies in other genetic disorders.


        Results and Discussion
        Using the
        DMN cDNA sequence (AF359284) as a
        query to blast the public human genome database, we found a
        genomic clone (AC018999) that included the entire desmuslin
        coding sequence. The alignment identified 5 exons which are
        schematically indicated in Figure 1. Eleven sets of primer
        pairs were developed to amplify the 5 exons and the
        flanking intron sequences (Table 1). The primers were
        designed to amplify overlapping segments of the desmuslin
        coding sequence as indicated in Figure 1.
        Desmin, a desmuslin-interacting protein, has been
        implicated in hereditary distal myopathies implying that
        desmuslin itself may also be involved in myopathies of
        unknown etiology. DNA samples isolated from 71 dystrophic
        and myopathic patients (as described in Table 2) were
        analyzed by direct sequencing to determine whether the
        phenotype was the result of a desmuslin mutation. All
        observed variants were subsequently tested in ≤ 156 control
        individuals. These analyses revealed 10 common and 2 rare
        SNPs [ 19, 20] that alter an amino acid codon; 7 result in
        non-conservative amino acids changes (Table 3).
        None of the SNPs seem associated with the patient
        phenotypes as each was also found in the control
        population. Nine silent SNPs, which did not alter an amino
        acid, were also identified in the patient population;
        several of these SNPs showed a high degree of
        heterozygosity. Most were tested for and detected in the
        control population, thus making desmuslin an unlikely
        candidate to be involved in these myopathies, but this
        first pass can be followed by others in a larger set of
        patient samples.
        Interestingly, SNP 3, a C598T substitution resulting in
        a premature stop codon in exon 1, was detected in a single
        Nemaline myopathy patient. Neither the proband's mother nor
        any of the other patients was found to carry this mutation
        (Figure 2A). The C598T mutation removed a Pvu II site, thus
        permitting detection of the alteration by restriction
        digest analysis of a PCR product generated from genomic
        DNA. The assay is outlined schematically in Figure 2Band
        documented in Figure 2C. Using this Pvu II assay, the C598T
        change was detected in the unaffected father of the
        patient, making it unlikely that heterozygosity for the
        C598T change is the causative mutation in the myopathic
        proband.
        The removal of the Pvu II site allowed rapid screening
        of additional patients and control samples by DNA
        amplification of the region and subsequent digestion of the
        PCR product with Pvu II. One of 312 control chromosomes was
        found to have lost the Pvu II site, and the heterozygous
        presence of the C598T mutation was confirmed by DNA
        sequencing of the PCR product. Thus it is likely that the
        C598T mutation is not responsible for the myopathic
        phenotype of the proband. This is a surprising result
        considering that a single copy of this stop codon is
        present in 0.44% (2/454) of the population and 0.002% of
        the population is predicted to carry this nonsense mutation
        in a homozygous state. The phenotype of the latter
        individuals is not known.
        There is the possibility that either the heterozygous
        C598T
        DMN mutation combined with another
        mutation in a different gene or the C598T in a homozygous
        state causes muscular dystrophy or myopathy of unknown
        genetic pathogenesis. The C598T
        DMN mutation is a good candidate to
        be a modifier for muscular and/or cardiac phenotypes,
        considering: (i) the frequency of the mutation in the
        normal population in the heterozygous as well as homozygous
        state; and (ii) the key role of desmuslin in connecting the
        Z-discs to the extracellular matrix. The desmuslin SNPs
        should be examined in a larger set of myopathy and muscular
        dystrophy patients to test this hypothesis. More
        specifically, it should be determined whether there is a
        statistically significant difference in the frequency of
        individual or clustered SNP haplotypes between the patient
        and the control populations.
        The desmuslin coding sequence is highly polymorphic with
        9 SNPs that do not alter an amino acid and 12 that do. Ten
        of these variations have minor allele frequencies that are
        represented in over 10% of the chromosomes sampled. These
        10 are spaced within a genomic interval of ≤ 28 kilobases,
        or approximately 1 per 2800 bases. These highly informative
        markers are thus very useful for genetic analysis. The
        presence of so many SNPs within the coding sequence of a
        protein is somewhat unexpected and is much greater than
        that documented for other genes. This degree of variability
        may reflect a redundancy of desmuslin at the Z-line where
        other IF proteins with potentially overlapping functions
        are located [ 21].


        Conclusions
        The characterization of the individual components that
        especially information concerning genotype-phenotype
        correlations, will increase our understanding of the
        other groups to test for the presence of the C598T
        DMN mutation in their human patient
        samples affected by muscular and cardiac diseases. The
        generation of desmuslin null animal models will also
        contribute to the understanding of the role of this protein


        Materials and Methods
        Blood samples were obtained from patients and control
        subjects under IRB-approved informed consent. The genomic
        DNA extracted from these blood samples was used as the
        template for the PCR assay. Using an Advantage-GC cDNA PCR
        polymerase (Clontech) and 
        Pfu DNA polymerase (Stratagene), PCR
        was carried out with primers specific to the exon and/or
        intron of
        DMN sequence (Table 1) under the
        DAPC: Dystrophin-associated protein complex; DMN:
        Desmuslin, SNP: Single-nucleotide polymorphism; IF:
        Intermediate filament
```
        
        This first use of ```grep -l``` I thought of was to be able to search through a certain file and find all the lines that didn't incluce any instance of the phrase "muscl". I chose that specifically so that I would be able to go through all the lines that didn't have any relation muscle and read through them.
       
      
```
       $ grep -vi a 1471-2156-2-8.txt




        unidentified function.
        region of protein encoded by exons 8-16 of α-dystrobrevin
        14].
        expression of
        The
        useful for future disequilibrium studies of this region of


        Using the
        C598T
        The desmuslin coding sequence is highly polymorphic with


        Conclusions
        other groups to test for the presence of the C598T 


        intron of
        following conditions: 94°C for 1 min followed by 35 cycles
        respectively.


        Desmuslin, SNP: Single-nucleotide polymorphism; IF:
```

In certain cases, you might want to search for lines that don't contain a certain character, in this case A (case-insensitive). This would definitely be one of the easiest to go aboout doing this, compared to going line by line.

