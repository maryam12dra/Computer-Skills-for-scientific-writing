Отчёт по лабораторной работе №6

Working with Bibliography

ДРАММЕХ МАРИАМА Л

Содержание

Список иллюстраций

Список таблиц

# 1 Цель работы

Целью данной лабораторной работы является освоение методов работы с библиографией в LaTeX, включая использование систем BibTeX и biblatex для управления цитированием и списками литературы.

The purpose of this lab work is to learn how to work with bibliography in LaTeX, including using BibTeX and biblatex systems for managing citations and reference lists.

# 2 Задание

1.  Освоить workflow с natbib и BibTeX для работы с библиографией
2.  Освоить workflow с biblatex и Biber и их особенности
3.  Сравнить два подхода к работе с библиографией и их применение
4.  Выполнить практические упражнения по созданию и управлению библиографическими ссылками

# 3 Теоретическое введение

## 3.1 6 Работа с библиографией / Working with Bibliography

Для библиографических ссылок обычно используется информация из внешних файлов - библиографических баз данных. For bibliographic citations, information is typically retrieved from external files - bibliographic databases.

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\usepackage{natbib}  
  
\\begin{document}  
Ссылка на книгу: \\citet{Graham1995}.  
Ссылка на статью: \\citep{Thomas2008}.  
  
\\bibliographystyle{plainnat}  
\\bibliography{learnlatex}  
\\end{document}

## 3.2 6.1 Библиографические базы данных / Reference Databases

Базы данных BibTeX содержат записи с различными полями. BibTeX databases contain entries with various fields.

\\documentclass{article}

\\usepackage\[T1\]{fontenc}

\\begin{document}

@article{Thomas2008,

author = {Thomas, Christine M. and Liu, Tianbiao and Hall,

 Michael B.

and Darensbourg, Marcetta Y.},

title = {Series of Mixed Valent {Fe(II)Fe(I)} Complexes

 That Model the

{H(OX)} State of \[{FeFe}\]Hydrogenase: Redox

 Properties,

Density-Functional Theory Investigation, and

 Reactivity with

Extrinsic {CO}},

journal = {Inorg. Chem.},

year = {2008},

volume = {47},

number = {15},

pages = {7009-7024},

doi = {10.1021/ic800654a},

}

@book{Graham1995,

author = {Ronald L. Graham and Donald E. Knuth and Oren

 Patashnik},

title = {Concrete Mathematics},

publisher = {Addison-Wesley},

year = {1995},

}

\\end{document}

![](./report.docx.%20LAB06_images/image-001.png)

## 3.3 6.2 Перенос информации из базы данных / Transferring Information from Database

Для работы с библиографией требуется несколько шагов компиляции: Working with bibliography requires multiple compilation steps:

-   **natbib + BibTeX**: LaTeX → BibTeX → LaTeX → LaTeX
-   **biblatex + Biber**: LaTeX → Biber → LaTeX

## 3.4 6.3 Workflow BibTeX с natbib / The BibTeX Workflow with natbib

Пакет natbib предоставляет расширенные возможности цитирования. The natbib package provides enhanced citation capabilities.

\\documentclass{article}

\\usepackage\[T1\]{fontenc}

\\usepackage{natbib}

\\begin{document}

The mathematics showcase is from \\citet{Graham1995}, whereas

there is some chemistry in \\citet{Thomas2008}.

Some parenthetical citations: \\citep{Graham1995}

and then \\citep\[p.~56\]{Thomas2008}.

\\citep\[See\]\[pp.~45--48\]{Graham1995}

Together \\citep{Graham1995,Thomas2008}

\\bibliographystyle{plainnat}

\\bibliography{learnlatex}

\\end{document}

![](./report.docx.%20LAB06_images/image-002.png)

## 3.5 6.4 Workflow biblatex / The biblatex Workflow

Пакет biblatex работает несколько иначе, с загрузкой ресурсов в преамбуле. The biblatex package works differently, loading resources in the preamble.

\\documentclass{article}

\\usepackage\[T1\]{fontenc}

\\usepackage\[style=authoryear\]{biblatex}

\\addbibresource{learnlatex.bib} % file of reference info

\\begin{document}

The mathematics showcase is from \\autocite{Graham1995}.

Some more complex citations: \\parencite{Graham1995} or

\\textcite{Thomas2008} or possibly \\citetitle{Graham1995}.

\\autocite\[56\]{Thomas2008}

\\autocite\[See\]\[45-48\]{Graham1995}

Together \\autocite{Thomas2008,Graham1995}

\\printbibliography

\\end{document}

![](./report.docx.%20LAB06_images/image-003.png)

## 3.6 6.5 Выбор между BibTeX и BibLaTeX / Choosing Between BibTeX and BibLaTeX

**BibTeX workflow:** - Более установленный и поддерживаемый издательствами - Использует .bst файлы для стилей - Ограниченная поддержка Unicode

**biblatex workflow:** - Лучшая кастомизация через LaTeX команды - Полная поддержка Unicode сортировки - Более сложные стили цитирования

## 3.7 6.6 Работа с не-английской сортировкой / Dealing with Non-English Sorting

Biber обеспечивает правильную сортировку для не-английских символов. Biber provides proper sorting for non-English characters.

@article{Müller2023,  
author = {Müller, Hans and École, Pierre and Смирнов, Иван},  
title = {Международное исследование},  
journal = {Журнал},  
year = {2023}  
}

## 3.8 6.7 Гиперссылки / Hyperlinks

Пакет hyperref автоматически создает ссылки в библиографии. The hyperref package automatically creates links in bibliography.

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\usepackage\[hidelinks\]{hyperref}  
\\usepackage\[style=authoryear\]{biblatex}  
\\addbibresource{learnlatex.bib}  
  
