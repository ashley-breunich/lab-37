![CF](http://i.imgur.com/7v5ASc8.png) LAB
=================================================

## Lab 37 - Login and Auth 

### Author: Ashley Breunich

### Links and Resources
* [repo](https://github.com/ashley-breunich/lab-37)
* [travis](https://codesandbox.io/s/3j1476xzp)

### Modules
#### `index.js`
##### Exported Values and Methods

###### `Main()`
--> Provider wrapper that creates the store 

--> App Component


#### `store/index.js`
##### Exported Values and Methods

###### `store()`
--> Creates the store with the reducers and applies middleware


#### `lib/api.js`
##### Exported Values and Methods

###### `get()`
<-- url

--> result.body OR error depending on what is returned


#### `record/actions.js`
##### Exported Values and Methods

###### `post()`
<-- payload, dispatch

--> dispatch(runPost) OR error depending on what is returned

###### `runPost()`
<-- payload

--> type: POST

--> payload

###### `get()`
<-- payload, dispatch

--> dispatch(runGet) OR error depending on what is returned

###### `runGet()`
<-- payload

--> type: GET

--> payload

###### `put()`
<-- payload, dispatch

--> dispatch(runPut) OR error depending on what is returned

###### `runPut()`
<-- payload

--> type: PUT

--> payload

###### `destroy()`
<-- payload, dispatch

--> dispatch(runDestroy) OR error depending on what is returned

###### `runDestory()`
<-- payload

--> type: DELETE

--> payload


#### Tests
* How do you run tests?
* What assertions were made?
* What assertions need to be / should be made?

#### UML
Link to an image of the UML for your application and response to events
