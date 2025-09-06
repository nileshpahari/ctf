## Approach

1. tried to directly cat the 'flag' file but didn't have the read permission
2. looked at fd.c and found out that the buffer (which depends on the file descriptor, which we pass as an arg) should be equal to "LETMEWIN\n" for an unexpected result
3. executed fd with 4660 as 0 is for stdin fd (x1234, whose decimal representation is 4660 was getting subtracted from the arg) and gave "LETMEWIN" as input.
4. it printed the flag

FLAG: Mama! Now_I_understand_what_file_descriptors_are!
