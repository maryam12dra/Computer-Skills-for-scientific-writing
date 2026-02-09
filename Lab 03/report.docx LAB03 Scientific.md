Отчёта по лабораторной работе №3

Mathematics Typing

ДРАММЕХ МАРИАМА Л

Содержание

Список иллюстраций

Список таблиц

# 1 Цель работы

Целью данной лабораторной работы является ознакомление с основами набора математических выражений в LaTeX.

The purpose of this lab work is to learn how to typeset mathematical formulas and equations using LaTeX math mode and related packages.

# 2 Задание

1.  Study inline and display math modes.  
    
2.  Use the amsmath package to align and format equations.  
    
3.  Apply different math fonts.  
    
4.  Use mathtools for advanced formatting.  
    
5.  Try bold math and Unicode math.  
    
6.  Perform the exercises with examples.

# 3 Теоретическое введение

## 3.1 3.1 Математический режим / Math mode

В LaTeX существует два математических режима: **inline** и **display**.  
In LaTeX there are two main math modes: inline (within text) and display (centered block).

documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\begin{document}  
A sentence with inline mathematics: $y = mx + c$.  
  
A second sentence with inline mathematics: $5^{2}=3^{2}+4^{2}$.  
  
A second paragraph containing display math.  
\\\[  
y = mx + c  
\\\]  
See how the paragraph continues after the display.  
\\end{document}

(рис.**¿fig:001?**)

![](./report.docx%20LAB03%20Scientific_images/image-001.png)

### 3.1.1 3.1.1 Inline math mode and mathematical notation

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\begin{document}  
Superscripts $a^{b}$ and subscripts $a\_{b}$.  
\\end{document}

(см. Рис. **¿fig:002?**)

![](./report.docx%20LAB03%20Scientific_images/image-002.png)

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\begin{document}  
Some mathematics: $y = 2 \\sin \\theta^{2}$.  
\\end{document}

(см. Рис. **¿fig:003?**)

![](./report.docx%20LAB03%20Scientific_images/image-003.png)

### 3.1.2 3.1.2 Display mathematics

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\begin{document}  
A paragraph about a larger equation  
\\\[  
\\int\_{-\\infty}^{+\\infty} e^{-x^2} \\, dx  
\\\]  
\\end{document}

(см. Рис. **¿fig:004?**)

![](./report.docx%20LAB03%20Scientific_images/image-004.png)

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\newcommand{\\diff}{\\mathop{}\\!d} % For italic  
% \\newcommand{\\diff}{\\mathop{}\\!\\mathrm{d}} % For upright  
\\begin{document}  
A paragraph about a larger equation  
\\\[  
\\int\_{-\\infty}^{+\\infty} e^{-x^2} \\diff x  
\\\]  
\\end{document}

(см. Рис. **¿fig:005?**)

![](./report.docx%20LAB03%20Scientific_images/image-005.png)

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\begin{document}  
A paragraph about a larger equation  
\\begin{equation}  
\\int\_{-\\infty}^{+\\infty} e^{-x^2} \\, dx  
\\end{equation}  
\\end{document}

(см. Рис. **¿fig:006?**)

![](./report.docx%20LAB03%20Scientific_images/image-006.png)

## 3.2 3.2 Пакет amsmath / The amsmath package

Пакет amsmath расширяет стандартные возможности для набора формул и выравнивания уравнений. The amsmath package enhances math typesetting and alignment.

\\documentclass{article}  
\\usepackage\[T1\]{fontenc}  
\\usepackage{amsmath}  
\\begin{document}  
\\begin{align\*}  
Q\_{n,k} &= Q\_{n-1,k} + Q\_{n-1,k-1} + \\binom{n}{k}, \\\\  
&\\quad \\text{for } n,k>0.  
\\end{align\*}  
\\end{document}

(см. Рис. **¿fig:007?**)

![](./report.docx%20LAB03%20Scientific_images/image-007.png)

(см. Рис. **¿fig:008?**)

![](./report.docx%20LAB03%20Scientific_images/image-008.png)

## 3.3 3.3 Шрифты в математическом режиме / Fonts in math mode

В математике разные шрифты обозначают разные типы объектов. Different font commands give different styles and meanings.

\\documentclass{article}  
\\usepackage{amsmath}  
\\begin{document}  
$\\mathrm{A}, \\mathit{A}, \\mathbf{A}, \\mathsf{A}, \\mathtt{A}, \\mathbb{A}$  
\\end{document}

(см. Рис. **¿fig:009?**)

![](./report.docx%20LAB03%20Scientific_images/image-009.png)

