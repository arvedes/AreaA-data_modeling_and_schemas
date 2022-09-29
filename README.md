# Area A: sample preparation data

## Keywords:  

### Electronic Lab Notebook (ELN) / Application definition / Schemes / Data structures  

- - - -

This is a collection of blueprint schemes that include several kinds of experiment.  

The schemes here implemented are compliant to the NOMAD data structure: the hierarchy is composed by Sections, Subsections and Quantities (data fields).

The users can follow the info in this repo to build their own schema for their experiment :thumbsup:.

Some further explanation on NOMAD Metainfo and Archive: https://nomad-lab.eu/prod/v1/staging/docs/archive.html#custom-metainfo-schemas-eg-for-elns

Each folder contains four categories of files, the user can try to drag and drop all of them in the upload page in nomad ([https://nomad-lab.eu/](https://nomad-lab.eu/)), they will be automatically parsed to create an "Entry" containing the experimental data in a structured fashion:

* schema file: it defines the structure that will host your data.
  The schema file has **.schema.archive.yaml** extension.

* data file: based on the schema file, it contains the actual data or links to metadata files, logfiles, dataset from instrument that will be parsed into your experiment Entry. The data file has **.data.archive.yaml** extension.

* data set: depending on the outcomes of the experiment, the user will have one or more files where the monitored parameters and metadata are stored. The data set files have **.txt.**, **.dat**, **.csv** or **.xlsx** extension.

* base classes: sections with fixed structure collected in base_classes folder, the user will find a zipped copy of this base_classes folder that must be included in the upload.

- - - -

In the subfolders, a dedicated README documents the file set for each use case.

- - - -
## The Structured Use Cases:

category | experiment | folder name
-|-|-|
Crystal Growth | Float Zone| FZ_IKZ
Crystal Growth | Melt Czochralski | melt_czochralski_Dadzis
Crystal Growth | Melt Czochralski | melt_czochralski_Dropka
Precursor Preparation | Oxide Powder | oxide_powder_preparation
Epitaxial Growth | Metalorganic vapour-phase epitaxy Strontium Lantanium Oxide (MOVPE-SrTiO) | movpe_STO
Epitaxial Growth | Metalorganic vapour-phase epitaxy Gallium Oxide (MOVPE-Ga2O3) | movpe_Ga2O3
Epitaxial Growth | Molecular Beam Epitaxy (MBE) | mbe_epitaxy
Sol-Gel Synthesis | Aerogels | wai_synthesis
Electric properties | Hall Measurements | hall
Database | Material_db from IKZ | material_db_IKZ
Surface Coating | Spin-coating | surface_coating_methods
Surface Coating | Dip-coating | surface_coating_methods
Surface Coating | Sputtering | surface_coating_methods
Surface Coating | Evaporation | surface_coating_methods
Transmission | Transmission measurements | transmission
Various | Experiments permormed in Max Planck Institute for Chemical Physics of Solids in Dresden | CPFS-Dresden

- - - -

## A Schema Prototype

### Base Sections (or Base Classes):

![Base Classes](https://box.hu-berlin.de/f/4582a93e93314b5b8dbd/?dl=1)

These base section have got an <em>a priori</em> **inheritance** structure. The user can further decide how to put together this bricks by means of **referencing**. 
