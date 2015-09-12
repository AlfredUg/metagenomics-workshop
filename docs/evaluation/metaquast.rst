MetaQUAST
=========

QUAST stands for QUality ASsessment Tool. The tool evaluates genome
assemblies by computing various metrics.  You can find all project
news and the latest version of the tool at `sourceforge
<http://sourceforge.net/projects/quast>`_.  QUAST utilizes MUMmer,
GeneMarkS, GeneMark-ES, GlimmerHMM, and GAGE. In addition, MetaQUAST
uses MetaGeneMark, Krona tools, BLAST, and SILVA 16S rRNA
database. See the `QUAST home page <http://quast.bioinf.spbau.ru//>`_
for more info.

To call ``metaquast.py`` we have to provide reference genomes which
are used to calculate a number of different metrics for evaluation of
the assembly. In real-world metagenomics, these references are usually
not available, of course::

  python ~/quast-3.1/metaquast.py --threads 16 --gene-finding --meta \
  -R /mnt/mg-tutorial/genomes/Aquifex_aeolicus_VF5_uid57765.fna,\
  /mnt/mg-tutorial/genomes/Bdellovibrio_bacteriovorus_HD100_uid61595.fna,\
  /mnt/mg-tutorial/genomes/Chlamydia_psittaci_MN_uid175573.fna,\
  /mnt/mg-tutorial/genomes/Chlamydophila_pneumoniae_CWL029_uid57811.fna,\
  /mnt/mg-tutorial/genomes/Chlamydophila_pneumoniae_J138_uid57829.fna,\
  /mnt/mg-tutorial/genomes/Chlamydophila_pneumoniae_LPCoLN_uid159529.fna,\
  /mnt/mg-tutorial/genomes/Chlamydophila_pneumoniae_TW_183_uid57997.fna,\
  /mnt/mg-tutorial/genomes/Chlamydophila_psittaci_C19_98_uid159523.fna,\
  /mnt/mg-tutorial/genomes/Finegoldia_magna_ATCC_29328_uid58867.fna,\
  /mnt/mg-tutorial/genomes/Fusobacterium_nucleatum_ATCC_25586_uid57885.fna,\
  /mnt/mg-tutorial/genomes/Helicobacter_pylori_26695_uid57787.fna,\
  /mnt/mg-tutorial/genomes/Lawsonia_intracellularis_PHE_MN1_00_uid61575.fna,\
  /mnt/mg-tutorial/genomes/Mycobacterium_leprae_TN_uid57697.fna,\
  /mnt/mg-tutorial/genomes/Porphyromonas_gingivalis_W83_uid57641.fna,\
  /mnt/mg-tutorial/genomes/Wigglesworthia_glossinidia_endosymbiont_of_Glossina_morsitans__Yale_colony__uid88075.fna \
  -o quast \
  -l MegaHit,Ray_31,velvet_31,velvet_51,idba_ud \
  megahit_out/final.contigs.fa \
  ray_31/Contigs.fasta \
  velvet_31/contigs.fa \
  velvet_51/contigs.fa \
  idba_ud_out/contig.fa

QUAST generated a HTML reports including a number of interactive graphics. To access there reports, copy the
quast directory to your `public_html` folder::

  cp -r quast ~/public_html

After that, the reports are available at

  http://YOUR_AWS_IP/~ubuntu/quast/summary
  http://YOUR_AWS_IP/~ubuntu/quast/summary


