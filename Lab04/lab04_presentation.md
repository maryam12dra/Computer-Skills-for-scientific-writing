# Лабораторная работа №4
## Including Graphics

**Отчёт по лабораторной работе №4**  
**Автор:** Драммех Мариама Л  
**Формат:** HTML presentation generated from Markdown

---

# 1. Цель работы

**Цель лабораторной работы:**

- познакомиться с основами включения графики в документы LaTeX;
- изучить пакет `graphicx`;
- научиться изменять размер, масштаб и поворот изображений;
- разобраться с плавающими объектами и перекрёстными ссылками.

**English summary:**
The purpose of this lab work is to learn how to include and manipulate graphics in LaTeX documents using the `graphicx` package and related tools.

---

# 2. Задание

В работе требовалось:

1. Study basic image inclusion with `graphicx` package.
2. Learn to modify graphic appearance (size, rotation, scaling).
3. Understand float environments for image placement.
4. Practice file naming and organization best practices.
5. Learn cross-referencing for figures.
6. Explore different float types and positioning options.
7. Complete the exercises with practical examples.

---

# 3. Включение графики / Including Graphics

Для вставки внешних изображений в LaTeX используется пакет `graphicx` и команда `\includegraphics`.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\usepackage{graphicx}
\begin{document}
This picture
\begin{center}
\includegraphics[height=2cm]{example-image}
\end{center}
is an imported PDF.
\end{document}
```

Главная идея: графика подключается как внешний файл и может быть встроена прямо в текст документа.

---

# 3.1 Изменение внешнего вида графики

Команда `\includegraphics` поддерживает множество опций:

- `height=...`
- `width=...`
- `scale=...`
- `angle=...`
- `clip` и `trim`

Примеры:

```latex
\includegraphics[height=0.5\textheight]{example-image}
\includegraphics[width=0.5\textwidth]{example-image}
\includegraphics[clip, trim=0 0 50 50]{example-image}
```

Эти параметры позволяют управлять размером, кадрированием и формой изображения.

---

# 3.2 Плавающие изображения / Making Images Float

Изображения часто оформляются как **floats**, чтобы LaTeX мог размещать их без больших пустот на странице.

```latex
\begin{figure}[ht]
\centering
\includegraphics[width=0.5\textwidth]{example-image-a.png}
\caption{An example image}
\end{figure}
```

Преимущества float-окружения:

- более аккуратная верстка;
- автоматический перенос изображения;
- нумерация и подписи.

---

# 3.3 Имена файлов и организация графики

Рекомендуется использовать простые имена файлов без пробелов и специальных символов.

```latex
\includegraphics[width=30pt]{pics/myimage.png}
```

Для хранения изображений в поддиректориях можно использовать:

```latex
\graphicspath{{figs/}{pics/}}
```

Это помогает поддерживать порядок в проекте и упрощает подключение графики.

---

# 3.4 Создание графики в LaTeX

LaTeX поддерживает растровую и векторную графику. Для векторной графики часто предпочитают PDF.

Пример с `TikZ`:

```latex
\documentclass{article}
\usepackage{tikz}
\begin{document}
\begin{tikzpicture}
\draw (0,0) circle (1cm);
\draw (-1,0) -- (1,0);
\end{tikzpicture}
\end{document}
```

Это показывает, что часть графики можно строить прямо средствами LaTeX.

---

# 3.5 Размещение плавающих объектов

Пакет `float` предоставляет спецификатор `H`, который фиксирует позицию объекта.

```latex
\usepackage{float}

\begin{figure}[H]
\centering
\includegraphics[width=0.5\textwidth]{example-image}
\caption{An example image}
\end{figure}
```

Типичные спецификаторы размещения:

- `h` — here;
- `t` — top;
- `b` — bottom;
- `H` — strict placement with `float` package.

---

# 3.6 Другие типы float и перекрёстные ссылки

Для новых типов плавающих сред можно использовать `trivfloat`:

```latex
\usepackage{trivfloat}
\trivfloat{image}
```

Для перекрёстных ссылок применяются `\label` и `\ref`:

```latex
\section{Title of the first section}
\label{subsec:labelone}
...
In subsection~\ref{subsec:labelone} ...
```

Это позволяет ссылаться на рисунки, разделы и уравнения автоматически.

---

# 4. Упражнения 1–4

Практическая часть включала:

- вставку собственного изображения;
- исследование опций `height`, `width`, `scale`, `angle`;
- сравнение `\textwidth` и `\linewidth`;
- проверку разных спецификаторов размещения float-объектов.

Пример:

```latex
\includegraphics[height=3cm]{my-photo.jpg}
\includegraphics[width=0.3\textwidth]{my-photo.jpg}
\includegraphics[scale=0.5]{my-photo.jpg}
\includegraphics[angle=45,width=0.2\textwidth]{my-photo.jpg}
```

---

# 4.1 Упражнения 5–7

Также были рассмотрены:

- перекрёстные ссылки и необходимость повторной компиляции;
- размещение `\label` до и после `\caption`;
- корректная и некорректная постановка `\label` в окружении `equation`.

Ключевой вывод:

- `\label` должен стоять **после `\caption`** для рисунков;
- `\label` для формулы должен располагаться **внутри** окружения `equation`.

---

# 5. Итоги и выводы

В ходе лабораторной работы были изучены:

- пакет `graphicx`;
- изменение размера и внешнего вида графики;
- плавающие объекты и их размещение;
- организация файлов изображений;
- перекрёстные ссылки на рисунки и формулы.

**Итог:** цель лабораторной работы достигнута — освоены базовые и практические приёмы включения графики в документы LaTeX.

---

# Примечание по иллюстрациям

В исходном Markdown-файле были ссылки на изображения `image-001.png` ... `image-016.png`,
но сами файлы изображений не были загружены вместе с документом.

Поэтому в презентацию включено:

- текстовое содержание отчёта;
- примеры LaTeX-кода;
- структура тем и упражнений;
- выводы без встроенных исходных скриншотов.

---

