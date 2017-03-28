file = xenobot

all: $(file).pdf

xenobot.pdf: $(file).tex
	pdflatex $^
	bibtex paper >/dev/null || echo
	pdflatex $^ 2>/dev/null >/dev/null

edit:
	texmaker $(file).tex &

clean:
	rm -f *.dvi *.aux *.log *.ps *.pdf *.out paper.bbl paper.blg
