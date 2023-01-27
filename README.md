# WWMB_Final_project

## Preparatory part 

- Downloading all the necessary materials for the bash terminal, namely various bioconda tools.
- Creation of a separate Snakemake script in PyCharm IDE for editing the pipeline.
- Creating notes for conducting an experiment

## Data Analysis

Operations below will help us to find out which possible mutations helped T5 phage to fight with bacteria defence-against-viruses system.
- Alignment(BWA). 
- Indexing(Samtools). 
- Sorting (samtools). 
- Calling(bcftools).

## Obtained results

Results were studied in the following files: 
- T5_AI_69_S60_variants.vcf (was obtained manually by using script step by step);
- variants_filtered_T5_sample_AI-70_S61.vcf (Snakemake),  
- variants_filtered_T5_sample_AI-72_S63.vcf (Snakemake),
- variants_filtered_T5_sample_AI-69_S60.vcf (Snakemake), 
- variants_filtered_T5_sample_AI-71_S62.vcf (Snakemake),
- variants_filtered_T5_sample_AI-73_S64.vcf (Snakemake).
- Other results were dropped because off insignificancy. 

### For the **69_S60** were obtained 2 significant mutations:
'''sh
#CHROM  POS     ID      REF     ALT     QUAL    FILTER  INFO    FORMAT  mapped_sorted/T5_AI_69_S60_aligned_sorted.bam
T5      57822   .       G       A       225     LowQual DP=243;VDB=0.000940976;SGB=-0.693147;MQSB=1;MQ0F=0;AC=1;AN=1;DP4=0,0,177,39;MQ=60       GT:PL   1:255,0
T5      65803   .       GTT     GT      199     LowQual INDEL;IDV=207;IMF=0.848361;DP=244;VDB=0.959859;SGB=-0.693147;MQSB=1;MQ0F=0;AC=1;AN=1;DP4=33,2,167,42;MQ=60      GT:PL   1:226,0
'''

### For the **70_S61** were obtained 4 significant mutations:
```sh
#CHROM  POS     ID      REF     ALT     QUAL    FILTER  INFO    FORMAT  mapped_sorted/sorted_T5_sample_AI-70_S61.bam
T5      57743   .       C       T       225     PASS    DP=240;VDB=0.00293369;SGB=-0.693147;MQSB=1;MQ0F=0;AC=1;AN=1;DP4=0,0,146,59;MQ=60        GT:PL   1:255,0
T5      61763   .       T       C       225     PASS    DP=245;VDB=0.895648;SGB=-0.693147;MQSB=1;MQ0F=0;AC=1;AN=1;DP4=0,0,156,67;MQ=60  GT:PL   1:255,0
T5      65861   .       C       T       225     PASS    DP=236;VDB=0.517555;SGB=-0.693147;MQSB=1;MQ0F=0;AC=1;AN=1;DP4=0,0,148,72;MQ=60  GT:PL   1:255,0
T5      82088   .       G       A       225     PASS    DP=245;VDB=0.27637;SGB=-0.693147;MQSB=0.98947;MQ0F=0;AC=1;AN=1;DP4=0,0,82,114;MQ=59     GT:PL   1:255,0
```

### For the **71_S62** were obtained 2 significant mutations:
```sh
#CHROM  POS     ID      REF     ALT     QUAL    FILTER  INFO    FORMAT  mapped_sorted/sorted_T5_sample_AI-71_S62.bam
T5      57746   .       T       C       225     PASS    DP=243;VDB=0.00670713;SGB=-0.693147;MQSB=1;MQ0F=0;AC=1;AN=1;DP4=0,0,182,41;MQ=60        GT:PL   1:255,0
T5      65853   .       TGGGG   TGGGGG  141     PASS    INDEL;IDV=195;IMF=0.795918;DP=245;VDB=0.517428;SGB=-0.693147;MQSB=1;MQ0F=0;AC=1;AN=1;DP4=24,13,162,46;MQ=60     GT:PL   1:168,0
```

### For the **72_S63** were obtained 2 significant mutations:
```sh
#CHROM  POS     ID      REF     ALT     QUAL    FILTER  INFO    FORMAT  mapped_sorted/sorted_T5_sample_AI-72_S63.bam
T5      57885   .       A       G       225     PASS    DP=245;VDB=0.235075;SGB=-0.693147;MQSB=1;MQ0F=0;AC=1;AN=1;DP4=0,0,192,38;MQ=60  GT:PL   1:255,0
T5      65930   .       A       G       225     PASS    DP=243;VDB=0.263467;SGB=-0.693147;MQSB=1;MQ0F=0;AC=1;AN=1;DP4=0,0,159,58;MQ=60  GT:PL   1:255,0
```

