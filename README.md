# hexeditplus
simple hexedit like program to edit and display binary files.
### Usage example
<pre> ./hexeditplus abc</pre>
Then the following will be displayed:
```
File: abc, choose action:
1-Mem Display
2-File Display
3-File Modify
4-Copy from File
5-Quit
```
If `Mem Display` was chosen prompt will be:
```
1
Please enter <address> <length> 
8048570 10
```
The output should look something like this:
```
31 ED 5E 89 E1 83 E4 F0 50 54
```

If the user chooses 2, he is prompted for location and length. It should look as follows: 
```
2
Please enter <location> <length>
12F 10
```
The program should open the file [abc](https://www.cs.bgu.ac.il/~caspl132/wiki.files/lab7/abc) and print the 10 bytes, from byte 303 to byte 312 in the file. The output should look like: 
```
00 01 00 00 00 2F 6C 69 62 2F
```
 After the user chooses 3 with location "12F" and val "2D" - the value of that byte will be 0x2D. The prompt should look as follows: 
 ```
3
Please enter <location> <val>
12F 2D
```
Running option 2 again should print:
```
2D 01 00 00 00 2F 6C 69 62 2F
```
For example, choosing option "4-Copy from File" using file afile, s-location 102, t-location 33 and length 4, the program should read length = 4 bytes of afile, starting at offset 0x102, and write them to the file abc, starting from offset 0x33 (overwriting what was originally there). It should look as follows: 
```
4
Please enter <source-file> <s-location> <t-location> <length>
afile 102 33 4
```
