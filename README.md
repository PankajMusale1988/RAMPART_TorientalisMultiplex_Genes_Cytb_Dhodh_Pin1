RAMPART_Theileria_orientalis_multiplex_genes_cytb_dhodh_pin1. This repository contains comprehensive scripts for analysis of the Theileria annulata multiplex genes cytb (cytochrome b), dhodh (dihydroorotate dehydrogenase), and pin1 (peptidyl-prolyl cis-trans isomerase NIMA-interacting 1). The repository aims to provide realtime nucleotide level mapping of nanopore sequencing to the reference sequences.

Complete Installation and Setup Process:

# Step 1: Install Miniconda
Download the Miniconda installer
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

# Run the installer
bash Miniconda3-latest-Linux-x86_64.sh

Follow the prompts to complete the installation
# Step 2: Clone the ARTIC pipeline repository
git clone https://github.com/artic-network/fieldbioinformatics.git cd fieldbioinformatics

# Step 3: Create the Conda environment
conda env create -f environment.yml conda activate artic-ncov2019

# Step 4: Install additional dependencies
conda install -c bioconda samtools

Running RAMPART with the Set Up Environment: Go to the folder containing the fastq_pass files

# Step 1: Activate Conda Environment
conda activate artic-ncov2019

# Step 2: Index the Reference FASTA
samtools faidx reference.fasta

# Step 3: Run RAMPART
rampart --protocol /path_to_folder_rampart_files/ --basecalledPath fastq_pass/

# Alternative command if default ports are in use
rampart --protocol /path_to_folder_rampart_files/ --basecalledPath fastq_pass/ --ports 3002 3004

# Contributing
Contributions to improve the script or add new features are welcome. 
Please fork the repository, make your changes, and submit a pull request or open an issue for discussion.
