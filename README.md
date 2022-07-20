# be-bucket-listed

Extract / collate data from lists of elements based on DOM Queries

```html
<details be-bucket-listed='{
    "selector": "label>span",
    "value": "textContent",
    "reduceTo": "uniqueList"
}'>
    <summary>...</summary>
    <template be-repeated be-bucket-listed='{
        "from": "details",
        "selector": "label>span",
        "value": "textContent",
        "reduceTo": "uniqueList",
        "passTo":{
            "proxy": "repeated",
            "prop": "listVal"
        }
    }'>
    <div aria-columnheader></div>
    </template>
    <details>
        <summary>...
        <label>
            <span>Input 1</span>
            <input>
        </label>
        <label>
            <span>Input 2</span>
            <input>
        </label>
    </details>
    <details>
        <summary>...
        <label>
            <span>Input 1</span>
            <input>
        </label>
        <label>
            <span>Input 2</span>
            <input>
        </label>
    </details>
</details>
```
