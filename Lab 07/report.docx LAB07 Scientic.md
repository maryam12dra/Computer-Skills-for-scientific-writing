Отчёт по лабораторной работе №7

LaTeX Presentations and Posters

ДРАММЕХ МАРИАМА Л

Содержание

Список иллюстраций

Список таблиц

# 1 Цель работы

Целью данной лабораторной работы является освоение создания презентаций и постеров в LaTeX с использованием пакета Beamer и других инструментов для визуального представления научных работ.

The purpose of this lab work is to learn how to create presentations and posters in LaTeX using the Beamer package and other tools for visual presentation of scientific work.

# 2 Задание

1.  Освоить создание презентаций с использованием класса Beamer
2.  Изучить структуру презентаций, создание слайдов и управление контентом
3.  Научиться использовать паузы и эффекты появления для динамических презентаций

# 3 Теоретическое введение

## 3.1 7 Презентации LaTeX / LaTeX Presentations

### 3.1.1 7.1 Презентации с Beamer / Presentation with Beamer

В LaTeX можно создавать презентации с использованием класса документов beamer. In LaTeX it is possible to make presentations using the beamer document class.

\\documentclass{beamer}  
  
\\usetheme{Copenhagen}  
\\author{Bert}  
\\title{A tale of two primes}  
  
\\begin{document}  
  
\\begin{frame}  
\\titlepage  
\\end{frame}  
  
\\end{document}

### 3.1.2 7.1.1 Структура презентации / Structure of a Presentation

Для создания слайдов используется окружение frame с заголовком слайда. To make slides you use the frame environment with the slide title.

\\documentclass{beamer}

\\usetheme{Copenhagen}

\\author{Bert}

\\title{A Tale of Two Primes}

\\date{November 24, 2025}

\\begin{document}

\\begin{frame}

\\titlepage

\\end{frame}

\\begin{frame}\[t\]{Article}

Some text about the article.

\\end{frame}

\\begin{frame}\[t\]{Mathematica}

A helpful tool for mathematicians.

\\end{frame}

\\end{document}

![](./report.docx%20LAB07%20Scientic_images/image-001.png)

### 3.1.3 7.1.2 Паузы / Pauses

Команда \\pause позволяет элементам появляться последовательно. The \\pause command allows elements to appear one by one.

\\documentclass{beamer}

\\usetheme{Copenhagen}

\\author{Bert}

\\title{A Tale of Two Primes}

\\begin{document}

\\begin{frame}{Article}

\\begin{block}{Definition}

This is a definition block.

\\end{block}

\\pause

