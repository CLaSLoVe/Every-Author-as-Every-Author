# Every Author as Every Author

The author block is an important component of a paper: $n$ authors are assigned to $n$ positions, and a strict ordering is made to appear as though it can summarize a collaboration that is often difficult to quantify. This practice may create conflicts among authors and, in turn, affect academic development. Conventional approaches in academia use randomization or alphabetical ordering, together with an explicit statement that the order carries no information. Yet this remains unfair: the order is still printed, and the reader's attention still falls on the first element. Prior work has addressed this issue by typesetting every author at the same position, but this introduces a serious obstacle to readability. We study the opposite, high-entropy regime. We regard the author block as a container and author names as an ideal gas diffusing within it. Each author's name appears several times per page, in the same font and at the same size, with positions drawn independently and uniformly over the page. Thus, every author has the same distribution. This makes it difficult for readers to identify a unique first author and thereby ensures fairness.

## Configuration

Set in the preamble before `\begin{document}`:

```latex
\usepackage{gasauthor}

\def\GasAuthors{Alice,Bob,Carol}   % comma-separated, no spaces after commas
\def\GasCopies{27}                  % instances per author per page
\def\GasAlpha{0.2}                  % opacity
\def\GasSeed{20260611}              % layout seed
\def\GasSat{0.60}                   % color saturation
\def\GasLuma{0.42}                  % target luminance
\def\GasHashMult{71}                % hue hash multiplier
\def\GasFont{\sffamily\bfseries\fontsize{10.5}{10.5}\selectfont}
```

Bibliography (optional):

```latex
\bibliographystyle{gasbib}
\bibliography{references}
```

Or per-entry overrides in `gasauthor.sty`: `\RefGasPerAuthor` (default `5`), `\RefGasAlpha` (default `0.2`).
