 ## Quest
<hr>

**1. How did we get the address of the user? Please explain in words and then in code.**<br/>
 By calling the handleAuthentication function once the user clicks the button, he can then login into his wallet and his address gets passed into the variable "user"
 ```
 <button onClick={handleAuthentication}>{user.loggedIn ? user.addr : "Log In"}</button>
 ```

**2. What do fcl.authenticate and fcl.unauthenticate do?**<br/>
 They handle the login / logoff states.

**3. Why did we make a config.js file? What does it do?**<br/>
 It provides the ability to use the FCL to login on testnet with Blocto & Lilico Wallet.

**4. What does our useEffect do?**<br/>
 Reruns the function every time the page is refreshed.
 
**5. How do we import FCL?**<br/>
 By first installing the FCL and then in the config.js folder >
 ```import { config } from "@onflow/fcl";```

**6. What does fcl.currentUser.subscribe(setUser); do?**<br/>
 Makes sure that the subscribed user tracks the setUser variable