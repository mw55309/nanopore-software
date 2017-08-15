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
  * It is possible to install an entire [Ubuntu sub-system on Windows 10](https://msdn.microsoft.com/en-gb/commandline/wsl/install_guide)
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

* Albacore
  * Available from the [Oxford Nanopore community](https://community.nanoporetech.com/)
```sh
# run with -l to figure out which model to use
read_fast5_basecaller.py -l

# run the basecaller
read_fast5_basecaller.py -i /vol/raw_fast5/ \
                         -r \
                         -t 4 \
                         -s output_dir \
                         -o fastq,fast5 \
                         -c r94_450bps_linear.cfg \
                         --barcoding
```

### QC
* minion_qc
  * [code](https://github.com/roblanf/minion_qc)
* NanoFilt
  * [blog](https://gigabaseorgigabyte.wordpress.com/2017/06/05/trimming-and-filtering-oxford-nanopore-sequencing-reads/)
* PoreChop
  * PoreChop
  * [code](https://github.com/rrwick/Porechop)

### Extract data from FAST5
* poretools
* poRe
* NanoOK

### Mapping / Aligning
* bwa mem
* LAST
* GraphMap
* MiniMap2
* NGMLR

### Variant Calling
* Nanopolish

### Assembly
* SPAdes
* Minimap / miniasm
* Canu

### Polishing
* Nanopolish

### Scaffolding
* SSPACE-LongReads
* LINKS

### Structural variants
* Sniffles 

### Pipelines
