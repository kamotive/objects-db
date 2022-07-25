# API

## Constructor

Data base initialization.

```js
/**
 * @returns {ObjectsDB} Created db instance
 */

const db = new ObjectsDB();
```

## Methods

### load

This method loads data base from wof-file.

```js
/**
 * @async
 * @param {string} url
 * @returns {Promise<void>}
 */

await db.load(url);
```

### reset

Reset data base.

```js
/**
 * @returns {void}
 */

db.reset();
```

### request

This method returns array of objects from data base.

```js
/**
 * @async
 * @param {Iterable<number>|null} ids Object ids. If null, then return all objects
 * @param {Iterable<string>} [properties]
 * @returns {Promise<Array<DBObject>>}
 */

const requestResult = await db.request([0, 1, 2], ['_id', 'originalName']);
/* [{ _id: 0, originalName: 'Cube1' }, { _id: 1, originalName: 'Cube2' }, { _id: 2, originalName: 'Cube3' }] */
```
