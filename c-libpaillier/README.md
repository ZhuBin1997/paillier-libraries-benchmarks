### Building the library

Run the following to build the libpaillier library:
```
cd libpaillier-0.8
./configure
make
cd ..
```
which on AWS must be done with the path to GMP explicitly specified:
```
cd libpaillier-0.8
./configure --with-gmp-include=/usr/include/x86_64-linux-gnu/ --with-gmp-lib=/usr/lib/x86_64-linux-gnu/
make
cd ..
```


### Building the bench

```
gcc -O3 bench.c libpaillier-0.8/paillier.o -Ilibpaillier-0.8 -lgmp -o bench
```


### Running the bench
```
./bench
```