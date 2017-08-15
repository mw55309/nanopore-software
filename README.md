# nanopore-software
A list of software for Oxford Nanopore data

### Moving data

* Robocopy.exe (Windows)
  * Installed on all Windows machines
  * File synchronisation tool run from within the cmd.exe command prompt
```dos
C:\Users\Mick> C:\Windows\System32\robocopy.exe C:\data\reads Z:\path\to\my\network\share /MIR /FFT /Z /XA:H /W:5
```
* rsync (Windows)
  * Can be (optionally) installed with [Cygwin](https://www.cygwin.com/)
  * run from within the cmd.exe command prompt or Cygwin Terminal
```sh
rsync -avP C:/data/reads mwatson9@myserver.ac.uk:/path/to/my/data
```
* rsync (Windows 10)
  * It is possible to install an entire Ubuntu sub-system on Windows 10
  * C:\ drive is accessible within bash from /mnt/c/
```sh
rsync -avP /mnt/c/data/reads/ mwatson9@myserver.ac.uk:/path/to/my/data
```
* rsync (Linux or Mac)
  * Terminal/shell available on both
```sh
rsync -avP /path/to/fast5/ mwatson9@myserver.ac.uk:/path/to/my/data
```

### Basecalling

### QC

### Extract data from FAST5

### Mapping / Aligning

### Variant Calling

### Assembly

### Polishing

### Scaffolding

### Structural variants

### Pipelines
