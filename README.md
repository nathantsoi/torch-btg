# Bridging the Gap: Unifying the Training and Evaluation of Neural Network Binary Classifiers

A PyTorch implementation of Bridging the Gap (BtG) losses including F-beta (F1), Accuracy, and AUROC.

## Usage

Install the `torch-btg` package:

```
pip install torch-btg
```

Use the desired loss in your code, for example,

- `F1-loss`:
```
from torch_btg.loss import fb_loss
...
criterion = fb_loss(beta=1.0)
...
```

- `Accuracy loss`:
```
from torch_btg.loss import accuracy_loss
...
criterion = accuracy_loss()
...
```

- `AUROC loss`:
```
from torch_btg.loss import auroc_loss
...
criterion = auroc_loss()
...
```

## Project Details

Project Webpage: [btg.yale.edu](https://btg.yale.edu)

[PDF Paper](https://btg.yale.edu/papers/Bridging_the_Gap_Unifying_the_Training_and_Evaluation_of_Neural_Network_Binary_Classifiers.pdf)

Citation:

```
@inproceedings{tsoi2022bridging,
  title         = {Bridging the Gap: Unifying the Training and Evaluation of Neural Network Binary Classifiers},
  author        = {Tsoi, Nathan and Candon, Kate and Li, Deyuan and Milkessa, Yofti and V{\'a}zquez, Marynel},
  booktitle     = {Advances in Neural Information Processing Systems},
  year          = {2022}
}
```

## Development

### Setup

```
python3 -m pip install --user tox
python3 -m pip install --upgrade build
python3 -m pip install --upgrade twine
```

#### Run tests

```
tox
```

#### Build

```
python3 -m build
```

#### Publish

```
python3 -m twine upload --repository pypi dist/*
```

Username: `__token__`
Password: `[the api key from pypi.org starting with pypi-]`