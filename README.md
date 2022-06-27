# CSV_TO_JSON

CMDS:- 

yarn install
yarn add csvtojson



CODE:- 

const csvtojson = require("csvtojson");
const fs = require("fs");

const csvfilepath = "sample.csv";

csvtojson()
    .fromFile(csvfilepath)
    .then((json) => {
        console.log("\n\ncsvtojson JSON ::::: ", json);

        fs.writeFileSync("output.json", JSON.stringify(json), "utf-8", (err) => {
            if (err) {
                console.log("error ::::: ", err);
            }
        })
    });
