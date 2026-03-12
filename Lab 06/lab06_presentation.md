# Лабораторная работа №6
## Working with Bibliography

**Автор:** ДРАММЕХ МАРИАМА Л  
**Формат:** HTML presentation generated from Markdown

---

# 1. Цель работы

- освоить методы работы с библиографией в LaTeX;
- изучить BibTeX + `natbib` и `biblatex` + Biber;
- сравнить оба подхода и выполнить практические упражнения.

**English summary:**
Learn how to manage bibliography in LaTeX using BibTeX and biblatex.

---

# 2. Задание

1. Освоить workflow с `natbib` и BibTeX.
2. Освоить workflow с `biblatex` и Biber.
3. Сравнить два подхода.
4. Выполнить упражнения по созданию и управлению ссылками.

---

# 3. Библиография в LaTeX

Библиографические ссылки обычно формируются из внешних баз данных `.bib`.

```latex
\usepackage{natbib}
...
\citet{Graham1995}
\citep{Thomas2008}
\bibliographystyle{plainnat}
\bibliography{learnlatex}
```

Это позволяет отделить данные о публикациях от основного текста документа.

---

# 3.1 Базы данных BibTeX

Записи в `.bib` содержат поля вроде `author`, `title`, `year`, `journal`, `doi`.

```bibtex
@article{Thomas2008,
  author = {Thomas, Christine M. and Liu, Tianbiao},
  title = {Series of Mixed Valent Complexes},
  journal = {Inorg. Chem.},
  year = {2008}
}
```

Такой формат удобен для автоматического построения списка литературы.

---

# 3.2 Workflow: natbib + BibTeX

Основная последовательность компиляции:

- LaTeX
- BibTeX
- LaTeX
- LaTeX

Пример:

```latex
The mathematics showcase is from \citet{Graham1995}.
Some parenthetical citations: \citep{Thomas2008}.
```

Пакет `natbib` даёт гибкие команды для авторских и скобочных ссылок.

---

# 3.3 Workflow: biblatex + Biber

Современный подход использует `biblatex` и Biber.

- LaTeX
- Biber
- LaTeX

```latex
\usepackage[style=authoryear]{biblatex}
\addbibresource{learnlatex.bib}
...
\textcite{Thomas2008}
\parencite{Graham1995}
\printbibliography
```

Преимущество — более гибкая настройка и лучшая поддержка Unicode.

---

# 3.4 Выбор между BibTeX и biblatex

**BibTeX workflow:**
- давно используется и хорошо поддерживается;
- опирается на `.bst` стили;
- слабее поддерживает Unicode.

**biblatex workflow:**
- более гибкий;
- лучше работает с неанглийской сортировкой;
- подходит для сложных стилей цитирования.

---

# 3.5 Дополнительные темы

В отчёте также рассматривались:

- неанглийская сортировка через Biber;
- гиперссылки в библиографии с `hyperref`;
- различия в лучших практиках ввода полей для старых и новых стилей.

Пример:

```latex
\usepackage[hidelinks]{hyperref}
```

---

# 4. Практические упражнения

Практика включала:

- использование `natbib` и `biblatex` на реальных примерах;
- добавление новой записи `Einstein1905`;
- ссылку на отсутствующую запись;
- эксперименты с числовыми стилями библиографии.

Главный вывод: корректность ссылок зависит не только от кода, но и от правильной последовательности компиляции.

---

# 5. Итоги и выводы

В ходе работы были освоены:

- два основных подхода к библиографии в LaTeX;
- создание и редактирование `.bib`-баз;
- управление стилями цитирования;
- работа с Unicode и гиперссылками.

**Итог:** пользователь освоил как традиционный, так и современный workflow библиографии в LaTeX.

---

# Примечание по иллюстрациям

В исходном файле были ссылки на изображения `image-001.png` ... `image-009.png`,
но сами изображения не были загружены вместе с Markdown.

Поэтому презентация включает:
- содержание отчёта;
- примеры кода;
- сравнительный обзор workflow.
