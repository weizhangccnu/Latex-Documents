### 1. Complie .tex file command
```
pdflatex LOCld55_Design_Document.tex
```
### 2. Auto generate bibliography
  - Add cite package
```
\usepackage{cite}
```
  - Edit LOCld55_Design_Document.bib file as shown in below text
```
@article{ref1,
title={Design Techniques for Signal Reflection Suppression in High-Speed 25-Gb/s Laser Drivers in CMOS},
author={Jingbo Shi and Bozhi Yin},
journal={IEEE PHOTONICS TECHNOLOGY LETTERS},
volume={VOL.30},
number={1},
pages={39--42},
year={2018},
}
```
  - Cite the reference via below command
```
\cite{ref1}
```
  - Compile LOCld55_Design_Document.tex file to generate LOCld55_Design_Document.aux file
```
pdflatex LOCld55_Design_Document.tex
```
  - Compile LOCld55_Design_Document.aux file through below command
```
bibtex LOCld55_Design_Document.aux
```
  - Finally, recompile LOCld55_Design_Document.tex file with command as below
```
pdflatex LOCld55_Design_Document.tex
```
### 3. How to install .sty package 
  - Auto install package
```
tlmgr packagename.sty

```
  - install texlive package through yum on CentOS system
```
sudo yum search texlive
sudo yum install texlive-amscls.noarch  #AMS document class for amscls
```
### 4. package download website:
  - [CTAN website](https://ctan.org)
### 5. Config git without username and password when executes git push command
  - Config ~/.gitconfig file
```
git config --global credential.helper store

```
  - Delete saved password
```
git credential-osxkeychain erase

or 

rm ~/.git-credentials
```
