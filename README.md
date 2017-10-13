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
    * https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.0.md
    * https://swagger.io/docs/specification/about/
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
1. Download [this repository](https://github.com/iurii-kyrylenko/rest-api-doc/archive/master.zip) and unzip it.
2. Open `swagger-ui-dist/index.html` in your browser.

### Run swagger-ui hosted on local server
1. Install http-server globally: `npm i -g http-server`.
2. Launch server: `cd swagger-ui-dist && http-server --cors -c-1`
3. Navigate to `http://localhost:8080`.

### Notes on blueprint/aglio:
1. Attributes aren't supported. Schema is rendered instead. (08).
2. Data structures are rendered as schemas. Body is not rendered. (10).
3. To render data in the body, the json model should be used instead of attributes. (real-world).
4. Do not has support for JSDoc.

### Notes on blueprint/apiary
Proprietary tool.

### Notes on open-api/swagger
1. Supports structures and attributes.
2. Swagger API currently supports Open API specification v2 and v3.
3. Supports for [JSDoc](https://github.com/Surnet/swagger-jsdoc): API descriptions are embedded in source code as comments with special formatting. swagger-jsdoc currently supports Open API v2.

### SUMMARY
1. Use API specificification `Open API`
2. Use tool Swagger UI to render Open API document.
3. The Swagger UI can be customized to change rendering.
4. Host Swagger UI as a static resourse on the http server.
5. Feed Swagger UI with Open API document in yaml or json format.
6. The source of Open API document can be:
    * a separate .yaml document;
    * an output of swagger-jsdoc API (in case when .yaml fragments embedded into source code)
7. Use Open API v3 in case of separate document.
8. Use Open API v2 in case of JSDoc fragments.
