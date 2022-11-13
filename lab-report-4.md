# Lab Report 4
## Part 1 - Changing DocSearchServer.java

I chose to change the name of the `start` parameter and all of its uses to `base`.

***Complete Sequence of Keys:*** `vim DocSearchServer.java<Enter>/start<Enter>cebase<Esc>n.n.:wq<Enter>`
- Type `vim DocSearchServer.java` into the terminal command line ![`vim DocSearchServer.java`](LabReport_4.1.png)
- Press `<Enter>` to open *DocSearchServer.java* in vim ![`Enter`](LabReport_4.2.png)
- Type `/start` to begin search ![`/start`](LabReport_4.3.png)
- Press `<Enter>` to execute search, and the cursor jumps to the first instance of *start* ![`<Enter>`](LabReport_4.4.png)
- Type `ce` to enter Insert Mode and delete the word *start* ![`ce`](LabReport_4.5.png)
- Type `base` ![`base`](LabReport_4.6.png)
- Press `<Esc>` to exit Insert Mode ![`<Esc>`](LabReport_4.15.png)
- Type `n` to jump to next instance of *start* ![`n`](LabReport_4.7.png)
- Type `.` to excute the last command done in InsertMode, which deleted the word *start* and added *base* ![`.`](LabReport_4.8.png)
- Type `n` to jump to next instance of *start* ![`n`](LabReport_4.9.png)
- Type `.` to replace *start* with *base* ![`.`](LabReport_4.10.png)
- Type `:wq` to save file and exit vim ![`:wq`](LabReport_4.16.png)
- Press `<Enter>` to execute `:wq` and return back to the terminal command line ![`:wq`](LabReport_4.14.png)

## Part 2

It took 7 min and 17 seconds for me to use `scp` to modify the DocSearchServer.java file, and 1 min 34 seconds using vim. 
