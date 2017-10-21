# styled-sanitize

Single file with sanitize.css for your [styled-components](https://styled-components.com/)

Original sanitize.css copied from [jonathantneal/sanitize.css](https://github.com/jonathantneal/sanitize.css)


## Usage

```bash
npm install --save styled-sanitize styled-components
```

### JavaScript

```javascript
// ----- styles/index.js
import styledSanitize from 'styled-sanitize'
import { injectGlobal } from 'styled-components'

export default () => injectGlobal`
  ${styledSanitize}

  body {
    padding: 0;
    background-color: black;
  }
`

// ----- client.js
// ... imports
import baseStyles from './styles/index'

const render = () => {
  baseStyles()

  ReactDOM.render(<AppContainer />, document.getElementById('app-root'))
}

render()
```

## ServerSide Rendering

Styled-components supports SSR, you can [read discussion](https://github.com/styled-components/styled-components/issues/386) or [open RURARAR](https://github.com/lestad/rurarar/)