(см. Рис. **¿fig:010?**)

![](./report.docx%20LAB03%20Scientific_images/image-010.png)

## 3.4 3.4 Дополнительные выравнивания / Further amsmath alignments

Environments like gather and multline are used for multi-line equations.

\\documentclass{article}  
\\usepackage{amsmath}  
\\begin{document}  
\\begin{gather}  
P(x)=ax^{5}+bx^{4}+cx^{3}+dx^{2}+ex+f\\\\  
x^2+x=10  
\\end{gather}  
\\end{document}

(см. Рис. **¿fig:011?**)

![](./report.docx%20LAB03%20Scientific_images/image-011.png)

## 3.5 3.4.1 Columns in math alignments

(см. Рис. **¿fig:012?**)

![](./report.docx%20LAB03%20Scientific_images/image-012.png)

(см. Рис. **¿fig:013?**)

![](./report.docx%20LAB03%20Scientific_images/image-013.png)

## 3.6 3.5 Жирный шрифт в формулах / Bold Math

To bold entire or partial equations, we can use \\boldmath or the bm package.

\\documentclass{article}  
\\usepackage{bm}  
\\begin{document}  
$(x+\\bm{y})(x-\\bm{y}) = x^2 - \\bm{y}^2$  
\\end{document}

(см. Рис. **¿fig:014?**)

![](./report.docx%20LAB03%20Scientific_images/image-014.png)

(см. Рис. **¿fig:015?**)

![](./report.docx%20LAB03%20Scientific_images/image-015.png)

## 3.7 3.6 Пакет Mathtools / Mathtools package

mathtools builds upon amsmath and provides extended features like column alignment in matrices.

\\documentclass{article}  
\\usepackage{mathtools}  
\\begin{document}  
\\\[  
\\begin{pmatrix\*}\[r\]  
10 & 11 \\\\  
1 & 2 \\\\  
\-5 & -6  
\\end{pmatrix\*}  
\\\]  
\\end{document}

(см. Рис. **¿fig:016?**)

![](./report.docx%20LAB03%20Scientific_images/image-016.png)

## 3.8 3.7 Юникодная математика / Unicode Math

Using unicode-math with OpenType fonts allows modern mathematical typesetting.

\\documentclass{article}  
\\usepackage{unicode-math}  
\\setmainfont{TeX Gyre Pagella}  
\\setmathfont{TeX Gyre Pagella Math}  
\\begin{document}  
\\\[  
\\log \\alpha + \\log \\beta = \\log(\\alpha\\beta)  
\\\]  
\\end{document}

(см. Рис. **¿fig:017?**)

![](./report.docx%20LAB03%20Scientific_images/image-017.png)

# 4 Выполнение лабораторной работы

## 4.1 3.8 Упражнения / Exercises

### 4.1.1 1. Переключение между режимами / Switching between math modes

(см. Рис. **¿fig:018?**) ![](./report.docx%20LAB03%20Scientific_images/image-018.png)

### 4.1.2 2. Греческие буквы / Greek letters

(см. Рис. **¿fig:019?**) ![](./report.docx%20LAB03%20Scientific_images/image-019.png)

### 4.1.3 3. Комбинирование шрифтов / Combining fonts

(см. Рис. **¿fig:020?**) ![](./report.docx%20LAB03%20Scientific_images/image-020.png)

### 4.1.4 4. Параметры класса документа для уравнений / Equation alignment

(см. Рис. **¿fig:021?**) ![](./report.docx%20LAB03%20Scientific_images/image-021.png)

(см. Рис. **¿fig:022?**) ![](./report.docx%20LAB03%20Scientific_images/image-022.png)

(см. Рис. **¿fig:023?**) ![](./report.docx%20LAB03%20Scientific_images/image-023.png)

### 4.1.5 5. Расширенное использование amsmath / Using Mathtools

(см. Рис. **¿fig:024?**) ![](./report.docx%20LAB03%20Scientific_images/image-024.png)

### 4.1.6 6. Математика выделена жирным шрифтом с bm / Math in bold with bm

(см. Рис. **¿fig:025?**) ![](./report.docx%20LAB03%20Scientific_images/image-025.png)

# 5 Выводы

В ходе лабораторной работы №3 я изучил основы набора математических выражений в LaTeX, познакомился с пакетами amsmath, mathtools, bm, и unicode-math. В результате я научился выравнивать уравнения, изменять математические шрифты, делать символы жирными и работать с многострочными выражениями.

As a result, the goal of the lab was achieved: mastering math mode in LaTeX and using key math packages for professional-quality typesetting.

# Список литературы