## Meetei Script (ꯃꯤꯇꯩ ꯃꯌꯦꯛ)

Meetei script is an abugida used for Meeteilon (the official language for the Manipuris). The word "Meetei" is sometimes written as "Meitei" and as such, they should be considered synonymous and interchageable although "Meitei" has reasons to be preferred. Historical records suggest that it is at least 900 years old. The name of its letters are the names of human body parts and they also serve as phonetic names. It was encoded in Unicode in 2009.

### Unicode (UTF-16)

The Unicode block for the Meitei script, called Meetei Mayek, is from U+ABC0 to U+ABFF. The official chart can be found [here](https://www.unicode.org/charts/PDF/UABC0.pdf). The following table should be self-explanatory. For instance, ꯇ is coded by U+ABC7. Likewise, ꯢ is coded by U+ABE2.

|        | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | A | B | C | D | E | F |
| ------ | ---| --- | ---| --- |--- |--- | --- | --- |--- |--- |--- |--- |--- |--- |--- |--- |
| U+ABCx | ꯀ | ꯁ| ꯂ | ꯃ |	ꯄ |	ꯅ |	ꯆ |	ꯇ |	ꯈ |	ꯉ | ꯊ |	ꯋ |	ꯌ |	ꯍ |	ꯎ |	ꯏ |
| U+ABDx | ꯐ | ꯑ | ꯒ| ꯓ | ꯔ | ꯕ |	ꯖ |	ꯗ |	ꯘ |	ꯙ |	ꯚ |	ꯛ |	ꯜ |	ꯝ |	ꯞ |	ꯟ |
| U+ABEx | ꯠ | ꯡ | ꯢ | ꯣ | ꯤ |	ꯥ |	ꯦ |	ꯧ |	ꯨ |	ꯩ |	ꯪ |	꯫ |	꯬ |	꯭ 	|  |  |
| U+ABFx | ꯰ | ꯱ | ꯲ | ꯳ | ꯴ | ꯵ | ꯶ | ꯷ | ꯸ | ꯹ |  |  |  |  |  |  |

A special attention should be given to U+ABFx. These are the corresponding digits in Meetei script. For instance, the digit 7 is given by U+ABF7, that is, ꯷ in Meeitei script is the digit 7.

### Typsetting in LaTeX

Using the package `inputech` with the option `utf8` does not help since the script is encoded in UTF-16. One way to natively use Meitei script in TeX/LaTeX is to first install a font that renders the script. For instance, You can download and install [Nano Sans Meitei Mayek](https://fonts.google.com/noto/specimen/Noto+Sans+Meetei+Mayek) available at Google Fonts. Then use the following code.

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

The sample TeX file is [here](meitei-script.tex). The PDF output generated through LuaTeX compilation is [here](meitei-script.pdf).

### Feedback

Any queries, comments, bug reports or suggestions shall be directed to [ronhuidrom@gmail.com](mailto:ronhuidrom@gmail.com).
