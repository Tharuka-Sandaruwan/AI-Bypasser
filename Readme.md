# Instructions for Using Obfuscated Text with Overleaf or LaTeX Editors

## Step 1: Obfuscate the Text

1. Use the provided `index.html` to obfuscate the words so that AI detectors will fail.
2. Copy and paste the obfuscated content into a Word document.
3. Word will show a lot of grammar errors as it includes a lot of non-English characters.

## Step 2: Prepare LaTeX Document

To use the obfuscated text with Overleaf or other LaTeX editors, add the following code to the preamble of your LaTeX document:

```latex
\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage{lmodern} % Optional: for better font rendering

% Declare specific Unicode characters if necessary
\DeclareUnicodeCharacter{200C}{\textcompwordmark} % Zero Width Non-Joiner
\DeclareUnicodeCharacter{200D}{\textcompwordmark} % Zero Width Joiner
\DeclareUnicodeCharacter{FEFF}{\textcompwordmark} % Zero Width No-Break Space
\DeclareUnicodeCharacter{2008}{\ } % Punctuation Space
\DeclareUnicodeCharacter{2007}{\ } % Figure Space
\DeclareUnicodeCharacter{212A}{K} % Kelvin Sign
\DeclareUnicodeCharacter{2236}{:} % Ratio
\DeclareUnicodeCharacter{0410}{A} % Cyrillic Capital Letter A
\DeclareUnicodeCharacter{0430}{a} % Cyrillic Small Letter a
\DeclareUnicodeCharacter{041C}{M} % Cyrillic Capital Letter Em
\DeclareUnicodeCharacter{0425}{X} % Cyrillic Capital Letter Ha
\DeclareUnicodeCharacter{0445}{x} % Cyrillic Small Letter Ha
\DeclareUnicodeCharacter{0415}{E} % Cyrillic Capital Letter Ie
\DeclareUnicodeCharacter{0435}{e} % Cyrillic Small Letter Ie
\DeclareUnicodeCharacter{041E}{O} % Cyrillic Capital Letter O
\DeclareUnicodeCharacter{043E}{o} % Cyrillic Small Letter O
