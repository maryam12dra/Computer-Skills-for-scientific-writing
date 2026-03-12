# Лабораторная работа №2
## Practical scientific writing

**Автор:** ДРАММЕХ МАРИАМА Л  
**Формат:** HTML presentation from Markdown

---

# 1. Цель работы

Цель данной лабораторной работы — ознакомиться со **структурой документа LaTeX** и базовыми приемами практического научного письма.

**Фокус работы:**
- создание первого документа;
- абзацы и пробелы;
- связь исходника и PDF;
- жесткие пробелы и переносы строк.

---

# 2. Задание

1. Try adding text to your first document, typesetting and seeing the changes in your PDF.
2. Make some different paragraphs and add variable spaces.
3. Explore how your editor works; click on your source and find how to go to the same line in your PDF.
4. Try adding some hard spaces and see how they influence line-breaking.

---

# 3. Теоретическое введение

Минимальный пример документа LaTeX:

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\begin{document}
Hey world!
This is a first document.
\end{document}
```

**Смысл примера:** показать базовую структуру документа — класс, подключение пакета и содержимое документа.

---

# 3.1 Running LaTeX

В исходном отчете этот раздел сопровождается иллюстрациями **fig:002–fig:005**.

Ключевая идея раздела:
- запустить компиляцию LaTeX;
- проверить, как исходный `.tex` превращается в PDF;
- увидеть, как редактор связывает текст и итоговый вывод.

> Иллюстрации были указаны в исходнике, но сами файлы изображений не были загружены вместе с Markdown-файлом.

---

# 3.2 Документ TeXlive с нижним колонтитулом

```latex
\documentclass[a4paper,12pt]{article}
% The document class with options
\usepackage[T1]{fontenc}
% A comment in the preamble
\begin{document}
% This is a comment
Trhis is a simple
 document\footnote{with a footnote}fi
This is a new paragraph.
\end{document}
```

В исходном отчете этот блок сопровождается иллюстрациями **fig:006–fig:008**.

---

# 4. Выполнение лабораторной работы
## 4.1 Первый документ и компиляция в PDF

```latex
\documentclass[12pt]{article}
\usepackage[english]{babel}
\usepackage[utf8]{inputenc}
\begin{document}
Hello world!

This is my first document with LaTeX.

Here is some content full of sentences to test the PDF rendering.
You can write text. *Article* class is freely available.

Here is a second paragraph. Words keep their spaces between words,
LaTeX automatically results in a single space.

Word~habit, "Brusubi~is a city", "Dupont~and Brusubi~cannot".

Chapter one example: introduction.
\end{document}
```

---

# 4.2–4.4 Наблюдения по заданиям

**4.2. Different paragraphs and variable spaces**
- LaTeX нормализует последовательности обычных пробелов.
- Абзацы определяются структурой текста, а не количеством пробелов.

**4.3. Source ↔ PDF navigation**
- редактор помогает перейти от строки исходника к соответствующему месту в PDF.

**4.4. Hard spaces**
- символ `~` создает неразрывный пробел;
- он предотвращает перенос строки в неудобном месте.

---

# Иллюстрации из исходного отчета

В файле были ссылки на изображения:

- `image-001.png` … `image-012.png`
- примеры помечены как **fig:001–fig:011**

**Важно:** в текущей загрузке присутствовал только один файл Markdown, поэтому в HTML-презентацию перенесены:
- структура отчета;
- текстовое содержание;
- LaTeX-код;
- пометки о местах, где должны быть иллюстрации.

---

# 5. Выводы

Таким образом, была достигнута цель лабораторной работы:
- установлен и использован TeXlive;
- выполнено знакомство со структурой документов LaTeX;
- рассмотрены абзацы, пробелы и неразрывные пробелы;
- изучена связь между исходным текстом и PDF-результатом.

---.
