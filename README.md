# Creedengo

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](https://green-code-challenge-2025.github.io/green-code-initiative-docs/creedengo-common/code-of-conduct.html)

This project contains the specifications of all Creedengo rules, for all languages.

## Structure

Rules are organized by folder based on their ID in the [root rules folder](src/main/rules).
Each of these folders contains a file with the metadata of the rule, and description by language.

The metadata file uses the format supported by
the [SonarSource Analyzers Commons](https://github.com/SonarSource/sonar-analyzer-commons/tree/master/commons) library.
To find out what values can be put there, we advise you to use the
official [SonarQube documentation](https://docs.sonarsource.com/sonarqube/latest/user-guide/rules/overview/), and to
rely on already existing files.

Here is an example:

```text
src/main/rules
├── GCI104
│   ├── java
│   │   ├── GCI104.asciidoc
│   │   ├── GCI104.json
│   ├── php
│   │   ├── GCI104.asciidoc
│   ├── python
│   │   ├── GCI104.asciidoc
│   └── GCI104.json
├── ...
```

To specify metadata for a given language (for example deprecate a rule only for a single language), it is possible to
create a json file in the language folder, and this will be merged with the common file during build. The keys in the
specific file have priority, and it is possible to add new ones but not to delete them from the global one.

## Description language

The description of the rules uses the ASCIIDOC format (with [Markdown compatibility](https://docs.asciidoctor.org/asciidoc/latest/syntax-quick-reference/#markdown-compatibility))
in order to allow the inclusion of other pages (this feature is not available with Markdown).

See:

- [AsciiDoc Syntax Quick Reference](https://docs.asciidoctor.org/asciidoc/latest/syntax-quick-reference/)
- [Compare AsciiDoc to Markdown](https://docs.asciidoctor.org/asciidoc/latest/asciidoc-vs-markdown/)

## 🚀 Getting Started

You can quickly explore Creedengo plugins using Docker. Refer to the "Getting Started" section of each plugin for
detailed instructions:

- [Java plugin](https://github.com/green-code-initiative/creedengo-java?tab=readme-ov-file#-getting-started)
- [PHP plugin](https://github.com/green-code-initiative/creedengo-php?tab=readme-ov-file#-getting-started)
- [Python plugin](https://github.com/green-code-initiative/creedengo-python?tab=readme-ov-file#-getting-started)
- [C# plugin](https://github.com/green-code-initiative/creedengo-csharp?tab=readme-ov-file#-getting-started)
- [Android Java plugin](https://github.com/green-code-initiative/ecoCode-android?tab=readme-ov-file#-quickstart)

