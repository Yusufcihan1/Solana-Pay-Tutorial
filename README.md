 <p align="center">
<img alt="Next.js" src="https://img.shields.io/badge/-Next.js-black?style=for-the-badge&logo=next.js&logoColor=white" /> 
<img alt="Web3.js" src="https://img.shields.io/badge/-Web3.js-F16822?style=for-the-badge&logo=web3.js&logoColor=white" />
<img alt="Solana" src="https://img.shields.io/badge/-Solana-3C3C3D?style=for-the-badge&logo=solana&logoColor=white" />
</p>

<img src="https://solanapay.com/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Fsolanapay-logo.e34e7b7f.svg&w=256&q=75"/>

### **Welcome 👋**

 
 
 **TUTORIAL : Taking Payments IRL with Solana Pay**
 -------------------------------------
This tutorial is for beginners. All concepts are explained in detail. The complete version of the code is included in places where you might get stuck.
We’re excited to partner with our friends at Solana to bring you this in-depth guide to payments on Solana.

Let’s get started!

![42](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/0707dee2-9de9-431e-975d-139ccb6b86dc)


**What we're building**
---------------------

We’re going to build a point-of-sale web app that allows us to take payments from customers in person. We’ll present a QR code that they can scan with a Solana wallet to make the payment. As soon as they do our app will update to show that they’ve paid. It’s pretty magic, and you’ll see just how easy it is to make it work!

We’re also going to look at online payments in Solana, and build a loyalty card scheme. You can do things like give users a 50% discount on every 5th purchase. Or whatever you like really, it’s super flexible. We’ll finish up with a sneak peek at some really cool upcoming Solana Pay functionality that pulls all of this together!


![12345](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/52376208-c10c-4882-87f5-96c37c5eeba5)
------------------------------------------------------------------------------------------------------------------------------
![123](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/d8337f8a-6f77-4b6e-bb77-04bb4769e026)
------------------------------------------------------------------------------------------------------------------------------
![1234](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/d418b2c8-e57b-4385-ac3d-7ed7008ed49d)
------------------------------------------------------------------------------------------------------------------------------

You can see our demo app at https://sol-music-shop-v8bx-5p1q2u2zc-yusufcihan1.vercel.app/

**Why Solana?**
-------------------

Well first, what is Solana? It’s a blockchain that developers can build awesome apps on! It has two main features that make it amazing for the payment use case:

It’s really fast. It’s as fast as paying by card in a shop. If you’ve used other blockchains and waited like 10 seconds for stuff to happen, you can forget about that here.

The fees are really low. Fractions of a cent. If you’ve ever bought an NFT or something and paid like $50 in gas, you can forget about that too.

This ain’t your grandma’s blockchain!

Their website shows some stats, here’s what they look like for me as I’m writing this:

![tutorial_W4JYPwWhtMzTJm91MqzkU](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/e1623a25-fcbb-4537-a837-78ecd5184c4e)



-The network is handling 2,070 transactions per second

-The average cost per transaction is $0.00025

-The network has done almost 62.3 billion transactions so far. By the time you read this, there’ll be hundreds of millions more transactions processed



What is Solana Pay?

Solana Pay is a specification for payments on Solana. It describes a way to encode a payment request in a URL, which can be displayed to users - for example as a QR code. And Solana mobile wallets are adding support for it, so users can seamlessly scan that QR code and make the payment.

In short, Solana Pay makes payments work IRL, really well. It works because of those features of Solana: it’s as fast as any card machine, and it’s miles cheaper than any credit card processor.

**Browser Wallet**
------------------



We’re going to start by getting a browser wallet set up, which we’ll use to get you onboarded to the Solana blockchain! Like in other blockchains, wallets are what we use to track our balances and interact with applications. If you already have a Solana wallet set up then feel free to speed through this!

The most popular browser wallet is called Phantom, and you can download it from their website here: https://phantom.app/download. They have browser extensions for Chrome, Brave, Firefox and Edge - so you’re probably covered! If you’d like to use a different wallet for any reason then feel free to, they’re all compatible.

When Phantom first launches you’ll have the option to create a new wallet or import an existing one:

<img width="448" alt="tutorial_NkbsjFlyOCxCC8_pDcSCS" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/cccb04dd-1f38-465c-849f-57a39488d620">


Click “Create a new wallet” unless you’ve used Solana before. Quick heads up on terminology, a wallet that you create here is also an “Account”. We’ll get into the account model of Solana later, but you might see that term as you look around.

You’ll be asked to create a password, this is for the Phantom extension only.

You’ll then be presented with your Secret Recovery Phrase. If you’ve used any blockchain before then you’ll be familiar with this! Your Secret Recovery Phrase will be 12 random words. This can be used to access all wallets you create in Phantom, for example to import them into another wallet. Make sure to never share this with anyone, they’ll be able to access all your wallets. Save it somewhere, you’ll need it when you want to import your wallets elsewhere!

Once you’re done with the setup you’ll be able to see your wallet in Phantom:

<img width="377" alt="tutorial_wgepRg6lqNRfbsieq-VZv" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/4f16f188-cdfe-471b-96ca-b31eb438e37b">


Before we do anything else let’s switch to Devnet. On devnet all the tokens are fake and have no real world value, so it’s great for learning! We can also send ourselves Solana for free which is handy!

In Phantom, go to Settings (gear icon in the bottom right), choose “Change Network” and select “Devnet”.

**Get some devnet SOL**
--------------------

Okay so that “0 SOL” thing is pretty boring, let’s get some Solana to play with! Head to https://solfaucet.com/ and put in your address. In Phantom your address is shown truncated at the top and you can click to copy the whole thing:

<img width="361" alt="6" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/e8899866-fc8b-4a37-aa97-863be7a128e4">


Paste your address in solfaucet and click Devnet:

<img width="970" alt="7" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/86e4de99-3397-4bce-96cb-c8351081d6fc">


BTW the current limit for each airdrop is 2 SOL. That should be more than enough for this tutorial :)

You’ll notice that you pretty much immediately get a success message:

<img width="397" alt="8" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/f95daa06-7e89-44b7-887d-988feb15a988">

Did I mention that Solana is fast? 🚀

Check Phantom and you’ll see your balance is now 1 SOL! Nice!

**Adding a second wallet (account)**
-----------------------------------

When we’re dealing with payments we need two accounts: one for the buyer and one for the seller. The buyer pays the seller! So far we’ve made one account and given it some SOL which it can use to buy stuff. Let’s make our seller account next.

In Phantom you can open the menu from the top left and add a new wallet:

<img width="365" alt="tutorial_b-4nwBRs2fbukEeDHTl4y" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/30375979-dcfe-4367-8259-9e5bc1560277">


Note that you won’t be asked to give a password or shown a Secret Recovery Phrase. Remember that the password is for the Phantom extension (it unlocks all wallets), and the Secret Recovery Phrase is for all wallets too!

One last thing, in Phantom (and most wallet apps) you can name your wallets to make them easier to identify. This is under Settings:

<img width="360" alt="tutorial_ZwWpUwYf7XSAlTW5FUBAz" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/adfefe27-5dd0-4d4a-b66b-440e9a2dad9c">


I recommend naming the first wallet (the one with SOL) “Buyer” and the second one “Shop”. Note that these names are just for you, they won’t be reflected on the blockchain at all. But they’ll make using Phantom a lot nicer!




**Grab the starter code**
----------------------------
That was a lot of setup, but now we’ve got your Solana wallets set up, we’ve got SOL in the buyer wallet and we’re ready to use it to buy stuff. Let’s start building our app!

You can download the starter code:
```
$ git clone -b start https://github.com/Yusufcihan1/Solana-Pay-Tutorial
```
This is a NextJS app. You can run it with npm:
```
$ npm install
$ npm run dev
```
By default it’ll run on localhost:3000. When it’s running, open it in your browser and you should see something like:

![11](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/47859b46-98e0-4343-a889-c717f4d85bf7)

The starter code gives you a simple ecommerce interface, where we can select some products and make an order! Although that checkout page is looking a bit bare right now.

**Customize it**
--------------------

The products displayed are in lib/products.ts, feel free to change them if you’d like to sell something other than cookies!


```
export const products = [
  {
    id: 'box-of-cookies',
    name: 'Box',
    description: 'A delicious box of handmade cookies',
    unitName: 'box', // shows after the price, eg. 0.05 SOL/box
    priceSol: 0.05,
    priceUsd: 5,
  },
  {
    id: 'basket-of-cookies',
    name: 'Basket',
    description: 'A large basket of handmade cookies',
    unitName: 'basket',
    priceSol: 0.1,
    priceUsd: 10,
  }
]
```

If you’re not a fan of the colours, fonts, whatever - it’s your app! Feel free to change whatever you like :)

When you’re happy with the starting code, go on to the next lesson and we’ll start building together!

**Our first sale**
------------------------
Before we take a look at building a point-of-sale app for taking IRL payments with Solana Pay, let’s make our app work as a simple e-commerce store: allow users to pay for their cookie order using SOL in their browser wallet. That’ll give us an idea of how Solana transactions work (we’ll see lots more of them later!) and what Solana Pay is doing behind the scenes.

Let’s start by installing some dependencies. These are maintained by Solana and handle wallet connection with a nice UI and React integration:

```
$ npm install @solana/web3.js @solana/wallet-adapter-react @solana/wallet-adapter-react-ui @solana/wallet-adapter-base @solana/wallet-adapter-wallets
```
Next we need to add code to handle the Solana connection and connected wallet at the top of our component hierarchy, which in Next means in pages/_app.tsx. We’re going to use a Solana connection to make requests to the blockchain, and the connected wallet to request the user to make a payment. Update pages/_app.tsx to look like:

```
import '../styles/globals.css'
import type { AppProps } from 'next/app'
import Layout from '../components/Layout'
import Head from 'next/head'
import { ConnectionProvider, WalletProvider } from '@solana/wallet-adapter-react'
import { WalletModalProvider } from '@solana/wallet-adapter-react-ui'
import { WalletAdapterNetwork } from '@solana/wallet-adapter-base'
import { clusterApiUrl } from '@solana/web3.js'
import { PhantomWalletAdapter, SolflareWalletAdapter } from '@solana/wallet-adapter-wallets'

// Default styles that can be overridden by your app
require('@solana/wallet-adapter-react-ui/styles.css');

function MyApp({ Component, pageProps }: AppProps) {
  // The network can be set to 'devnet', 'testnet', or 'mainnet-beta'.
  const network = WalletAdapterNetwork.Devnet;

  // You can also provide a custom RPC endpoint.
  const endpoint = clusterApiUrl(network);

  // @solana/wallet-adapter-wallets includes all the adapters but supports tree shaking and lazy loading --
  // Only the wallets you configure here will be compiled into your application, and only the dependencies
  // of wallets that your users connect to will be loaded.
  const wallets = [
    new PhantomWalletAdapter(),
    new SolflareWalletAdapter({ network }),
  ];

  return (
    <ConnectionProvider endpoint={endpoint}>
      <WalletProvider wallets={wallets} autoConnect>
        <WalletModalProvider>
          <Layout>
            <Head>
              <title>Cookies Inc</title>
            </Head>
            <Component {...pageProps} />
          </Layout>
        </WalletModalProvider>
      </WalletProvider>
    </ConnectionProvider>
  )
}

export default MyApp
```
There’s a lot new here! We’re creating a connection to the devnet Solana network. We’re also defining the wallets that we want to allow to connect to our app. Here I’ve used Phantom and Solflare, but there are adapters for loads of wallets so feel free to add any others you like! Once we’ve defined the endpoint and wallets, we wrap our app in some context providers so that we have access to the Solana connection and any connected wallet from every page in our app. This code is pretty much the same in any app using these Solana libraries.

None of this will immediately change anything about our current app, but it does give us lots of new capabilities. Let’s add the ability to connect a wallet to our home page. Update pages/index.tsx to the following:

```
import { useWallet } from '@solana/wallet-adapter-react'
import { WalletMultiButton } from '@solana/wallet-adapter-react-ui'
import Products from '../components/Products'
import SiteHeading from '../components/SiteHeading'

export default function HomePage() {
  // We get the public key of the connected wallet, if there is one
  const { publicKey } = useWallet()

  return (
    <div className="flex flex-col gap-8 max-w-4xl items-stretch m-auto pt-24">
      <SiteHeading>Cookies Inc</SiteHeading>

      {/* We add the Solana wallet connect button */}
      <div className="basis-1/4">
        <WalletMultiButton className='!bg-gray-900 hover:scale-105' />
      </div>

      {/* We disable checking out without a connected wallet */}
      <Products submitTarget='/checkout' enabled={publicKey !== null} />
    </div>
  )
}

```
I’ve added comments showing what’s new, and there’s some new imports too from the same libraries we used in pages/_app.tsx.

Now the page should look like this:



![13](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/13799aea-8767-4dcf-821e-e08b00b5c164)

If you click that “Select Wallet” button then you should see a modal to choose your wallet:

![14](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/d1d2d747-b3ba-4378-bf0c-a336e2b6dc72)

Click Phantom (make sure you’re connecting the buyer wallet), and approve the connection. The page should now look like this:

![15](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/fc0db40f-ef39-4ed8-908d-6f77f637968a)

Nice! We can connect the wallet and check out. Our checkout page doesn’t do anything yet so that’s our next job.

```
In reality we’d need to collect more information for an e-commerce purchase, like the buyer’s name and where they want their cookies delivered. Since we’re just using this to understand the Solana structures though, we’re going to skip that here.
```

**Generating the transaction**
----------------------
We could generate the transaction on the frontend, and send it to the user’s wallet. You might’ve seen apps that do this, for example for buying NFTs. But in an e-commerce use case, it makes more sense to use an API route to generate the transaction because that gives us the ability to record expected transactions reliably. Remember that any code we run on the frontend can be modified by the client!

The first thing we need is the shop address. We’ll use this in a few different places throughout the tutorial so let’s create a new file lib/addresses.ts:

```
import { PublicKey } from "@solana/web3.js"

// Your shop wallet address
export const shopAddress = new PublicKey('...') 
```
Make sure you put your shop address where I have the ...! Note that public key is another term we use for address, so we’re just storing the address here in a way that the Solana libraries expect it.

Okay let’s create our API route. Add a new file pages/api/makeTransaction.ts. We’re going to use this to generate a transaction for a given checkout, and then we’ll have the frontend request the user to approve that transaction. BTW don’t worry if you don’t understand all of this, I’ll go through it below. Here’s the code for it:

