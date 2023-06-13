# OS_Assignment4_Tests

Here are my tests for Assignment 4.
### To run them: 
1) Add the 3 files to /user
2) Add the line $U/_as4_test to the makefile
3) Execution:
    i) Use as4_test to run the tests as they are
    ii) Use the -p flag to generate extra prints which might be helpful to some.
    iii) Use the -seek or -random flags to run only -seek or -random (Obviously using both flags runs everything anyways)
    
### Edge cases:
#### Seek:
###### i) Seeking beyond file size => Should set offset to file size
###### ii) Seeking an offset (be it with whence = SEEK_SET or SEEK_CUR) that's smaller than 0 (I.E. new offset < 0) => Should set offset to 0

#### Random:
###### i) Continuity of generation beyond closing and re-opening of the device
###### ii) Looping through lfsr_char 255 times returns the original value
###### iii) Concurrently reading from the same device by multiple processes
###### iiii) Concurrently reading from some process and writing by another

##### Note that all of the above edge cases are tested, if you pass repeatedly you *should* be okay, *BUT* don't give your full trust to these tests. Test further on your own.

Feel free to suggest more tests by submitting a pull request, or ask about issues here or in the group if you have any.
##### Please do not DM me on random code compilation errors, you should be able to handle them by yourselves. It's probably mostly makefile errors anyways.
