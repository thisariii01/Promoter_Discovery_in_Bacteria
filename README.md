# Promoter Discovery in Bacteria - Azotobacter vinelandii

## Project Overview
This project focuses on identifying promoters in the bacterial genome of *Azotobacter vinelandii* using different sequence alignment techniques. The detection of promoters, which play a crucial role in gene regulation, is performed using local alignment and statistical alignment algorithms. The study aims to compare the effectiveness of these approaches in identifying promoter sequences and analyzing their characteristics.

## Features
- **Genome Data Acquisition**: Extraction of genomic sequences from the NCBI GenBank database.
- **Local Alignment Analysis**: Identification of promoters using a "WWWW" motif.
- **Statistical Alignment Using Position Probability Matrix (PPM)**: Alignment of promoters based on probability matrices.
- **Comparison of Alignment Techniques**: Evaluating the performance of local vs. statistical alignment methods.
- **Visualization**: Histogram plots for promoter positions and lengths.

## Methodology
1. **Data Acquisition**:
   - Downloaded *Azotobacter vinelandii* genome (accession CP001157.1) from NCBI.
   - Extracted 100 bases upstream and 3 bases downstream of coding sequences.

2. **Verification of Sequences**:
   - Checked the presence of Methionine (ATG) start codon.
   - Verified extracted sequences against genomic loci.

3. **Local Alignment**:
   - Detected promoters by aligning the "WWWW" motif within sequences.
   - Applied a match score of 1 and a gap penalty of -2.
   - Identified promoter positions and computed detection percentage.

4. **Promoter Extension Analysis**:
   - Analyzed consecutive "W" extensions to determine promoter lengths.

5. **Position Probability Matrix (PPM) Construction**:
   - Created a 6-base PPM based on detected promoters.
   - Determined consensus sequence and score.

6. **Statistical Alignment**:
   - Computed norm scores using PPM.
   - Detected promoters based on a predefined threshold.

7. **Comparison of Techniques**:
   - Evaluated detection rates and positional distribution of promoters.
   - Analyzed strengths and weaknesses of each method.

## Results
- Local alignment detected promoters in **67.12%** of sequences.
- Statistical alignment detected promoters in **66.28%** of sequences.
- Local alignment favored promoters towards the sequence's end, whereas statistical alignment distributed promoter positions more evenly.

## Dependencies
- Python 3.x
- Biopython
- NumPy
- Matplotlib

## Installation
```bash
# Clone the repository
git clone https://github.com/your-repo/promoter-discovery.git
cd promoter-discovery

# Install dependencies
pip install -r requirements.txt
```

## Usage
1. **Prepare Input Data**: Ensure genome sequences are available in FASTA format.
2. **Run Analysis**:
   ```bash
   python promoter_analysis.py --input genome.fna --output results.txt
   ```
3. **Visualize Results**:
   - Use `matplotlib` to generate promoter position and length distribution histograms.

## Contributors
- **A. T. P. Amarasekara** (University of Moratuwa, Sri Lanka)

## References
- *NCBI GenBank Database*
- *Genomic Signal Processing - BM4321*

