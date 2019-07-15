Data in __train_dataset.dat__



# Execute

```
docker build -t local/libsvm .
docker run -it --rm -v $(pwd):/code -w /code local/libsvm sh
```

## epsilon-SVR with RBF

```
export OMP_NUM_THREADS=4
svm-train -s 3 -t 2 -g 0.1 -c 1 -e 0.0001 -h 0 train_dataset.dat
```


## nu-SVR with RBF

```
export OMP_NUM_THREADS=4
svm-train -s 4 -t 2 -g 0.1 -c 1 -n 0.5 -e 0.0001 -h 0 train_dataset.dat
```
