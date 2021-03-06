# @neos21/template-html : template-html

[![NPM Version](https://img.shields.io/npm/v/@neos21/template-html.svg)](https://www.npmjs.com/package/@neos21/template-html) [![GPR Version](https://img.shields.io/github/package-json/v/neos21/template-html?label=github)](https://github.com/Neos21/template-html/packages/328041)

Generate static HTML files from templates and content files.


## Installation

```sh
$ npm install -g @neos21/template-html
```


## Help

```sh
Usage: template-html content.html -t template.html [options]

-h|--help      display this help message
-v|--version   display the version number
-o|--output    directory to output processed HTML
-t|--template  template file to use
--preserve-tree  output files will keep the same directory structure as the source files
```


## Sample usage

For the most basic use case of this plugin, create a template file with
placeholders and a file containing the content that should replace the
placeholders in the template.

`template.html`:

```html
<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="utf-8">
<title>{{ title }}</title>
</head>
<body>
  <div id="content">{{ content }}</div>
</body>
</html>
```

`content.html`:

```html
{{ title }}Lorem ipsum{{ /title }}
{{ content }}
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua.
{{ /content }}
```


## Documentation

### `Templator(options)`
Creates a new `Templator` instance.

#### Params
- **Object** `options`: An object containing the following fields:
  - `templateFile` (String): Path to template file to use.


### `processFile(contentFile)`
Run the contents of an HTML file through the `Templator`

#### Params
- **String** `contentFile`: Path to HTML file to be processed

#### Return
- **String** The processed HTML

### `processContent(content)`
Generate HTML from template file and content file

#### Params
- **String** `content`: HTML content to be used in template

#### Return
- **String** The processed HTML


## How to contribute

1. File an issue in the repository, using the bug tracker, describing the
   contribution you'd like to make. This will help us to get you started on the
   right foot.
2. Fork the project in your account and create a new branch:
   `your-great-feature`.
3. Commit your changes in that branch.
4. Open a pull request, and reference the initial issue in the pull request
   message.


## License

See the [LICENSE](./LICENSE) file.


## Links

- [Neo's World](https://neos21.net/)
- [GitHub - Neos21](https://github.com/Neos21/)
- [GitHub - template-html](https://github.com/Neos21/template-html)
- [npm - @neos21/template-html](https://www.npmjs.com/package/@neos21/template-html)