```
import { WalletAdapterNetwork } from "@solana/wallet-adapter-base"
import { clusterApiUrl, Connection, PublicKey, Transaction, SystemProgram, LAMPORTS_PER_SOL } from "@solana/web3.js"
import { NextApiRequest, NextApiResponse } from "next"
import { shopAddress } from "../../lib/addresses"
import calculatePrice from "../../lib/calculatePrice"

export type MakeTransactionInputData = {
  account: string,
}

export type MakeTransactionOutputData = {
  transaction: string,
  message: string,
}

type ErrorOutput = {
  error: string
}

export default async function handler(
  req: NextApiRequest,
  res: NextApiResponse<MakeTransactionOutputData | ErrorOutput>
) {
  try {
    // We pass the selected items in the query, calculate the expected cost
    const amount = calculatePrice(req.query)
    if (amount.toNumber() === 0) {
      res.status(400).json({ error: "Can't checkout with charge of 0" })
      return
    }

    // We pass the reference to use in the query
    const { reference } = req.query
    if (!reference) {
      res.status(400).json({ error: "No reference provided" })
      return
    }

    // We pass the buyer's public key in JSON body
    const { account } = req.body as MakeTransactionInputData
    if (!account) {
      res.status(400).json({ error: "No account provided" })
      return
    }
    const buyerPublicKey = new PublicKey(account)
    const shopPublicKey = shopAddress

    const network = WalletAdapterNetwork.Devnet
    const endpoint = clusterApiUrl(network)
    const connection = new Connection(endpoint)

    // Get a recent blockhash to include in the transaction
    const { blockhash } = await (connection.getLatestBlockhash('finalized'))

    const transaction = new Transaction({
      recentBlockhash: blockhash,
      // The buyer pays the transaction fee
      feePayer: buyerPublicKey,
    })

    // Create the instruction to send SOL from the buyer to the shop
    const transferInstruction = SystemProgram.transfer({
      fromPubkey: buyerPublicKey,
      lamports: amount.multipliedBy(LAMPORTS_PER_SOL).toNumber(),
      toPubkey: shopPublicKey,
    })

    // Add the reference to the instruction as a key
    // This will mean this transaction is returned when we query for the reference
    transferInstruction.keys.push({
      pubkey: new PublicKey(reference),
      isSigner: false,
      isWritable: false,
    })

    // Add the instruction to the transaction
    transaction.add(transferInstruction)

    // Serialize the transaction and convert to base64 to return it
    const serializedTransaction = transaction.serialize({
      // We will need the buyer to sign this transaction after it's returned to them
      requireAllSignatures: false
    })
    const base64 = serializedTransaction.toString('base64')

    // Insert into database: reference, amount

    // Return the serialized transaction
    res.status(200).json({
      transaction: base64,
      message: "Thanks for your order! 🍪",
    })
  } catch (err) {
    console.error(err);

    res.status(500).json({ error: 'error creating transaction', })
    return
  }
}
```
The API takes as input a JSON object {"account": "public-key"} and returns:

```
{
  "transaction": "base-64 encoded transaction",
  "message": "Thanks for your order! 🍪"
}
```
It also takes input in the request query:

The items selected in the form on the home page, for example ?box-of-cookies=2 if the user has bought 2 boxes of cookies. If you want to see how this looks a bit more, try selecting some products on the home page and checking out. You’ll see the checkout URL looks like: http://localhost:3000/checkout?box-of-cookies=2&basket-of-cookies=1. Currently we’re using those query params in the URL to display the total price on the checkout page, but we’ll also pass them to our API so it can calculate the price to charge too.

A reference: const { reference } = req.query. This is a new Solana public key that we’ll generate on the checkout page. I’ll explain that a bit more in a moment.

Let’s take a look in a bit more detail at how our API works and what it’s doing.

```
const network = WalletAdapterNetwork.Devnet
const endpoint = clusterApiUrl(network)
const connection = new Connection(endpoint)
```
This is the same sort of code we have in _app.tsx, we’re initializing a connection to Solana’s devnet network.

```
// Get a recent blockhash to include in the transaction
const { blockhash } = await (connection.getLatestBlockhash('finalized'))
```
A transaction should only be valid for a short time. We include the latest block seen on the network so far, and the transaction can then be rejected if that is too old.



```
const transaction = new Transaction({
  recentBlockhash: blockhash,
  // The buyer pays the transaction fee
  feePayer: buyerPublicKey,
})
```
Here we’re creating a new Solana transaction. We’re setting the recentBlockhash to that block we just fetched. We’re also setting our buyer as the fee payer for the transaction. This means that the buyer must sign the transaction before it is processed by the network, giving their authority for it to go ahead.

```
// Create the instruction to send SOL from the buyer to the shop
const transferInstruction = SystemProgram.transfer({
  fromPubkey: buyerPublicKey,
  lamports: amount.multipliedBy(LAMPORTS_PER_SOL).toNumber(),
  toPubkey: shopPublicKey,
})
```
A Solana transaction can contain a sequence of instructions, and it’s atomic - they either all succeed or the transaction fails with no changes. In this case, our transaction just has one instruction: send SOL from the buyer to the shop. Note that our store is currently priced in SOL but the transfer instruction expects to be given the number in lamports. There are 1 billion (10^9) lamports in 1 SOL but it’s best to always use the constant LAMPORTS_PER_SOL when converting between them.

```
// Add the reference to the instruction as a key
// This will mean this transaction is returned when we query for the reference
transferInstruction.keys.push({
  pubkey: new PublicKey(reference),
  isSigner: false,
  isWritable: false,
})

// Add the instruction to the transaction
transaction.add(transferInstruction)
```

Each instruction has a set of keys associated with it. The transaction can be looked up by any of these keys. Each key can be a signer (or not), and writeable (or not). In our case the transfer function is creating an instruction with some default keys:

The buyer public key: is a signer, because they’re transferring their SOL and must give their authority. Is writeable, because their SOL balance will change

The shop public key: is writeable, because their SOL balance will change. Is not a signer, they don’t need to give authority to receive SOL

In the code above we’re adding an additional key, the reference. Remember that this is a public key passed as input to our API, unique to the specific checkout session. It doesn’t need to be a signer or writeable, because it’s not involved in the actual transfer of SOL. But by adding it to our instruction, we’re able to look the transaction up using that reference. That will allow our checkout page to detect that a payment has been made!

Once we’ve added the extra key, we add the transfer instruction to the transaction. Our transaction now has one instruction.
```
// Serialize the transaction and convert to base64 to return it
const serializedTransaction = transaction.serialize({
  // We will need the buyer to sign this transaction after it's returned to them
  requireAllSignatures: false
})
const base64 = serializedTransaction.toString('base64')
```

We serialize the transaction and then convert it to base-64. This will allow us to return it from the API and consume it on the /checkout page. We must pass requireAllSignatures: false when we serialize it because our transaction requires the buyer’s signature and we don’t have that yet. We’ll request it from their connected wallet on the /checkout page.



```
One last thing before we move on: In reality you’d want to record this transaction in a database as part of the API call. This would allow us to later validate that the paid transaction is correct. Again because we’re focusing on the Solana structures here I’ve skipped over that in this tutorial.

```
That was a lot of theory! Let’s update our app so that we can call this API and see the transaction in practice.


**Requesting the transaction**
----------------------

First let’s just make sure that we can call this API and deserialize the returned transaction back.

Update pages/checkout.tsx to the following:

```
import { useWallet } from "@solana/wallet-adapter-react";
import { WalletMultiButton } from "@solana/wallet-adapter-react-ui";
import { Keypair, Transaction } from "@solana/web3.js";
import { useRouter } from "next/router";
import { useEffect, useMemo, useState } from "react";
import BackLink from "../components/BackLink";
import Loading from "../components/Loading";
import { MakeTransactionInputData, MakeTransactionOutputData } from "./api/makeTransaction";

export default function Checkout() {
  const router = useRouter();
  const { publicKey } = useWallet();

  // State to hold API response fields
  const [transaction, setTransaction] = useState<Transaction | null>(null);
  const [message, setMessage] = useState<string | null>(null);

  // Read the URL query (which includes our chosen products)
  const searchParams = new URLSearchParams();
  for (const [key, value] of Object.entries(router.query)) {
    if (value) {
      if (Array.isArray(value)) {
        for (const v of value) {
          searchParams.append(key, v);
        }
      } else {
        searchParams.append(key, value);
      }
    }
  }

  // Generate the unique reference which will be used for this transaction
  const reference = useMemo(() => Keypair.generate().publicKey, []);

  // Add it to the params we'll pass to the API
  searchParams.append('reference', reference.toString());

  // Use our API to fetch the transaction for the selected items
  async function getTransaction() {
    if (!publicKey) {
      return;
    }

    const body: MakeTransactionInputData = {
      account: publicKey.toString(),
    }

    const response = await fetch(`/api/makeTransaction?${searchParams.toString()}`, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify(body),
    })

    const json = await response.json() as MakeTransactionOutputData

    if (response.status !== 200) {
      console.error(json);
      return;
    }

    // Deserialize the transaction from the response
    const transaction = Transaction.from(Buffer.from(json.transaction, 'base64'));
    setTransaction(transaction);
    setMessage(json.message);
    console.log(transaction);
  }

  useEffect(() => {
    getTransaction()
  }, [publicKey])

  if (!publicKey) {
    return (
      <div className='flex flex-col gap-8 items-center'>
        <div><BackLink href='/'>Cancel</BackLink></div>

        <WalletMultiButton />

        <p>You need to connect your wallet to make transactions</p>
      </div>
    )
  }

  return (
    <div className='flex flex-col gap-8 items-center'>
      <div><BackLink href='/'>Cancel</BackLink></div>

      <WalletMultiButton />

      {message ?
        <p>{message} Please approve the transaction using your wallet</p> :
        <p>Creating transaction... <Loading /></p>
      }
    </div>
  )
}
```

There’s quite a lot new here! Let’s step through it:

```
const { publicKey } = useWallet();
```
This just reads the connected wallet from the home page. It’ll be null if there’s no connected wallet.
```
// State to hold API response fields
const [transaction, setTransaction] = useState<Transaction | null>(null);
const [message, setMessage] = useState<string | null>(null);
```
Just some react state. Our API returns a transaction + a message, so we’ll set these from the response when we get it.
```
// Read the URL query (which includes our chosen products)
const searchParams = new URLSearchParams();
for (const [key, value] of Object.entries(router.query)) {
  if (value) {
    if (Array.isArray(value)) {
      for (const v of value) {
        searchParams.append(key, v);
      }
    } else {
      searchParams.append(key, value);
    }
  }
}
```
Just converting the query params to a URLSearchParams object. This is easier to work with than the type Next gives us for query params! Remember that the selected products are in the query params, and we need to pass them on to our API.

```
// Generate the unique reference which will be used for this transaction
const reference = useMemo(() => Keypair.generate().publicKey, []);

// Add it to the params we'll pass to the API
searchParams.append('reference', reference.toString());
```

This is the reference that we discussed in the API. We generate it on this page, and add it to the params we’re passing in. We’ll be able to use this to detect the transaction shortly.
```
// Use our API to fetch the transaction for the selected items
async function getTransaction() {
  if (!publicKey) {
    return;
  }

  const body: MakeTransactionInputData = {
    account: publicKey.toString(),
  }

  const response = await fetch(`/api/makeTransaction?${searchParams.toString()}`, {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json'
    },
    body: JSON.stringify(body),
  })

  const json = await response.json() as MakeTransactionOutputData

  if (response.status !== 200) {
    console.error(json);
    return;
  }

  // Deserialize the transaction from the response
  const transaction = Transaction.from(Buffer.from(json.transaction, 'base64'));
  setTransaction(transaction);
  setMessage(json.message);
  console.log(transaction);
}

useEffect(() => {
  getTransaction()
}, [publicKey])
```

We’re making an API call to our /api/makeTransaction and passing it our query params + the account body. We decode the response from base64 and deserialize it back into a Transaction object.



```
if (!publicKey) {
  return (
    <div className='flex flex-col gap-8 items-center'>
      <div><BackLink href='/'>Cancel</BackLink></div>

      <WalletMultiButton />

      <p>You need to connect your wallet to make transactions</p>
    </div>
  )
}

return (
  <div className='flex flex-col gap-8 items-center'>
    <div><BackLink href='/'>Cancel</BackLink></div>

    <WalletMultiButton />

    {message ?
      <p>{message} Please approve the transaction using your wallet</p> :
      <p>Creating transaction... <Loading /></p>
    }
  </div>
)
```

Our render is a bit more interesting now! First we handle the case where there isn’t a publicKey - we can’t create the transaction without that. We just show the wallet connect button and let the user know they’ll need to connect.

Otherwise, we first show a little loading indicator while we fetch the transaction. Once we have it, we show the message returned by the API. If you refresh the page you should see the transaction fetched and logged and the message shown:

![16](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/d40d14cf-0a46-4801-94da-41cdc630796b)

**Sending the transaction**
----------------------
Okay nice, we’ve got a transaction from our API! Now let’s update the page to send that to the user’s wallet and ask them to approve it.

First we need to grab a bit more context using hooks:
```
import { useConnection, useWallet } from "@solana/wallet-adapter-react";

export default function Checkout() {
  const router = useRouter();
  const { connection } = useConnection();
  const { publicKey, sendTransaction } = useWallet();

  // unchanged below here
```

We’re getting the Solana connection, and we’re also getting sendTransaction from the connected wallet. That’s a function that we can use to send a transaction using the connected wallet.

Now after getTransaction and its useEffect hook, we need to add another function and hook:
```
// unchanged code before this
useEffect(() => {
  getTransaction()
}, [publicKey])

// Send the fetched transaction to the connected wallet
async function trySendTransaction() {
  if (!transaction) {
    return;
  }
  try {
    await sendTransaction(transaction, connection)
  } catch (e) {
    console.error(e)
  }
}

// Send the transaction once it's fetched
useEffect(() => {
  trySendTransaction()
}, [transaction])

// render code unchanged
```

