## Investigation on REST API documenting

### Useful links:
* Comparison:
    * https://nordicapis.com/top-specification-formats-for-rest-apis/
    * https://medium.com/@clsource/swagger-vs-raml-vs-api-blueprint-daccab31f0f2
    * https://idratherbewriting.com/learnapidoc/restapispecifications.html
* Blueprint API:
    * https://apiblueprint.org/
    * https://github.com/apiaryio/api-blueprint
    * https://apiary.io/
    * https://github.com/danielgtaylor/aglio
* Open API:
    * https://swagger.io/
    * https://github.com/Surnet/swagger-jsdoc 
* Others:
    * http://apidocjs.com/#examples

### Install aglio:
```
npm i
```
### aglio: generate html from md:
```
./node_modules/.bin/aglio -i 08.md -o 08.html
```

### Run swagger-ui
1. Download this repository(https://github.com/iurii-kyrylenko/rest-api-doc/archive/master.zip) and unzip it.
2. Open swagger-ui-dist/index.html in your browser.

### Notes on blueprint/aglio:
1. Attributes aren't supported. Schema is rendered instead. (08).
2. Data structures are rendered as schemas. Body is not rendered. (10).
3. To render data in the body, the json model should be used instead of attributes. (real-world).
4. Do not has support for JSDoc.

### Notes on blueprint/apiary
Proprietary tool.

### Notes on open-api/swagger
1. Supports structures and attributes.
2. Swagger API currently supports open-api 2.0 
3. Supports for [JSDoc](https://github.com/Surnet/swagger-jsdoc)

### Conclusion
To generate REST API use:
1. API specificification: Open API 2.0
2. Tools: swagger
3. JSDoc tool: swagger-jsdoc
