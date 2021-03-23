# react-mock-api

need to install package json-server
npm install --save-dev json-server

### then add following two command in package.json scripts section:

```

"prestart:api": "node tools/createMockDb.js",
    "start:api": "node tools/apiServer.js"

#### copy and paste tools folder and api folder to your project "/src" folder

add your own mock apis
then in the component you want to use the api:

import * as familyTreeApi from "../../../../api/familyTreeApi";

  useEffect(() => {
    // debugger;
    familyTreeApi
      .getFamilyTree("user1")
      .then((data: any) => {
        console.log("family tree info: ", data);
        setFamilyTreeInfo(data);
      })
      .catch();
  }, []);
```
