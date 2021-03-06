# react-only-office

> React Only Office

[![NPM](https://img.shields.io/npm/v/react-only-office.svg)](https://www.npmjs.com/package/react-only-office) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install --save react-only-office
```

```bash
yarn add react-only-office
```

## Usage

```jsx
import React from 'react'
import OnlyOffice, { useOnlyOffice, OODocument } from 'react-only-office'

// @see https://api.onlyoffice.com/editors/advanced
const config = {...}
const Example = () => {
  render () {
    return (
      <OnlyOffice {...config}>
      <span>Only Office:</span>

      <MyComponent/>
      </>
    )
  }
}

const MyComponent = () => {
  const { getDownloadUrl } = useOnlyOffice();
  return <button onClick={async ()=>{
    const url = await getDownloadUrl();
    window.open(url)
  }}>Download file!</button>
}

```

## License

MIT © [nlopezm](https://github.com/nlopezm)
