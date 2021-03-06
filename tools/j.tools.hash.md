<!-- toc -->
## j.tools.hash

- /opt/jumpscale7/lib/JumpScale/baselib/hash/HashTool.py

### Methods

#### def crc32 

##### arguments

- path

##### comments

```
Calculate CRC32 hash of data available in a file

The file will be opened in read/binary mode and blocks of the blocksize
used by the hashing implementation will be read.

@param path: Path to file to calculate content hash
@type path: string

@returns: CRC32 hash of data available in the given file
@rtype: number

```

#### def crc32_string 

##### arguments

- s

##### comments

```
Calculate CRC32 hash of input string

@param s: String value to hash
@type s: string

@returns: CRC32 hash of the input value
@rtype: number

```

#### def hashDir 

##### arguments

- rootpath

##### comments

```
walk over all files, calculate md5 and of sorted list also calc md5 this is the resulting
    hash for the dir independant from time and other metadata (appart from path)

```

#### def md5 

##### arguments

- path

##### comments

```
Calculate %(alg)s hash of data available in a file

The file will be opened in read/binary mode and blocks of the blocksize
used by the hashing implementation will be read.

@param path: Path to file to calculate content hash
@type path: string

@returns: %(alg)s hash hex digest of data available in the given file
@rtype: string

```

#### def md5_string 

##### arguments

- s

##### comments

```
Calculate %(alg)s hash of input string

@param s: String value to hash
@type s: string

@returns: %(alg)s hash hex digest of the input value
@rtype: string

```

#### def sha1 

##### arguments

- path

##### comments

```
Calculate %(alg)s hash of data available in a file

The file will be opened in read/binary mode and blocks of the blocksize
used by the hashing implementation will be read.

@param path: Path to file to calculate content hash
@type path: string

@returns: %(alg)s hash hex digest of data available in the given file
@rtype: string

```

#### def sha1_string 

##### arguments

- s

##### comments

```
Calculate %(alg)s hash of input string

@param s: String value to hash
@type s: string

@returns: %(alg)s hash hex digest of the input value
@rtype: string

```

#### def sha256 

##### arguments

- path

##### comments

```
Calculate %(alg)s hash of data available in a file

The file will be opened in read/binary mode and blocks of the blocksize
used by the hashing implementation will be read.

@param path: Path to file to calculate content hash
@type path: string

@returns: %(alg)s hash hex digest of data available in the given file
@rtype: string

```

#### def sha256_string 

##### arguments

- s

##### comments

```
Calculate %(alg)s hash of input string

@param s: String value to hash
@type s: string

@returns: %(alg)s hash hex digest of the input value
@rtype: string

```

#### def sha512 

##### arguments

- path

##### comments

```
Calculate %(alg)s hash of data available in a file

The file will be opened in read/binary mode and blocks of the blocksize
used by the hashing implementation will be read.

@param path: Path to file to calculate content hash
@type path: string

@returns: %(alg)s hash hex digest of data available in the given file
@rtype: string

```

#### def sha512_string 

##### arguments

- s

##### comments

```
Calculate %(alg)s hash of input string

@param s: String value to hash
@type s: string

@returns: %(alg)s hash hex digest of the input value
@rtype: string

```

