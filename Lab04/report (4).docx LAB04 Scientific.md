Отчёт по лабораторной работе №4

Including Graphics

Драммех Мариама Л

Содержание

Список иллюстраций

Список таблиц

# 1 Цель работы

Целью данной лабораторной работы является ознакомление с основами включения графики в документы LaTeX.

The purpose of this lab work is to learn how to include and manipulate graphics in LaTeX documents using the graphicx package and related tools.

# 2 Задание

1.  Study basic image inclusion with graphicx package
2.  Learn to modify graphic appearance (size, rotation, scaling)
3.  Understand float environments for image placement
4.  Practice file naming and organization best practices
5.  Learn cross-referencing for figures
6.  Explore different float types and positioning options
7.  Complete the exercises with practical examples

# 3 Теоретическое введение

## 3.1 4 Включение графики / Including Graphics

Для включения внешних изображений в LaTeX используется пакет graphicx, который предоставляет команду \\includegraphics. To include external images in LaTeX, use the graphicx package which provides the \\includegraphics command.  
![](./report%20(4).docx%20LAB04%20Scientific_images/image-001.png)

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\usepackage{graphicx}  
\\begin{document}  
This picture  
\\begin{center}  
\\includegraphics\[height=2cm\]{example-image}  
\\end{center}  
is an imported PDF.  
\\end{document}

## 3.2 4.1 Изменение внешнего вида графики / Altering Graphic Appearance

Команда \\includegraphics имеет множество опций для управления размером и формой изображений. The \\includegraphics command has many options to control image size and appearance.

\\documentclass{article}

\\usepackage\[T1\]{fontenc}

\\usepackage{graphicx}

\\begin{document}

\\begin{center}

\\includegraphics\[height = 0.5\\textheight\]{example-image}

\\end{center}

Some text

\\begin{center}

\\includegraphics\[width = 0.5\\textwidth\]{example-image}

\\end{center}

\\end{document}

![](./report%20(4).docx%20LAB04%20Scientific_images/image-002.png)

\\documentclass{article}

\\usepackage\[T1\]{fontenc}

\\usepackage{graphicx}

\\begin{document}

\\begin{center}

\\includegraphics\[clip, trim = 0 0 50 50\]{example-image}

\\end{center}

\\end{document}

  
  
  
![](./report%20(4).docx%20LAB04%20Scientific_images/image-003.png)

## 3.3 4.2 Создание плавающих изображений / Making Images Float

Изображения обычно включаются как плавающие объекты (floats) чтобы избежать больших пробелов на странице. Images are typically included as floats to avoid large gaps on the page.

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\usepackage{graphicx}  
\\usepackage{lipsum} % produce dummy text as filler  
\\begin{document}  
\\lipsum\[1-4\] % Just a few filler paragraphs  
Test location.  
\\begin{figure}\[ht\]  
\\centering  
\\includegraphics\[width=0.5\\textwidth\]{example-image-a.png}  
\\caption{An example image}  
\\end{figure}  
\\lipsum\[6-10\] % Just a few filler paragraphs  
\\end{document}

![](./report%20(4).docx%20LAB04%20Scientific_images/image-004.png)

## 3.4 4.3 Именование графических файлов / Naming Graphics Files

Рекомендуется использовать простые имена файлов без пробелов и специальных символов. It’s recommended to use simple file names without spaces or special characters.

\\includegraphics\[width=30pt\]{pics/myimage.png}

## 3.5 4.4 Хранение графики в поддиректории / Storing Graphics in Subdirectory

Для организации файлов изображения можно хранить в поддиректориях. To organize files, images can be stored in subdirectories.

  
\\graphicspath{{figs/}{pics/}}

## 3.6 4.5 Создание графики / Producing Graphics

LaTeX поддерживает различные форматы изображений. Предпочтительно использовать PDF для векторной графики. LaTeX supports various image formats. PDF is preferred for vector graphics.

% создания графики с TikZ  
\\documentclass{article}  
\\usepackage{tikz}  
\\begin{document}  
\\begin{tikzpicture}  
\\draw (0,0) circle (1cm);  
\\draw (-1,0) -- (1,0);  
\\end{tikzpicture}  
\\end{document}

## 3.7 4.6 Размещение плавающих объектов / Placing Floats

Пакет float предоставляет опцию H для точного размещения плавающих объектов. The float package provides the H option for precise float placement.

\\documentclass{article}

\\usepackage\[T1\]{fontenc}

\\usepackage{graphicx}

\\usepackage{lipsum} % dummy text for filler

\\usepackage{float}

\\begin{document}

\\lipsum\[1-7\]

\\begin{figure}\[H\]

\\centering

\\includegraphics\[width=0.5\\textwidth\]{example-image}

\\caption{An example image}

\\end{figure}

\\lipsum\[8-15\]

