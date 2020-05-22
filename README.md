# group-object
Javascript helper functions for json object grouping and sorting for multiple properties

![npm](https://img.shields.io/npm/v/@jshunters/jutil?color=green&style=flat-square)   ![NPM](https://img.shields.io/npm/l/@jshunters/jutil)  ![GitHub issues](https://img.shields.io/github/issues/jshunters/jutil)  ![Snyk Vulnerabilities for npm package](https://img.shields.io/snyk/vulnerabilities/npm/@jshunters/jutil)

## Installation

Install with npm

```
npm install @jshunters/jutil
```

## Usage

Include the module

## Options available 




### for groupig 

```javascript
//we can pass either a single property
jutil.group(arrObj,'price');

//we can pass either  multiple properties as array
jutil.group(arrObj,['price','city']);
```

### for sortting

```javascript
// we can pass single property 
jutil.objSort(arrObj,'city');

// we can pass array of properties 
jutil.objSort(arrObj,['city','state','price']);

// we can pass s properties with order as object
jutil.objSort(arrObj,{'city':1,'state':1,'price':-1});
```


```javascript
var jutil = require('@hunters/group-object');
// group an object for multiple properties

let arrObj = [{
    "h_id": "3",
    "city": "Dallas",
    "state": "TX",
    "zip": "75201",
    "price": "162500"
},
{
    "h_id": "4",
    "city": "Bevery Hills",
    "state": "CA",
    "zip": "90210",
    "price": "319250"
},
{
    "h_id": "6",
    "city": "Dallas",
    "state": "TX",
    "zip": "75000",
    "price": "556699"
},
{
    "h_id": "5",
    "city": "New York",
    "state": "NY",
    "zip": "00010",
    "price": "962500"
}
];

var groupedData = jutil.group(arrObj,['price','city']);
console.log(groupedData); 

var groupedData = jutil.group(arrObj,'city');
console.log(groupedData); 

// sort a json object for multiple properties
let sortedData = jutil.objSort(arrObj,['city','state','price']);
console.log(sortedData); 

//sort for multiple keys with defined order where 1/-1 is for ascending/descending orders
let sortedData = jutil.objSort(arrObj,{'city':1,'state':1,'price':-1});
console.log(sortedData); 

//sort for single property
var sortedData = jutil.objSort(arrObj,'city');
console.log(sortedData); 
```
## Notes

Javascript helper functions for json object grouping and sorting for multiple properties

## License

**MIT**
