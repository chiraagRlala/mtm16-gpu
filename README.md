# mtm16-gpu

## Theano

```
virtualenv theano-py3 --system-site-packages --python=python3
. theano-py3/bin/activate
pip install theano
```

```
python -m ipykernel install --user --name theano-py3 --display-name "Python (py3)"
mkdir -p ~/.ipython/kernels
mv ~/.local/share/jupyter/kernels/theano-py3 ~/.ipython/kernels/theano-py3
```
