# ESOLatexTemplate

Templates to write ESO documents using LaTeX.  Two templates are currently available for CUBES and ANDES.

# Workflow

- Download and unzip the [template](https://github.com/gcalderone/ESOLatexTemplate/archive/refs/heads/main.zip);
- The main files are `ANDES_template.tex` and `CUBES_template.tex`.  Rename one of these file into the final document name, e.g.: `mv CUBES_template.tex CUBES_InstrumentSoftwareRequirements.tex`.  You may delete the other template files which are not relevant for you. The main file contains:
    - A standard preamble;
    - The document properties (title, ESO number, document owner, etc.) which you should customize for your document;
    - The code to generate the title page, the running headers, the list of authors and the change record;
    - A list of `\include` statements to include the actual content of the document. It is recommended to split the document sections in separate files (see examples in `introduction.tex`, `related_documents.tex`, `section.tex`, etc.);
- Insert images into the `media` folder, and insert text in `introduction.tex`, `related_documents.tex`, `section.tex`, etc.  You may also add new files to be included with the `\include{filename.tex}` command;
- Use the provided environments and commands for specific tasks:
  - Applicable documents (`ADlist` environment and `\ARDitem` command);
  - Reference documents (`RDlist` environment and `\ARDitem` command);
  - Cite applicable or reference documents (`\citedoc` command);
  - Reference a requirement (`\citereq`) or a question (`\citequestion`);
  - Generate the table of rquirements (`\listofreq`) and questions (`\listofquestion`).
- Finally, compile into a PDF file with the command:
  ```
  pdflatex CUBES_InstrumentSoftwareRequirements.tex
  ```
  You may need to run the command multiple times to get the correct references.
