# mtm16-gpu

## SGE

Connect to one of following with your *mtm* account:

```
ssh freki.ufal.ms.mff.cuni.cz
ssh geri.ufal.ms.mff.cuni.cz
ssh ufallab.ms.mff.cuni.cz
```

Connect to random *solX* node with `cluster` command.

```
qstat
qstat -u '*' -q gpu.q
qsub -N job_name -V -cwd -b y -j y "commnad; another_command"
qdel
```

- `-V` exports environment variables to the qsub job
- for unbuffred output: `python -u`
- to exclude Titan: `qsub -l h=!titan-gpu` or use 2 slots (somewhat complicated on SGE)

## Theano

Run this on *solX*

```
virtualenv venv --system-site-packages
. venv/bin/activate
pip install theano
```

`THEANO_FLAGS='device=cuda'`
