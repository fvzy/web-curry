[![Npm Downloades](https://img.shields.io/npm/dm/web-curry?label=npm%20downloads)](https://www.npmjs.com/package/web-curry    )

## NodeJS based website downloader

Download a website locally without any configuration right from you terminal

__Note:__ The script is based entirely on [node-webiste-scraper](https://github.com/website-scraper/node-website-scraper), an awesome website scraper library :)

## Requirments

* Nodejs version >= 14

## Installation

```bash
npm install -g web-curry
```

## Usage

### Bash
```bash
web-curry download DOMAIN START_POINT OUTPUT_FOLDER [VERBOSE] [OUTPUT_FOLDER_SUFFIX] [INCLUDE_IMAGES]
```

### JavaScript 
```javascript
exec(`web-curry download -s START_POINT -d DOMAIN -o OUTPUT_FOLDER -v --include-images`, async (error, stdout, stderr) => {
if (error) {
        console.log(`error: ${error.message}`);
        return;
    }
    if (stderr) {
        console.log(`stderr: ${stderr}`);
        return;
    }
    console.log(`stdout: ${stdout}`);
})

```


## Example

### Bash
```bash
# Download all of the english jest documentation
web-curry download -s https://jestjs.io/docs/en/getting-started -d https://jestjs.io/docs/en/ -o jest-docs -v --include-images
```

### JavaScript 
```javascript
exec(`web-curry download -s https://jestjs.io/docs/en/getting-started -d https://jestjs.io/docs/en/ -o jest-docs -v --include-images`, async (error, stdout, stderr) => {
if (error) {
        console.log(`error: ${error.message}`);
        return;
    }
    if (stderr) {
        console.log(`stderr: ${stderr}`);
        return;
    }
    console.log(`stdout: ${stdout}`);
})

```


__For more information please run__
```bash
web-curry --help
web-curry download --help
```
## Options

* domain (-d) - The script will download all of the urls under the specified url.
* start point (-s) - The page from which the script should start scraping
* include-images (--include-images) - Should the script download relevant images as well?
* output folder (--output-folder) - The folder in which the script should save the downloaded assets,
  __Note:__ The folder should not exist!
* verbose (-v) - If flag is present the script will print every url that was downloaded.
* output folder suffix (--output-folder-suffix) - The suffix that will be added to `OUTPUT_FOLDER`, defaults to: `.zyy.sh`

