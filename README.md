#MYOB 

MYOB Library 

## Why use MYOB Library?


## Installation
```javascript
$npm install --save myob-exo-api
```
 
## Usage

**Initiation**

```javascript
// ES5 
const MYOB = require('myob-exo-api').default;
// ES6
import MYOB from 'myob-exo-api';
const myob = new MYOB({
        url: EXO_WIN_API_URL,
        username: EXO_WIN_API_USERNAME,
        password: EXO_WIN_API_PASSWORD,
        token: EXO_WIN_API_TOKEN
})
```

**Debtor**

```javascript
// Get debtors
(async() => {
    const items = await myob.Debtor.find({
        // where : {
        //      Active : true
        // },
        // order : ['id', 'desc'],
        // limit : 10,
    });
    console.log(items);
})();

// Get the specific debtor and edit it
(async() => {
    const item = await myob.Debtor.find(1);
    item.website = "http://www.bizex.co.nz";
    await item.save();
    console.log(item);
    
})();

```


**Stock Item**

```javascript
// Get stock items
(async() => {
    const items = await myob.StockItem.find({
        // where : {
        //      Active : true
        // },
        // order : ['id', 'desc'],
        // limit : 10,
    });
    console.log(items);
})();

// Get the specific stock item
(async() => {
    const item = await myob.StockItem.find(1);
    item.website = "http://www.bizex.co.nz";
    await item.save();
    console.log(item);
    
})();

```


**Sales Order**

```javascript
// Get sales orders
(async() => {
    const items = await myob.SalesOrder.find({
        // where : {
        //      Active : true
        // },
        // order : ['id', 'desc'],
        // limit : 10,
    });
    console.log(items);
})();

// Get the specific sales order and edit it
(async() => {
    const item = await myob.SalesOrder.find(1);
    item.website = "http://www.bizex.co.nz";
    await item.save();
    console.log(item);
    
})();

```
