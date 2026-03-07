# balanced-match

Match balanced string pairs, like `{` and `}` or `<b>` and `</b>`.

## Example

```javascript
const balanced = require('balanced-match');

console.log(balanced('{', '}', 'pre{in{nested}}post'));
console.log(balanced('{', '}', 'pre{first}between{second}post'));
console.log(balanced(/\s+\{\s+/, /\s+\}\s+/, 'pre  {   in{nest}   }  post'));
```

Output:

```
{ start: 3, end: 14, pre: 'pre', body: 'in{nested}', post: 'post' }
{ start: 3, end: 9, pre: 'pre', body: 'first', post: 'between{second}post' }
{ start: 3, end: 17, pre: 'pre', body: 'in{nest}', post: 'post' }
```

## Installation

```bash
npm install balanced-match
```
