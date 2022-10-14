# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)





























Create a new folder on your computer with the project name 'reactproject'

Go inside that project directory and create a react app in that project directory

Open that project directory in vs code and open an interated terminal (cmd)

To create a react application type 'npx create-react-app register-app'

Type 'cd register-app' to go inside the project directory

To run the react app, type 'npm start' in cmd 

In the 'App.css' file, we can add our css 
[
        body{
    background-color: #b2aba9;
    }

    .container{
    background-color: #f2f2f2;
    justify-content: center;
    width: 50%;
    margin-left: 26%;
    margin-top: 5%;
    text-align: center;
    }

    input[type=text], select {
    width: 80%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing:border-box;
    }

    input[type=password], select {
    width: 80%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    }

    button:hover {
    background-color: #45a049;
    }

    .header{
    width: 95%;
    background-color: rgb(243, 240, 243);
    margin-left: 25%;
    width: 50%;
    padding: 20px 30px;
    margin-top: 5%;
    }


]

Let us create a new component in the 'src' folder as 'Form.js' 

In the 'Form.js' file, let us create a react functional component by typing 'rfc' 
you can see below code gets created
[
    import React from 'react'

    export default function Form() {
    return (
        <div>Form</div>
    )
    }

]

Let us remove the '<div>Form</div>' and create a form tag '<form></form>'

Let us add a classname 'container' in the opening tag of form tag

Inside the form tag let us create a 'div' tag and give a classname 'header' to it 

Inside this div, let us create a h1 header and write the content inside it as 'Registration Form'

Now let us import this 'Form' component in the 'App.js' file 

Goto 'App.js' file and remove everything inside 'return' statement and add the form component
[
     <>
      <Form></Form>
    </>
]

comment out the logo import statement in the 'App.js' file 
    '// import logo from './logo.svg';'

Now, if see the output in the browser, we can see 'Registration Form'

Let us create our input fields in the 'Form.js' file 

Goto 'Form.js' file, and below the closing div, let's create one more div

Inside that div, let us create an input field with type textt and a palceholder 

Inside the placehoder we can write "Enter Your Name"

We'll also add the name property name="name"
[
    <input type="text" placeholder='Enter Your Name' name='name'></input>
]

Duplicate this div 2 more times (for email and password) so that we have 3 input fileds 

[
      <div>
            <input type="text" placeholder='Enter Your Name' name='name'></input>
        </div>
        <div>
            <input type="text" placeholder='Enter Your Email' name='email'></input>
        </div>
        <div>
            <input type="text" placeholder='Enter Your Password' name='password'></input>
        </div>
]

Let us now create a button in the 'Form.js' file

Goto 'Form.js' file and create a div element 

Inside that div element let us create a button and give type of the button as submit
[
     <button type='submit'>Submit</button>
]

You can check the output in the browser, that a button is created 

To save the input values of form given by user, we'll create an object in the 'Form.js' file

Goto 'Form.js' file, and just above the return statement create an object data
[
    const data = {name:"", email:"", password:""};
]

To handle all these values, we'll need to call 'useState'

So, just below object, let us call useState and set initial value as 'data' as shown below
[
    const [inputData, setInputData] = useState(data)
]

Now let us add a 'value' property to input tag for name="name" as shown below
[
    value={inputData.name}
]

Let us do the same for email and password input fields
[
    value={inputData.email}
]

[
    value={inputData.password}
]



We'll also need an onChange event handler for every input tag

[
    onChange=
             {handleData} 
]

If we check the output in the browser we'll get an error
saying ''handleData' is not defined'

Let us resolve this error by declaring that event handler function at the top

[
    function handleData(e){
        
    }
]

THIS 'handleData' event handler will manage all our input data

Now , whenever any user is entering any values for the input fileds like name, email and password, we want to store that data into the 'inputData' object 

Let us code through the above steps 
[
     function handleData(e){
        setInputData({...inputData, [e.target.name]: 
            e.target.value})
    }
]

Here, '...' means previous value and next we have a key value pair wherein '[e.target.name]' is the key and ' e.target.value' is the value

To check whether our values are set or not, we can console log all the 'inputData' filed values 

So, in the 'Form.js' file, add the below print statement below 'setInput'
[
    console.log(inputData)
]

Now, if we go to browser console and input some text in input fields, you should see that data will be printed in console

Let us add the 'onSubmit' functionality to the form as shown below
[
    <form className='container' onSubmit={handleSubmit}>
]

Let us now define that 'handleSubmit' below this closing curly bracket of console log statement
[
    function handleSubmit(e){
        e.preventDefault();
    }
]

Now let us write our functionality i.e. 
    1. if input data is not present for name, email and password, then let us display an alert message notifying about the same 
[
        function handleSubmit(e){
        e.preventDefault();
         if(!inputData.name || !inputData.email || !inputData.password){
            alert("All Input Fields are Mandatory")
        }
    }
]

Now, let us check if this functionality is working or not by reloading the web page and click on the submit button without filling the input fields. You'll see an alert notifying the message

Now, let us create a functionality wherein if all the input fileds are filled by the user, we have to submit the form data. For that let us create an else condition as shown below 

[
    else{
            setFlag(true)
        }
]

Now, we'll get an error in the browser output as we did not define the 'setFlag'

So, let us define this setFlag in the declarations just above the function 
[
    const [flag, setFlag] = useState(false)
]

We are changing the flag value since we are going to utilize 'useEffect' below flad declaration 
[
     useEffect(() =>{
        console.log("Registered")
    }, [flag])
]

useEffect hook is used to re render data in jsx 
we have a dependency in useEfect 'flag' and if that value is set to a different value, the data will re render once all the input values are entered by the user  

Let us add a fragment inside the return statement of our 'Form.js' file 
[
    <>

    </>
]

Now let us add a pre tag for flag just below the fragment opening tag 
[
        <pre>{(flag)?<h2 className='ui-define'>Hello {inputData.name}, You've Registered Successfully</h2>:""}</pre>
]

Now, we can test out functionalities in our browser output 

you can enter you last name wherein you can see dynamically you name will be updated. 

















