# `uuid`

[npmjs](https://www.npmjs.com/package/uuid)

To create RFC4122 UUID.

## Install

```zsh
npm i uuid
```

## Usage

```javascript
// random UUID
import { v4 as uuidv4 } from 'uuid';
uuidv4(); // ⇨ '9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d'
```

`v4` is specifically for random UUID. See [docs](https://github.com/uuidjs/uuid#api-summary) for other versions.
