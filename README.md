## Blueprint API investigation

### Useful links:
* https://apiblueprint.org/
* https://apiary.io/
* https://github.com/apiaryio/api-blueprint
* https://github.com/danielgtaylor/aglio

### Install:
```
npm i
```

### Generate html from md:
```
./node_modules/.bin/aglio -i 08.md -o 08.html
```

### Notes on aglio:
1. Attributes aren't supported. Schema is rendered instead. (08)
2. Data structures are rendered as schemas. Body is not rendered. (10)
3. To render data in the body, the json model should be used instead of attributes. (real-world)
