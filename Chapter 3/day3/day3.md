 ## Quest
<hr>

**1. Explain why we wouldn't call changeGreeting in a script.**<br/>
 Scripts only deal with viewing the data, rather than changing it as transactions do.

**2. What does the AuthAccount mean in the prepare phase of the transaction?**<br/>
 AuthAccount refferences your account, so in the prepare phase the relevant data that is linked with your account is prepared for the transaction.

**3. What is the difference between the prepare phase and the execute phase in the transaction?**<br/>
 The prepare phase first prepare all the required data from the user account. <br/>
 The execute phase then uses the data (via functions) that was previously prepared.

Account 0x01
```
pub contract HelloWorld {

    pub var myNumber: Int

    pub fun updateMyNumber(newNumber: Int) {
    self.myNumber = newNumber
    }

    init() {
        self.myNumber = 0
    }
}
```

Transaction
```
import HelloWorld from 0x01

transaction(myNewNumber: Int) {
    prepare(signer: AuthAccount) {}

    execute {
    HelloWorld.updateMyNumber(newNumber: myNewNumber)
    }
}
```

Script
```
import HelloWorld from 0x01

pub fun main(): Int {
    return HelloWorld.myNumber
}
```

