
------------------------------------------------------------------------
		RNAdetect package for ncRNA detection
------------------------------------------------------------------------
RNAdetect is a tool for ncRNA detection through comparative genome analysis
piRNAdetect is a tool for piRNA detection through support vector machine
RNAdetect package utilizes ViennaRNA package and RNAstructure package 

--------------------Package implementation for RNAdetect----------------

 RNAdetect

 Usage:
		RNAdetect input_sequence -w=120 -s=40 -o=score.txt -t=0.5
    -w (window) 		Size of window for comparative genome analysis
    -s (slide)  		Size of slide for comparative genome analysis
    -o (output)			Output file to list probability of ncRNA
    -t (threshold) 	Threshold of decision to make ncRNA assertion
    -m (model) 			Path of data model


--------------------Package implementation for piRNAdetect----------------

 piRNAdetect

 Usage:
		piRNAdetect input_sequence -o=score.txt -t=0.5 -s=human
    -o (output)			Output file to list probability of piRNA
    -t (threshold) 	Threshold of decision to make piRNA assertion
    -s (species) 		Species for decision (human/mouse/rat)
    -m (model) 			Path of data model



--------------------Installation of RNAdetect package--------------------

Please run "setup_rnadetect" to build & install RNAdetect and piRNAdetect
The compiled tools can be found in the "bin" folder.



--------------------Included packages------------------------------------

For user convenience, we have included the Vienna Package (ver 2.1.7) and
the RNAstructure Package (ver 5.8) in this distribution.
Please refer to the official distribution sites for these packages for the
latest updates, copyright information, and more.



ViennaRNA Package: Version 2.1.7
--------------------------------
See the NEWS and Changelog files for differences to previous versions.

The ViennaRNA Package consists of a few stand alone programs and a 
library that you can link your own programs with. 
Together with this version we distribute the Kinfold and RNAforester
programs. See the README files in the respective sub-directories.

The package allows you to

- predict minimum free energy secondary structures
- calculate the partition function for the ensemble of structures
- calculate suboptimal structures in a given energy range
- compute local structures in long sequences
- predict consensus secondary structures from a multiple sequence alignment
- predict melting curves
- search for sequences folding into a given structure
- compare two secondary structures 
- predict hybridization structures of two RNA molecules

The package includes a Perl5 module that gives access to almost all
functions of the C library from Perl.

There is also a set of programs for analyzing sequence and distance
data using split decomposition, statistical geometry, and cluster methods.
They are not maintained any more and not built by default.

See the NEWS and Changelog files for changes between versions.

Please read the copyright notice in the file COPYING!

The package should be easily portable. It is known to compile without
modifications at least under
SunOS 5.x, IRIX 5.x and 6.x, linux, and windows with the CygWin environment.
Other UNIX flavors should present no problems.
You need a compiler that understands ANSI C. See the INSTALL file for details.

A couple of useful utilities can be found in the Utils directory.

All executables read from stdin and write to stdout and use command line
switches rather than menus to be easily usable in pipes.

For more detailed information see the man pages. Perl utilities contain
POD documentation that can be read by typing e.g.
perldoc relplot.pl

We have included a patched version of D.G. Gilbert's readseq program
for those who often process sequence files from databanks. See the
the documentation in that directory for details.

Since version 2.0 the build-in energy parameters (available as parameter
file default.par as well) are taken from:

D.H. Mathews et al. (2004),
"Incorporating chemical modification constraints into a dynamic programming
algorithm for prediction of RNA secondary structure",
Proc. Natl. Acad. Sci. USA: 101, pp 7287-7292

and

D.H Turner et al. (2009), "NNDB: The nearest neighbor parameter database
for predicting stability of nucleic acid secondary structure",
Nucleic Acids Research: 38, pp 280-282

For backward compatibility we also provide energy parameters from Turner et al.
1999 in the file 'rna_turner1999.par'. Additionally, a set of trained RNA energy
parameters from Andronescou et al. 2007 'rna_andronescou2007.par' and two sets
of DNA parameters ('dna_mathews1999.par' and 'dna_mathews2004.par') are included
in the package as well.
The code very rarely uses static arrays, and all programs should work for 
sequences up to a length of 32700 (if you have huge amounts of memory that
is).

If you're a commercial user and find these programs useful, please consider
supporting further developments with a donation.

The most recent source code and documentation should always be available on
the web at 
http://www.tbi.univie.ac.a/~ivo/RNA

We need your feedback! Send your comments, suggestions, and questions to
rna@tbi.univie.ac.at

Ivo Hofacker, Spring 2006



RNAstructure Package: Version 5.8
---------------------------------
The package help is provided in the manual directory as html files.
It can also be found online at:
http://rna.urmc.rochester.edu/RNAstructureHelp.html



------------------------------------------------------------------------
For more information on the algorithms, please refer to the following references:

Chun-Chi Chen, Xiaoning Qian and Byung-Jun Yoon, ?RNAdetect: Efficient computational detection of novel noncoding RNAs? (under review)

Chun-Chi Chen, Xiaoning Qian and Byung-Jun Yoon, ?Effective computational detection of piRNAs using n-gram models and support vector machine?, BMC Bioinformatics, 18(Suppl 14):517. 2017.

Contact: aky3100@tamu.edu, bjyoon@ece.tamu.edu