It can be a bit confusing slotting new code in like this, if you get lost here’s the full pages/checkout.tsx at this point:
```

import { useConnection, useWallet } from "@solana/wallet-adapter-react";
import { WalletMultiButton } from "@solana/wallet-adapter-react-ui";
import { Keypair, Transaction } from "@solana/web3.js";
import { useRouter } from "next/router";
import { useEffect, useMemo, useState } from "react";
import BackLink from "../components/BackLink";
import Loading from "../components/Loading";
import { MakeTransactionInputData, MakeTransactionOutputData } from "./api/makeTransaction";

export default function Checkout() {
  const router = useRouter();
  const { connection } = useConnection();
  const { publicKey, sendTransaction } = useWallet();

  // State to hold API response fields
  const [transaction, setTransaction] = useState<Transaction | null>(null);
  const [message, setMessage] = useState<string | null>(null);

  // Read the URL query (which includes our chosen products)
  const searchParams = new URLSearchParams();
  for (const [key, value] of Object.entries(router.query)) {
    if (value) {
      if (Array.isArray(value)) {
        for (const v of value) {
          searchParams.append(key, v);
        }
      } else {
        searchParams.append(key, value);
      }
    }
  }

  // Generate the unique reference which will be used for this transaction
  const reference = useMemo(() => Keypair.generate().publicKey, []);

  // Add it to the params we'll pass to the API
  searchParams.append('reference', reference.toString());

  // Use our API to fetch the transaction for the selected items
  async function getTransaction() {
    if (!publicKey) {
      return;
    }

    const body: MakeTransactionInputData = {
      account: publicKey.toString(),
    }

    const response = await fetch(`/api/makeTransaction?${searchParams.toString()}`, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify(body),
    })

    const json = await response.json() as MakeTransactionOutputData

    if (response.status !== 200) {
      console.error(json);
      return;
    }

    // Deserialize the transaction from the response
    const transaction = Transaction.from(Buffer.from(json.transaction, 'base64'));
    setTransaction(transaction);
    setMessage(json.message);
    console.log(transaction);
  }

  useEffect(() => {
    getTransaction()
  }, [publicKey])

  // Send the fetched transaction to the connected wallet
  async function trySendTransaction() {
    if (!transaction) {
      return;
    }
    try {
      await sendTransaction(transaction, connection)
    } catch (e) {
      console.error(e)
    }
  }

  // Send the transaction once it's fetched
  useEffect(() => {
    trySendTransaction()
  }, [transaction])

  if (!publicKey) {
    return (
      <div className='flex flex-col gap-8 items-center'>
        <div><BackLink href='/buy'>Cancel</BackLink></div>

        <WalletMultiButton />

        <p>You need to connect your wallet to make transactions</p>
      </div>
    )
  }

  return (
    <div className='flex flex-col gap-8 items-center'>
      <div><BackLink href='/buy'>Cancel</BackLink></div>

      <WalletMultiButton />

      {message ?
        <p>{message} Please approve the transaction using your wallet</p> :
        <p>Creating transaction... <Loading /></p>
      }
    </div>
  )
}
```

When the transaction state gets updated (which we do when we call setTransaction) we send that transaction to the user’s wallet using sendTransaction.

If you refresh the checkout page now then Phantom should prompt you to approve the transaction:

<img width="1399" alt="17" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/9e964970-2f08-43b0-ad6f-ff965932e2f0">

BTW when that first opens it might say something like “Transaction may fail to confirm” before it shows the SOL price. That’s normal! What’s actually happening there is that the wallet is asking the Solana network to simulate the transaction so that it can advise you what will happen if you approve it - in this case that you’ll be charged 0.05 SOL. It also might say that if you leave the transaction unapproved for a while. That’s because of the recent blockhash that we talked about before, the transaction becomes stale and will need to be generated again.

If you approve it though, then you’ll send your first Solana transaction! Sweet!

Our UI won’t know that you’ve paid yet, so nothing will happen there. That’s our next job! But if you check your account in Phantom you’ll see the transaction there:

<img width="358" alt="18" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/718a9db4-f3d8-4e5c-aa27-0fee3ccb9c10">

And that’s all we have to do to send a transaction!



**Detecting Payment**
----------------------------

The UX so far is a bit limited, once we present the transaction the user has to go and check their own wallet to see that they’ve paid. We can do way better than that!

Technically we can do this without Solana Pay, but it has a super handy function that’ll make it really straightforward. So let’s install it now:

```
npm install @solana/pay@0.2.0
```

We version this dependency just to make sure the APIs used in this tutorial don’t change before we get a chance to update it.
We’re going to add one more useEffect to our pages/checkout.tsx:
```
// New import
import { findReference, FindReferenceError } from "@solana/pay";

// unchanged code before this
// Send the transaction once it's fetched
useEffect(() => {
  trySendTransaction()
}, [transaction])

// Check every 0.5s if the transaction is completed
useEffect(() => {
  const interval = setInterval(async () => {
    try {
      // Check if there is any transaction for the reference
      const signatureInfo = await findReference(connection, reference);
      console.log('They paid!!!')
    } catch (e) {
      if (e instanceof FindReferenceError) {
        // No transaction found yet, ignore this error
        return;
      }
      console.error('Unknown error', e)
    }
  }, 500)
  return () => {
    clearInterval(interval)
  }
}, [])

// render code unchanged
if (!publicKey) {
  return (
    ...
 
```
Again if you need it then here's the full file at this point:
```
import { useConnection, useWallet } from "@solana/wallet-adapter-react";
import { WalletMultiButton } from "@solana/wallet-adapter-react-ui";
import { Keypair, Transaction } from "@solana/web3.js";
import { findReference, FindReferenceError } from "@solana/pay";
import { useRouter } from "next/router";
import { useEffect, useMemo, useState } from "react";
import BackLink from "../components/BackLink";
import Loading from "../components/Loading";
import { MakeTransactionInputData, MakeTransactionOutputData } from "./api/makeTransaction";

export default function Checkout() {
  const router = useRouter();
  const { connection } = useConnection();
  const { publicKey, sendTransaction } = useWallet();

  // State to hold API response fields
  const [transaction, setTransaction] = useState<Transaction | null>(null);
  const [message, setMessage] = useState<string | null>(null);

  // Read the URL query (which includes our chosen products)
  const searchParams = new URLSearchParams();
  for (const [key, value] of Object.entries(router.query)) {
    if (value) {
      if (Array.isArray(value)) {
        for (const v of value) {
          searchParams.append(key, v);
        }
      } else {
        searchParams.append(key, value);
      }
    }
  }

  // Generate the unique reference which will be used for this transaction
  const reference = useMemo(() => Keypair.generate().publicKey, []);

  // Add it to the params we'll pass to the API
  searchParams.append('reference', reference.toString());

  // Use our API to fetch the transaction for the selected items
  async function getTransaction() {
    if (!publicKey) {
      return;
    }

    const body: MakeTransactionInputData = {
      account: publicKey.toString(),
    }

    const response = await fetch(`/api/makeTransaction?${searchParams.toString()}`, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify(body),
    })

    const json = await response.json() as MakeTransactionOutputData

    if (response.status !== 200) {
      console.error(json);
      return;
    }

    // Deserialize the transaction from the response
    const transaction = Transaction.from(Buffer.from(json.transaction, 'base64'));
    setTransaction(transaction);
    setMessage(json.message);
    console.log(transaction);
  }

  useEffect(() => {
    getTransaction()
  }, [publicKey])

  // Send the fetched transaction to the connected wallet
  async function trySendTransaction() {
    if (!transaction) {
      return;
    }
    try {
      await sendTransaction(transaction, connection)
    } catch (e) {
      console.error(e)
    }
  }

  // Send the transaction once it's fetched
  useEffect(() => {
    trySendTransaction()
  }, [transaction])

  // Check every 0.5s if the transaction is completed
  useEffect(() => {
    const interval = setInterval(async () => {
      try {
        // Check if there is any transaction for the reference
        const signatureInfo = await findReference(connection, reference);
        console.log('They paid!!!')
      } catch (e) {
        if (e instanceof FindReferenceError) {
          // No transaction found yet, ignore this error
          return;
        }
        console.error('Unknown error', e)
      }
    }, 500)
    return () => {
      clearInterval(interval)
    }
  }, [])

  if (!publicKey) {
    return (
      <div className='flex flex-col items-center gap-8'>
        <div><BackLink href='/'>Cancel</BackLink></div>

        <WalletMultiButton />

        <p>You need to connect your wallet to make transactions</p>
      </div>
    )
  }

  return (
    <div className='flex flex-col items-center gap-8'>
      <div><BackLink href='/'>Cancel</BackLink></div>

      <WalletMultiButton />

      {message ?
        <p>{message} Please approve the transaction using your wallet</p> :
        <p>Creating transaction... <Loading /></p>
      }
    </div>
  )
}
```
We’ve added an interval that checks every 0.5s to see if there is any transaction using our reference. If there isn’t then findReference will throw a FindReferenceError which we catch and ignore. So now our checkout page will just keep polling in the background to see if the user has paid.

```
The call to findReference will find any transaction using our reference, which is not secret. It doesn’t guarantee that the correct transaction has been made. In this case, it’s OK because we’re just showing feedback to the user. Later in the tutorial, we’ll see ways to improve the security here.
```

If you refresh and approve the transaction, you should see a log message indicating that it’s paid:

<img width="1144" alt="19" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/3fd1d88c-99ae-4786-81d8-c3a5ab8adf51">

Now we just need to let the user know that we’ve received their payment!

**Adding a /confirmed page**
-------------------------
We’re going to add a new page to tell the user that their payment has been accepted.

I’m going to show you how I built mine, but if you’d like to do something else then feel free! Your app 🙂

First there’s one new dependency:
```
npm install react-circular-progressbar
```
This lets us animate a circular progress bar, which I think looks really nice! It comes with a bit of state for the animation, so we’ll put it in its own component:

```
import { useEffect, useState } from "react"
import { buildStyles, CircularProgressbar } from "react-circular-progressbar"
import 'react-circular-progressbar/dist/styles.css';

export default function Confirmed() {
  const [percentage, setPercentage] = useState(0)
  const [text, setText] = useState('🍪')

  useEffect(() => {
    const t1 = setTimeout(() => setPercentage(100), 100)
    const t2 = setTimeout(() => setText('✅'), 600)

    return () => {
      clearTimeout(t1)
      clearTimeout(t2)
    }
  }, [])

  return (
    <CircularProgressbar value={percentage} text={text} styles={
      buildStyles({
        pathColor: '#00BA00',
      })
    } />
  )
}
```

The progress bar library has animation built in, but it only animates on state changes - so if we just create a progress bar with 100% progress then it won’t animate. And the animation is nice! So we create it with 0% and then animate it to 100% after 100ms.
There are a lot of neat options available in react-circular-progressbar! Their docs are here: 
And let's add a page to display that component.
Create pages/confirmed.tsx :

```
import BackLink from '../components/BackLink';
import Confirmed from '../components/Confirmed';
import PageHeading from '../components/PageHeading';

export default function ConfirmedPage() {
  return (
    <div className='flex flex-col gap-8 items-center'>
      <BackLink href='/'>Home</BackLink>

      <PageHeading>Thankyou, enjoy your cookies!</PageHeading>

      <div className='h-80 w-80'><Confirmed /></div>
    </div>
  )
}
```

And finally, we can update the useEffect in our checkout page to redirect to this page as soon as we see the payment!
```
  // Check every 0.5s if the transaction is completed
  useEffect(() => {
    const interval = setInterval(async () => {
      try {
        // Check if there is any transaction for the reference
        const signatureInfo = await findReference(connection, reference);
        router.push('/confirmed')
      } catch (e) {
        if (e instanceof FindReferenceError) {
          // No transaction found yet, ignore this error
          return;
        }
        console.error('Unknown error', e)
      }
    }, 500)
    return () => {
      clearInterval(interval)
    }
  }, [])
```
I've just edited the console.log line to be router.push('/confirmed').

And now when we receive a valid payment we’ll display the new confirmed screen:

![tutorial__7clC2VD3oSsgx8mbh6Ak](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/11c7d3a9-4ba4-4551-a3da-35cf8b290951)

At this point we can sell cookies on our site using Solana!

But lots of people coming into our cookie shop might not know what the value of a SOL is. It’d be nice if we could charge them in dollars instead! That’s what we’ll explore in the next step.


**Charging Dollars**
----------------------------
We can’t exchange literal US dollars on the Solana blockchain. But Solana does have a program that handles exchanging arbitrary tokens, in addition to SOL. You might have heard of these tokens before (they’re sometimes called altcoins or fungible tokens). In Solana, they’re called SPL tokens, SPL stands for Solana Program Library. We can hold these tokens in our wallets and pay/receive them in Solana transactions.

Some of these tokens are designed to have a fixed value in fiat currency, most often $1. This works because someone guarantees to always buy and sell them for exactly $1, usually by holding an equivalent number of dollars as there are tokens. This means that we can perform payments on the blockchain with tokens that are guaranteed to be worth exactly $1. These tokens are sometimes called stablecoins.

A popular stablecoin is USDC, which is available on many blockchains including Solana. But since we’re on Solana devnet we need to use a token that’s available there, which we’re going to call USDC-Dev.

**Getting some USDC-Dev**
-----------------------

We’re going to use a token faucet: https://spl-token-faucet.com/?token-name=USDC-Dev

You’ll see a button to connect your wallet using your browser wallet, make sure you connect the buyer account.

From here you’ll be able to airdrop yourself some of the token:
<img width="1262" alt="20" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/0f1bb3a7-5417-4569-9ed2-4ce567cf297e">

$1000 should be enough for our testing, but you can increase that amount if you need to!

Now click the “Get USDC-Dev” and your browser wallet should show a transaction:
<img width="364" alt="21" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/1167e315-f063-4674-93dc-d0372dba1ca0">

This should be familiar, it’s the same UI our app uses for transactions. All Solana transactions are sent to the connected wallet, which displays them in a consistent way.

We’re paying a small amount of SOL (shown in red), which is covering the cost of creating a USDC account for us. We'll get into more detail about these accounts later, so don't worry about it for now. Note that if you request USDC twice for the same address then you won't pay this again! If you need more SOL you can get more on the same page or from the faucet we used before.

We’re receiving 1000 USDC-Dev. That’s what the Gh9Zw... token is. Your wallet might show it as USDC-Dev or using the USDC logo. They’re a bit inconsistent about whether or not they display the metadata on devnet, and in this case, my wallet isn’t showing it.

The network fee is tiny, just like the transaction on our app are! Solana transaction fees are always tiny 🔥

Once you approve that transaction it should complete within a second or so, and then you should see the new token in your wallet:

![22](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/8380673a-cfa2-4b5d-8c91-00063b29d547)

That screenshot is from the iOS Phantom app which does display metadata for devnet tokens. But again your wallet might vary a bit in how it shows this token. In particular, Phantom's browser wallet might show it as Unknown token.

As long as it’s showing the token you’re good to go though!

Before continuing, make sure you use your wallet or the same faucet to send some USDC to your shop account too. For now, we need the shop account to have some USDC before transferring it in our own code. Later on, we'll see how to avoid needing to do this :)


**Updating our UI**
--------------------------------

Now that our buyer has some USDC-Dev, let’s update our app so that they can use it to buy our cookies!

We’ve actually already got prices in USD in lib/products.ts :

```
{
    id: 'box-of-cookies',
    name: 'Box',
    description: 'A delicious box of handmade cookies',
    unitName: 'box', // shows after the price, eg. 0.05 SOL/box
    priceSol: 0.05,
    priceUsd: 5,
},

```

So we just need to update our app to use those prices instead of the SOL ones.

First is the home page where we display the products with their pricing. This is in the components/Products.tsx component. We just need to change the price line in the loop that displays each product there.

See if you can find where that line is and update it yourself. Here’s how we want the page to look:

![23](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/269342c9-c197-40d2-99e1-059e6daa4aad)
Solution (components/Products.tsx) :
```
<div className="grid grid-cols-2 gap-8">
  {products.map(product => {
    return (
      <div className="rounded-md bg-white text-left p-8" key={product.id}>
        <h3 className="text-2xl font-bold">{product.name}</h3>
        <p className="text-sm text-gray-800">{product.description}</p>
        <p className="my-4">
          {/* We updated the next line */}
          <span className="mt-4 text-xl font-bold">${product.priceUsd}</span>
          {product.unitName && <span className="text-sm text-gray-800"> /{product.unitName}</span>}
        </p>
        <div className="mt-1">
          <NumberInput name={product.id} formRef={formRef} />
        </div>
      </div>
    )
  })}
</div>
```

