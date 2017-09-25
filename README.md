# apidoc-contentType-plugin
Add different content types support to apidoc

## Usage:
First, clone and issue `npm install` in the plugin directory.
You have to use the template provided and the custome parser, add `-t apidoc-contentType-plugin/template/ --parse-parsers apicontenttype=apidoc-contentType-plugin/api_content_type.js`
to your command line.

By instance, if you fork the plugin in the same directory as your project. Run this command from the directory of your project.
```
apidoc -i lib/ -o doc -t ../apidoc-contentType-plugin/template/ --parse-parsers apicontenttype=../apidoc-contentType-plugin/api_content_type.js
```
Then, you can use the `@apiContentType` tag in your doc.
```
/**
 * @apiParam {String} [id] Beer ID.
 * @apiParam {String} [name] Beer name.
 * @apiGroup Beer
 * @apiVersion 0.1.0
 * @api {post} /beerJSON Get a list of beers
 * @apiContentType application/json
 */
```
