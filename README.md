# ISSEC

ISSEC adopts deep learning to learn specific patterns within predicted inter-residue contacts and subsequently identifies the objects having these patterns as inter-SSE contacts.

## Requirements

- [Python 2.7.14](https://www.python.org/downloads/release/python-2714/)
- [Tensorflow-gpu](https://www.tensorflow.org/install/install_linux)
- [Numpy](https://github.com/numpy/numpy/blob/master/INSTALL.rst.txt)

## Need to do

1. Set your config in `./libs/config/config_v1.py`.
2. Specify your raw data path in `read_into_tfrecord.py`, put your data in the path (Example in `./data/traindata`) and run `python read_into_tfrecord.py` for tfrecord generation.
3. Run `python train.py` for training, model will be saved in `./output`.
4. To test your model on your dataset, you should put the files (`.ccmpred`, `.ss3`, `.pdb` and `.fasta`) of your dataset in `./data/testdata/<dataset name>/`, and run `python test.py -m <model path> -d <dataset name> [options]`; example that `python test.py -m output/new_train_ss3 -d psicov`.
