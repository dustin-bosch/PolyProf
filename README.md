# PolyProf
Polymorphic toxin effector and immunity metagenome profiler

# Software dependencies
HUMAnN 3.0
https://huttenhower.sph.harvard.edu/humann/
https://elifesciences.org/articles/65088

DIAMOND
http://ab.inf.uni-tuebingen.de/software/diamond
https://www.nature.com/articles/nmeth.3176

# Installation
Use the pre-constructed DIAMOND marker protein database polymorphic_profiler_database.dmnd
OR
Construct a marker gene database from database_sequences_1.fasta, which can be expanded with new sequences and effector/immunity families

  diamond makedb --in database_sequences_1.fasta -d <output directory>

# Run HUMAnN with a custom marker protein database

  humann -i <metagenome.fastq> -o <output_directory> --protein-database <path_to_DIAMOND_database> --bypass-nucleotide-search
