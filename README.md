# insurance_qa_python

### About

Insurance QA data formatted as Python objects and pickled.

### Example usage

Clone locally

```bash
git clone https://github.com/codekansas/insurance_qa_python.git
cd insurance_qa_python
pwd # where files are stored
```

Load a file in Python

```python
import pickle

def load(file_name):
  return pickle.load(open(os.path.join(path, file_name), 'rb'))
```

About files:

 - `vocabulary`: `dict` object of `(word index <int> -> word <str>)` relationships
 - `answers`: `dict` object of `(answer index <int> -> word indices <list of ints>)` relationships
 - `train`: `list` of `dict` (one `dict` per entry), where each `dict` has:
   - `question`: the word indices for the question
   - `answers`: the answer indices for each of the question's ground truth
 - `dev / test1 / test2`: `list` of `dict` (one `dict` per entry), where each `dict` has:
   - `question`: the word indices for the question
   - `good`: the ground truth
   - `bad`: the other answers from the dataset

### Resources
 - [Original Github page](https://github.com/shuzi/insuranceQA)
 - [arXiv paper](http://arxiv.org/abs/1508.01585)

### Cite

    Applying Deep Learning to Answer Selection: A Study and An Open Task
    Minwei Feng, Bing Xiang, Michael R. Glass, Lidan Wang, Bowen Zhou ASRU 2015