### For the **73_S64** were obtained 17! significant mutations:
```sh
#CHROM  POS     ID      REF     ALT     QUAL    FILTER  INFO    FORMAT  mapped_sorted/sorted_T5_sample_AI-73_S64.bam
T5      6972    .       A       T       4.38466 PASS    DP=249;VDB=0;SGB=-0.693147;MQSB=1;MQ0F=0.895582;AC=1;AN=1;DP4=0,0,132,91;MQ=0   GT:PL   1:32,0
T5      6984    .       T       G       6.51248 PASS    DP=261;VDB=0;SGB=-0.693147;MQSB=1;MQ0F=0.977012;AC=1;AN=1;DP4=0,0,152,103;MQ=0  GT:PL   1:35,0
T5      7023    .       G       T       4.38466 PASS    DP=223;VDB=3.18185e-16;SGB=-0.693147;MQSB=1;MQ0F=0.856502;AC=1;AN=1;DP4=0,0,105,86;MQ=0 GT:PL   1:32,0
T5      7122    .       A       G       19.4636 PASS    DP=237;VDB=4.48416e-44;SGB=-0.693147;MQSB=1;MQ0F=0.962025;AC=1;AN=1;DP4=0,0,94,134;MQ=0 GT:PL   1:49,0
T5      7125    .       A       G       18.4764 PASS    DP=252;VDB=9.15157e-37;SGB=-0.693147;MQSB=1;MQ0F=0.948413;AC=1;AN=1;DP4=0,0,103,136;MQ=0        GT:PL   1:48,0
T5      7146    .       A       G       17.4923 PASS    DP=249;VDB=1.2023e-21;SGB=-0.693147;MQSB=1;MQ0F=0.931727;AC=1;AN=1;DP4=0,0,102,130;MQ=0 GT:PL   1:47,0
T5      7197    .       A       G       4.38466 PASS    DP=52;VDB=0.109922;SGB=-0.693147;MQSB=1;MQ0F=0.961538;AC=1;AN=1;DP4=0,0,23,27;MQ=0      GT:PL   1:32,0
T5      7202    .       A       T       8.13869 PASS    DP=36;VDB=1.21986e-12;SGB=-0.693139;MQSB=1;MQ0F=1;AC=1;AN=1;DP4=0,0,15,21;MQ=0  GT:PL   1:37,0
T5      7203    .       C       T       8.13869 PASS    DP=36;VDB=1.21986e-12;SGB=-0.693139;MQSB=1;MQ0F=1;AC=1;AN=1;DP4=0,0,15,21;MQ=0  GT:PL   1:37,0
T5      7206    .       C       T       8.13869 PASS    DP=36;VDB=2.70297e-12;SGB=-0.693139;MQSB=1;MQ0F=1;AC=1;AN=1;DP4=0,0,15,21;MQ=0  GT:PL   1:37,0
T5      7207    .       C       A       8.13869 PASS    DP=36;VDB=4.7837e-12;SGB=-0.693139;MQSB=1;MQ0F=1;AC=1;AN=1;DP4=0,0,15,21;MQ=0   GT:PL   1:37,0
T5      7211    .       T       A       6.51248 PASS    DP=71;VDB=0.918534;SGB=-0.693147;MQSB=1;MQ0F=0.746479;AC=1;AN=1;DP4=0,0,23,30;MQ=0      GT:PL   1:35,0
T5      7245    .       C       T       5.04598 PASS    DP=231;VDB=0.997285;SGB=-0.693147;MQSB=1;MQ0F=0.835498;AC=1;AN=1;DP4=0,0,104,89;MQ=0    GT:PL   1:33,0
T5      7581    .       G       A       3.22451 PASS    DP=80;VDB=1.24375e-26;SGB=-0.693147;MQSB=1;MQ0F=0.975;AC=1;AN=1;DP4=0,0,37,41;MQ=0      GT:PL   1:30,0
T5      7593    .       C       T       19.4636 PASS    DP=252;VDB=0.999945;SGB=-0.693147;MQSB=1;MQ0F=0.948413;AC=1;AN=1;DP4=0,0,101,138;MQ=0   GT:PL   1:49,0
T5      7606    .       A       G       13.6078 PASS    DP=224;VDB=1.10703e-43;SGB=-0.693147;MQSB=1;MQ0F=0.928571;AC=1;AN=1;DP4=0,0,93,115;MQ=0 GT:PL   1:43,0
T5      7611    .       T       C       13.6078 PASS    DP=253;VDB=8.84157e-17;SGB=-0.693147;MQSB=1;MQ0F=0.920949;AC=1;AN=1;DP4=0,0,111,122;MQ=0        GT:PL   1:43,0
```

## Discussions

_Comming soon, this section should be defintely obtained with the use of ncbi sources..._

## **Additional materials**

### Contacts: 
Telegram: @nagibator113

### Link to the notion with all usefull notes
There you go: [Notion link]

![Alt Text](https://media.istockphoto.com/id/1320162763/de/foto/vielen-dank-f%C3%BCr-ihre-aufmerksamkeit-farbwalze-mit-blauer-farbe-auf-einer-holzoberfl%C3%A4che.jpg?s=612x612&w=0&k=20&c=22inaTbjjWxcEmdEzEeldHR4FpwLcQ9TxRhedwNh7Rk=)

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)
[Notion link]: <https://www.notion.so/c64a9219030349128c0fd11a4f097248?v=42a6084c5b034b24a79c41ea4e49110e>
