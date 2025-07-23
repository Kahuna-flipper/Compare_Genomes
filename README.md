# compare_assemblies.py

A Python utility to **compare two genome assemblies** (FASTA + GFF) and generate quick summary statistics on assembly quality, sequence similarity, and gene content overlap.  
Can work any FASTA/GFF pairs.

---

## Features

1. **Assembly statistics**:
   - Total genome size
   - Number of contigs
   - N50
   - Average GC%

2. **Average Nucleotide Identity (ANI)**:
   - Uses **Mash**, **fastANI**, or **MUMmer4/dnadiff** (if installed).
   - Falls back gracefully if no tools are available.

3. **Gene content similarity**:
   - Calculates **Jaccard index** of shared gene identifiers or product annotations between the two genomes.

4. **Optional Reciprocal Best Hits (RBH)** mapping:
   - BLASTP-based bidirectional gene mapping (requires `makeblastdb` and `blastp` from BLAST+).

5. **Generates a human-readable comparison report** for quick inspection.

---

## Requirements

### Python dependencies
- Python ≥ 3.7
- [Biopython](https://biopython.org/) (`pip install biopython`)
- [pandas](https://pandas.pydata.org/) (`pip install pandas`)

### External tools (optional but strongly recommended for full functionality)
Install at least one of:
- [Mash](https://mash.readthedocs.io/en/latest/)  
- [fastANI](https://github.com/ParBLiSS/fastANI)  
- [MUMmer4](https://mummer4.github.io/) (for `dnadiff`)  

For reciprocal best hits (optional):
- [NCBI BLAST+](https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/) (`makeblastdb`, `blastp`)

Ensure all executables are available in your `PATH`.

---

## Installation

Clone this repository and install dependencies:
```bash
git clone https://github.com/yourusername/genome-tools.git
cd genome-tools
pip install biopython pandas

=======
# Compare_Genomes
Light-weight python script to compare genome similarity between pairs of organisms
>>>>>>> 1d3ad4dd3be7cfa9c56e4c5fd7e4b95fc71d60d6
