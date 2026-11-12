# Resume

LaTeX source files for the English and Portuguese resumes, with a shared layout.

## Structure

- `resumes/english/resume_en.tex` — English resume
- `resumes/portuguese/resume_pt_br.tex` — Brazilian Portuguese resume
- `styles/` — shared layout and formatting
- LaTeX support files and PDFs are generated beside each source, keeping each resume's outputs separate

## Build

With `latexmk` installed, run each command from the repository root. Outputs stay in that resume's folder:

```powershell
Push-Location resumes/english
latexmk -pdf -interaction=nonstopmode resume_en.tex
Pop-Location

Push-Location resumes/portuguese
latexmk -pdf -interaction=nonstopmode resume_pt_br.tex
Pop-Location
```

The shared formatting lives in `styles/resume-style.sty`. Edit it to change the layout across both language versions.
