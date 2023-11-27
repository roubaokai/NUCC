# NUCC
NUCC is a novel tumor neoantigen prediction tool for personalized vaccine design

## NUCC training code.ipynb
This is a training source code example that provides a detailed explanation of the steps involved in obtaining the NUCC model.

## training.zip
This is a training dataset resource package. It comprises a collection of antigen peptides-MHC selected through screening from the IEDB database. It is presented as a CSV table with "Assay" serving as the label (where "Positive" represents positive peptides, and "Negative" represents negative peptides). The selected features include "Epitope," "MHC," "MixMHCpred Score," "Aff(nM)," and "Thalf(h)."

## testing.zip
This is a compressed package of a test dataset, containing a collection of antigen peptides-MHC synthesized and validated in vitro by the Tumor Neoantigen Alliance and the Ronsenberg team. Similar to the training set, "Assay" serves as the label (where "Positive" represents positive peptides, and "Negative" represents negative peptides), and the selected features include "Epitope," "MHC," "MixMHCpred Score," "Aff(nM)," and "Thalf(h)."

## NUCC model.h5
This is an H5 model file saved after training using the code in "NUCC training code.ipynb." It can be loaded using the statement tf.keras.models.load_model(). When making predictions, the test set should be processed using the code in "NUCC training code.ipynb," and then predictions can be obtained using the statement NUCC model.predict(). The NUCC model will output immunogenicity scores for each peptide in the test set.
