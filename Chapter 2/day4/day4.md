 ## Quest
<hr>


```
import Head from 'next/head'
import styles from '../styles/Home.module.css'
import Nav from "../components/Nav.jsx"
import { useState } from 'react';

export default function Home() {
  const [newGreeting, setNewGreeting] = useState('');
  function runTransaction(){
    console.log(newGreeting);
  }
  return (
    <div className={styles.container}>
      <Head>
        <title>Emerald DApp</title>
        <meta name="description" content="Created by Emerald Academy" />
        <link rel="icon" href="https://i.imgur.com/hvNtbgD.png" />
      </Head>

      <Nav/>
      <main className={styles.main}>
        <h1 className={styles.title}>
          Welcome to my <a href="https://github.com/Xernaxe" target="_blank">Emerald DApp!</a>
        </h1>
        <p>Some text</p>
        <div className={styles.flex}>
        <button onClick={runTransaction}>Run Transaction</button>
        <input onChange={(e) => setNewGreeting(e.target.value)} placeholder="Hello, Idiots!" />

        </div>
      </main>
    </div>
  )
}
```


<img src="./day4img1.png" width="40%">
