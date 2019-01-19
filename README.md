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


#### `record/list.js`
##### Exported Values and Methods

###### `CLASS Records`
Sets the state: id to null

###### `deleteRecord()`
<-- id

--> this.props.handleDelete();

###### `editRecord()`
<-- id

sets the state of the id

###### `reset()`
--> this.props.handleGetAll();

###### `render()`
--> div tag with all the record components embedded

###### `mapStateToProps()`
<-- state

--> records

###### `mapDispatchToProps()`
<-- dispatch, getState

--> handleDelete

--> handleGetAll


#### `record/record.js`
##### Exported Values and Methods

###### `CLASS Record`
Sets the state: schema to an empty object {}

###### `componentDidMount()`
Set the state - schema

###### `resetPlayer()`
<-- id

sets the state of the id to null

###### `reset()`
--> this.props.handleGetAll();

###### `handleSubmit()`
<-- form

--> this.props.handlePut() OR this.props.handlePost() depending on if the event is a put or post

###### `render()`
--> h3 tag and Form component

###### `mapStateToProps()`
<-- state

--> records

###### `mapDispatchToProps()`
<-- dispatch, getState

--> handlePost

--> handlePut

--> handlePatch


#### `record/reducers.js`
##### Exported Values and Methods

###### `export default`
<-- state, action

--> type


#### `app.js`
##### Exported Values and Methods

###### `CLASS App`
--> Login Context 

--> Login Component

--> RecordList Component


#### `if/index.js`
##### Exported Values and Methods

###### `If()`
<-- props

--> props.condition OR null depending


#### `auth/auth.js`
##### Exported Values and Methods

###### `CLASS Auth`
--> LoginContext.Consumer

--> context function


#### `auth/context.js`
##### Exported Values and Methods

###### `CLASS LoginProvider`
Set the state - loggedIn, token, login(), logout()

###### `setLoginState()`
<-- loggedIn

Sets the state - loggedIn, token

###### `login()`
<-- tokin

this.setLoginState(true)

###### `logout()`
this.setLoginState(true)

###### `render()`
--> LoginContext.Provider 

--> this.props.children


#### `auth/login.js`
##### Exported Values and Methods

###### `CLASS Login`
no state

###### `handleChange()`
<-- e

Sets the state - e.target.value

###### `handleSubmit()`
<-- e, loginMethodFromContext

--> loginMethodFromContext(token) OR error depending

###### `logout()`
<-- e, loginMethodFromContext

--> logoutMethodFromProvider()

###### `render()`
--> LoginContext.Consumer

--> context function

--> The login forms

#### Tests
I am having issues testing out this program - it keeps throwing an error for the simplest of tests (like asserting that a div is present). Any suggestions? 

#### UML
Link to an image of the UML for your application and response to events
