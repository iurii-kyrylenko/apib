## Blueprint API investigation

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

### Install:
```
npm i
```

### aglio: generate html from md:
```
./node_modules/.bin/aglio -i 08.md -o 08.html
```

### Notes on blueprint/aglio:
1. Attributes aren't supported. Schema is rendered instead. (08).
2. Data structures are rendered as schemas. Body is not rendered. (10).
3. To render data in the body, the json model should be used instead of attributes. (real-world).
4. Do not has support for JSDoc.

### Notes on apiary
Proprietary tool.

### Notes on swagger
1. Supports structures and attributes.
2. Supports for [JSDoc](https://github.com/Surnet/swagger-jsdoc)
