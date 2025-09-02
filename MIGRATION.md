# Migration Guide: Vue Peer Dependency Change

## What Changed

Vue has been moved from `dependencies` to `peerDependencies` to allow library users to control their Vue version.

## Before (v0.1.10 and earlier)

```json
{
  "dependencies": {
    "oc-mina-ui": "^0.1.10"
  }
}
```

Vue was automatically installed with the library.

## After (v0.1.11+)

```json
{
  "dependencies": {
    "oc-mina-ui": "^0.1.11",
    "vue": "^2.6.0"
  }
}
```

You must explicitly install Vue alongside the library.

## Supported Vue Versions

This library supports:
- Vue 2.6.x
- Vue 2.7.x

## Installation Instructions

### For Vue 2.6.x projects:
```bash
npm install oc-mina-ui vue@^2.6.0
# or
yarn add oc-mina-ui vue@^2.6.0
```

### For Vue 2.7.x projects:
```bash
npm install oc-mina-ui vue@^2.7.0
# or
yarn add oc-mina-ui vue@^2.7.0
```

## Benefits

- **Smaller bundle size**: Vue is no longer included in the library bundle
- **Version control**: You can choose your preferred Vue version
- **No conflicts**: Prevents Vue version conflicts in your application
- **Better compatibility**: Works with both Vue 2.6.x and 2.7.x

## Usage

Library usage remains unchanged:

```javascript
import Vue from 'vue';
import MinaUI from 'oc-mina-ui';
import 'oc-mina-ui/dist/mina-ui.css';

Vue.use(MinaUI);
```