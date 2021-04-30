# Polito-HPC

Slides source and Code Samples

## Slides preparation ##

See code at the end of Slides.t2t

### Programs used:
- txt2tags : GIT Version V2 (More features but python 2.x)
- Pandoc
- Some easy cleanup w/ sed
- pdfLaTEX

/home/avaresio/GIT/txt2tags/txt2tags -t txt2t Slides.t2t
pandoc -s -t beamer -V theme:Copenhagen -V colortheme:wolverine -f t2t -o Slides.tex Slides.txt2t
sed -i "/^ *:$/d" Slides.tex
sed -i "/^ *-$/d" Slides.tex
sed -i "/^ *+$/d" Slides.tex
sed -i "/^ *- - :$/d" Slides.tex
pdflatex Slides.tex > Slides.plog
rm Slides{.out,.vrb,.toc,.snm,.nav,.aux,.log,.plog}'

