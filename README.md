# NightwatchJS-Remote-File-Upload
Custom NightwatchJS command for file upload using remote selenium grid

## Dependencies
This works only for NightwatchJS v1.4+
This project requires [adm-zip](https://www.npmjs.com/package/adm-zip)
```
npm i adm-zip
```

## Installation
1. Place the folder customCommands in the root of your project
2. Update NightwatchJ Config:
```javascript
  custom_commands_path: ["customCommands"],
```

## Sample Test
```javascript
module.exports = {
  'File Upload Test' : function (browser) {
    browser
      .url('https://the-internet.herokuapp.com/upload')
      .UploadLocalFile("/path_to_file/testfile.txt", "#file-upload")
      .click('#file-submit')
      .pause(10000)
      .end();
  }
};

```