\\end{document}

![](./report%20(4).docx%20LAB04%20Scientific_images/image-005.png)

## 3.8 4.7 Другие типы плавающих объектов / Other Types of Float

Пакет trivfloat позволяет создавать новые типы плавающих сред. The trivfloat package allows creating new types of float environments.

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\usepackage{graphicx}  
\\usepackage{lipsum} % dummy text for filler  
\\usepackage{trivfloat}  
\\trivfloat{image}  
\\begin{document}  
\\begin{image}  
\\centering  
\\includegraphics\[width=0.5\\textwidth\]{example-image}  
\\caption{An example image}  
\\end{image}  
\\end{document}

  
![](./report%20(4).docx%20LAB04%20Scientific_images/image-006.png)

##   
  
  
3.9 4.8 Перекрёстные ссылки / Cross-referencing

Механизм \\label и \\ref позволяет создавать ссылки на пронумерованные элементы. The \\label and \\ref mechanism allows creating references to numbered elements.

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\begin{document}  
Hey world!  
This is a first document.  
\\section{Title of the first section}  
Text of material for the first section.  
\\subsection{Subsection of the first section}  
\\label{subsec:labelone}  
Text of material for the first subsection.  
\\begin{equation}  
e^{i\\pi}+1 = 0  
\\label{eq:labeltwo}  
\\end{equation}  
In subsection~\\ref{subsec:labelone} is  
equation~\\ref{eq:labeltwo}.  
\\end{document}

![](./report%20(4).docx%20LAB04%20Scientific_images/image-007.png)

![](./report%20(4).docx%20LAB04%20Scientific_images/image-008.png)

\\documentclass{article}

\\usepackage\[T1\]{fontenc}

\\usepackage\[hidelinks\]{hyperref}

\\begin{document}

\\section{Introduction}

Some exciting text with a reference~\\ref{sec:next}.

\\section{Next thing}

\\label{sec:next}

More text here.

\\end{document}

![](./report%20(4).docx%20LAB04%20Scientific_images/image-009.png)

# 4 Выполнение лабораторной работы

## 4.1 4.10 Упражнения / Exercises

### 4.1.1 Упражнение 1: Включение собственного изображения / Including Your Own Image

\\documentclass{article}

\\usepackage{graphicx}

\\begin{document}

\\begin{figure}\[ht\]

    \\centering

    % \\includegraphics\[width=0.7\\textwidth\]{my-photo.jpg}

    \\caption{My Photo from LAB04 Folder}

    \\label{fig:photo1}

\\end{figure}

\\end{document}

![](./report%20(4).docx%20LAB04%20Scientific_images/image-010.png)

### 4.1.2 Упражнение 2: Исследование опций размера и поворота / Exploring Size and Rotation Options

\\documentclass{article}

\\usepackage{graphicx}

\\begin{document}

\\includegraphics\[height=3cm\]{my-photo.jpg}

\\includegraphics\[width=0.3\\textwidth\]{my-photo.jpg}

\\includegraphics\[scale=0.5\]{my-photo.jpg}

\\includegraphics\[angle=45, width=0.2\\textwidth\]{my-photo.jpg}

\\end{document}

![](./report%20(4).docx%20LAB04%20Scientific_images/image-011.png)

### 4.1.3 Упражнение 3: Сравнение textwidth и linewidth / Comparing textwidth and linewidth

\\documentclass\[twocolumn\]{article}

\\usepackage\[utf8\]{inputenc}

\\usepackage\[T2A\]{fontenc}

\\usepackage{graphicx}

\\usepackage{lipsum}

\\begin{document}

\\lipsum\[1\]

\\begin{figure}\[ht\]

    \\centering

    \\includegraphics\[width=0.8\\linewidth\]{my-photo.jpg}

    \\caption{С использованием \\textbackslash linewidth}

\\end{figure}

\\begin{figure}\[ht\]

    \\centering

    \\includegraphics\[width=0.5\\textwidth\]{my-photo.jpg}

    \\caption{С использованием \\textbackslash textwidth (50\\%)}

\\end{figure}

\\lipsum\[2-5\]

\\end{document}

![](./report%20(4).docx%20LAB04%20Scientific_images/image-012.png)

### 4.1.4 Упражнение 4: Размещение плавающих объектов с разными спецификаторами / Float Placement with Different Specifiers

\\documentclass{article}

\\usepackage\[utf8\]{inputenc}

\\usepackage\[T2A\]{fontenc}

\\usepackage{graphicx}

\\usepackage{lipsum}

\\begin{document}

\\lipsum\[1-2\]

\\begin{figure}\[h\]

    \\centering

    \\includegraphics\[width=0.4\\textwidth\]{my-photo.jpg}

    \\caption{Опция h (здесь)}

\\end{figure}

\\lipsum\[3\]

