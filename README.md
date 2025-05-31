# 2025-Geroscience

Aging and cognitive impairment increase the risk for Alzheimer’s disease (AD), and growing evidence shows that transposable elements (TEs) in the genome play a role in aging and AD. The mechanisms of TE dysregulation in this context are unclear, but one possibility is that epigenetic changes, including DNA hypomethylation and/or reduced chromatin structure, underlie age- and AD-related TE activity. 

The purpose of the present study was to: 1) generate a resource that could be used to study TE epigenetics in aging and AD; and 2) determine if epigenetically dysregulated TEs are related to age/AD-relevant clinical outcomes. 

We performed RNA-seq on peripheral blood/cell samples from 45 healthy older adults, mild cognitive impairment (MCI) and AD dementia patients, and we observed a pattern of undulating TE transcript expression with MCI and AD, consistent with previous reports. We then used whole-genome bisulfite sequencing (WGBS) and transposase-accessible chromatin sequencing (ATAC-seq) to characterize global DNA methylation and chromatin accessibility in the same subjects. We found that most TEs that were enriched/dysregulated in our RNA-seq data with MCI and AD could be found within hypomethylated and chromatin-accessible regions of the genome.

Transcriptomic analyses of TE transcripts used the standard TEtranscripts pipeline. More information on this program and its dependencies can be found through the Hammell Lab website (https://www.mghlab.org/software/tetranscripts)


ATAC-seq analyses followed a standard MACS2 pipeline. If MACS2 is not installed, pip can be used as shown below:
More information on MACS2 can be found at: https://pypi.org/project/MACS2/


WGBS analyses used the MethPipe software package, which has since been retired. More information on MetPipe can be found here: https://github.com/smithlabcode/methpipe
However, future analyses may with to use the newer package, DNMTools (https://github.com/smithlabcode/dnmtools)

To determine if dysregulated TE transcripts were potentially originating from hypomethylated and/or chromatin-accessible genome regions, we intersected the epigenomic alignment data (peaks for ATAC-seq and dmrs for WGBS) with a human genome repeatmasker bed file that contains locations of each insertion/instance.
Bedtools was utilized through the intersect function. More information on the bedtools intersect program, see https://bedtools.readthedocs.io/en/latest/content/tools/intersect.html
