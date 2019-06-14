# API Blueprint 101 [14/06/2019]
Workshop by P'Aun @Appman

## MSON - Model script object notation (Subset of JSON)
Convert to JSON in the last

## Prerequisite
- using `npm` or `yarn`
- `yarn add aglio`
- `yarn add drakov`

## Setup package.json:
- add scripts
```
"doc": "aglio -i api.apib -s"
"mock": "drakov -f api.apib"
```

## Documentation
- run script with `yarn doc`

## Mocking
- run script with `yarn mock`
- `curl localhost:3000/path`
- show more infomation with options verbose (-v) `curl -v localhost:3000/path` 

## Structure of file (api.apib)
```
# Resouce group
## Resource
    [/path] affect only this path
### Action
+  Response status_code (content/type)
    body  // Recommended 6 tabs
```
- Response
```
+ Response 200 (text/plain)
  + Headers
    Cache-Control: max-age=86400
    ...
  + Body
    This is response!!
    ...
```
- Request with different condition
```
+ Request [Condition description] (text/plain)
    + Headers
      Cache-Control: max-age=86400
      ...
    + Body
      Hello request
      ...
``` 

## MSON - More specification
- How about response headers?
- How about request?
- How to handle multiple condition?