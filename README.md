#!/bin/bash
set -euo pipefail
fdump=sratoolkit.2.10.5-ubuntu64/bin/fastq-dump
sra=DRR006760.sra
fq1=DRR006760_1.fastq
fq2=DRR006760_2.fastq

{fdump} --split-files ${sra}
gzip ${fq1}
gzip ${fq2}
