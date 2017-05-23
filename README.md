# Express Practice
# Part 1

### src/index.js
* This is the starting point of the server, put all code here

### Body
* Add body parser middleware to express

### Create express routes to get all things
* Add a .get() route for /contact, /vehicles, /comments, /products
* response.json() the appropriate array

### Create express routes to get one thing
* Add a .get() route for /contact, /vehicles, /comments, /products
* add a path variable for id
* use the id to .find() the item from the appropriate array
* response.json() the item found

### Create express routes to create one thing
* Add a .post() route for /contact, /vehicles, /comments, /products
* Add the information from the body to the appropriate array

At this point, the web page should operate in the same manner as the redux fetch practice

## Part 2

## Redux

### Reducers
* create 4 more reducers for the state: vehicle, product, comment, contact
* vehicle
    * look for “GET_VEHICLE_DONE”
* product
    * look for “GET_PRODUCT_DONE”
* comment
    * look for “GET_COMMENT_DONE”
* contact
    * look for “GET_CONTACT_DONE”
* 

### Actions
* Create actions in actions/index.js
* Create actions to do to a fetch call to one item. When complete, dispatch to the done action.
    * getProduct(id)
        * fetch(“/products/“ + id)
    * getVehicle(id)
        * fetch(“/vehicles/“ + id)
    * getComment(id)
        * fetch(“/comments/“ + id)
    * getContact(id)
        * fetch(“/contacts/“ + id)
* Create actions to handle the data 
    * getProductDone(product)
        * GET_PRODUCT_DONE
    * getVehicleDone(product)
        * GET_VEHICLE_DONE
    * getComment(comment)
        * GET_COMMENT_DONE
    * getContact(contact)
        * GET_CONTACT_DONE


### Components
* Create class components to show the details of each Type in our system
* Vehicle.js, Product.js, Contact.js, Comment.js
* Use the instructions from Containers to decide what props to use
* You decide what to show in the detail
* In componentDidMount
    * Extract the path parameter id
    * call the appropriate get action to get one thing
    * for Vehicle.js you would call getVehicle(id)

### Containers
* Create containers for Vehicle, Product, Contact, Comment
* Implement mapStateToProps
    * For Vehicle.js, map a prop called vehicle to the state.vehicle
    * What should the state be for Product.js, Contact.js and Comment.js
* Implement mapDispatchToProps
    * For Vehicle.js map a prop called getVehicle to the action getVehicle
    * What should you do for Product.js, Contact.js and Comment.js

### Router
* Use react-router-dom 
* Import BrowserRouter, Switch and Route into App.js
* Create routes for each detail component
    * /vehicle/:id -> Vehicle
    * …etc
    * / -> show the Main component

#### Link
* Look at CollapsableMapper.js
* Change the <a> tag to <Link>


### Points
* Base - 10pts
* Data shows in the page for the Lists - 5pts each (20pts)
* Creating data works - 10pts each (40pts)
* Can view one item at a time by id - 30pts