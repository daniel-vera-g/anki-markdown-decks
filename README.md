# Template to write Anki markdown decks

[![Check code quality](https://github.com/daniel-vera-g/anki-markdown-decks/actions/workflows/code-quality.yml/badge.svg)](https://github.com/daniel-vera-g/anki-markdown-decks/actions/workflows/code-quality.yml)
[![Generate Anki decks](https://github.com/daniel-vera-g/anki-markdown-decks/actions/workflows/gen-decks.yml/badge.svg)](https://github.com/daniel-vera-g/anki-markdown-decks/actions/workflows/gen-decks.yml)

> Template to use markdown as markup language for Anki decks

- Uses: [md2apkg](https://github.com/Steve2955/md2apkg)

## Usage

1. Choose: _Use this template_
2. Run `npm i`

### Generate decks

#### Example

- This template has 2 examples to generate decks for learning the capitals of europe and south america. You can take
  this as examples.

Run `npm run gen-europe` and `npm run gen-south-america` to generate each deck.

#### Add your own decks

1. Add your own decks in the `./decks/` folder.
2. Customize the `npm` commands in the `package.json`
3. This template comes with a CI/CD pipeline to automatically generate the decks. Change the values there. Otherwise,
   they will just fail.

## CI/CD

This template comes with 2 Pipelines:

1. A code quality pipeline which check the code for format and linting compliance. You can run the check locally with:
   `npm run prettier` to check for formatting or `npm run lint` to check your linting with `markdownlint`
2. A deck generation pipeline which automatically generates the Anki `.apkg` file. With this in place, you can directly
   download the deck and import it to Anki.

**NOTE:** You will need to customize the `.github/workflows/gen-decks.yml` pipeline when you add your custom decks,
remove the current, or want to have your decks generated.
