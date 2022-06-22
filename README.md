## Meetei Script (ꯃꯤꯇꯩ ꯃꯌꯦꯛ)

Meetei script is an abugida used for Meeteilon (the official language for the Manipuris). The word "Meetei" is sometimes written as "Meitei" and as such, they should be considered synonymous and interchageable although "Meetei" has reasons to be preferred. Historical records suggest that it is at least 900 years old. The name of its letters are the names of human body parts and they also serve as phonetic names. It was encoded in Unicode in 2009.

### Unicode (UTF-16)

The Unicode block for the Meetei script, called Meetei Mayek, is from U+ABC0 to U+ABFF. The official chart can be found [here](https://www.unicode.org/charts/PDF/UABC0.pdf). The following table should be self-explanatory. For instance, ꯇ is coded by U+ABC7. Likewise, ꯢ is coded by U+ABE2.

|        | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | A | B | C | D | E | F |
| ------ | ---| --- | ---| --- |--- |--- | --- | --- |--- |--- |--- |--- |--- |--- |--- |--- |
| U+ABCx | ꯀ | ꯁ| ꯂ | ꯃ |	ꯄ |	ꯅ |	ꯆ |	ꯇ |	ꯈ |	ꯉ | ꯊ |	ꯋ |	ꯌ |	ꯍ |	ꯎ |	ꯏ |
| U+ABDx | ꯐ | ꯑ | ꯒ| ꯓ | ꯔ | ꯕ |	ꯖ |	ꯗ |	ꯘ |	ꯙ |	ꯚ |	ꯛ |	ꯜ |	ꯝ |	ꯞ |	ꯟ |
| U+ABEx | ꯠ | ꯡ | ꯢ | ꯣ | ꯤ |	ꯥ |	ꯦ |	ꯧ |	ꯨ |	ꯩ |	ꯪ |	꯫ |	꯬ |	꯭ 	|  |  |
| U+ABFx | ꯰ | ꯱ | ꯲ | ꯳ | ꯴ | ꯵ | ꯶ | ꯷ | ꯸ | ꯹ |  |  |  |  |  |  |

A special attention should be given to U+ABFx. These are the corresponding digits in Meetei script. For instance, the digit 7 is given by U+ABF7, that is, ꯷ in Meetei script is the digit 7.

### Typsetting in LaTeX

Using the package `inputech` with the option `utf8` does not help since the script is encoded in UTF-16. One way to natively use Meetei script in TeX/LaTeX is to first install a font that renders the script. For instance, You can download and install [Nano Sans Meetei Mayek](https://fonts.google.com/noto/specimen/Noto+Sans+Meetei+Mayek) available at Google Fonts. Then use the following code.

```latex
\documentclass{article}
\usepackage{fontspec}
\begin{document}
  Let's type some Meetei Mayek! 
  {\fontspec{Noto Sans Meetei Mayek}
    ꯍꯨꯏꯗꯔꯣꯝ ꯔꯣꯅꯜꯗ ꯃꯉꯥꯡ 
  }
  If you don't have a keyboard or copy-paste at your disposal, you can simply use unicode.
  {\fontspec{Noto Sans Meetei Mayek}
    \symbol{"ABE2
  }
\end{document}
```

Compiling the above code with the usual `pdfLaTeX` shall lead to fatal error. Compilation shall be done using `LuaTeX` or `XeTeX` (because `fontspec` requires them).

The sample TeX file is [here](meetei-script.tex). The PDF output generated through LuaTeX compilation is [here](meetei-script.pdf).

### Typesetting in HTML and Markdown

There are two ways to typeset Meetei Script in HTML. The first is to directly use the script which is possible if you already have a Meetei Mayek keyboard or just copy-paste from somewhere else. If this is not feasible, the second method is to (you guess it right!) use Unicode. For this simply use the usual syntax for entering Unicode code points in HTML. Suppose you want to enter ꯔ which is coded as U+ABD4, you write in the form `&#xY;` where Y is replaced by ABD4. See a sample HTML filel [here](meetei-script.html).

Typesetting in Markdown is just the same as in HTML. However, be warned that I have only verified this on GitHub Markdown although there is no reason why it shouldn't work elsewhere.

### Feedback

Any queries, comments, bug reports or suggestions shall be directed to [ronhuidrom@gmail.com](mailto:ronhuidrom@gmail.com).
