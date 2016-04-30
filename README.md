# React Application Components for Electron (SuperAlpha)

Compose multi-window electron applications which render in electron's main context,
and eventually pass off rendering and props to `react-dom` in the browser context.



```js
import React, { Component, PropTypes as types } from 'react'
import { render, Workspace, Panel } from 'react-electron-renderer'

import NativeMenu from './native/menus'

import { app } from 'electron'

import WebApp from 'my-react-webapp'

class ElectronApplication extends Component {
  render () {
    <Workspace>
      <NativeMenu title='My Menu' />

      <Panel>
        <WebApp {...propsForWebapp } />
      </Panel>
    </Workspace>
  }
}

render(<ElectronApplication />, app)
```