Nice! We’re displaying our cookie prices in dollars on our store. Next we need to update our API to create a transaction priced in USDC instead of SOL.


**Updating our API**
-------------------------

Our API uses the function calculatePrice in lib/calculatePrice.ts to get the total price of the cookies being bought. We need to update that to use the priceUsd field:
```
export default function calculatePrice(query: ParsedUrlQuery): BigNumber {
  let amount = new BigNumber(0);
  for (let [id, quantity] of Object.entries(query)) {
    const product = products.find(p => p.id === id)
    if (!product) continue;

    const price = product.priceUsd // we just updated this from priceSol
    const productQuantity = new BigNumber(quantity as string)
    amount = amount.plus(productQuantity.multipliedBy(price))
  }

  return amount
}
```
Next we need to get the USDC address, which we’ll use to make a transaction that transfers USDC from the buyer to the shop.

Go to lib/addresses.ts and add our new address:
```
import { PublicKey } from "@solana/web3.js"

// this is your shop wallet address
export const shopAddress = new PublicKey('...')
// this is the same for everyone!
export const usdcAddress = new PublicKey('Gh9ZwEmdLJ8DscKNTkTqPbNwLNNBjuSzaG9Vp2KGtKJr')
```
Now we can update our API to send the transaction in USDC instead of SOL using that address. We’ll use a new dependency, which provides functionality for SPL tokens:
```
npm install @solana/spl-token
```
Here’s the updated code for pages/api/makeTransaction.ts, I’ll talk through the changes below:
```
import { createTransferCheckedInstruction, getAssociatedTokenAddress, getMint } from "@solana/spl-token"
import { WalletAdapterNetwork } from "@solana/wallet-adapter-base"
import { clusterApiUrl, Connection, PublicKey, Transaction } from "@solana/web3.js"
import { NextApiRequest, NextApiResponse } from "next"
import { shopAddress, usdcAddress } from "../../lib/addresses"
import calculatePrice from "../../lib/calculatePrice"

export type MakeTransactionInputData = {
  account: string,
}

export type MakeTransactionOutputData = {
  transaction: string,
  message: string,
}

type ErrorOutput = {
  error: string
}

export default async function handler(
  req: NextApiRequest,
  res: NextApiResponse<MakeTransactionOutputData | ErrorOutput>
) {
  try {
    // We pass the selected items in the query, calculate the expected cost
    const amount = calculatePrice(req.query)
    if (amount.toNumber() === 0) {
      res.status(400).json({ error: "Can't checkout with charge of 0" })
      return
    }

    // We pass the reference to use in the query
    const { reference } = req.query
    if (!reference) {
      res.status(400).json({ error: "No reference provided" })
      return
    }

    // We pass the buyer's public key in JSON body
    const { account } = req.body as MakeTransactionInputData
    if (!account) {
      res.status(400).json({ error: "No account provided" })
      return
    }
    const buyerPublicKey = new PublicKey(account)
    const shopPublicKey = shopAddress

    const network = WalletAdapterNetwork.Devnet
    const endpoint = clusterApiUrl(network)
    const connection = new Connection(endpoint)

    // Get details about the USDC token
    const usdcMint = await getMint(connection, usdcAddress)
    // Get the buyer's USDC token account address
    const buyerUsdcAddress = await getAssociatedTokenAddress(usdcAddress, buyerPublicKey)
    // Get the shop's USDC token account address
    const shopUsdcAddress = await getAssociatedTokenAddress(usdcAddress, shopPublicKey)

    // Get a recent blockhash to include in the transaction
    const { blockhash } = await (connection.getLatestBlockhash('finalized'))

    const transaction = new Transaction({
      recentBlockhash: blockhash,
      // The buyer pays the transaction fee
      feePayer: buyerPublicKey,
    })

    // Create the instruction to send USDC from the buyer to the shop
    const transferInstruction = createTransferCheckedInstruction(
      buyerUsdcAddress, // source
      usdcAddress, // mint (token address)
      shopUsdcAddress, // destination
      buyerPublicKey, // owner of source address
      amount.toNumber() * (10 ** (await usdcMint).decimals), // amount to transfer (in units of the USDC token)
      usdcMint.decimals, // decimals of the USDC token
    )

    // Add the reference to the instruction as a key
    // This will mean this transaction is returned when we query for the reference
    transferInstruction.keys.push({
      pubkey: new PublicKey(reference),
      isSigner: false,
      isWritable: false,
    })

    // Add the instruction to the transaction
    transaction.add(transferInstruction)

    // Serialize the transaction and convert to base64 to return it
    const serializedTransaction = transaction.serialize({
      // We will need the buyer to sign this transaction after it's returned to them
      requireAllSignatures: false
    })
    const base64 = serializedTransaction.toString('base64')

    // Insert into database: reference, amount

    // Return the serialized transaction
    res.status(200).json({
      transaction: base64,
      message: "Thanks for your order! 🍪",
    })
  } catch (err) {
    console.error(err);

    res.status(500).json({ error: 'error creating transaction', })
    return
  }
}
```
We have these new variables:
```
// Get details about the USDC token
const usdcMint = await getMint(connection, usdcAddress)
// Get the buyer's USDC token account address
const buyerUsdcAddress = await getAssociatedTokenAddress(usdcAddress, buyerPublicKey)
// Get the shop's USDC token account address
const shopUsdcAddress = await getAssociatedTokenAddress(usdcAddress, shopPublicKey)
```
The first line gets the metadata about the USDC token.

The second and third lines are getting the associated token accounts for the buyer and the shop. When we transfer an SPL token (like USDC) we don’t do it between the buyer and shop public keys, like we did with SOL. This might be a bit different if you’ve used other blockchains, where the contract will often map data directly to the address. In Solana the contract itself (in this case the token program, which allows exchanging tokens like USDC) is stateless, and it generates accounts that hold the data. So when we call getAssociatedTokenAddress(usdcAddress, buyerPublicKey) we’re getting the address of the buyer’s USDC account.

We’ve also updated the transaction instruction:
```
// Create the instruction to send USDC from the buyer to the shop
const transferInstruction = createTransferCheckedInstruction(
  buyerUsdcAddress, // source
  usdcAddress, // mint (token address)
  shopUsdcAddress, // destination
  buyerPublicKey, // owner of source address
  amount.toNumber() * (10 ** (await usdcMint).decimals), // amount to transfer (in units of the USDC token)
  usdcMint.decimals, // decimals of the USDC token
)
```
There’s a bit more here than the SOL transfer instruction that we saw before. I’ve put comments by each argument, so hopefully you can see what each of them represent. Note that buyerPublicKey will be the signer key, because we need their authority to transfer USDC from their USDC account.

The amount is slightly different too. Instead of using lamports (the smallest unit for SOL) like before, we need to use the units for the token. Tokens can have any number of decimals, so the safest way to do this is to multiply by (10 ** decimals). We get the number of decimals from the mint metadata that we fetched.

And that’s all we need to change to transfer USDC in a transaction! Everything else can stay the same, which shows the power of this transaction/instruction abstraction that Solana provides. We can update the instructions without changing anything else about the transaction.

And now if you checkout you should see a transaction in USDC:
<img width="676" alt="24" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/92287275-d7ef-4ee3-9caf-1a4908c32a26">

Again note that wallets will differ a bit in how they display the metadata here.

Once approved you’ll see our familiar confirmed page! We’ve updated our app to use USDC! 🎉

In the next lesson we’re going to jump into Solana Pay properly and see how we can take payments IRL without users having to connect their own wallet to our app to pay!


**SOLANA PAY**
----------------------
The magic of Solana Pay is that it takes the speed and tiny fees we’ve seen from the Solana network and it makes it work for in-person payments. Any shop, any market stall, can take payments without signing up for any services and without paying credit card processing fees. And it’s really cool to see it in action!

Here’s how it’s going to work:

We select the cookies the user is buying

We display a QR code on our checkout page

The user scans this with a mobile wallet app and approves the payment

We instantly see that they’ve done so and give them their cookies!

Mobile Wallet

Before we can build this we need to get ourselves a mobile wallet app! If you already have one for Solana then you can skip this, just make sure to import your buyer account into it. Otherwise, let’s get you set up!

For both iOS and Android you can use Phantom, the same as the browser wallet we’re using. You download it on the App Store, but to make sure you’re getting the correct app use the link on their download page: phantom.app/download

The nice thing about decentralized blockchains is that all the wallets etc. are compatible and you can choose whatever you like. If you prefer something else, go for it!

Whichever mobile wallet you’re using, you’re going to want to import your Buyer wallet from Phantom. To do this you’ll need to import using its private key. You can export the private key from your browser wallet under Settings:

<img width="369" alt="25" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/c9c0254b-0d2f-425a-b978-97ceb1b600e3">

Note that you’ll be asked for the password you used when setting up Phantom.

You can then import that private key into your mobile wallet. For example in Phantom (mobile) this option is under “Add/Connect Wallet” which you can find in the side menu:

![26](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/75cb8311-6ab4-4a40-86e9-9ff9240db757)
The best way to get the private key between devices is using a password manager that you share between your browser and phone. If you’re using macOS and iOS then copy/paste works too (usually)!

Note that we don’t need the Shop wallet on mobile, but if you want it there then feel free to import it too.

**Point of Sale Page**
----------------------

Let’s start by creating the page where we select the cookies somebody wants to buy. This will look super familiar because that’s what our ecommerce page does, we just don’t want all that stuff about connecting a wallet 🙂

Create a new pages/shop/index.tsx. We’ll put our point-of-sale shop interface at /shop. Here’s the code you’ll want, it’s just a cut down version of our pages/index.tsx:

```
import Products from '../../components/Products'
import SiteHeading from '../../components/SiteHeading'

export default function ShopPage() {
  return (
    <div className="flex flex-col gap-8 max-w-4xl items-stretch m-auto pt-24">
      <SiteHeading>Cookies Inc</SiteHeading>
      <Products submitTarget='/shop/checkout' enabled={true} />    </div>
  )
}
```

Nice and straightforward! If you check /shop now then you should see something like this:
![27](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/193cdb3c-8d02-4d78-bbc3-32c78a3fa5c7)

You can add cookies, but if you checkout then you’ll get a 404. We don’t have a shop checkout page yet! That’s where the Solana Pay magic will go.



**Checkout Page**
---------------
Create a new file pages/shop/checkout.tsx. Here’s some starter code, it’s just the starter code from pages/checkout.tsx but using USD:
```
import { useRouter } from "next/router";
import { useMemo } from "react";
import BackLink from "../../components/BackLink";
import PageHeading from "../../components/PageHeading";
import calculatePrice from "../../lib/calculatePrice";

export default function Checkout() {
  const router = useRouter()

  const amount = useMemo(() => calculatePrice(router.query), [router.query])

  return (
    <div className="flex flex-col gap-8 items-center">
      <BackLink href='/shop'>Cancel</BackLink>
      <PageHeading>Checkout ${amount.toString()}</PageHeading>
    </div>
  )
}
```
Nothing special there! It should look like this:

![28](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/91012c41-db0f-473f-b15d-5d4a7565f05d)

We’re calculating the amount we want to charge the user. Now we need to generate the Solana Pay QR code to charge them that amount.

Here’s the updated code, and then I’ll talk through it:
```
import { createQR, encodeURL, TransferRequestURLFields } from "@solana/pay";
import { Keypair } from "@solana/web3.js";
import { useRouter } from "next/router";
import { useEffect, useMemo, useRef } from "react";
import BackLink from "../../components/BackLink";
import PageHeading from "../../components/PageHeading";
import { shopAddress, usdcAddress } from "../../lib/addresses";
import calculatePrice from "../../lib/calculatePrice";

export default function Checkout() {
  const router = useRouter()

  // ref to a div where we'll show the QR code
  const qrRef = useRef<HTMLDivElement>(null)

  const amount = useMemo(() => calculatePrice(router.query), [router.query])

  // Unique address that we can listen for payments to
  const reference = useMemo(() => Keypair.generate().publicKey, [])

  // Solana Pay transfer params
  const urlParams: TransferRequestURLFields = {
    recipient: shopAddress,
    splToken: usdcAddress,
    amount,
    reference,
    label: "Cookies Inc",
    message: "Thanks for your order! 🍪",
  }

  // Encode the params into the format shown
  const url = encodeURL(urlParams)
  console.log({ url })

  // Show the QR code
  useEffect(() => {
    const qr = createQR(url, 512, 'transparent')
    if (qrRef.current && amount.isGreaterThan(0)) {
      qrRef.current.innerHTML = ''
      qr.append(qrRef.current)
    }
  })

  return (
    <div className="flex flex-col items-center gap-8">
      <BackLink href='/shop'>Cancel</BackLink>

      <PageHeading>Checkout ${amount.toString()}</PageHeading>

      {/* div added to display the QR code */}
      <div ref={qrRef} />
    </div>
  )
}
```
At a high level, we generate a QR code that encodes a URL. That URL will be something like this:
```
solana:EXWr1Go8UyfA39U1dfRkcH8uUvqunbRhQEUQNm36UsyQ?amount=15&spl-token=Gh9ZwEmdLJ8DscKNTkTqPbNwLNNBjuSzaG9Vp2KGtKJr&reference=25hRCjMFz46o9cEmNNwguNKTMXt2rCj7cEqAjW3w4gU8&label=Cookies%20Inc&message=Thanks%20for%20your%20order!%20%F0%9F%8D%AA
```

It starts with solana: and that’s followed by the recipient’s public key (our shop). Then there are optional params: the amount, the SPL token, the reference, the label, and the message. These parameters define the transaction that we want to create: the buyer should pay 15 USDC to the shop. It also includes some display parameters - like label and message which the user’s mobile wallet should show them to help understand the transaction.

The reference is exactly the same as what we saw on the ecommerce checkout page:
```
const reference = useMemo(() => Keypair.generate().publicKey, [])
```
We’ll use it for the same purpose here: to listen for our transaction.

