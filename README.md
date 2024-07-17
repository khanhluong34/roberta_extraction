
To train the RoBERTa model, first download the pretrained weights from [here](https://dl.fbaipublicfiles.com/fairseq/models/roberta.large.tar.gz) and uncompress the tar file so that the `roberta.large/` is placed in this directory. Then you can preprocess, train, and extract the context-independent feature vectros for the IEMOCAP dataset as follows:

```bash
python init_iemocap.py
bash preprocess_iemocap.sh
bash train_iemocap.sh
python feature_extract_iemocap.py
```

The features will be saved in the `iemocap/` directory.

Use the other corresponding scripts to extract the features for the other datasets. You can then use the COMET and RoBERTa features to train the models using the scripts in `COSMIC/erc-training`. For reproduction of our results, we provide the features that we used in our experimets [here](https://drive.google.com/file/d/1TQYQYCoPtdXN2rQ1mR2jisjUztmOzfZr/view?usp=sharing).