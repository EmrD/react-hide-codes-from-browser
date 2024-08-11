****Hide React Codes From Browser****

If you want to hide your codes in production deployment; you can do this with React.

You can test my project: https://react-bu-a6073.web.app/

**To hide codes, follow these steps**
1. Add this code to your build script in ```package.json```:

   ```
   GENERATE_SOURCEMAP=false
   ```
   
3. Run your build script, for example

   ```
   npm run build
   ```
   
4. Just add your ```dist``` folder to production server.
5. Test your app.

***Example Usage:***

This code was my React code:
```
import { useState } from 'react'
import reactLogo from './assets/react.svg'
import viteLogo from '/vite.svg'
import './App.css'

function App() {
  const [count, setCount] = useState(0)

  return (
    <>
      <div>
        <a href="https://vitejs.dev" target="_blank">
          <img src={viteLogo} className="logo" alt="Vite logo" />
        </a>
        <a href="https://react.dev" target="_blank">
          <img src={reactLogo} className="logo react" alt="React logo" />
        </a>
      </div>
      <h1>Vite + React</h1>
      <div className="card">
        <button onClick={() => setCount((count) => count + 1)}>
          count is {count}
        </button>
        <p>
          Edit <code>src/App.jsx</code> and save to test HMR
        </p>
      </div>
      <p className="read-the-docs">
        Click on the Vite and React logos to learn more
      </p>
    </>
  )
}

export default App
```

***In production deployment:***

```
(function() {
    const n = document.createElement("link").relList;
    if (n && n.supports && n.supports("modulepreload"))
        return;
    for (const l of document.querySelectorAll('link[rel="modulepreload"]'))
        r(l);
    new MutationObserver(l=>{
        for (const o of l)
            if (o.type === "childList")
                for (const u of o.addedNodes)
                    u.tagName === "LINK" && u.rel === "modulepreload" && r(u)
    }
    ).observe(document, {
        childList: !0,
        subtree: !0
    });
    function t(l) {
        const o = {};
        return l.integrity && (o.integrity = l.integrity),
        l.referrerPolicy && (o.referrerPolicy = l.referrerPolicy),
        l.crossOrigin === "use-credentials" ? o.credentials = "include" : l.crossOrigin === "anonymous" ? o.credentials = "omit" : o.credentials = "same-origin",
        o
    }
    function r(l) {
        if (l.ep)
            return;
        l.ep = !0;
        const o = t(l);
        fetch(l.href, o)
    }
}
)();
var Bi = {
    exports: {}
}
  , br = {}
  , Hi = {
    exports: {}
}
  , L = {};
/**
 * @license React
 * react.production.min.js
 *
 * Copyright (c) Facebook, Inc. and its affiliates.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
 */
var Yt = Symbol.for("react.element")
  , tc = Symbol.for("react.portal")
  , rc = Symbol.for("react.fragment")
  , lc = Symbol.for("react.strict_mode")
  , oc = Symbol.for("react.profiler")
  , uc = Symbol.for("react.provider")
  , ic = Symbol.for("react.context")
  , sc = Symbol.for("react.forward_ref")
  , ac = Symbol.for("react.suspense")
  , cc = Symbol.for("react.memo")
  , fc = Symbol.for("react.lazy")
  , Mu = Symbol.iterator;

and more...
```