So the code that generates that solana:... URL is:
```
  // Solana Pay transfer params
  const urlParams: TransferRequestURLFields = {
    recipient: shopAddress,
    splToken: usdcAddress,
    amount,
    reference,
    label: "Cookies Inc",
    message: "Thanks for your order! 🍪",
  }

  // Encode the params into the format shown
  const url = encodeURL(urlParams)
```
TransferRequestURLFields is provided by Solana Pay and gives us a type to define the parameters. encodeURL encodes these parameters into the solana:... URL format.
```
If you want to charge in SOL with Solana Pay that’s super easy: just remove splToken from TransferRequestURLFields. It’s an optional field and if it’s missing then everything will use SOL.
```
We then convert that URL into a QR code. To display it we have to append the QR code to an element. We use a react ref to hold that element:
```
  // Show the QR code
  useEffect(() => {
    const qr = createQR(url, 512, 'transparent')
    if (qrRef.current && amount.isGreaterThan(0)) {
      qrRef.current.innerHTML = ''
      qr.append(qrRef.current)
    }
  })
```
And we add the qrRef to our render at the bottom:
```
return (
    <div className="flex flex-col gap-8 items-center">
      <BackLink href='/shop'>Cancel</BackLink>

      <PageHeading>Checkout ${amount.toString()}</PageHeading>

      {/* div added to display the QR code */}
      <div ref={qrRef} />
    </div>
  )
```
Now if you refresh the shop checkout page you should see a QR code displayed!
![29](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/e8a52ca4-216f-4579-adb5-948bb35e9db5)

Nice! Now for the fun bit: open your mobile wallet and find its scan QR code feature. In Phantom it’s here:
![30](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/0312cd90-43df-4a48-b74b-8e862e86476a)
And when the code is scanned:

![tutorial__tMk5xsSpueuFwZTjfL5Q](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/79eb9010-56be-4e81-8d8d-39198f7a1770)

Note that different wallets will have different layouts, and may not show all fields/may show them in different ways.

This is a real Solana transaction! You can send it using the mobile wallet, and within a few seconds you’ll see the balance of each account update in your wallet apps.

Just like we did with the ecommerce checkout page, we can detect that payment and show the confirmation page. When we see that we can give them the cookies because they’ve paid!

**Detecting Payment**
-------------------
First let’s add a new pages/shop/confirmed.tsx, this is what we’ll redirect to after we see the payment. It’ll look very familiar:
```
import 'react-circular-progressbar/dist/styles.css';
import BackLink from '../../components/BackLink';
import Confirmed from '../../components/Confirmed';
import PageHeading from '../../components/PageHeading';

export default function ConfirmedPage() {
  return (
    <div className='flex flex-col gap-8 items-center'>
      <BackLink href='/shop'>Next order</BackLink>

      <PageHeading>Thankyou, enjoy your cookies!</PageHeading>

      <div className='h-80 w-80'><Confirmed /></div>
    </div>
  )
}

```
Pretty much the same as the e-commerce one!

And now in pages/shop/checkout.tsx we need to add similar logic we have on the e-commerce one: an interval to check for a transaction matching our reference. Here’s how that looks:
```
/* Updated imports */
import { createQR, encodeURL, TransferRequestURLFields, findReference, validateTransfer, FindReferenceError, ValidateTransferError } from "@solana/pay";
import { WalletAdapterNetwork } from "@solana/wallet-adapter-base";
import { clusterApiUrl, Connection, Keypair } from "@solana/web3.js";
import { useRouter } from "next/router";
import { useEffect, useMemo, useRef } from "react";
import BackLink from "../../components/BackLink";
import PageHeading from "../../components/PageHeading";
import { shopAddress, usdcAddress } from "../../lib/addresses";
import calculatePrice from "../../lib/calculatePrice";

/* Add code to the component to get the Solana connection */
// Unique address that we can listen for payments to
const reference = useMemo(() => Keypair.generate().publicKey, [])

// Get a connection to Solana devnet
const network = WalletAdapterNetwork.Devnet
const endpoint = clusterApiUrl(network)
const connection = new Connection(endpoint)

// Solana Pay transfer params
const urlParams: TransferRequestURLFields = {
  recipient: shopAddress,
  splToken: usdcAddress,
  amount,
  reference,
  label: "Cookies Inc",
  message: "Thanks for your order! 🍪",
}

/* Add a new useEffect to detect payment */
// Check every 0.5s if the transaction is completed
useEffect(() => {
  const interval = setInterval(async () => {
    try {
      // Check if there is any transaction for the reference
      const signatureInfo = await findReference(connection, reference, { finality: 'confirmed' })
      // Validate that the transaction has the expected recipient, amount and SPL token
      await validateTransfer(
        connection,
        signatureInfo.signature,
        {
          recipient: shopAddress,
          amount,
          splToken: usdcAddress,
          reference,
        },
        { commitment: 'confirmed' }
      )
      router.push('/shop/confirmed')
    } catch (e) {
      if (e instanceof FindReferenceError) {
        // No transaction found yet, ignore this error
        return;
      }
      if (e instanceof ValidateTransferError) {
        // Transaction is invalid
        console.error('Transaction is invalid', e)
        return;
      }
      console.error('Unknown error', e)
    }
  }, 500)
  return () => {
    clearInterval(interval)
  }
}, [amount])
```
If you need it, here’s the full file at this point:
```
import { createQR, encodeURL, TransferRequestURLFields, findReference, validateTransfer, FindReferenceError, ValidateTransferError } from "@solana/pay";
import { WalletAdapterNetwork } from "@solana/wallet-adapter-base";
import { clusterApiUrl, Connection, Keypair } from "@solana/web3.js";
import { useRouter } from "next/router";
import { useEffect, useMemo, useRef } from "react";
import BackLink from "../../components/BackLink";
import PageHeading from "../../components/PageHeading";
import { shopAddress, usdcAddress } from "../../lib/addresses";
import calculatePrice from "../../lib/calculatePrice";

export default function Checkout() {
  const router = useRouter()

  // ref to a div where we'll show the QR code
  const qrRef = useRef<HTMLDivElement>(null)

  const amount = useMemo(() => calculatePrice(router.query), [router.query])

  // Unique address that we can listen for payments to
  const reference = useMemo(() => Keypair.generate().publicKey, [])

  // Get a connection to Solana devnet
  const network = WalletAdapterNetwork.Devnet
  const endpoint = clusterApiUrl(network)
  const connection = new Connection(endpoint)

  // Solana Pay transfer params
  const urlParams: TransferRequestURLFields = {
    recipient: shopAddress,
    splToken: usdcAddress,
    amount,
    reference,
    label: "Cookies Inc",
    message: "Thanks for your order! 🍪",
  }

  // Encode the params into the format shown
  const url = encodeURL(urlParams)
  console.log({ url })

  // Show the QR code
  useEffect(() => {
    const qr = createQR(url, 512, 'transparent')
    if (qrRef.current && amount.isGreaterThan(0)) {
      qrRef.current.innerHTML = ''
      qr.append(qrRef.current)
    }
  })

  // Check every 0.5s if the transaction is completed
  useEffect(() => {
    const interval = setInterval(async () => {
      try {
        // Check if there is any transaction for the reference
        const signatureInfo = await findReference(connection, reference, { finality: 'confirmed' })
        // Validate that the transaction has the expected recipient, amount and SPL token
        await validateTransfer(
          connection,
          signatureInfo.signature,
          {
            recipient: shopAddress,
            amount,
            splToken: usdcAddress,
            reference,
          },
          { commitment: 'confirmed' }
        )
        router.push('/shop/confirmed')
      } catch (e) {
        if (e instanceof FindReferenceError) {
          // No transaction found yet, ignore this error
          return;
        }
        if (e instanceof ValidateTransferError) {
          // Transaction is invalid
          console.error('Transaction is invalid', e)
          return;
        }
        console.error('Unknown error', e)
      }
    }, 500)
    return () => {
      clearInterval(interval)
    }
  }, [amount])

  return (
    <div className="flex flex-col items-center gap-8">
      <BackLink href='/shop'>Cancel</BackLink>

      <PageHeading>Checkout ${amount.toString()}</PageHeading>

      {/* div added to display the QR code */}
      <div ref={qrRef} />
    </div>
  )
}

```

This is slightly different from what we used on our other checkout page. Let’s take a closer look at the inner loop:
```
try {
  // Check if there is any transaction for the reference
  const signatureInfo = await findReference(connection, reference, { finality: 'confirmed' })
  // Validate that the transaction has the expected recipient, amount and SPL token
  await validateTransfer(
    connection,
    signatureInfo.signature,
    {
      recipient: shopAddress,
      amount,
      splToken: usdcAddress,
      reference,
    },
    { commitment: 'confirmed' }
  )
  router.push('/shop/confirmed')
}
```

We’ve updated our call to find the signature:
```
const signatureInfo = await findReference(connection, reference, { finality: 'confirmed' })
```

This is the same function we used before, except I’ve added an extra argument of {finality: 'confirmed'}. Solana transactions are very quickly confirmed, but take a little longer (up to a few seconds) to get finalized. If you’re dealing with really big transactions you might prefer to use finalized, but confirmed is usually enough. It’s also super fast! If you like you can update this function call in pages/checkout.tsx to match, it’ll make it a bit faster. It’s much more noticeable with Solana Pay than a browser wallet though.

This is new:
```
await validateTransfer(
  connection,
  signatureInfo.signature,
  {
    recipient: shopAddress,
    amount,
    splToken: usdcAddress,
    reference,
  },
  { commitment: 'confirmed' }
)
```
Earlier I mentioned that findReference will find any transaction with the reference. In that case it wasn’t a big deal, we were just showing the user that we’d accepted their transaction. We’d be going through payments before dispatching orders!

But in our shop, we’re going to give them the cookies as soon as they’ve paid. So we need to be a bit more sure! Imagine somebody wrote an app that scans our QR code, extracts the reference, and then makes its own random Solana transaction that isn’t paying us. Or maybe it does pay us, but only $0.01. findReference will dutifully report that a transaction with our reference has been made, because it has! But it’s not the transaction we wanted.

That’s where validateTransfer comes in. It will fetch the transaction that findReference identified, and check that it matches the parameters we expect. If it didn’t pay us, or it paid us the wrong amount, it won’t validate and we won’t show the confirmed page.

At this point you have Solana Pay working! When you approve the payment in your mobile wallet you’ll see our UI quickly displays the confirmed page. The customer gets their cookies and we serve the next customer!

![tutorial_WqUwdeE-_azecW4lR-ObG](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/0d079415-3ab5-44cb-8b1a-5306f439e693)
So far Solana Pay is able to do exactly what our makeTransaction API is doing: it’s just transferring USDC from the buyer to the shop. This is called a transfer request. In the next lesson, we’re going to discuss a more powerful specification called transaction requests. It'll let us do some really cool things!

**Transaction Requests**
-----------------------
So far the transactions we’ve dealt with - both ones created by our API and those handled by Solana Pay - have been very simple. We’ve just been writing transactions that do a single transfer, either SOL or USDC.

But Solana transactions are much more powerful than that. They can include multiple instructions, and they give a guarantee that the transaction either executes in full or not at all. Instructions can pass any data to any Solana program. When we transferred SOL we were actually sending that request to the System program, and for USDC it’s the token program.

Some examples of what we could do with transactions:

Have the buyer send USDC to multiple recipients, or SOL to one and USDC to another, etc!

Send USDC to the shop, and have the shop send an NFT in return

Send USDC to the shop, and have the shop send a loyalty coupon in return

Send a discounted amount of USDC to the shop, in addition to some collected loyalty coupons

We’re going to build those last two in the next lesson, which will give us a chance to go a bit deeper on transactions.

This flexibility to send any transaction isn’t available to us in Solana Pay’s transfer requests, but it is available with transaction requests. Instead of encoding parameters that describe a single transfer, we encode a URL that the wallet should use to request a transaction. It will then display that transaction to the user to approve. This API can return any transaction at all!

Here’s a diagram of how this works:

![31](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/b18fbe87-ace1-46e4-8ee8-38dd77088775)
The wallet makes two requests to our URL. In the first it sends a GET request, and we can return some data identifying ourselves. The wallet can display this to the user so they understand who they’re transacting with. In the second it sends a POST request with the public key of the buyer, and we return our transaction and message.

Not coincidentally, that POST request is exactly the same shape as the API we’ve already built for our ecommerce store. You basically already know how to use transaction requests!

Another really important and powerful feature here is that the account is sent to our API when the transaction is requested. We’re currently using that to get the USDC account for that user in our transaction. But we could do things like looking at the user’s balances or tokens on the blockchain, or their transaction history, and return a different transaction depending on who the buyer is. Maybe we want holders of a certain NFT to get a discount at our cookie shop? Maybe we want to give new customers who usually go to a lame competing cookie shop some extra loyalty coupons? Knowing the buyer’s address gives us a huge amount of flexibility! And with transaction requests, we can do all of this for IRL payments, as well as on our site.

**Handling the GET request**
----------------------------

Our API already does the most complicated part of transaction requests: returning a serialized transaction. But let’s extend it to handle the GET request too, so we’ll be able to use our API with mobile wallets.

The specification expects us to respond to a GET request with:
```
{
  "label": "<some label>",
  "icon": "<url of some icon>"
}
```
Pretty easy! Here’s our updated pages/api/makeTransaction.ts:
```
import { createTransferCheckedInstruction, getAssociatedTokenAddress, getMint } from "@solana/spl-token"
import { WalletAdapterNetwork } from "@solana/wallet-adapter-base"
import { clusterApiUrl, Connection, PublicKey, Transaction } from "@solana/web3.js"
import { NextApiRequest, NextApiResponse } from "next"
import { shopAddress, usdcAddress } from "../../lib/addresses"
import calculatePrice from "../../lib/calculatePrice"

export type MakeTransactionInputData = {
  account: string,
}

type MakeTransactionGetResponse = {
  label: string,
  icon: string,
}

export type MakeTransactionOutputData = {
  transaction: string,
  message: string,
}

type ErrorOutput = {
  error: string
}

function get(res: NextApiResponse<MakeTransactionGetResponse>) {
  res.status(200).json({
    label: "Cookies Inc",
    icon: "https://freesvg.org/img/1370962427.png",
  })
}

async function post(
  req: NextApiRequest,
  res: NextApiResponse<MakeTransactionOutputData | ErrorOutput>
) {
  try {
    // We pass the selected items in the query, calculate the expected cost
    const amount = calculatePrice(req.query)
    if (amount.toNumber() === 0) {
      res.status(400).json({ error: "Can't checkout with charge of 0" })
      return
    }

    // We pass the reference to use in the query
    const { reference } = req.query
    if (!reference) {
      res.status(400).json({ error: "No reference provided" })
      return
    }

    // We pass the buyer's public key in JSON body
    const { account } = req.body as MakeTransactionInputData
    if (!account) {
      res.status(40).json({ error: "No account provided" })
      return
    }
    const buyerPublicKey = new PublicKey(account)
    const shopPublicKey = shopAddress

    const network = WalletAdapterNetwork.Devnet
    const endpoint = clusterApiUrl(network)
    const connection = new Connection(endpoint)

    // Get details about the USDC token
    const usdcMint = await getMint(connection, usdcAddress)
    // Get the buyer's USDC token account address
    const buyerUsdcAddress = await getAssociatedTokenAddress(usdcAddress, buyerPublicKey)
    // Get the shop's USDC token account address
    const shopUsdcAddress = await getAssociatedTokenAddress(usdcAddress, shopPublicKey)

    // Get a recent blockhash to include in the transaction
    const { blockhash } = await (connection.getLatestBlockhash('finalized'))

    const transaction = new Transaction({
      recentBlockhash: blockhash,
      // The buyer pays the transaction fee
      feePayer: buyerPublicKey,
    })

    // Create the instruction to send USDC from the buyer to the shop
    const transferInstruction = createTransferCheckedInstruction(
      buyerUsdcAddress, // source
      usdcAddress, // mint (token address)
      shopUsdcAddress, // destination
      buyerPublicKey, // owner of source address
      amount.toNumber() * (10 ** usdcMint.decimals), // amount to transfer (in units of the USDC token)
      usdcMint.decimals, // decimals of the USDC token
    )

    // Add the reference to the instruction as a key
    // This will mean this transaction is returned when we query for the reference
    transferInstruction.keys.push({
      pubkey: new PublicKey(reference),
      isSigner: false,
      isWritable: false,
    })

    // Add the instruction to the transaction
    transaction.add(transferInstruction)

    // Serialize the transaction and convert to base64 to return it
    const serializedTransaction = transaction.serialize({
      // We will need the buyer to sign this transaction after it's returned to them
      requireAllSignatures: false
    })
    const base64 = serializedTransaction.toString('base64')

    // Insert into database: reference, amount

    // Return the serialized transaction
    res.status(200).json({
      transaction: base64,
      message: "Thanks for your order! 🍪",
    })
  } catch (err) {
    console.error(err);

    res.status(500).json({ error: 'error creating transaction', })
    return
  }
}

export default async function handler(
  req: NextApiRequest,
  res: NextApiResponse<MakeTransactionGetResponse | MakeTransactionOutputData | ErrorOutput>
) {
  if (req.method === "GET") {
    return get(res)
  } else if (req.method === "POST") {
    return await post(req, res)
  } else {
    return res.status(405).json({ error: "Method not allowed" })
  }
}
```
Everything that we had before is in the post function, and there’s a new get function that returns:
```
{
    "label": "Cookies Inc",
    "icon": "https://freesvg.org/img/1370962427.png"
}
```

