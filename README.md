# TableWithButtons
A table component for Pentaho Ctools with buttons for copy, Print, CSV, Excel, PDF and ColVis
# WARNING
** This component comes we no warranty. I won't assume any damage caused by its use! **

# Description
This is a rework of https://github.com/fernandommota/table-bootstrap-component (Many thanks to Fernando Maia da Mota) based on the Buttons extension of dataTables (http://datatables.net/extensions/buttons/)
I have tested it with Pentaho BA CE 5.4
## Caveat
*The Buttons extension needs a more recent version of DataTables that the one used by Pentaho CDE : The component includes DataTables 1.10.10 ; as far as I know, there is no conflict, but I didn't make exhaustiv tests
*In order to have nice pdf, Buttons uses pdfmake.js (http://pdfmake.org/#/), but the current version (0.1.20) is conflicting with CDE (see : https://github.com/bpampuch/pdfmake/pull/443), so I have used the version of this pullrequest although it is not commited.
Here again, I didn't make exhaustiv tests
## Usage
### Installation
*Download and extract the zip file on this path:

biserver-ce/pentaho-solutions/system/pentaho-cdf-dd/resources/custom/components/

*Restart your server

### Properties

* oLanguage : enter here your language (e.g. French) : if there is a French.json file in the subdirectory i18n, it will be used : The file commes from dataTables with addition of keys for the Buttons

* Orientation : landscape or portrait (for pdf)

* sDom : by default,'Bfrtip' (see Datatables for the syntax)

The remaining is like Table Component

# TODO

1. Hide oLanguage and add a property Language and, if empty, infer the language from the 'locale' (e.g : fr_FR, fr_CA,...)
2. Currently, all buttons are visible. Introduce a property 'buttons' as a 2 dimensional array, example :
(see the syntax on Datatables)

Button   |   Options
---------|----------
pdf      |   orientation : 'landscape', papersize : '...'
csv      |  fieldSeparator: '\t'

etc...
3. Add property filename, title,...
4. Use version 1.1.1 of buttons instead of 1.1.0 (some imprvoments)
