### Cool commands

Trims all images to its content but pads it with one pixel line on the top and bottom. The padding is needed, because sometimes the `\includegraphics` command is trimming a pixel line.

`mogrify -trim -gravity north -splice 0x1 -gravity south -splice 0x1 *.png`


Convert *.puml file (PlantUML) to a PDF file containing vectorized data.

`cat myfile.puml | plantuml -tsvg -p | inkscape --export-type="pdf" -p > myfile.pdf`


Convert *.puml file (PlantUML) to a PDF file containing vectorized data rotated by 90 degrees clockwise.

`cat overview.puml | plantuml -tsvg -p | inkscape --export-type="pdf" -p | pdfjam --angle 90 --outfile overview.pdf`

## LibreOffice slide to PDF

1. Select all objects of figure
2. Export
4. Choose PDF as file type
3. Tick 'Selection'
5. Export
6. Finally, execute this command to crop the PDF to content:
```shell
inkscape figure.pdf --export-area-drawing -o figure.pdf
```


## License

[![Creative Commons License][license-image]][license]

This template is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License][license], meaning that:

 * You can share (copy, redistribute) and adapt (remix, transform, build upon) this template for any purpose, even commercially.
 * If you share the template or a modified (derived) version of it, you must attribute the template to the original authors ([Florian Walch and contributors][template-authors]) by providing a [link to the original template][template-url] and indicate if changes were made.
 * Any derived template has to use the [same][license] or a [compatible license][license-compatible].

The license **applies only to the template**; there are no restrictions on the resulting PDF file or the contents of your thesis.

[issue]: https://github.com/TUM-Dev/tum-thesis-latex/issues
[latex-wikibook]: https://en.wikibooks.org/wiki/LaTeX
[license-compatible]: https://creativecommons.org/compatiblelicenses
[license-image]: https://i.creativecommons.org/l/by-sa/4.0/88x31.png
[license]: https://creativecommons.org/licenses/by-sa/4.0/
[overleaf]: https://www.overleaf.com/
[sample-pdf]: https://raw.github.com/TUM-Dev/tum-thesis-latex/master/build/main.pdf
[overleaf-learn]: https://www.overleaf.com/learn
[tum-sharelatex]: https://sharelatex.tum.de/ldap/login
[template-authors]: https://github.com/TUM-Dev/tum-thesis-latex/graphs/contributors
[template-download]: https://github.com/TUM-Dev/tum-thesis-latex/archive/master.zip
[template-url]: https://github.com/TUM-Dev/tum-thesis-latex
[tex-se]: https://tex.stackexchange.com/
[thesis-guidelines]: https://www.cit.tum.de/en/cit/studies/students/thesis-completing-your-studies/informatics/
[wiki]: https://github.com/TUM-Dev/tum-thesis-latex/wiki/