My icon is just this nice lil cookie: https://freesvg.org/1370962427 - feel free to change it!

The handler function just checks the request method and calls either get or post. There’s nothing new in post so don’t worry about going through it here.

Nice! Now our API is fully compatible with the transaction requests specification. Before we make our transaction more powerful, let's get it working in our shop.

**Updating the QR code**
-----------------------

Currently our shop checkout page is displaying a QR code for a transfer request. We're going to update it to instead display a transaction request, pointing at our /api/makeTransaction API. Then when we add functionality to that API, it'll work for customers in our shop as well as online.

I'll show the updated file and then talk through the changes.
```
import { createQR, encodeURL, TransferRequestURLFields, findReference, validateTransfer, FindReferenceError, ValidateTransferError, TransactionRequestURLFields } from "@solana/pay";
import { WalletAdapterNetwork } from "@solana/wallet-adapter-base";
import { clusterApiUrl, Connection, Keypair } from "@solana/web3.js";
import { useRouter } from "next/router";
import { useEffect, useMemo, useRef } from "react";
import BackLink from "../../components/BackLink";
import PageHeading from "../../components/PageHeading";
import { shopAddress, usdcAddress } from "../../lib/addresses";
import calculatePrice from "../../lib/calculatePrice";

export default function Checkout() {
  const router = useRouter()

  // ref to a div where we'll show the QR code
  const qrRef = useRef<HTMLDivElement>(null)

  const amount = useMemo(() => calculatePrice(router.query), [router.query])

  // Unique address that we can listen for payments to
  const reference = useMemo(() => Keypair.generate().publicKey, [])

  // Read the URL query (which includes our chosen products)
  const searchParams = new URLSearchParams({ reference: reference.toString() });
  for (const [key, value] of Object.entries(router.query)) {
    if (value) {
      if (Array.isArray(value)) {
        for (const v of value) {
          searchParams.append(key, v);
        }
      } else {
        searchParams.append(key, value);
      }
    }
  }

  // Get a connection to Solana devnet
  const network = WalletAdapterNetwork.Devnet
  const endpoint = clusterApiUrl(network)
  const connection = new Connection(endpoint)

  // Show the QR code
  useEffect(() => {
    // window.location is only available in the browser, so create the URL in here
    const { location } = window
    const apiUrl = `${location.protocol}//${location.host}/api/makeTransaction?${searchParams.toString()}`
    const urlParams: TransactionRequestURLFields = {
      link: new URL(apiUrl),
      label: "Cookies Inc",
      message: "Thanks for your order! 🍪",
    }
    const solanaUrl = encodeURL(urlParams)
    const qr = createQR(solanaUrl, 512, 'transparent')
    if (qrRef.current && amount.isGreaterThan(0)) {
      qrRef.current.innerHTML = ''
      qr.append(qrRef.current)
    }
  })

  // Check every 0.5s if the transaction is completed
  useEffect(() => {
    const interval = setInterval(async () => {
      try {
        // Check if there is any transaction for the reference
        const signatureInfo = await findReference(connection, reference, { finality: 'confirmed' })
        // Validate that the transaction has the expected recipient, amount and SPL token
        await validateTransfer(
          connection,
          signatureInfo.signature,
          {
            recipient: shopAddress,
            amount,
            splToken: usdcAddress,
            reference,
          },
          { commitment: 'confirmed' }
        )
        router.push('/shop/confirmed')
      } catch (e) {
        if (e instanceof FindReferenceError) {
          // No transaction found yet, ignore this error
          return;
        }
        if (e instanceof ValidateTransferError) {
          // Transaction is invalid
          console.error('Transaction is invalid', e)
          return;
        }
        console.error('Unknown error', e)
      }
    }, 500)
    return () => {
      clearInterval(interval)
    }
  }, [])

  return (
    <div className="flex flex-col items-center gap-8">
      <BackLink href='/shop'>Cancel</BackLink>

      <PageHeading>Checkout ${amount.toString()}</PageHeading>

      {/* div added to display the QR code */}
      <div ref={qrRef} />
    </div>
  )
}
```

The first new piece of code is for converting the query params:
```
// Read the URL query (which includes our chosen products)
const searchParams = new URLSearchParams({ reference: reference.toString() });
for (const [key, value] of Object.entries(router.query)) {
  if (value) {
    if (Array.isArray(value)) {
      for (const v of value) {
        searchParams.append(key, v);
      }
    } else {
      searchParams.append(key, value);
    }
  }
}
```

We've seen this before on our pages/checkout.tsx for the online checkout. We're going to be calling the same API that that page uses, so it makes sense we'd want to do the same query param wrangling!

Next, we remove the code that generated TransferRequestURLFields - unsurprisingly we won't be using that any more.

The remaining changes are to the useEffect block that generates the QR code:
```
  // Show the QR code
  useEffect(() => {
    // window.location is only available in the browser, so create the URL in here
    const { location } = window
    const apiUrl = `${location.protocol}//${location.host}/api/makeTransaction?${searchParams.toString()}`
    const urlParams: TransactionRequestURLFields = {
      link: new URL(apiUrl),
      label: "Cookies Inc",
      message: "Thanks for your order! 🍪",
    }
    const solanaUrl = encodeURL(urlParams)
    const qr = createQR(solanaUrl, 512, 'transparent')
    if (qrRef.current && amount.isGreaterThan(0)) {
      qrRef.current.innerHTML = ''
      qr.append(qrRef.current)
    }
  })
```

This looks a bit different from what we used before. Previously we were generating the Solana URL outside of the useEffect and just creating the QR code inside it.

But now we need to build an absolute URL to our API, and then encode that in the solana:... URL. When we're running on localhost:3000 that API URL looks something like http://localhost:3000/api/makeTransaction?reference=abc&box-of-cookies=1

But when we deploy our app we'll want it to be something like https://awesome-cookies.com/api/makeTransaction?reference=abc&box-of-cookies=1

It changes depending on where our app is running!

In the browser, we can access parts of the current URL on the window.location object. Since this is only available in the browser we put it inside our useEffect hook, these always only run in the browser. As an example on the current page (feel free to try these in your console!), window.location.protocol will return https: and window.location.host will return www.pointer.gg. So between these and our searchParams we already defined, we can build an absolute URL to our API: ${location.protocol}//${location.host}/api/makeTransaction?${searchParams.toString()}

This becomes our link param in TransactionRequestURLFields , alongside our familiar label and message params. These are the parameters that will be encoded in our Solana Pay QR code.

The rest of the useEffect will be familiar, it's just taking the URL params and encoding them into the QR code and displaying it.

At this point if you try to make a purchase from your /shop page you'll see a QR code on the /checkout page just like before. But unfortunately it won't scan:
![32](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/09ed1466-dbec-4796-813b-86021a142bff)
The reason for this is that the API URL we've encoded is http://localhost:3000/... and for security Solana Pay requires https URLs. The common ways to run https locally are a bit fiddly here too because remember it's our phone that's making the request. The easiest way to get this working is using a tool called ngrok.

**Testing with ngrok**
-----------------------
Ngrok will provide us a HTTPS URL accessible from anywhere, that points at our localhost:3000 port. That'll make transaction requests super easy to test! If you've used ngrok before then feel free to skim over this setup.

Sign up at https://ngrok.com  and make sure you verify your email. This is required before we can serve our app.

Next visit https://ngrok.com/download and follow the instructions to install ngrok.

Once you have it installed, log in to ngrok.com and get your auth token. You should see something like this:
<img width="1174" alt="33" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/7fd6feb4-2ac5-444a-8400-6704ca9e12b9">
Run that command and you'll have ngrok configured and ready to go.

Now make sure your app is running npm run dev and then in another terminal run ngrok http 3000. This will spin up an ngrok URL pointing at your localhost:3000 You should see something like:
```
ngrok                                                                                                                                                                                      (Ctrl+C to quit)
                                                                                                                                                                                                           
Session Status                online                                                                                                                                                                       
Account                       Callum (Plan: Free)                                                                                                                                                          
Version                       3.0.3                                                                                                                                                                        
Region                        Europe (eu)                                                                                                                                                                  
Latency                       calculating...                                                                                                                                                               
Web Interface                 http://127.0.0.1:4040                                                                                                                                                        
Forwarding                    https://df59-2a02-c7f-ed73-c000-ec6d-25e6-eea2-965d.eu.ngrok.io -> http://localhost:3001                                                                                     
                                                                                                                                                                                                           
Connections                   ttl     opn     rt1     rt5     p50     p90                                                                                                                                  
                              0       0       0.00    0.00    0.00    0.00
```

That big Forwarding URL should now be serving your app! If you visit it you should see your store, and if you make updates locally you should see them reflected immediately. Now your app is running on a public https URL and transaction requests will work!

Head to your /shop page on the ngrok URL and now you should be able to scan the checkout QR code!

![34](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/4ba262b5-d7b1-4be8-8d4f-6e5ee2592c34)
And when you pay the UI will update, just like it did with the transfer request.

Now our app uses transaction requests to share the same transaction between online and in-shop payments. In the next lesson we're going to look at introducing a loyalty coupon to our store. We'll do this by updating /api/makeTransaction and now our enhancements there will apply wherever people are buying our cookies! All we have to do is update the transaction our API returns and the behaviour will update everywhere.

**Loyalty Scheme**
--------------------
Let’s say some other cookie shops are opening near our store. In addition to our superior cookies, we want to use a loyalty scheme to keep our customers coming back!

You’ve probably seen something like this before:
![35](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/66513034-f88d-4e54-a27a-4b01622bc754)
Each time you buy a coffee in some coffee shop you get a stamp, and when the card is full you get one free, or you get a discount.

We can use an SPL token to create something like this, where the current number of stamps is stored on the blockchain as the user’s balance for our token. That’ll let us have a digital loyalty card. I’m going to make mine give a 50% discount after collecting 5 coupons. But it’s totally up to you!

Using Solana transactions, we’ll be able to guarantee that everybody who buys our cookies gets a coupon with every purchase. And using that account input to our API, we’ll be able to check the current balance and automatically send a transaction where they can use their coupons and receive a discount if they have enough coupons. Users will never forget their coupon card!

**Creating a coupon**
---------------------

There’s a CLI that we can install to create tokens: https://spl.solana.com/token#reference-guide - you’re welcome to install this and use it if you’d like to. The Solana CLI is very powerful and definitely worth getting familiar with at some point. For this tutorial though we’re going to stay in Javascript and use functions from the @solana/spl-token library that we’ve already seen.

Create a new top-level directory (same level as eg pages/) called scripts/. In this directory first create a file package.json with the following content:
```
{
  "type": "module"
}
```

That’s just to make imports work in our script!

Next we need a couple of new dependencies. Make sure you run this at the top-level, not inside 
```
npm install bs58 dotenv
```

One more thing before we can write our code, we need our shop account private key. Create a new file .env with the content:
```
SHOP_PRIVATE_KEY=thePrivateKey
```

```
Never check in a file with a private key or share it with anybody. Anyone with your private key can steal everything from your wallet.
```

Remember that you can export the private key from Phantom. With the shop account selected, go to settings and then click Export Private Key. You’ll need your Phantom password!

Now we can write the script to create our coupon. Create a new file scripts/create-coupon.js with the following content:
```
import { createAssociatedTokenAccount, createMint, getAccount, mintToChecked } from '@solana/spl-token'
import { WalletAdapterNetwork } from '@solana/wallet-adapter-base'
import { clusterApiUrl, Connection, Keypair } from '@solana/web3.js'
import base58 from 'bs58'

// Read .env into process.env
import 'dotenv/config'

// Initialise Solana connection
const network = WalletAdapterNetwork.Devnet
const endpoint = clusterApiUrl(network)
const connection = new Connection(endpoint)

// Initialise shop account
const shopPrivateKey = process.env.SHOP_PRIVATE_KEY
if (!shopPrivateKey) {
  throw new Error('SHOP_PRIVATE_KEY not set')
}
const shopAccount = Keypair.fromSecretKey(base58.decode(shopPrivateKey))

// Create the token, returns the token public key
console.log("Creating token...")
const myCouponAddress = await createMint(
  connection,
  shopAccount, // payer
  shopAccount.publicKey, // who has permission to mint?
  shopAccount.publicKey, // who has permission to freeze?
  0 // decimals (0 = whole numbers)
)
console.log("Token created:", myCouponAddress.toString())

// Create the associated token account for the shop
console.log("Creating token account for the shop...")
const shopCouponAddress = await createAssociatedTokenAccount(
  connection,
  shopAccount, // payer
  myCouponAddress, // token
  shopAccount.publicKey, // who to create an account for
)
console.log("Token account created:", shopCouponAddress.toString())

// Mint 1 million coupons to the shop account
console.log("Minting 1 million coupons to the shop account...")
await mintToChecked(
  connection,
  shopAccount, // payer
  myCouponAddress, // token
  shopCouponAddress, // recipient
  shopAccount, // authority to mint
  1_000_000, // amount
  0, //decimals
)
console.log("Minted 1 million coupons to the shop account")

