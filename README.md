# blackDile
blackDile is drop files to gist. single motion and simple drop the box, for gist, for image, for files.

### promise
status word strong ___=>fix___ ___=>rot___    
if draft fix, write the "=>fix"   
if source wrote, write the "=>rot"
```
- one box ___=>fix___ ___=>rot___ 
- usage inner blackDile ___=>fix___

```
### spec and status
 - one box ___=>fix___
 - usage inner blackDile, so include the markdown parser
  1. choice is one. showdown.js or markdown-js.js or marked.js 
  [ref](http://kannokanno.hatenablog.com/entry/2013/06/19/132042)
  [testdata](https://gist.github.com/kannokanno/ce495a4708cee4a7fca4) 
 - gist auth
   1. package name gistCtrl.js
   1. gistCtrl.auth(name,password)
   1. gistCtrl.seek(url)
   1. gistCtrl.uploads({ \[ filename,blob,comment ],\[..array..]}) 
   ```
    uploads is POST
    image mime type is gif,jpeg,jpg,png,svg
    other is text.
    comment default '20180112z1920. use blackDile.'
   ```
   1. gistCtrl.updates(...same uploads..) ```updates is PATCH```
   1. gistCtrl.deletes(...same uploads..) ```deletes is DELETE```
 - show the blackDile list
    1. list column.
    ```
    use icon for minimum and need tooltip for icon. 
    |filename|date|star signal| <=leftWay |copy|embed| rightWay=> |download|update|delete|
    |gist id|page number|
    hide column. for api.
    ```
 - description is storage name. #gistStorage #blackDile #page001
   1. auto rotation the pagination #page001 #page002 ... #pageXXX
