# PFU Localizer

## Introduction

The purpose of this application is to automate the process of converting CSV files exported from the official ProjectFU localization Google Sheet into formatted JSON files for each language, to be used with ProjectFU system for FoundryVTT. This application utilizes PapaParse for parsing.

### Prerequisite Software

- [Git](https://git-scm.com/)
- [Node v16.16.0 (LTS) or higher](https://nodejs.org/en/blog/release/v16.16.0)
- Code editor (recommended: [Visual Studio Code](https://code.visualstudio.com/))

## Setup

Clone the repository using the following command in your terminal:

```bash
git clone https://github.com/League-of-Fabulous-Developers/pfu-localizer.git
```

Navigate to the project folder and use npm to install the dependencies specified in `package-lock.json`:

```bash
npm ci
```

### Convert from CSV to JSON

Ensure you have all the necessary CSV files and move them into the `csvtojson/import` folder:

```text
Project FU Localization - ACTOR.csv
Project FU Localization - ITEM.csv
Project FU Localization - FU.csv
Project FU Localization - TYPES.csv
```

Run the following command to convert the CSV files to JSON:

```bash
npm run c2j
```

After conversion, import all the files from `csvtojson/export` into the system's language path: `systems/projectfu/lang`.

### Convert from JSON to CSV

Copy all the necessary JSON files into the `jsontocsv/import` folder. Then, run the following command to convert the JSON files back to CSV:

```bash
npm run j2c
```

Import the generated CSV files into any spreadsheets as needed.