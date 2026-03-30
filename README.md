# PDF Report Template

A Quarto PDF template for academic research, publications, and reports.

This template controls the overall layout and aesthetics of the PDF report:

- a dark navy banner at the top of the first page
- a summary section, presented as bullet points 
- font, line spacing, and table/figure displays

## Main File

- `quarto/pdf/header.tex`: the styling template for generating PDF reports

## Usage

This folder should contain only the *reusable* PDF layout files.
Actual write-up of the report, raw/processed data, python/r scripts, and outputs that are *specific* to the research project should be stored in its own project directory.