const { amount } = await getAccount(connection, shopCouponAddress)
console.log({
  myCouponAddress: myCouponAddress.toString(),
  balance: amount.toLocaleString(),
})
```

Hopefully, this is reasonably straightforward! We create a token, then we create a token account for that token that belongs to the shop, and then we put 1 million coupons into that token account. The parameters for these functions can be a bit confusing because we end up with so many objects of similar types. These functions can be a bit slow too, so I’ve added plenty of logging so we can see its progress.

One thing to highlight here is this line of code:
```
const shopAccount = Keypair.fromSecretKey(base58.decode(shopPrivateKey))
```
We’re loading the Solana account from the private key we’ve exported from Phantom. This will allow us to use it as a payer (it creates the token) and as a signer/authority (it grants permission to mint the token).

If you run this script you should see something like this:
```
$ node scripts/create-coupon.js
Creating token...
Token created: 74aFyMgbKppdab4wEVz5AXL3UGbxMkwkwgK2LVzn3MmG
Creating token account for the shop...
Token account created: F7UTRfFp2oFQMzk797yUuZCqrPFQxXpHkPtKo4CyiFov
Minting 1 million coupons to the shop account...
Minted 1 million coupons to the shop account
{
  myCouponAddress: '74aFyMgbKppdab4wEVz5AXL3UGbxMkwkwgK2LVzn3MmG',
  balance: '1,000,000'
}
```
That’s pretty magical, you just created your own trade-able token on the Solana blockchain. It belongs to your shop account. Only you can mint them, but we’ll soon see how anyone can hold and trade your token.

Before continuing it’s worth sanity checking that token. If you go to solscan.io/?cluster=devnet and enter the myCouponAddress address in the search, you should get something like this:
![36](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/1f2fef5a-e682-41fc-89ad-7ce41454feec)
You should see a total supply of 1 million (or however many you minted!), and the Authority (on the right) should be the public key of your shop account. Here I’m in the Holders tab which is the only one with anything interesting right now. You should see a single Address with the Owner also being the public key of your shop account, and the Quantity should be however many you minted (in my case 1 million). If you see all that and everything matches then your token is on the Solana blockchain and good to go!

You should also be able to see the token in Phantom, under the Shop account:
<img width="364" alt="37" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/5e41a2ea-2eec-4f8a-9346-8d59da4ce047">

```
You might find it a bit odd that we don’t have any metadata associated with our token, like a name or logo. This metadata is primarily stored in this Github repo:  which most wallets will read to get information about tokens. That’s where our USDC-Dev metadata is! There’s no need to add your coupon for this tutorial and we don’t need to spam them, but if you were shipping this for real then you could :)
```

**Displaying the user’s coupon balance**
------------------------------------

Let’s get our coupon onto our site!

Since I’m going to give a discount after 5 purchases, I’m going to show a ‘coupon book’ on the site with up to 5 stamps, and after that 6th transaction where they use the discount, it’ll be cleared.

We’ll need the token address so that we can query it. This is the one labeled myCouponAddress in the output from our script and should show as Token (not Token Account) in solscan. Update lib/addresses.ts:

```
import { PublicKey } from "@solana/web3.js"

// This is your shop address
export const shopAddress = new PublicKey('EXWr1Go8UyfA39U1dfRkcH8uUvqunbRhQEUQNm36UsyQ')
// This is the same for everyone
export const usdcAddress = new PublicKey('Gh9ZwEmdLJ8DscKNTkTqPbNwLNNBjuSzaG9Vp2KGtKJr')
// This is your token/coupon address
export const couponAddress = new PublicKey('74aFyMgbKppdab4wEVz5AXL3UGbxMkwkwgK2LVzn3MmG')
```
Create a new file components/CouponBook.tsx:
```
import { getAssociatedTokenAddress, getAccount, TokenAccountNotFoundError } from "@solana/spl-token"
import { useConnection, useWallet } from "@solana/wallet-adapter-react"
import { useState, useEffect } from "react"
import { couponAddress } from "../lib/addresses"

export default function CouponBook() {
  const { connection } = useConnection()
  const { publicKey } = useWallet()
  const [couponBalance, setCouponBalance] = useState(0)


  async function getCouponBalance() {
    if (!publicKey) {
      setCouponBalance(0)
      return
    }

    try {
      const userCouponAddress = await getAssociatedTokenAddress(couponAddress, publicKey)
      const userCouponAccount = await getAccount(connection, userCouponAddress)
      const coupons = userCouponAccount.amount > 5 ? 5 : Number(userCouponAccount.amount)

      console.log("balance is", coupons)
      setCouponBalance(coupons)
    } catch (e) {
      if (e instanceof TokenAccountNotFoundError) {
        // This is ok, the API will create one when they make a payment
        console.log(`User ${publicKey} doesn't have a coupon account yet!`)
        setCouponBalance(0)
      } else {
        console.error('Error getting coupon balance', e)
      }
    }
  }

  useEffect(() => {
    getCouponBalance()
  }, [publicKey])

  const notCollected = 5 - couponBalance

  return (
    <>
      <div className="flex flex-col bg-gray-900 text-white rounded-md p-1 items-center">
        <p>Collect 5 cookies to receive a 50% discount on your next purchase!</p>

        <p className="flex flex-row gap-1 place-self-center">
          {[...Array(couponBalance)].map((_, i) => <span key={i}>🍪</span>)}
          {[...Array(notCollected)].map((_, i) => <span key={i}>⚪</span>)}
        </p>
      </div>
    </>
  )
}
```
This fetches the account belonging to the connected user for our coupon. They might not have one yet, if they haven’t received any coupons. In that case we set their balance to 0. If they do have one then we can get its balance and display it.

That weird render code at the bottom is just showing the balance and total length as a number of emojis.

So if the balance is 3 then we show 🍪🍪🍪⚪⚪  Fancy!

Let’s add that to our home page! Update pages/index.tsx:
```
import { useWallet } from '@solana/wallet-adapter-react'
import { WalletMultiButton } from '@solana/wallet-adapter-react-ui'
import CouponBook from '../components/CouponBook'
import Products from '../components/Products'
import SiteHeading from '../components/SiteHeading'

export default function HomePage() {
  // We get the public key of the connected wallet, if there is one
  const { publicKey } = useWallet()

  return (
    <div className="flex flex-col gap-8 max-w-4xl items-stretch m-auto pt-24">
      <SiteHeading>Cookies Inc</SiteHeading>

      {/* We add the Solana wallet connect button */}
      <div className="basis-1/4">
        <WalletMultiButton className='!bg-gray-900 hover:scale-105' />
      </div>

      {/* We display the coupon book if there's a connected wallet */}
      {publicKey && <CouponBook />}

      {/* We disable checking out without a connected wallet */}
      {/* Also the submitTarget is /buy/transaction instead of /checkout */}
      <Products submitTarget='/checkout' enabled={publicKey !== null} />
    </div>
  )
}
```
The only new thing here is {publicKey && <CouponBook />} (and the import).

Now if you visit your home page and connect your wallet (make sure you switch back to the buyer one), you should see something like:
![38](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/750782a6-9bbe-471f-86fe-034c6eeef53f)
The coupon balance will show as 0, because the buyer wallet doesn’t have a token account yet. There’s only one Holder of our coupon ATM, and it’s the shop. Let’s look at how we can send a coupon to our buyer!

**Sending a coupon to the buyer**
---------------------------------

We need to update our pages/api/makeTransaction.ts to create a transaction that, in addition to sending USDC from the buyer to our shop, sends a coupon from the shop to the buyer. I’ll show you the new code and then I’ll talk through what’s changed:
```
import { createTransferCheckedInstruction, getAssociatedTokenAddress, getMint, getOrCreateAssociatedTokenAccount } from "@solana/spl-token"
import { WalletAdapterNetwork } from "@solana/wallet-adapter-base"
import { clusterApiUrl, Connection, Keypair, PublicKey, Transaction } from "@solana/web3.js"
import { NextApiRequest, NextApiResponse } from "next"
import { couponAddress, usdcAddress } from "../../lib/addresses"
import calculatePrice from "../../lib/calculatePrice"
import base58 from 'bs58'

export type MakeTransactionInputData = {
  account: string,
}

type MakeTransactionGetResponse = {
  label: string,
  icon: string,
}

export type MakeTransactionOutputData = {
  transaction: string,
  message: string,
}

type ErrorOutput = {
  error: string
}

function get(res: NextApiResponse<MakeTransactionGetResponse>) {
  res.status(200).json({
    label: "Cookies Inc",
    icon: "https://freesvg.org/img/1370962427.png",
  })
}

async function post(
  req: NextApiRequest,
  res: NextApiResponse<MakeTransactionOutputData | ErrorOutput>
) {
  try {
    // We pass the selected items in the query, calculate the expected cost
    const amount = calculatePrice(req.query)
    if (amount.toNumber() === 0) {
      res.status(400).json({ error: "Can't checkout with charge of 0" })
      return
    }

    // We pass the reference to use in the query
    const { reference } = req.query
    if (!reference) {
      res.status(400).json({ error: "No reference provided" })
      return
    }

    // We pass the buyer's public key in JSON body
    const { account } = req.body as MakeTransactionInputData
    if (!account) {
      res.status(40).json({ error: "No account provided" })
      return
    }

    // We get the shop private key from .env - this is the same as in our script
    const shopPrivateKey = process.env.SHOP_PRIVATE_KEY as string
    if (!shopPrivateKey) {
      res.status(500).json({ error: "Shop private key not available" })
    }
    const shopKeypair = Keypair.fromSecretKey(base58.decode(shopPrivateKey))

    const buyerPublicKey = new PublicKey(account)
    const shopPublicKey = shopKeypair.publicKey

    const network = WalletAdapterNetwork.Devnet
    const endpoint = clusterApiUrl(network)
    const connection = new Connection(endpoint)

    // Get the buyer and seller coupon token accounts
    // Buyer one may not exist, so we create it (which costs SOL) as the shop account if it doesn't 
    const buyerCouponAddress = await getOrCreateAssociatedTokenAccount(
      connection,
      shopKeypair, // shop pays the fee to create it
      couponAddress, // which token the account is for
      buyerPublicKey, // who the token account belongs to (the buyer)
    ).then(account => account.address)

    const shopCouponAddress = await getAssociatedTokenAddress(couponAddress, shopPublicKey)

    // Get details about the USDC token
    const usdcMint = await getMint(connection, usdcAddress)
    // Get the buyer's USDC token account address
    const buyerUsdcAddress = await getAssociatedTokenAddress(usdcAddress, buyerPublicKey)
    // Get the shop's USDC token account address
    const shopUsdcAddress = await getAssociatedTokenAddress(usdcAddress, shopPublicKey)

    // Get a recent blockhash to include in the transaction
    const { blockhash } = await (connection.getLatestBlockhash('finalized'))

    const transaction = new Transaction({
      recentBlockhash: blockhash,
      // The buyer pays the transaction fee
      feePayer: buyerPublicKey,
    })

    // Create the instruction to send USDC from the buyer to the shop
    const transferInstruction = createTransferCheckedInstruction(
      buyerUsdcAddress, // source
      usdcAddress, // mint (token address)
      shopUsdcAddress, // destination
      buyerPublicKey, // owner of source address
      amount.toNumber() * (10 ** usdcMint.decimals), // amount to transfer (in units of the USDC token)
      usdcMint.decimals, // decimals of the USDC token
    )

    // Add the reference to the instruction as a key
    // This will mean this transaction is returned when we query for the reference
    transferInstruction.keys.push({
      pubkey: new PublicKey(reference),
      isSigner: false,
      isWritable: false,
    })

    // Create the instruction to send the coupon from the shop to the buyer
    const couponInstruction = createTransferCheckedInstruction(
      shopCouponAddress, // source account (coupon)
      couponAddress, // token address (coupon)
      buyerCouponAddress, // destination account (coupon)
      shopPublicKey, // owner of source account
      1, // amount to transfer
      0, // decimals of the token - we know this is 0
    )

    // Add both instructions to the transaction
    transaction.add(transferInstruction, couponInstruction)

    // Sign the transaction as the shop, which is required to transfer the coupon
    // We must partial sign because the transfer instruction still requires the user
    transaction.partialSign(shopKeypair)

    // Serialize the transaction and convert to base64 to return it
    const serializedTransaction = transaction.serialize({
      // We will need the buyer to sign this transaction after it's returned to them
      requireAllSignatures: false
    })
    const base64 = serializedTransaction.toString('base64')

    // Insert into database: reference, amount

    // Return the serialized transaction
    res.status(200).json({
      transaction: base64,
      message: "Thanks for your order! 🍪",
    })
  } catch (err) {
    console.error(err);

    res.status(500).json({ error: 'error creating transaction', })
    return
  }
}

export default async function handler(
  req: NextApiRequest,
  res: NextApiResponse<MakeTransactionGetResponse | MakeTransactionOutputData | ErrorOutput>
) {
  if (req.method === "GET") {
    return get(res)
  } else if (req.method === "POST") {
    return await post(req, res)
  } else {
    return res.status(405).json({ error: "Method not allowed" })
  }
}
```
```
You might get a Typescript error from the bs58 import. You can fix it with npm install --save-dev @types/bs58. We didn’t see that before because we used Javascript not Typescript for the create-coupon script.
```

All the new stuff is in the post function. The first new thing is here:
```
// We get the shop private key from .env - this is the same as in our script
const shopPrivateKey = process.env.SHOP_PRIVATE_KEY as string
if (!shopPrivateKey) {
  res.status(500).json({ error: "Shop private key not available" })
}
const shopKeypair = Keypair.fromSecretKey(base58.decode(shopPrivateKey))
```
This should look familiar because we used it in the script where we created the token! Since we’re going to be sending a coupon from the shop account, we’re going to need to sign the transaction as the shop. So we use the shop’s private key (which we have in .env from the script), and load the shop account from it just like we did in the script.

```
If you haven't restarted the Next app for a while, now is a good time to! It doesn't automatically pick up changes to .env so without a restart it won't be able to read that private key.
```
Next new thing:
```
// Get the buyer and seller coupon token accounts
// Buyer one may not exist, so we create it (which costs SOL) as the shop account if it doesn't 
const buyerCouponAddress = await getOrCreateAssociatedTokenAccount(
  connection,
  shopKeypair, // shop pays the fee to create it
  couponAddress, // which token the account is for
  buyerPublicKey, // who the token account belongs to (the buyer)
).then(account => account.address)
const shopCouponAddress = await getAssociatedTokenAddress(couponAddress, shopPublicKey)
```

This is similar to how we got the USDC accounts for the buyer and seller, but in this case we need to account for the buyer not having a coupon account yet! We use getOrCreateAssociatedTokenAccount with the shop keypair (from the code snippet just above) acting as the payer. So in our API if the user doesn’t have a coupon account yet, the shop pays to create one for them before creating the transaction.

Next new thing:
```
// Create the instruction to send the coupon from the shop to the buyer
const couponInstruction = createTransferCheckedInstruction(
  shopCouponAddress, // source account (coupon)
  couponAddress, // token address (coupon)
  buyerCouponAddress, // destination account (coupon)
  shopPublicKey, // owner of source account
  1, // amount to transfer
  0, // decimals of the token - we know this is 0
)