\\begin{figure}\[t\]

    \\centering

    \\includegraphics\[width=0.4\\textwidth\]{example-image-b}

    \\caption{Опция t (верх)}

\\end{figure}

\\begin{figure}\[b\]

    \\centering

    \\includegraphics\[width=0.4\\textwidth\]{example-image-c}

    \\caption{Опция b (низ)}

\\end{figure}

\\lipsum\[4-8\]

\\end{document}

![](./report%20(4).docx%20LAB04%20Scientific_images/image-013.png)

### 4.1.5 Упражнение 5: Перекрёстные ссылки и количество компиляций / Cross-references and Number of Compilations

\\documentclass{article}

\\usepackage\[T1\]{fontenc}

\\usepackage{graphics}

\\usepackage{lipsum}

\\usepackage{float}

\\usepackage{amsmath}

\\usepackage\[colorlinks\]{hyperref}

\\begin{document}

\\section\*{Exercise 5: Cross-references and Number of Compilations}

\\subsection\*{Useful document}

\\subsubsection\*{Section (Introduction)}

\\label{sec:intro}

In section~\\ref{sec:intro}, we present...

\\subsubsection\*{Subsection (first subsection)}

\\label{sub:first}

As seen in subsection~\\ref{sub:first}...

\\begin{enumerate}

\\item First point

\\item Second point \\label{item:second}

\\item Reference to point~\\ref{item:second}

\\end{enumerate}

% \\begin{figure}\[ht\]

%   \\centering

%     \\includegraphics\[width=0.5\\textwidth\]{my-photo.jpg}

%     \\caption{Test figure}

%     \\label{fig:test}

% \\end{figure}

% Figure~\\ref{fig:test} shows...

\\end{document}

![](./report%20(4).docx%20LAB04%20Scientific_images/image-014.png)

### 4.1.6 Упражнение 6: Размещение label до/после caption / Placing label Before/After caption

\\documentclass{article}

\\usepackage\[utf8\]{inputenc}

\\usepackage\[T2A\]{fontenc}

\\usepackage{graphicx}

\\begin{document}

\\begin{figure}\[ht\]

    \\centering

    \\includegraphics\[width=0.4\\textwidth\]{example-image-a}

    \\label{fig:before}

    \\caption{Рисунок с label до caption}

\\end{figure}

\\begin{figure}\[ht\]

    \\centering

    \\includegraphics\[width=0.4\\textwidth\]{my-photo.jpg}

     \\caption{Рисунок с label после caption}

    \\label{fig:after}

\\end{figure}

Ссылка на рисунок~\\ref{fig:before} (неправильная)\\\\

Ссылка на рисунок~\\ref{fig:after} (правильная)

\\end{document}

![](./report%20(4).docx%20LAB04%20Scientific_images/image-015.png)

### 4.1.7 Упражнение 7: label после end{equation} / label After end{equation}

\\documentclass{article}

\\usepackage\[T1\]{fontenc}

\\usepackage{graphicx}

\\usepackage{lipsum}

\\usepackage{float}

\\usepackage{amsmath}

\\usepackage{hyperref}

\\title{Exercise 7: \\textbackslash label After \\textbackslash end\\{equation\\}}

\\author{}

\\date{}

\\begin{document}

\\maketitle

\\section\*{Exercise 7: \\textbackslash label After \\textbackslash end\\{equation\\}}

\\begin{equation}

E = mc^2

\\end{equation}

\\label{eqafter} % AFTER end{equation} - INCORRECT

\\begin{equation}

F = ma

\\label{eqinside} % INSIDE equation - CORRECT

\\end{equation}

Reference to equation \\ref{eqafter} (incorrect)

Reference to equation \\ref{eqinside} (correct)

\\textbf{**Result:**}

\\begin{itemize}

    \\item \\textbackslash label after \\textbackslash end\\{equation\\} $\\rightarrow$ incorrect reference (usually to previous equation or section)

    \\item \\textbackslash label inside the equation environment $\\rightarrow$ correct reference to the equation

\\end{itemize}

\\end{document}

![](./report%20(4).docx%20LAB04%20Scientific_images/image-016.png)

# 5 Выводы

В ходе лабораторной работы №4 я изучил основы включения и управления графикой в документах LaTeX. Освоил работу с пакетом graphicx, научился создавать плавающие объекты, управлять их размещением и создавать перекрёстные ссылки на изображения. Также изучил лучшие практики организации графических файлов и их именования.

In this lab work #4, I learned the fundamentals of including and manipulating graphics in LaTeX documents. I mastered the graphicx package, learned to create float objects, control their placement, and create cross-references to images. I also studied best practices for organizing graphic files and naming them.

# Список литературы

LaTeX/Математические формулы — Викиучебник. https://ru.wikibooks.org/wiki/LaTeX/