[![Build Status](https://travis-ci.org/mapbox/password-rules.png)](https://travis-ci.org/mapbox/password-rules)

# password-rules

Enforce rules on passwords.

## install

    npm install --save password-rules

## api

### `rules('pw', options)`

Options:

* `minimumLength`: default 8
* `requireCapital`: default true
* `requireLower`: default true
* `requireNumber`: default true

Returns `false` if there are no issues. Otherwise, returns an object like

```js
{ sentence: 'Password must be at least 8 letters long, contain a capital letter, and contain a number.',
  issues:
   [ { reason: 'minimumLength',
       message: 'Password must be at least 8 letters long',
       part: 'be at least 8 letters long' },
     { reason: 'requireCapital',
       message: 'Password must contain a capital letter',
       part: 'contain a capital letter' },
     { reason: 'requireNumber',
       message: 'Password must contain a number',
       part: 'contain a number' } ] }
```