// Add both instructions to the transaction
transaction.add(transferInstruction, couponInstruction)
```
This is very similar to the instruction we use to send USDC from the buyer to the shop, but it sends exactly 1 coupon from the shop to the buyer. We add both instructions to the transaction.

And finally:
```
// Sign the transaction as the shop, which is required to transfer the coupon
// We must partial sign because the transfer instruction still requires the user
transaction.partialSign(shopKeypair)
```

Since the shop is now sending a token to the user, it must sign this transaction for it to be allowed to take place. As the comment says, this is only a partial sign because the user will still need to sign it afterward!

So now our API is producing a transaction where the buyer sends us USDC and we send a coupon back. It’s signed by our shop, which actually gives us some nice extra protection. Nobody can modify this transaction without invalidating the shop’s signature, and if they do that then the transaction can’t be processed. So when we’re reviewing the e-commerce transactions we don’t need to go checking the transaction details anymore, we just need to check we’ve signed it!

**Receiving Coupons**
-----------------------

If you make a purchase from your home page now then the transaction sent to your wallet should look something like this:

![39](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/fe7a7958-389d-47d9-ad45-605b3f7a2aed)
There’s the USDC-Dev payment, and the +1 by the coupon - showing that the buyer will receive a coupon as a result of this transaction.

And after that transaction on the home page you should immediately see that your coupon balance has been updated:

![40](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/9aea1ffa-37c7-4c9f-a9fa-e6cdb4d94611)
So at this point, we’ve got a transaction where whenever someone buys cookies off us they get a coupon sent to them. But we don’t yet have any way to use that coupon to get the 50% off that we promise! For that, we need to update our transaction API once more!

Coupon Discount

To handle the discount we need to check the user’s coupon balance in our API, and then adjust the transaction that we create for them based on it.

You might like to try working out how to update the transaction yourself before you read on to see how I did it. Hint: getOrCreateAssociatedTokenAccount returns an Account object including an amount field.

Again I’ll show the new code in full and then talk through what’s changed:
```
import { createTransferCheckedInstruction, getAssociatedTokenAddress, getMint, getOrCreateAssociatedTokenAccount } from "@solana/spl-token"
import { WalletAdapterNetwork } from "@solana/wallet-adapter-base"
import { clusterApiUrl, Connection, Keypair, PublicKey, Transaction } from "@solana/web3.js"
import { NextApiRequest, NextApiResponse } from "next"
import { couponAddress, shopAddress, usdcAddress } from "../../lib/addresses"
import calculatePrice from "../../lib/calculatePrice"
import base58 from 'bs58'

export type MakeTransactionInputData = {
  account: string,
}

type MakeTransactionGetResponse = {
  label: string,
  icon: string,
}

export type MakeTransactionOutputData = {
  transaction: string,
  message: string,
}

type ErrorOutput = {
  error: string
}

function get(res: NextApiResponse<MakeTransactionGetResponse>) {
  res.status(200).json({
    label: "Cookies Inc",
    icon: "https://freesvg.org/img/1370962427.png",
  })
}

async function post(
  req: NextApiRequest,
  res: NextApiResponse<MakeTransactionOutputData | ErrorOutput>
) {
  try {
    // We pass the selected items in the query, calculate the expected cost
    const amount = calculatePrice(req.query)
    if (amount.toNumber() === 0) {
      res.status(400).json({ error: "Can't checkout with charge of 0" })
      return
    }

    // We pass the reference to use in the query
    const { reference } = req.query
    if (!reference) {
      res.status(400).json({ error: "No reference provided" })
      return
    }

    // We pass the buyer's public key in JSON body
    const { account } = req.body as MakeTransactionInputData
    if (!account) {
      res.status(40).json({ error: "No account provided" })
      return
    }

    // We get the shop private key from .env - this is the same as in our script
    const shopPrivateKey = process.env.SHOP_PRIVATE_KEY as string
    if (!shopPrivateKey) {
      res.status(500).json({ error: "Shop private key not available" })
    }
    const shopKeypair = Keypair.fromSecretKey(base58.decode(shopPrivateKey))

    const buyerPublicKey = new PublicKey(account)
    const shopPublicKey = shopKeypair.publicKey

    const network = WalletAdapterNetwork.Devnet
    const endpoint = clusterApiUrl(network)
    const connection = new Connection(endpoint)

    // Get the buyer and seller coupon token accounts
    // Buyer one may not exist, so we create it (which costs SOL) as the shop account if it doesn't 
    const buyerCouponAccount = await getOrCreateAssociatedTokenAccount(
      connection,
      shopKeypair, // shop pays the fee to create it
      couponAddress, // which token the account is for
      buyerPublicKey, // who the token account belongs to (the buyer)
    )

    const shopCouponAddress = await getAssociatedTokenAddress(couponAddress, shopPublicKey)

    // If the buyer has at least 5 coupons, they can use them and get a discount
    const buyerGetsCouponDiscount = buyerCouponAccount.amount >= 5

    // Get details about the USDC token
    const usdcMint = await getMint(connection, usdcAddress)
    // Get the buyer's USDC token account address
    const buyerUsdcAddress = await getAssociatedTokenAddress(usdcAddress, buyerPublicKey)
    // Get the shop's USDC token account address
    const shopUsdcAddress = await getAssociatedTokenAddress(usdcAddress, shopPublicKey)

    // Get a recent blockhash to include in the transaction
    const { blockhash } = await (connection.getLatestBlockhash('finalized'))

    const transaction = new Transaction({
      recentBlockhash: blockhash,
      // The buyer pays the transaction fee
      feePayer: buyerPublicKey,
    })

    // If the buyer has the coupon discount, divide the amount in USDC by 2
    const amountToPay = buyerGetsCouponDiscount ? amount.dividedBy(2) : amount

    // Create the instruction to send USDC from the buyer to the shop
    const transferInstruction = createTransferCheckedInstruction(
      buyerUsdcAddress, // source
      usdcAddress, // mint (token address)
      shopUsdcAddress, // destination
      buyerPublicKey, // owner of source address
      amountToPay.toNumber() * (10 ** usdcMint.decimals), // amount to transfer (in units of the USDC token)
      usdcMint.decimals, // decimals of the USDC token
    )

    // Add the reference to the instruction as a key
    // This will mean this transaction is returned when we query for the reference
    transferInstruction.keys.push({
      pubkey: new PublicKey(reference),
      isSigner: false,
      isWritable: false,
    })

    // Create the instruction to send the coupon from the shop to the buyer
    const couponInstruction = buyerGetsCouponDiscount ?
      // The coupon instruction is to send 5 coupons from the buyer to the shop
      createTransferCheckedInstruction(
        buyerCouponAccount.address, // source account (coupons)
        couponAddress, // token address (coupons)
        shopCouponAddress, // destination account (coupons)
        buyerPublicKey, // owner of source account
        5, // amount to transfer
        0, // decimals of the token - we know this is 0
      ) :
      // The coupon instruction is to send 1 coupon from the shop to the buyer
      createTransferCheckedInstruction(
        shopCouponAddress, // source account (coupon)
        couponAddress, // token address (coupon)
        buyerCouponAccount.address, // destination account (coupon)
        shopPublicKey, // owner of source account
        1, // amount to transfer
        0, // decimals of the token - we know this is 0
      )

    // Add the shop as a signer to the coupon instruction
    // If the shop is sending a coupon, it already will be a signer
    // But if the buyer is sending the coupons, the shop won't be a signer automatically
    // It's useful security to have the shop sign the transaction
    couponInstruction.keys.push({
      pubkey: shopPublicKey,
      isSigner: true,
      isWritable: false,
    })

    // Add both instructions to the transaction
    transaction.add(transferInstruction, couponInstruction)

    // Sign the transaction as the shop, which is required to transfer the coupon
    // We must partial sign because the transfer instruction still requires the user
    transaction.partialSign(shopKeypair)

    // Serialize the transaction and convert to base64 to return it
    const serializedTransaction = transaction.serialize({
      // We will need the buyer to sign this transaction after it's returned to them
      requireAllSignatures: false
    })
    const base64 = serializedTransaction.toString('base64')

    // Insert into database: reference, amount

    const message = buyerGetsCouponDiscount ? "50% Discount! 🍪" : "Thanks for your order! 🍪"

    // Return the serialized transaction
    res.status(200).json({
      transaction: base64,
      message,
    })
  } catch (err) {
    console.error(err);

    res.status(500).json({ error: 'error creating transaction', })
    return
  }
}

export default async function handler(
  req: NextApiRequest,
  res: NextApiResponse<MakeTransactionGetResponse | MakeTransactionOutputData | ErrorOutput>
) {
  if (req.method === "GET") {
    return get(res)
  } else if (req.method === "POST") {
    return await post(req, res)
  } else {
    return res.status(405).json({ error: "Method not allowed" })
  }
}
```
Again all the changes are in post.

That’s a lot of code, but here’s what’s new:
```
// Get the buyer and seller coupon token accounts
// Buyer one may not exist, so we create it (which costs SOL) as the shop account if it doesn't 
const buyerCouponAccount = await getOrCreateAssociatedTokenAccount(
  connection,
  shopKeypair, // shop pays the fee to create it
  couponAddress, // which token the account is for
  buyerPublicKey, // who the token account belongs to (the buyer)
)
const shopCouponddress = await getAssociatedTokenAddress(couponAddress, shopPublicKey)

// If the buyer has at least 5 coupons, they can use them and get a discount
const buyerGetsCouponDiscount = buyerCouponAccount.amount >= 5
```

When we call getOrCreateAssociatedTokenAccount the return is actually an Account object. Previously we only needed the address, but now we also need to check the amount so we keep it in this form. We have a new variable buyerGetsCouponDiscount that we’ll use whenever we need to change the behavior of our transaction.

Here’s the next change:
```
// If the buyer has the coupon discount, divide the amount in USDC by 2
const amountToPay = buyerGetsCouponDiscount ? amount.dividedBy(2) : amount

// Create the instruction to send USDC from the buyer to the shop
const transferInstruction = createTransferCheckedInstruction(
  buyerUsdcAccount, // source account (USDC)
  usdcAddress, // token address (USDC)
  shopUsdcAccount, // destination account (USDC)
  buyerPublicKey, // owner of source account
  amountToPay.toNumber() * (10 ** usdcMint.decimals), // amount to transfer (in units of the token)
  usdcMint.decimals, // decimals of the token
)
```
The amount we charge the user in the transferInstruction is now based on buyerGetsCouponDiscount - if they have the coupon discount then we charge them half as much.

The next change is to couponInstruction:
```
const couponInstruction = buyerGetsCouponDiscount ?
  // The coupon instruction is to send 5 coupons from the buyer to the shop
  createTransferCheckedInstruction(
    buyerCouponAccount.address, // source account (coupons)
    couponAddress, // token address (coupons)
    shopCouponAddress, // destination account (coupons)
    buyerPublicKey, // owner of source account
    5, // amount to transfer
    0, // decimals of the token - we know this is 0
  ) :
  // The coupon instruction is to send 1 coupon from the shop to the buyer
  createTransferCheckedInstruction(
    shopCouponAddress, // source account (coupon)
    couponAddress, // token address (coupon)
    buyerCouponAccount.address, // destination account (coupon)
    shopPublicKey, // owner of source account
    1, // amount to transfer
    0, // decimals of the token - we know this is 0
  )
```
The change in this instruction is a lot more significant. If we’re applying the coupon discount then the direction of the coupon exchange swaps - the buyer must send us 5 coupons in exchange for the discount. If they don’t yet have enough coupons for the discount then the shop continues to send them a single coupon with each transaction.

Next new thing:

```
// Add the shop as a signer to the coupon instruction
// If the shop is sending a coupon, it already will be a signer
// But if the buyer is sending the coupons, the shop won't be a signer automatically
// It's useful security to have the shop sign the transaction
couponInstruction.keys.push({
  pubkey: shopPublicKey,
  isSigner: true,
  isWritable: false,
})
```
Earlier we discussed how having the shop sign transactions gives us a nice way to verify each transaction is as we expected because it stops anybody from changing it. If a transaction has our signature then we know we created it with our API. But our shop was only a required signer because of the coupon instruction where it sent a coupon to the buyer. It’s no longer a required signer in the case where the buyer is sending the coupons and receiving the discount because the shop isn’t sending anything to the buyer in that transaction. In this code, we add our shop as a signer on the coupon instruction. So whichever instruction we end up using, the transaction can only be made with the shop’s signature.

Last but not least:
```
const message = buyerGetsCouponDiscount ? "50% Discount! 🍪" : "Thanks for your order! 🍪"

// Return the serialized transaction
res.status(200).json({
  transaction: base64,
  message,
})
```
Remember that we display the message on the transaction page when we ask the buyer to approve the transaction. It’s nice to let them know about a discount! With transaction requests, the wallet should display this message to the user too!

Now if the buyer has less than the full 5 coupons then they should get the same transaction we saw before - they buy the cookies and receive a coupon. But if they have 5 coupons then they should get a transaction with a 50% discount in exchange for their 5 coupons:
<img width="1039" alt="41" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/bae17f47-7f6e-43d7-8e21-19deaa4fb54f">
We now have a complete automated loyalty scheme built on Solana! We send a coupon with each purchase of our cookies and automatically provide the discount to any buyer who is eligible. Our site displays their coupon balance, and any Solana wallet can too. Nobody’s going to choose any of those lame other cookie shops now!

**Back to mobile**
-------------------

What about in-shop payments? They use this API so they automatically work exactly the same. Wherever people buy our cookies they receive our loyalty coupon and they get the automatic discount. You'll just need to run ngrok http 3000 and use that URL like before. Here's a lil demo where we get the 50% discount by scanning a QR code:


![tutorial_SnDFh3py-QYH00TloFABN](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/53cf0f19-a7a7-423f-88e4-e6af50388378)

**🎉 Wrapping Up**
------------------
Table of Contents
We’ve covered a lot of ground in this tutorial, and I hope you’re hyped about Solana after this whirlwind tour! Its speed really is a game-changer, and Solana Pay is a super exciting example of what it enables.



If you’d like to deploy your store to share it, Vercel is probably the easiest option! If you prefer deploying your NextJS apps somewhere else then feel free to! There aren’t any limitations on where you can deploy this. The only thing to note is that you’ll need to set the SHOP_PRIVATE_KEY environment variable.
Next steps

Take what you learned and go build something on your own! Remix this project or build a fresh idea.

Looking for work opportunities on Solana? 

Here are a few good places to get started: 

SuperteamDAO - A community that helps Solana projects launch and grow in ascending markets. This is a link to their talent network :) Make sure you say we sent you!

Solana Job Board - Official Solana Jobs board

Until next time ✌️

