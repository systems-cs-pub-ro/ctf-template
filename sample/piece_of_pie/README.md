Name: Piece of Pie

Description
-----------

It's simple: get the flag.

  Hint 1: That's some pretty weird `read()` call you use.
  Hint 2: You already have the bits you need in the executable.

  Score: 50

Vulnerability
-------------

  There is a buffer overflow vulnerability. Overwrite the return address with the address of the `system("/bin/sh")` call conveniently placed in the binary. End up calling `system("/bin/sh").` and then getting the flag.

Exploit
-------

  Script in `./sol/exploit.py`

Environment
-----------

  64-bit, ASLR on, DEP on, stack guard off

Deploy
------

Use a classical xinetd-based approach for deployment. Place flag in `/home/ctf/flag` folder.
