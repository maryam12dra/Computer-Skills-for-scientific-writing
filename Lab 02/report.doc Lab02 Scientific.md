Шаблон отчёта по лабораторной работе №2

Practical scientific writing

ДРАММЕХ МАРИАМА Л

Содержание

Список иллюстраций

Список таблиц

# 1 Цель работы

Целью данной лабораторной работы является ознакомление с работа с структура документа Latex

# 2 Задание

1.  Try adding text to your first document, typesetting and seeing the changes in your PDF.
2.  Make some different paragraphs and add variable spaces.
3.  Explore how your editor works; click on your source and find how to go to the same line in your PDF.
4.  Try adding some hard spaces and see how they influence line-breaking.

# 3 Теоретическое введение

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\begin{document}  
Hey world!  
This is a first document.  
\\end{document}

(см. Рис. **¿fig:001?**).

![](./report.doc%20Lab02%20Scientific_images/image-001.png)

## 3.1 Running LaTeX

(см. Рис. **¿fig:002?**).

![](./report.doc%20Lab02%20Scientific_images/image-002.png)

(см. Рис. **¿fig:003?**).

![](./report.doc%20Lab02%20Scientific_images/image-003.png)

(см. Рис. **¿fig:004?**).

![](./report.doc%20Lab02%20Scientific_images/image-004.png)

(см. Рис. **¿fig:005?**).

![](./report.doc%20Lab02%20Scientific_images/image-005.png)

## 3.2 Документ TeXlive с нижним колонтитулом

\\documentclass\[a4paper,12pt\]{article} % The document class with options  
% select T1 font encoding: suitable for Western European Latin scripts  
\\usepackage\[T1\]{fontenc}  
% A comment in the preamble  
\\begin{document}  
% This is a comment  
Trhis is a simple  
document\\footnote{with a footnote}fi  
This is a new paragraph.  
\\end{document}

(см. Рис. **¿fig:006?**).

![](./report.doc%20Lab02%20Scientific_images/image-006.png)

(см. Рис. **¿fig:007?**).

![](./report.doc%20Lab02%20Scientific_images/image-007.png)

(см. Рис. **¿fig:008?**).

![](./report.doc%20Lab02%20Scientific_images/image-008.png)

# 4 Выполнение лабораторной работы

## 4.1 Try adding text to your first document, typesetting and seeing the changes in your PDF.

(см. Рис. **¿fig:009?**).

![](./report.doc%20Lab02%20Scientific_images/image-009.png)

\\documentclass\[12pt\]{article}

\\usepackage\[english\]{babel}

\\usepackage\[utf8\]{inputenc}

\\begin{document}

Hello world!

This is my first document with LaTeX.

% Paragraph 1

Here is some content full of sentences to test the PDF rendering.

You can write text. \*Article\* class is freely available.

% Paragraph 2

Here is a second paragraph. Words keep their spaces between words,

LaTeX automatically results in a single space.

% Non-breaking spaces (hard spaces):

Word~habit, "Brusubi~is a city", "Dupont~and Brusubi~cannot".

% Paragraph 3, stays on one line

Chapter one example: introduction.

Without it, LaTeX could cut "Chapter" and "one" on two lines.

\\end{document}

## 4.2 Make some different paragraphs and add variable spaces.

(см. Рис. **¿fig:010?**).

![](./report.doc%20Lab02%20Scientific_images/image-010.png)

## 4.3 Explore how your editor works; click on your source and find how to go to the same line in your PDF.

## 4.4 Try adding some hard spaces and see how they influence line-breaking.

![](./report.doc%20Lab02%20Scientific_images/image-011.png)

(см. Рис. **¿fig:011?**).

# 5 Выводы

Таким образом, была достигнута цель установил TeXlive, я познакомелся с работа с его структуры а также с системой LaTeX.

# Список литературы  
![](./report.doc%20Lab02%20Scientific_images/image-012.png)