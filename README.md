# PDF Report Template

A Quarto PDF template for academic research, publications, and reports.

This template controls the overall layout and aesthetics of the PDF report:

- a dark navy banner at the top of the first page
- a summary section, presented as bullet points 
- font, line spacing, and table/figure displays

## Preview

<img src="images/template-preview.png" alt="Template preview" width="420">

## Main File

- `quarto/pdf/header.tex`: the styling template for generating PDF reports

## Usage

This folder should contain only the *reusable* PDF layout files.
Actual write-up of the report, raw/processed data, python/r scripts, and outputs that are *specific* to the research project should be stored in its own project directory.

## Applying the Template

Clone the template repository once:

```bash
git clone https://github.com/quinnei/quarto-report-template.git ~/Documents/report-template
```

Then run the following commands from the project directory:

```bash
mkdir -p 3_Output/quarto/pdf
ln -s ~/Documents/report-template/quarto/pdf/header.tex 3_Output/quarto/pdf/header.tex
```

Make sure the report YAML includes:

```yaml
format:
  pdf:
    include-in-header: quarto/pdf/header.tex
```

Render the report from `3_Output`:

```bash
cd 3_Output
quarto render "Report Name.qmd" --to pdf
```
