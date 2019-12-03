# Repro instructions

```sh
$ cd a
$ go build # success

$ cd ../b
$ go build # success

$ cd ../c
$ time go build -v

go: alltom.com/b@v0.0.0-00010101000000-000000000000 requires
	alltom.com/a@v0.0.0-00010101000000-000000000000: unrecognized import path "alltom.com/a" (https fetch: Get https://alltom.com/a?go-get=1: dial tcp 52.216.205.138:443: i/o timeout)

real	0m30.281s
user	0m0.075s
sys	0m0.036s
```
