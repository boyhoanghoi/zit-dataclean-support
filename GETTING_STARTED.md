# Getting started with Zit DataClean

Zit DataClean processes CSV and Excel tables on your computer. No account,
internet connection or Python installation is needed for the portable build.

## Your first cleanup

1. Open ZitDataClean.exe. Keep its entire folder, including _internal, together.
2. Click **Try sample data**, or drag CSV/XLSX files into the window.
3. Check the files and worksheets you want to combine in the left panel.
4. Choose your rules on the right. **Duplicate keys** lets you match by order ID,
   email or other columns instead of comparing the whole row.
5. Click **Apply rules**. Compare **Original** with **Preview** and review the counts.
6. Click **Export clean file** and choose a new .xlsx or .csv destination.
7. Use **Save recipe** to reuse the same rules for your next report. **Load recipe**
   restores these settings; it does not load or store your original data.

The interface starts in English. An optional Vietnamese interface is available
in the top-right language selector. An explicitly selected language is remembered.
The sample records are fictional and are not customer data.

## CSV import

Automatic detection supports UTF-8 and BOM-marked UTF-16. For Windows-1252,
Windows-1258 or an ambiguous delimiter, select the correct import settings before
adding files. Settings apply to new imports; clear the list to reimport a file.

## Data preservation and export

Source files cannot be overwritten. Export creates a new file, or replaces an
existing output file only after confirmation. Check the preview before using
cleaned data for important work. Use small, redacted files when requesting support.

This is a table-value utility, not a workbook-formatting editor. It does not
preserve Excel formatting, charts, macros, numeric display formats or formula
calculation. Formulas are imported as literal strings, never executed. XLSX output
uses text cells to preserve identifiers with leading zeroes. Convert appropriate
columns to numbers in Excel if you need calculations.

Safe CSV export prefixes formula-like cells with an apostrophe, including strings
that start with a minus sign. You can explicitly disable this protection for
trusted machine-to-machine workflows. Exported CSV text can still be interpreted
by another program according to that program's import rules; use text-typed XLSX
when preserving identifiers in Excel is important.

## Limits

Windows x64, Windows 10 build 19041+ or Windows 11. Up to 30 files, 50 MB each,
250,000 combined rows, 3 million combined cells and 1,000 columns, subject to
available memory. XLSX workbooks support up to 100 worksheets and 200 MB expanded
ZIP content. Legacy XLS/XLSM files are not supported.

Preview and search cover the first 5,000 rows. Export includes all processed rows.

The application does not upload tables or retain them between sessions. Recipes
contain rules and column names, not row contents. Processing reports include
counts and warnings, which can include file/worksheet names. See PRIVACY.txt.

The unsigned MSIX is intended for Partner Center upload. Microsoft signs the
Store-distributed package after certification. The owner/tester portable build
is unsigned; this is separate from Microsoft Store certification.
