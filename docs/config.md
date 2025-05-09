# Configuration

HonKit allows you to customize your book using a flexible configuration. These options are specified in a `book.json` file. For authors unfamiliar with the JSON syntax, you can validate the syntax using tools such as [JSONlint](http://jsonlint.com).

### General Settings

| Variable | Description |
| -------- | ----------- |
| `root` | Path to the root folder containing all the book's files, except `book.json` |
| `structure` | To specify paths for Readme, Summary, Glossary etc. See [Structure paragraph](#structure). |
| `title` | Title of your book, default value is `HonKit`. |
| `description` | Description of your book, default value is extracted from the README. |
| `author` | Name of the author(s), multiple authors should be separated by ampersands. |
| `authorSort` | String to be used when sorting by author. |
| `producer` | Name of the producer. |
| `publisher` | Name of the publisher. |
| `series` | The series this book belongs to. |
| `seriesIndex` | Index of the book in this series. |
| `pubdate` | Publication date of the book, formatted as YYYY-MM-DDTHH:MM:SS. |
| `isbn` | ISBN of the book |
| `language` | [ISO code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) of the book's language, default value is `en` |
| `direction` | Text's direction. Can be `rtl` or `ltr`, the default value depends on the value of `language` |
| `gitbook` | Version of HonKit that should be used. Uses the [SemVer](http://semver.org) specification and accepts conditions like `">= 3.0.0"` |
| `honkit` | Version of HonKit that should be used. Uses the [SemVer](http://semver.org) specification and accepts conditions like `">= 3.0.0"` |

### Plugins

Plugins and their configurations are specified in the `book.json`. See [the plugins section](plugins/README.md) for more details.

Since version 3.0.0, HonKit can use themes. See [the theming section](themes/README.md) for more details.

| Variable | Description |
| -------- | ----------- |
| `plugins` | List of plugins to load |
| `pluginsConfig` |Configuration for plugins |

### Structure

In addition to the `root` variable, you can tell HonKit the name of the files for Readme, Summary, Glossary, Languages (instead of using the default names such as `README.md`).
These files must be at the root of your book (or the root of every language book). Paths such as `dir/MY_README.md` are not accepted.

| Variable | Description |
| -------- | ----------- |
| `structure.readme` | Readme file name (defaults to `README.md`) |
| `structure.summary` | Summary file name (defaults to `SUMMARY.md`) |
| `structure.glossary` | Glossary file name (defaults to `GLOSSARY.md`) |
| `structure.languages` | Languages file name (defaults to `LANGS.md`) |

### PDF Options

PDF Output can be customized using a set of options in the `book.json`:

| Variable | Description |
| -------- | ----------- |
| `pdf.pageNumbers` | Add page numbers to the bottom of every page (default is `true`) |
| `pdf.fontSize` | Base font size (default is `12`) |
| `pdf.fontFamily` | Base font family (default is `Arial`) |
| `pdf.paperSize` | Paper size, options are `'a0', 'a1', 'a2', 'a3', 'a4', 'a5', 'a6', 'b0', 'b1', 'b2', 'b3', 'b4', 'b5', 'b6', 'legal', 'letter'` (default is `a4`) |
| `pdf.margin.top` | Top margin (default is `56`) |
| `pdf.margin.bottom` | Bottom margin (default is `56`) |
| `pdf.margin.right` | Right margin (default is `62`) |
| `pdf.margin.left` | Left margin (default is `62`) |
| `pdf.embedFonts` | Embed all fonts into the PDF (default is `false`) |

### Styles

The default theme allows additional stylesheets to be specified in the `book.json`. The file paths should be specified relative to the `root` path if provided. When provided, `ebook` applies to `epub`, `mobi`, and `pdf` output unless those are provided individually as well.

| Variable | Description |
| -------- | ----------- |
| `styles.ebook` | Location of stylesheet specific to ebook output |
| `styles.epub` | Location of stylesheet specific to epub output |
| `styles.mobi` | Location of stylesheet specific to mobi output |
| `styles.pdf` | Location of stylesheet specific to PDF output |
| `styles.print` | Location of stylesheet specific to print formatting |
| `styles.website` | Location of stylesheet specific to the website output |
