# OSG-EVOLINC-I: A rapid Long-Intergenic Noncoding RNA (lincRNA) detection pipeline using the Open Science Grid and CyVerse

## Introduction

Evolinc-I is a long intergenic noncoding RNA (lincRNA) identification workflow that also facilitates genome browser visualization of identified lincRNAs and downstream differential gene expression analysis. 

The OSG is a consortium of research communities which facilitates distributed high throughput computing for scientific research. The Open Science Grid (OSG) enables distributed computing at more than 120 institutions, supports efficient data processing and provides large scale scientific computing of more than 2 million CPU hours per day. More about OSG can be found here

## How do the OSG and DE help EVOLINC-I?

EVOLINC-I is currently available as a Docker image and also as an app in CyVerse's Discovery Environment (DE). Many users find using EVOLINC-I in the DE to be quite useful because the DE provides a GUI (graphical user interface) for the RMTA tool and is coupled with CyVerse's Data store for storing the data. In addition, running jobs within the DE removes the computational requirements for running the analysis from the user. However, processing thousands of RNA-seq datasets in the DE is limited to the concurrent job restrictions in place (there is a limit of 8 concurrent jobs). 

Thus, for processing large data sets in a timely manner, the OSG serves as the perfect alternative to the DE. However, jobs submitted to the OSG typically require command-line experience. In order to allow users with minimal command-line experience to address their large RNA-seq data set questions, we have developed OSG-EVOLINC-I which is a highly scalable RMTA for identifying long-noncoding RNA from RNA-Seq data using computational resources available to U.S-based researchers on the OSG. Users familiar with command line can run the OSG-EVOLINC-I workflow directly on the OSG by submitting the jobs to the HTCondor or run it in CyVerse Discovery Environment as the OSG-EVOLINC-I app. Running jobs through CyVerse's DE is recommended because these jobs are decomposed into multiple tasks that can be carried out in parallel. In sum, input data transfers from the DE to the OSG, compute tasks (read mapping and transcript assembly) are performed on the OSG, and then results are returned to CyVerse's Datastore.  

OSG-Evolinc-I minimally requires the following input data

1. A set of assembled and merged transcripts from Cuffmerge or Cuffcompare in gene transfer format (GTF)
2. A reference genome (FASTA)
3. A reference genome annotation (GFF/GTF/GFF3)

Optional input data

1. Transposable Elements database (FASTA)
2. Known LincRNA (GFF)
3. Transcription start site coordinates (BED)

# Availablility

## OSG-EVOLINC-I in CyVerse's DE

The OSG-EVOLINC-I-v1.7.4 app is currently integrated in CyVerse’s Discovery Environment (DE) and is free to use by researchers. Register for a free account at [CyVerse](https://user.cyverse.org). The complete tutorial is available at this location [CyVerse wiki](https://wiki.cyverse.org/wiki/display/DEapps/OSG-EVOLINCI+v1.7.4). CyVerse's DE is a free and easy to use GUI that simplifies many aspects of running bioinformatics analyses. If you do not currently have access to a high performance computing cluster, consider taking advantange of the DE. You can submit thousands of jobs using the OSG-EVOLINC-I v1.7.4 app and they will run on OSG instead of on the DE.

## OSG-EVOLINC-I on OSG

The OSG-EVOLINC-I-v1.7.4 Docker image app is currently available on the OSG and is free to use by researchers. In order to run OSG-RMTA on OSG, you first need to have an account with OSG. Register for a free account at [osg-connect](http://osgconnect.net/). After you register, you need to add your keys because OSG no longer allows password access. You can find more information [here](https://support.opensciencegrid.org/support/solutions/articles/12000027675-generate-ssh-key-pair-and-add-the-public-key-to-your-account). 

The complete tutorial for running OSG-EVOLINC-I on the OSG is available in [here](https://hackmd.io/s/HJDaVO1QN).

# Issues

If you experience any issues with running OSG-Evolinc-I (DE app or source code or Docker image), please open an issue on this github repo. Alternatively post your query or future requests in this [google group](https://groups.google.com/forum/#!forum/evolinc)

# Copyright free

The sources in this [Github](https://github.com/Evolinc/OSG-Evolinc-I) repository, are copyright free. Thus you are allowed to use these sources in which ever way you like. Here is the full [MIT](https://choosealicense.com/licenses/mit/#) license.
