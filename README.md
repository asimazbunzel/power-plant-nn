# Power plant output

In this repository, a simple multilayer perceptron (MLP) neural network (NN) is implemented to
predict the energy output in a power plant based on 4 independent features

The dataset comes from the [UCI Irvine Machine Learning Repository](https://archive.ics.uci.edu/),
called Combined Cycle Power Plant, this [link](https://archive.ics.uci.edu/dataset/294/combined+cycle+power+plant)

## Dependencies

Modules needed to run:

* numpy
* pandas
* scikit-learn
* tensorflow
* matplotlib
* jupyter

One more dependency:

* openpyxl -> needed to open xlsx files in pandas

Recommended way: install them in a separate conda environment that will automatically handle
versions between dependencies:

```
conda create -n nn-3.11 python=3.11 numpy pandas scikit-learn tensorflow matplotlib openpyxl jupyter
```

## Issues found

When trying to run from a conda environment in my computer, `scipy` had an error,
`version 'GLIBCXX_3.4.30' not found`. To solve this issue, I preppended a location to the
environment variable `LD_LIBRARY_PATH`: `LD_LIBRARY_PATH=/path-to-your-conda/envs/your-env-name/lib:$LD_LIBRARY_PATH`

In my case, I have conda installed in `~/.local/bin`, so the solution for me was:
`LD_LIBRARY_PATH=~/.local/bin/conda/lib:$LD_LIBRARY_PATH`
