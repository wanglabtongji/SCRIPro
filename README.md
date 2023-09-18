# SCRIPro

[![Documentation Status](https://readthedocs.org/projects/scripro/badge/?version=latest)](https://scripro.readthedocs.io/en/latest/?badge=latest)


The increasing availability of single-cell genomics data allows characterizing gene regulation networks (GRNs) at an unprecedented resolution. Previously we developed SCRIP, a computational method that integrates single-cell ATAC-seq data with a large-scale transcription regulator (TR) ChIP-seq data and motif reference for reconstructing single-cell TR activities and GRNs. Here, we present SCRIPro, an extended framework of SCRIP that suits both single-cell and spatial multi-ome data. SCRIPro first performed a density clustering based on expression and spatial similarity of the data to generate high coverage SuperCells. Next, SCRIPro performed in silico deletion analyses based on matched scATAC-seq or reconstructed chromatin landscapes from Cistrome accessibility data to evaluate the importance of TRs in regulating each SuperCell. Finally, SCRIPro combines the importance score of each TR with its gene expression using GRNBOOST2, which generates the TR-centered GRNs at Supercell resolution. We applied SCRIPro on human PBMC and human B-cell lymphoma scMulti-ome data, as well as mouse developing embryo spatial transcriptomic data, and demonstrated that SCRIPro is able to identify cell-type-specific TR regulations and show superior performance compared to conventional motif-based methods such as SCENIC+. Taken together, SCRIPro is a convenient and fast method that could reconstruct TR activities and GRNs for both single-cell and spatial multi-omic data.

![avatar](docs/_static/img/workflow_new.png)


PyPI
~~~~

It is recommended to install lisa to a virtual environment:

.. code-block:: bash

  $ python3 -m venv .venvs/lisa_env
  $ source .venvs/lisa_env/bin/activate
  
Install LISA to this virtual env using this command:

.. code-block:: bash

  (lisa_env) $ pip install lisa2

Conda
~~~~~

