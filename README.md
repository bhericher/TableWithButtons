# TableWithButtons
A table component for Pentaho Ctools with buttons for Copy, Print, CSV, Excel, PDF and ColVis
# WARNING
** This component comes we no warranty. I won't assume any damage caused by its use! **

# Description
This is a rework of https://github.com/fernandommota/table-bootstrap-component (Many thanks to Fernando Maia da Mota) based on the Buttons extension of dataTables (http://datatables.net/extensions/buttons/)
I have tested it with Pentaho BA CE 5.4
## Caveat
*The Buttons extension needs a more recent version of DataTables that the one used by Pentaho CDE : The component includes DataTables 1.10.10 ; as far as I know, there is no conflict, but I didn't make comprehensive tests
*In order to have nice pdf, Buttons uses pdfmake.js (http://pdfmake.org/#/), but the current version (0.1.20) is conflicting with CDE (see : https://github.com/bpampuch/pdfmake/pull/443), so I have used the version of this pullrequest although it is not commited.
Here again, I didn't make comprehensive tests
## Usage
### Installation
*Download and extract the zip file on this path:

biserver-ce/pentaho-solutions/system/pentaho-cdf-dd/resources/custom/components/

*Restart your server

### Properties

* oLanguage : enter here your language (e.g. French) : if there is a French.json file in the subdirectory i18n, it will be used : The file commes from dataTables with addition of keys for the Buttons

* Buttons definition : define the buttons. This is an array. The first column is the name of the button (pdf, colvis,...). The second one is a comma-separated list of properties of the button. For example for a pdf :
       title: My report,
       orientation: landscape,
       pageSize : A5

* sDom : by default,'Bfrtip' (see Datatables for the syntax)

* pdf Customize : You can enter here a function to customize the pdf (see pdfmake documentation)

See the sample dashboard in the sample directory

The remaining is like Table Component

# TODO

* Hide oLanguage and add a property Language and, if empty, infer the language from the 'locale' (e.g : fr_FR, fr_CA,...)
* Add a customize function for other buttons
* Add exportoptions
* Allow custom buttons
