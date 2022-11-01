
# Tasks
## Initialize
./dtcw tasks --group=doctoolchain
./dtcw downloadTemplate
## Build
./dtcw generateHTML
./dtcw generatePDF
./dtcw generateSite
./dtcw generateExcel //looking for excel sheets to transform them to asciidoc.


## local to avoid Docker.
./dtcw local getJava

## OpenAPI
Beside being able to publish it to confluence, you could generate HTML or PDF files. For this to work it is necessary to configure it properly and to execute command for generating respective output format (generateHTML|generatePDF).

Regarding configuration, you would need to declare location of OpenAPI spec as json file in config.groovy, like:

openApi.with {
    specFile = 'src/docs/petstore-v2.0.yaml'
    infoUrl = 'https://my-api.company.com'
    infoEmail = 'info@company.com'
}

InfoUrl and InfoEmail are just meta parameters which will be used for the HTML/PDF header.




