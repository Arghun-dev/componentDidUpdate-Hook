# componentDidUpdate-Hook

To make React `useEffect` to render just in `componentDidUpdate` and not `componentDidMount` Do this

in the below example I want make the `edit button` enable when user changes `customerId` not in the first render

```js
import React, { useLayoutEffect } from 'react'



const firstUpdate = useRef(true);


useLayoutEffect(() => {
        if (firstUpdate.current) {
            firstUpdate.current = false;
            return;
        }

        setBtnDisable(false)
    }, [customerId]);
    ```
