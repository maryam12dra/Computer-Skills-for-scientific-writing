<!doctype html>
<html lang="ru">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Lab02 Scientific Writing Presentation</title>
<style>
  :root {
    --bg1: #0b1020;
    --bg2: #1a2456;
    --text: #eef2ff;
    --muted: #b8c2f2;
    --accent: #87b7ff;
    --accent2: #8ef0c2;
    --code: #0f172a;
    --border: rgba(255,255,255,0.15);
  }
  * { box-sizing: border-box; }
  html, body { margin: 0; height: 100%; background: radial-gradient(circle at top right, #243b8f 0%, var(--bg1) 42%, #050814 100%); color: var(--text); font-family: Inter, Segoe UI, Arial, sans-serif; overflow: hidden; }
  .deck { width: 100vw; height: 100vh; position: relative; }
  .slide { display: none; width: 100%; height: 100%; padding: 56px 64px 72px; position: absolute; inset: 0; }
  .slide.active { display: block; }
  .slide-inner { width: 100%; height: 100%; border: 1px solid var(--border); border-radius: 28px; background: linear-gradient(180deg, rgba(255,255,255,0.11), rgba(255,255,255,0.05)); box-shadow: 0 24px 70px rgba(0,0,0,0.28); padding: 46px 54px; overflow: auto; backdrop-filter: blur(12px); }
  h1, h2, h3 { margin: 0 0 16px; line-height: 1.1; }
  h1 { font-size: 2.15rem; letter-spacing: -0.03em; }
  h2 { font-size: 1.35rem; color: var(--accent2); font-weight: 700; margin-top: 6px; }
  h3 { font-size: 1.05rem; color: var(--accent); margin-top: 20px; }
  p, li, blockquote { font-size: 1.08rem; line-height: 1.55; color: var(--text); }
  ul, ol { padding-left: 1.4rem; margin: 14px 0; }
  li + li { margin-top: 8px; }
  code { font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, monospace; background: rgba(255,255,255,0.08); border-radius: 6px; padding: 2px 6px; font-size: 0.95em; }
  pre { background: var(--code); color: #d7e3ff; padding: 18px 20px; border-radius: 18px; overflow: auto; border: 1px solid rgba(255,255,255,0.12); margin: 18px 0; }
  pre code { background: transparent; padding: 0; border-radius: 0; font-size: 0.94rem; }
  strong { color: white; }
  blockquote { margin: 18px 0 0; padding: 14px 18px; border-left: 4px solid var(--accent); background: rgba(0,0,0,0.18); border-radius: 10px; color: var(--muted); }
  .nav { position: fixed; left: 28px; right: 28px; bottom: 24px; display: flex; align-items: center; justify-content: space-between; gap: 16px; z-index: 5; }
  .nav .group { display: flex; gap: 10px; align-items: center; }
  button { appearance: none; border: 0; background: rgba(255,255,255,0.12); color: white; padding: 12px 16px; border-radius: 12px; font-size: 0.95rem; cursor: pointer; }
  button:hover { background: rgba(255,255,255,0.18); }
  .counter { background: rgba(255,255,255,0.12); border: 1px solid var(--border); padding: 10px 14px; border-radius: 12px; color: var(--muted); min-width: 110px; text-align: center; }
  .hint { color: var(--muted); font-size: 0.92rem; }
  .source-toggle { position: fixed; top: 20px; right: 22px; z-index: 6; }
  .source-panel { display:none; position: fixed; inset: 24px; background: rgba(5, 8, 20, 0.96); border: 1px solid var(--border); border-radius: 22px; padding: 24px; z-index: 10; }
  .source-panel.open { display:block; }
  .source-panel h3 { margin-top: 0; }
  .source-panel pre { height: calc(100% - 74px); white-space: pre-wrap; }
  .badge { display:inline-block; padding: 6px 10px; border-radius: 999px; font-size: 0.86rem; color: white; background: rgba(142,240,194,0.12); border: 1px solid rgba(142,240,194,0.25); margin-bottom: 14px; }
  @media (max-width: 900px) {
    .slide { padding: 16px 16px 78px; }
    .slide-inner { padding: 28px 24px; border-radius: 20px; }
    h1 { font-size: 1.6rem; }
    h2 { font-size: 1.05rem; }
    p, li, blockquote { font-size: 0.98rem; }
    .nav { left: 16px; right: 16px; bottom: 16px; }
    .hint { display:none; }
  }
</style>
</head>
<body>
<div class="deck"><section class="slide active" data-index="0"><div class="slide-inner"><div class="badge">Markdown HTML Presentation</div><h1>Лабораторная работа №2</h1>
<h2>Practical scientific writing</h2>
<p><strong>Автор:</strong> ДРАММЕХ МАРИАМА Л<br />
<strong>Формат:</strong> HTML presentation from Markdown</p>
</div></section><section class="slide" data-index="1"><div class="slide-inner"><div class="badge">Markdown HTML Presentation</div><h1>1. Цель работы</h1>
<p>Цель данной лабораторной работы — ознакомиться со <strong>структурой документа LaTeX</strong> и базовыми приемами практического научного письма.</p>
<p><strong>Фокус работы:</strong></p>
<ul>
<li>создание первого документа;</li>
<li>абзацы и пробелы;</li>
<li>связь исходника и PDF;</li>
<li>жесткие пробелы и переносы строк.</li>
</ul>
</div></section><section class="slide" data-index="2"><div class="slide-inner"><div class="badge">Markdown HTML Presentation</div><h1>2. Задание</h1>
<ol>
<li>Try adding text to your first document, typesetting and seeing the changes in your PDF.</li>
<li>Make some different paragraphs and add variable spaces.</li>
<li>Explore how your editor works; click on your source and find how to go to the same line in your PDF.</li>
<li>Try adding some hard spaces and see how they influence line-breaking.</li>
</ol>
</div></section><section class="slide" data-index="3"><div class="slide-inner"><div class="badge">Markdown HTML Presentation</div><h1>3. Теоретическое введение</h1>
<p>Минимальный пример документа LaTeX:</p>
<pre><code class="language-latex">\documentclass{article}
\usepackage[T1]{fontenc}
\begin{document}
Hey world!
This is a first document.
\end{document}
</code></pre>
<p><strong>Смысл примера:</strong> показать базовую структуру документа — класс, подключение пакета и содержимое документа.</p>
</div></section><section class="slide" data-index="4"><div class="slide-inner"><div class="badge">Markdown HTML Presentation</div><h1>3.1 Running LaTeX</h1>
<p>В исходном отчете этот раздел сопровождается иллюстрациями <strong>fig:002–fig:005</strong>.</p>
<p>Ключевая идея раздела:</p>
<ul>
<li>запустить компиляцию LaTeX;</li>
<li>проверить, как исходный <code>.tex</code> превращается в PDF;</li>
<li>увидеть, как редактор связывает текст и итоговый вывод.</li>
</ul>
<blockquote>
<p>Иллюстрации были указаны в исходнике, но сами файлы изображений не были загружены вместе с Markdown-файлом.</p>
</blockquote>
</div></section><section class="slide" data-index="5"><div class="slide-inner"><div class="badge">Markdown HTML Presentation</div><h1>3.2 Документ TeXlive с нижним колонтитулом</h1>
<pre><code class="language-latex">\documentclass[a4paper,12pt]{article}
% The document class with options
\usepackage[T1]{fontenc}
% A comment in the preamble
\begin{document}
% This is a comment
Trhis is a simple
 document\footnote{with a footnote}fi
This is a new paragraph.
\end{document}
</code></pre>
<p>В исходном отчете этот блок сопровождается иллюстрациями <strong>fig:006–fig:008</strong>.</p>
</div></section><section class="slide" data-index="6"><div class="slide-inner"><div class="badge">Markdown HTML Presentation</div><h1>4. Выполнение лабораторной работы</h1>
<h2>4.1 Первый документ и компиляция в PDF</h2>
<pre><code class="language-latex">\documentclass[12pt]{article}
\usepackage[english]{babel}
\usepackage[utf8]{inputenc}
\begin{document}
Hello world!

This is my first document with LaTeX.

Here is some content full of sentences to test the PDF rendering.
You can write text. *Article* class is freely available.

Here is a second paragraph. Words keep their spaces between words,
LaTeX automatically results in a single space.

Word~habit, &quot;Brusubi~is a city&quot;, &quot;Dupont~and Brusubi~cannot&quot;.

Chapter one example: introduction.
\end{document}
</code></pre>
</div></section><section class="slide" data-index="7"><div class="slide-inner"><div class="badge">Markdown HTML Presentation</div><h1>4.2–4.4 Наблюдения по заданиям</h1>
<p><strong>4.2. Different paragraphs and variable spaces</strong></p>
<ul>
<li>LaTeX нормализует последовательности обычных пробелов.</li>
<li>Абзацы определяются структурой текста, а не количеством пробелов.</li>
</ul>
<p><strong>4.3. Source ↔ PDF navigation</strong></p>
<ul>
<li>редактор помогает перейти от строки исходника к соответствующему месту в PDF.</li>
</ul>
<p><strong>4.4. Hard spaces</strong></p>
<ul>
<li>символ <code>~</code> создает неразрывный пробел;</li>
<li>он предотвращает перенос строки в неудобном месте.</li>
</ul>
</div></section><section class="slide" data-index="8"><div class="slide-inner"><div class="badge">Markdown HTML Presentation</div><h1>Иллюстрации из исходного отчета</h1>
<p>В файле были ссылки на изображения:</p>
<ul>
<li><code>image-001.png</code> … <code>image-012.png</code></li>
<li>примеры помечены как <strong>fig:001–fig:011</strong></li>
</ul>
<p><strong>Важно:</strong> в текущей загрузке присутствовал только один файл Markdown, поэтому в HTML-презентацию перенесены:</p>
<ul>
<li>структура отчета;</li>
<li>текстовое содержание;</li>
<li>LaTeX-код;</li>
<li>пометки о местах, где должны быть иллюстрации.</li>
</ul>
</div></section><section class="slide" data-index="9"><div class="slide-inner"><div class="badge">Markdown HTML Presentation</div><h1>5. Выводы</h1>
<p>Таким образом, была достигнута цель лабораторной работы:</p>
<ul>
<li>установлен и использован TeXlive;</li>
<li>выполнено знакомство со структурой документов LaTeX;</li>
<li>рассмотрены абзацы, пробелы и неразрывные пробелы;</li>
<li>изучена связь между исходным текстом и PDF-результатом.</li>
</ul>
</div></section><section class="slide" data-index="10"><div class="slide-inner"><div class="badge">Markdown HTML Presentation</div><h1>Список литературы / Источник</h1>
<p><strong>Исходный файл:</strong> <code>report.doc Lab02 Scientific.md</code></p>
<p>Эта презентация является HTML-версией, собранной из Markdown-структуры исходного отчета.</p>
</div></section></div>
<button class="source-toggle" id="sourceBtn">Markdown source</button>
<div class="source-panel" id="sourcePanel"><h3>Presentation markdown</h3><pre># Лабораторная работа №2
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

&gt; Иллюстрации были указаны в исходнике, но сами файлы изображений не были загружены вместе с Markdown-файлом.

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

Word~habit, &quot;Brusubi~is a city&quot;, &quot;Dupont~and Brusubi~cannot&quot;.

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

---


</pre></div>
<div class="nav"><div class="group"><button id="prevBtn">◀ Previous</button><button id="nextBtn">Next ▶</button></div><div class="counter" id="counter">1 / 11</div><div class="hint">Use ← → or Space to navigate</div></div>
<script>
  const slides = [...document.querySelectorAll('.slide')];
  const counter = document.getElementById('counter');
  let current = 0;
  function show(i) {
    current = (i + slides.length) % slides.length;
    slides.forEach((s, idx) => s.classList.toggle('active', idx === current));
    counter.textContent = `${current + 1} / ${slides.length}`;
    location.hash = `slide-${current + 1}`;
  }
  function parseHash() {
    const m = location.hash.match(/slide-(\d+)/);
    if (m) {
      const idx = Math.max(0, Math.min(slides.length - 1, parseInt(m[1], 10) - 1));
      show(idx);
    }
  }
  document.getElementById('prevBtn').addEventListener('click', () => show(current - 1));
  document.getElementById('nextBtn').addEventListener('click', () => show(current + 1));
  document.addEventListener('keydown', (e) => {
    if (['ArrowRight', 'PageDown', ' '].includes(e.key)) { e.preventDefault(); show(current + 1); }
    if (['ArrowLeft', 'PageUp'].includes(e.key)) { e.preventDefault(); show(current - 1); }
    if (e.key === 'Home') show(0);
    if (e.key === 'End') show(slides.length - 1);
    if (e.key.toLowerCase() === 'm') document.getElementById('sourcePanel').classList.toggle('open');
    if (e.key === 'Escape') document.getElementById('sourcePanel').classList.remove('open');
  });
  document.getElementById('sourceBtn').addEventListener('click', () => document.getElementById('sourcePanel').classList.toggle('open'));
  document.getElementById('sourcePanel').addEventListener('click', (e) => { if (e.target.id === 'sourcePanel') e.currentTarget.classList.remove('open'); });
  window.addEventListener('hashchange', parseHash);
  parseHash();
</script>
</body>
</html>