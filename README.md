# openai-playground

This repository demonstrates a simple SNP calling workflow using Snakemake.

## Usage

All workflow files now live in the `codes-snakefile/` directory. To run the
pipeline:

1. Place your sample FASTA files in `codes-snakefile/data/raw/`.
2. Provide a reference genome at `codes-snakefile/reference/genome.fasta`.
3. Execute Snakemake from within that folder:
   ```bash
   cd codes-snakefile
   snakemake --use-conda --cores 4
   ```

Intermediate results are stored in numbered folders (`000.fasta`, `010.fastqc`,
`020.align`, etc.) inside `codes-snakefile/`. A final MultiQC report is
generated in `codes-snakefile/999.reports/`.
