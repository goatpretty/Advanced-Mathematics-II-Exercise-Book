# BBox Type Changes

## Summary
- Added bbox optional parameter to tag question type: `big`, `choice`, `blank`.
- Applied extra spacing only for `blank` type in standard layout.

## Files Updated
- `ExBook.cls`
  - Added bbox type flags and parsing for `[big|choice|blank]`.
  - Standard `bbox` now applies:
    - `big`: `\vspace*{4cm}`
    - `blank`: `\vspace*{4mm}`
    - `choice`: no extra spacing
- `example_text_type.tex`
  - Replaced `\begin{bbox}` with `\begin{bbox}[type]`.
  - Removed `\bigq` in favor of `[big]`.

## Usage
```
\begin{bbox}[choice]
  \qitem ... \blankbox
  \fourchoices{...}{...}{...}{...}
\end{bbox}

\begin{bbox}[blank]
  \qitem ... \blankline
\end{bbox}

\begin{bbox}[big]
  \qitem ...
\end{bbox}
```