\\begin{block}{Euclid's theorem}

This is a theorem.

\\end{block}

\\end{frame}

\\end{document}

![](./report.docx%20LAB07%20Scientic_images/image-002.png)

### 3.1.4 7.1.3 Появление элементов / Uncover

Команда \\uncover дает больше контроля над появлением элементов. The \\uncover command gives more control over element appearance.

\\documentclass{article}

\\usepackage{amsmath}

\\begin{document}

\\section\*{Sets}

A set is a collection of objects. For example:

\\\[

Z = \\{ \\text{one, two, three} \\}

\\\]

We call the objects in \\( Z \\) the elements of \\( Z \\). We write

\\\[

\\text{elem} \\in Z

\\\]

\\end{document}

![](./report.docx%20LAB07%20Scientic_images/image-003.png)

### 3.1.5 7.1.4 Оформление / Layout

Beamer предоставляет различные темы для изменения внешнего вида. Beamer provides various themes to change appearance.

\\usetheme{Warsaw}  
\\usecolortheme{beaver}

### 3.1.6 7.1.5 Советы для коротких презентаций / Tips for Short Presentations

-   Изолируйте основную тему и представьте её рано / Isolate the main subject and cover it early
-   Используйте картинки вместо текста / Use pictures instead of text
-   Примеры вместо абстрактных определений / Examples instead of abstract definitions
-   Следите за временем / Watch the time

## 3.2 7.2 Постеры / Posters

### 3.2.1 Основные методы создания постеров / Main Poster Creation Methods

1.  **Класс a0poster** - похож на article с колонками
2.  **Пакет beamerposter** - использует возможности Beamer
3.  **Класс tikzposter** - основан на TikZ с блочной структурой

### 3.2.2 7.2.1 Класс a0poster / The a0poster documentclass

\\documentclass\[a0, portrait\]{a0poster}  
\\usepackage{multicol}  
\\setlength{\\columnsep}{100pt}  
  
\\begin{document}  
\\begin{multicols}{2}  
% Содержание постерa / Poster content  
\\end{multicols}  
\\end{document}

### 3.2.3 7.2.2 Пакет beamerposter / The beamerposter package

\\documentclass\[xcolor={svgnames}\]{beamer}

\\usepackage\[utf8\]{inputenc}

\\usepackage\[T2A\]{fontenc}

\\usepackage\[russian\]{babel}

\\usepackage\[orientation=portrait,size=a0,scale=1\]{beamerposter}

\\usepackage{bookmark}

\\usetheme{Berlin}

\\title{Научный постер с Beamer}

\\author{Maryam}

\\institute{РУДН}

\\begin{document}

\\begin{frame}

\\begin{columns}

\\begin{column}{0.32\\textwidth}

\\begin{block}{Введение}

Beamerposter позволяет использовать все возможности Beamer для создания постеров

\\end{block}

\\begin{block}{Преимущества}

\\begin{itemize}

\\item Единый стиль с презентациями

\\item Богатые возможности оформления

\\item Простота использования

\\end{itemize}

\\end{block}

\\end{column}

\\begin{column}{0.32\\textwidth}

\\begin{exampleblock}{Пример}

\\begin{center}

\\includegraphics\[width=0.8\\textwidth\]{example-image}

\\end{center}

Графическое представление данных

\\end{exampleblock}

\\end{column}

\\begin{column}{0.32\\textwidth}

\\begin{alertblock}{Важная информация}

LaTeX обеспечивает высокое качество типографики и математических формул

\\end{alertblock}

\\begin{block}{Заключение}

Beamerposter - отличный выбор для научных постеров

\\end{block}

\\end{column}

\\end{columns}

\\end{frame}

\\end{document}

![](./report.docx%20LAB07%20Scientic_images/image-004.png)

### 3.2.4 7.2.3 Класс tikzposter / The tikzposter documentclass

\\documentclass\[24pt, a0paper, portrait\]{tikzposter}

\\usepackage{graphicx}

\\usepackage{caption}

\\usepackage{tikz}

\\title{Look I'm making a poster!}

\\author{Ostap S. Bender \\\\ RUDN University}

\\usetheme{Default}

\\begin{document}

\\maketitle

\\begin{columns}

    % LEFT COLUMN

    \\column{0.5}

    \\block{Experimental Setup and Methodology}{

        \\begin{center}

            \\includegraphics\[width=0.9\\textwidth, height=8cm\]{instituteLogo.jpg}

            \\captionof{figure}{Experimental Setup and Methodology}

        \\end{center}

        Figure illustrates the experimental configuration used in our research. The setup includes...

    }

    % RIGHT COLUMN  

    \\column{0.5}

    \\block{Mathematical Analysis}{

        \\begin{center}

            \\begin{tikzpicture}\[scale=1.2\]

                % Example mathematical visualization

                \\draw\[->\] (-2,0) -- (2,0) node\[right\] {$x$};

                \\draw\[->\] (0,-1) -- (0,2) node\[above\] {$y$};

                \\draw\[domain=-1.5:1.5, smooth, thick, blue\] plot (\\x, {\\x\*\\x});

                \\node at (1,2.5) {$y = x^2$};

                % Grid (optional)

                \\draw\[gray, very thin\] (-2,-1) grid (2,2);

            \\end{tikzpicture}

        \\end{center}

        The mathematical analysis shows the quadratic relationship between variables...

    }

\\end{columns}

\\end{document}

![](./report.docx%20LAB07%20Scientic_images/image-005.png)

# 4 Выполнение лабораторной работы

## 4.1 Создание постера с beamerposter / Creating Poster with beamerposter

\\documentclass\[xcolor={svgnames},10pt,utf8\]{beamer}

\\usepackage\[utf8\]{inputenc}

\\usepackage\[T1\]{fontenc}

\\usepackage\[russian\]{babel}

\\frenchspacing

\\usepackage\[orientation=portrait,size=a0,scale=1.4\]{beamerposter}

\\usepackage{lmodern}

\\usetheme{Berlin}

\\title{Научный постер с Beamer}

\\author{Maryam}

\\institute{РУДН}

\\begin{document}

\\begin{frame}

\\begin{columns}

\\begin{column}{0.32\\textwidth}

\\begin{block}{Введение}

Beamerposter позволяет использовать все возможности Beamer для создания постеров

\\end{block}

\\begin{block}{Преимущества}

\\begin{itemize}

\\item Единый стиль с презентациями

\\item Богатые возможности оформления

\\item Простота использования

\\end{itemize}

\\end{block}

\\end{column}

\\begin{column}{0.32\\textwidth}

\\begin{exampleblock}{Пример}

\\begin{center}

\\includegraphics\[width=0.8\\textwidth\]{example-image}

\\end{center}

Графическое представление данных

\\end{exampleblock}

\\end{column}

\\begin{column}{0.32\\textwidth}

\\begin{alertblock}{Важная информация}

LaTeX обеспечивает высокое качество типографики и математических формул

\\end{alertblock}

\\begin{block}{Заключение}

Beamerposter - отличный выбор для научных постеров

\\end{block}

\\end{column}

\\end{columns}

\\end{frame}

\\end{document}

![](./report.docx%20LAB07%20Scientic_images/image-006.png)

# 5 Выводы

В ходе лабораторной работы №7 я освоил создание презентаций и постеров в LaTeX. Изучил работу с классом Beamer для создания динамических презентаций с паузами и эффектами появления. Освоил три основных метода создания постеров: a0poster, beamerposter и tikzposter, изучил их преимущества и особенности применения. На практике создал презентации с математическим содержанием и научные постеры, что позволило закрепить полученные знания.

In this lab work 7, I mastered creating presentations and posters in LaTeX. I studied working with the Beamer class for creating dynamic presentations with pauses and appearance effects. I mastered three main methods for creating posters: a0poster, beamerposter and tikzposter, studied their advantages and application features. In practice, I created presentations with mathematical content and scientific posters, which allowed me to consolidate the acquired knowledge.

# Список литературы

1.  Practical scientific writing - Presentations and Posters chapter
2.  Beamer User Guide - Till Tantau
3.  LaTeX/Beamer - Wikibooks
4.  a0poster, beamerposter, tikzposter package documentation