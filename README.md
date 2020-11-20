# A useless example

This is an example of the absolute minimum needed to create an OpenSSL
engine using autoconf, automake and libtool

## Build

Build as follows:

    $ gcc -fPIC -o e_useless.o -c e_useless.c
	$ gcc -shared -o e_useless.so -lcrypto e_useless.o

A quick and easy test goes like this:

    $  openssl engine -t -c `pwd`/e_useless.so

And you can see the output like this:

```shell
A useless engine for demonstration purposes
Loaded: (useless) A useless engine for demonstration purposes
     [ available ]
```

Considering this engine has no futher use, we'll stop here.