\\begin{document}  
Ссылка \\autocite{Graham1995} будет гиперссылкой.  
  
\\printbibliography  
\\end{document}

## 3.9 6.8 Различия в лучших практиках для BibTeX / Differences in Best Practice for BibTeX Input

Различные стили библиографии поддерживают разные поля. Different bibliography styles support different fields.

% Для старых стилей  
@misc{Website2023,  
author = {Author},  
title = {Website Title},  
howpublished = {\\url{https://example.com}}  
}  
  
% Для новых стилей  
@misc{Website2023,  
author = {Author},  
title = {Website Title},  
url = {https://example.com}  
}

# 4 Выполнение лабораторной работы

## 4.1 6.9 Упражнения / Exercises

### 4.1.1 Упражнение 1: Использовать примеры с natbib и biblatex

**natbib workflow:**

\\documentclass{article}

\\usepackage\[utf8\]{inputenc}

\\usepackage\[T1\]{fontenc}

\\usepackage{natbib}

\\begin{document}

Ссылка на книгу: \\citet{Graham1995}. Ссылка на статью: \\citep{Thomas2008}.

\\bibliographystyle{plainnat}

\\bibliography{learnlatex}

\\end{document}

*Компиляция: LaTeX → BibTeX → LaTeX → LaTeX*

![](./report.docx.%20LAB06_images/image-004.png)

**biblatex workflow:**

\\documentclass{article}

\\usepackage\[utf8\]{inputenc}

\\usepackage\[T1\]{fontenc}

\\usepackage\[style=authoryear\]{biblatex}

\\addbibresource{learnlatex.bib}

\\begin{document}

Авторская ссылка: \\textcite{Graham1995}. Скобочная ссылка: \\parencite{Thomas2008}.

\\printbibliography

\\end{document}

*Компиляция: LaTeX → Biber → LaTeX*

![](./report.docx.%20LAB06_images/image-005.png)

### 4.1.2 Упражнение 2: Создать новые записи в базе данных и новые ссылки

**Новая запись в learnlatex.bib:**

@article{Einstein1905,  
author = {Albert Einstein},  
title = {On the Electrodynamics of Moving Bodies},  
journal = {Annalen der Physik},  
year = {1905},  
volume = {322},  
number = {10},  
pages = {891--921},  
doi = {10.1002/andp.19053221004}  
}

**Документ с новой ссылкой:**

\\documentclass{article}

\\usepackage\[utf8\]{inputenc}

\\usepackage\[T1\]{fontenc}

\\usepackage\[style=authoryear\]{biblatex}

\\addbibresource{learnlatex.bib}

\\begin{document}

Новая ссылка: \\cite{Einstein1905}. Комбинированные ссылки: \\cite{Graham1995,Einstein1905,Thomas2008}.

\\printbibliography

\\end{document}

![](./report.docx.%20LAB06_images/image-006.png)

### 4.1.3 Упражнение 3: Добавить ссылку на отсутствующую запись в базе данных

\\documentclass{article}

\\usepackage\[T1\]{fontenc}

\\usepackage\[style=authoryear\]{biblatex}

\\addbibresource{learnlatex.bib}

\\begin{document}

Ссылка на существующую запись: \\cite{Graham1995}.

Ссылка на отсутствующую запись: \\cite{MissingEntry2024}.

Комбинированные ссылки: \\cite{Graham1995,MissingEntry2024,Thomas2008}.

\\printbibliography

\\end{document}

![](./report.docx.%20LAB06_images/image-007.png)

### 4.1.4 Упражнение 4: Экспериментировать с числовыми стилями библиографии

**natbib с числовым стилем:**

\\documentclass{article}

\\usepackage\[utf8\]{inputenc}

\\usepackage\[T1\]{fontenc}

\\usepackage\[english,russian\]{babel}

\\usepackage\[numbers\]{natbib}

\\begin{document}

\\begin{thebibliography}{99}

\\bibitem{Graham1995} Graham, R. L. (1995). Some results in combinatorics.

\\bibitem{Thomas2008} Thomas, R. (2008). Recent developments in graph theory.

\\end{thebibliography}

Числовые ссылки: \\cite{Graham1995} и \\cite{Thomas2008}.

Множественные ссылки: \\cite{Graham1995,Thomas2008}.

\\end{document}

![](./report.docx.%20LAB06_images/image-008.png)

**biblatex с числовым стилем:**

\\documentclass{article}

\\usepackage\[T1\]{fontenc}

\\usepackage\[dutch\]{babel}

\\begin{document}

Numerical values link: \\cite{Graham1995} \\cite{Thomas2008}.

Plenty link: \\cite{Graham1995, Thomas2008}.

\\bibliographystyle{plain}  % or plainnat, unsrt, etc.

\\bibliography{references}   % references.bib file without extension

\\end{document}

![](./report.docx.%20LAB06_images/image-009.png)

# 5 Выводы

В ходе лабораторной работы №6 я освоил методы работы с библиографией в LaTeX. Изучил два основных подхода: традиционный workflow с natbib и BibTeX, а также современный подход с biblatex и Biber. Научился создавать библиографические базы данных, управлять стилями цитирования, работать с не-английской сортировкой и создавать гиперссылки в библиографии.

In this lab work #6, I mastered bibliography management methods in LaTeX. I studied two main approaches: traditional workflow with natbib and BibTeX, as well as modern approach with biblatex and Biber. I learned to create bibliographic databases, manage citation styles, work with non-English sorting, and create hyperlinks in bibliography.

# Список литературы

1.  Practical scientific writing - Tables chapter
2.  LaTeX/Tables - Wikibooks. https://en.wikibooks.org/wiki/LaTeX/Tables
3.  array package documentation
4.  booktabs package documentation