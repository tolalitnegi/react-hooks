# react hooks 

## firebase config 
- update the below config ins firebase.util.js 

```
const config = {
  apiKey: "AIzaSyDouYv9znYuedlBDK8CrfiGnRM9HVOBse0",
    authDomain: "app-grpql.firebaseapp.com",
    projectId: "app-grpql",
    storageBucket: "app-grpql.appspot.com",
    messagingSenderId: "448271751409",
    appId: "1:448271751409:web:0f3b07e8525fbe12a33150"
}
```

### login
- create a new user using signup and login
- use email user1@user1.com / password:user1@user1.com

### setup
nvm use 14
yarn install
yarn start
https://devcenter.heroku.com/articles/heroku-cli#download-and-install 

## Hooks
```
const hooksExample = () => {
  const [user, setUser] = useState(null); // initial state
  const [searchQuery, setSearchQuery] = useState('Bret');

  useEffect({
    
  },[]);
}
```
1. useEffect called after every render
- useEffect groups simillar lifecycle methods better handling
2. componentDidMount -> useEffect for the first time
2. componentDidUpdate -> useEffect only , pass the state attribute in the array 2nd parameter to look for change
3. componentWillUnmount -> is same as the  return method of useEffect
4. restrict multiple execution of useEffect -> use second paramenter array and pass the state attributes on change of  which the method should be called useEffect(()={}, [])
5. useState -> state object with a setter
6. hooks not relying on this keywords lots of pitfalls with this.
7. useState -> to get previous state just use the object in the setter method argumnet
8. we cant do "export default with arrow function" has to use a function keyword only export default function(){}
9. Updating an array object in reducer : use map and return the same object if not updated and merge the sate with the updated array
10. Removing an array item in reducer: use array.filter , filter out the non matching items
11. state.todos.push(newObj) ==> [...state.todos, newObj]
return {
	...state,
	todos: newTodosArray
}