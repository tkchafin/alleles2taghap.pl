## alleles2taghap.pl

alleles2taghap.pl by Tyler Chafin

This script converts from the .alleles file output by pyRAD to create the input for fineRADstructure

NOTE: 
- All samples are assumed to be diploid.
- Sample names CANNOT contain underscores.
- Columns containing Ns or gaps will be deleted from final output
- Popmap file should be tab-delimited, like so: SampleName [tab] PopID
- If populations to include/exclude are not given, all samples in popmap are used.
- You can specify multiple popIDs as: ID1+ID2+ID3, as long as these match IDs in popmap
- For the -s filter, singletons are evaluated within the selected subset of individuals

Options:
~~~~
    -a	: Path to input file (.alleles)
    -p	: Path to popmap file (tab-delimited)
    -o	: Output file prefix. [Default = out, i.e. out.taghap]
    -c	: Min number of samples for which data must be present per locus [Default = 1]
    -n	: Minumum proportion of loci an individual must be present at to be retained [def = 0.2]
    -i	: PopIDs to include in output file (e.g. -i pop1+pop4)
    -x	: PopIDs to exclude (e.g. -x catenatus or -x sistrTX+sistrIN)
    -m	: Maximum number of SNPs per locus. Loci exceeding are deleted [default:10]
    -s	: Skip SNPs that are singletons [Boolean; Default = false]
    -h	: Displays this help message
~~~~
