Mineral
=======

MINimal Embedded sysRoot using Alpine Linux.

Let's you very quickly setup a sysroot with...
- ...any number of Alpine packages installed.
- ...running any architecture supported by Alpine.
- ...without requiring any special privileges.

As an example, on an `x86_64` system, we can easily setup a `aarch64`
sysroot and run a command inside it like so:

```
~/src/github.com/wkz/mineral$ uname -m
x86_64
~/src/github.com/wkz/mineral$ ./mineral init -a aarch64
fetch http://dl-cdn.alpinelinux.org/alpine/latest-stable/main/aarch64/APKINDEX.tar.gz
(1/19) Installing musl (1.1.24-r0)
(2/19) Installing busybox (1.31.1-r9)
Executing busybox-1.31.1-r9.post-install
(3/19) Installing alpine-baselayout (3.2.0-r3)
Executing alpine-baselayout-3.2.0-r3.pre-install
Executing alpine-baselayout-3.2.0-r3.post-install
(4/19) Installing openrc (0.42.1-r2)
Executing openrc-0.42.1-r2.post-install
(5/19) Installing alpine-conf (3.8.3-r4)
(6/19) Installing libcrypto1.1 (1.1.1d-r3)
(7/19) Installing libssl1.1 (1.1.1d-r3)
(8/19) Installing ca-certificates-cacert (20191127-r0)
(9/19) Installing libtls-standalone (2.9.1-r0)
(10/19) Installing ssl_client (1.31.1-r9)
(11/19) Installing zlib (1.2.11-r3)
(12/19) Installing apk-tools (2.10.4-r3)
(13/19) Installing busybox-suid (1.31.1-r9)
(14/19) Installing busybox-initscripts (3.2-r2)
Executing busybox-initscripts-3.2-r2.post-install
(15/19) Installing scanelf (1.2.4-r0)
(16/19) Installing musl-utils (1.1.24-r0)
(17/19) Installing libc-utils (0.7.2-r0)
(18/19) Installing alpine-keys (2.1-r2)
(19/19) Installing alpine-base (3.11.3-r0)
Executing busybox-1.31.1-r9.trigger
OK: 8 MiB in 19 packages
~/src/github.com/wkz/mineral$ ./mineral exec uname -m
aarch64
~/src/github.com/wkz/mineral$ 
```
