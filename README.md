# Firebase Notes
### Run scripts in emulator
Set env variable `FIRESTORE_EMULATOR_HOST=localhost:8080`  
[Docs](https://firebase.google.com/docs/emulator-suite/connect_firestore#admin_sdks)

### Delete a field in a document
```javascript
doc.ref.update(
  { someField: firebase.firestore.FieldValue.delete() }
)
```

### Action URL
Located in **Authentication > Templates**.  
Set the action url from the firebase console.  
This url is used by the `generateSignInWithEmailLink` function in the auth and client libraries.
```javascript
 auth.generateSignInWithEmailLink(email, actionCode)
 ```
### Resources region
Set region for resources.  
Client `getFunctions(app, "southamerica-east1")`  
Functions `functions.region("southamerica-east1")`  
