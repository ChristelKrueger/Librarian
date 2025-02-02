---
hide:
  - footer
---


### Q: My sample doesn't come up as the library type that I expect. How worried do I need to be?

It depends - there can be a number of reasons for this. It could of course be the case that something has gone wrong with the library preparation and the composition isn't what it should be. These are the cases that we want to catch with a QC tool. However, there may be a number of other scenarios in which the top predicition doesn't match the expected library type: 

- Several library types share simliar compostions. For example, RNA-Seq, ssRNA-Seq and RIP-seq have related input in terms of which parts of the genome they represent. This results in similar base compositions and makes it hard for Librarian to distinguish between them. Check the probability heatmap and see if the expected library type is for example the second most likely prediction.

- The reference data collected from published datasets is dominated by standard, commercially available library preparation kits. If you were using an unsual or custom library preparation, the base composition of your samples may differ from the ones that were used to build the model. For example: The reference data includes some samples which were tagged as RNA-seq but used tagmentation for library preparation. These group with ATAC-seq. If all your samples group with an unexpected library type it may be due to the specifics of library preparation.

- When samples are submitted to GEO only a limited list of library types are available to choose from. These are the types that we have included to build the model. If your sample doesn't match one of the indicated library types, Librarian cannot make a correct prediction.



### Q: My samples isn't from human or mouse. Can I still use Librarian?

A: We chose mouse and human samples to generate the database because of the abundance of published libraries and their similar genomic GC content. While we did not find biases between mouse and human, we found that the predictions were off when using samples from organisms with substantially different GC content. We therefore do **not** recommend using Librarian for other species apart from mouse or human although it seems likely that it would work for more closely related species with similar genomic GC content and biology.



### Q: Can Librarian be used for non-Illumina sequencing technologies?

A: Librarian is specifically for Illumina samples. Other sequencing technologies have very different library types.



### Q: When I use the Librarian web app, will I have to upload the entire FASTQ file?

A: No. Librarian will extract base compositions from a random selection of 100 000 reads. Only the compositions will be submitted to the web server.


### Q: Do you collect any data from samples submitted to the web app?

A: No.


### Q: When I try to upload a file to web app, fastq.gz files are greyed out. Shouldn't this work?

A: This seems to be an issue outside Librarian which we found happens on some Mac/browser combinations. Try drag & dropping the file onto the upload button instead.




