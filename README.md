 #Solana Pay Marketplace Uygulaması 
 -------------------------------------

Sizlere Solana Pay kullanarak Solana'daki ödemelerle ilgili kapsamlı bir kılavuz hazırladım.Bugün Javascript kullanarak Marketplace uygulaması inşa edeceğiz.Ardından Solana Pay'in bütün nimetlerinden faydalanarak gerçek hayatta kripto ile ödeme almanın ve işlem yapmanın tadını çıkaracağız. :D
Size Solana'daki ödemelerle ilgili bu kapsamlı kılavuzu sunmaktan heyecan duyuyoruz.
Başlayalım! 👋

UYGULAMANIN AMACI :
----------------------
Gerçek hayatta müşterilerden ödemeleri kabul etmemizi sağlayan bir satış noktası web uygulaması oluşturacağız. Müşterilere tarama yapabilecekleri bir Solana cüzdanıyla ödeme yapmalarını sağlayan bir QR kodu sunacağız. Ödemeyi yaptıklarında uygulamamız güncellenecek ve ödemelerini gösterecektir. Gerçekten büyüleyici bir deneyim ve nasıl çalıştığını gördüğünüzde ne kadar kolay olduğunu anlayacaksınız!

Ayrıca Solana'da çevrimiçi ödemeleri inceleyecek ve bir sadakat kartı sistemi oluşturacağız. Kullanıcılara her 5. satın alımda %50 indirim gibi içerikler üretebilirsiniz. Aslında istediğiniz herhangi bir şeyi yapabilirsiniz, çok esnek bir sistem. Son olarak, tüm bunları bir araya getiren gerçekten harika bir gelecek olan Solana Pay'in bazı cool özelliklerinede bir göz atacağız!

![1](https://github.com/Yusufcihan1/Solana-Pay-Marketplace-Uygulamasi/assets/50721899/a1bf785c-2d65-4823-9e32-d612e0af2a5a)
------------------------------------------------------------------------------------------------------------------------------
![2](https://github.com/Yusufcihan1/Solana-Pay-Marketplace-Uygulamasi/assets/50721899/192f40b9-b97b-4bfa-8ad8-33ac8593b0ba)
------------------------------------------------------------------------------------------------------------------------------
![3](https://github.com/Yusufcihan1/Solana-Pay-Marketplace-Uygulamasi/assets/50721899/b73ce982-6fe3-4391-9a38-30644b68dfc9)
------------------------------------------------------------------------------------------------------------------------------

Uygulamanın demo halini https://sol-music-shop-v8bx-5p1q2u2zc-yusufcihan1.vercel.app/ adresinden inceleyebilirsiniz.

NEDEN SOLANA'DA iNŞA EDİYORUZ ? 
---------------------------------------
Öncelikle, Solana nedir? Solana, geliştiricilerin muhteşem uygulamalar oluşturabilecekleri bir blok zinciridir! Ödeme kullanım senaryosu için mükemmel kılan iki ana özelliği vardır:
Son derece hızlıdır. Bir mağazada kartla ödeme yapmak kadar hızlıdır. Daha önce başka blok zincirleri kullandıysanız ve işlemlerin gerçekleşmesini 10 saniye gibi bir süre beklediyseniz, Solana'da bunu unutabilirsiniz.
Ücretler çok düşüktür. Birkaç kuruşluk miktarlardadır. Daha önce bir NFT veya benzer bir şey satın aldığınızda 50 dolarlık işlem ücreti ödediyseniz, Solana'da bunu da unutabilirsiniz.
Burası, büyükannenizin blok zinciri değil!
İşte size bazı istatistikler : 
![image](https://github.com/Yusufcihan1/Solana-Pay-Marketplace-Uygulamasi/assets/50721899/e863db97-4aaf-47f6-80dd-3fbeb17c162a)

-Ağ şu anda saniyede 2.070 işlemi yönetiyor.
-Ortalama işlem başına maliyet 0.00025 dolar.
-Ağ şu ana kadar neredeyse 62,3 milyar işlem gerçekleştirdi. Bu metni okuduğunuzda, yüz milyonlarca daha fazla işlemin gerçekleşmiş olması muhtemeldir.

Peki,SOLANA PAY NEDİR ? 
Solana Pay, Solana üzerinde ödemeler için bir spesifikasyondur. Bir ödeme talebini URL olarak kodlamak için bir yol tanımlar ve kullanıcılara gösterilebilir ( örneğin bir QR kodu olarak). Solana mobil cüzdanlar, bu QR kodunu sorunsuz bir şekilde tarayarak ödeme yapmayı destekliyor.
Kısacası, Solana Pay gerçek hayatta ödemeleri harika bir şekilde çalıştırır. Bunun nedeni, Solana'nın sunduğu özelliklerdir: herhangi bir kart makinesi kadar hızlı çalışır ve herhangi bir kredi kartı işleminden çok daha ucuzdur.

KURULUM : 
Phantom Cüzdan (https://phantom.app/download)
Phantom cüzdan üzerinde ikinci bir hesap açın.
Devnet Sol  (https://solfaucet.com/)

Tarayıcı Cüzdanı
------------------

İlk olarak, sizi Solana blok zincirine dahil etmek için bir tarayıcı cüzdanı oluşturarak başlayacağız! Diğer blok zincirlerinde olduğu gibi, cüzdanlar bakiyelerimizi takip etmek ve uygulamalarla etkileşimde bulunmak için kullandığımız araçlardır. Eğer zaten bir Solana cüzdanınız varsa, bu adımı hızlıca geçebilirsiniz!

En popüler tarayıcı cüzdanı Phantom adını taşımaktadır ve aşağıdaki web sitesinden indirebilirsiniz: https://phantom.app/download. Chrome, Brave, Firefox ve Edge için tarayıcı eklentilerine sahiptir, bu yüzden büyük ihtimalle kullandığınız tarayıcıya uygun bir seçenek bulunmaktadır! Başka bir cüzdan kullanmak isterseniz herhangi bir nedenle, serbestçe tercih edebilirsiniz, hepsi birbiriyle uyumludur.

Phantom ilk açıldığında yeni bir cüzdan oluşturma veya mevcut bir cüzdanı içe aktarma seçeneği sunacaktır:

<img width="448" alt="4" src="https://github.com/Yusufcihan1/Solana-Pay-Marketplace-Uygulamasi/assets/50721899/338da127-626b-4b02-a8c6-428f4ec98d18">

Solana'yı daha önce kullanmadıysanız "Yeni bir cüzdan oluştur"a tıklayın. Terminoloji konusunda hızlı bilgi, burada oluşturduğunuz bir cüzdan aynı zamanda bir "Hesap"tır. Solana'nın hesap modeline daha sonra değineceğiz, ancak etrafınıza baktığınızda bu terimi görebilirsiniz.

Sizden bir parola oluşturmanız istenecektir, bu yalnızca Phantom uzantısı içindir.

Daha sonra size Gizli Kurtarma İfadeniz sunulacaktır. Daha önce herhangi bir blockchain kullandıysanız, buna aşina olacaksınız! Gizli Kurtarma İfadeniz 12 rastgele kelime olacaktır. Bu, Phantom'da oluşturduğunuz tüm cüzdanlara erişmek, örneğin onları başka bir cüzdana aktarmak için kullanılabilir. Bunu asla kimseyle paylaşmadığınızdan emin olun, tüm cüzdanlarınıza erişebilecekler. Bir yere kaydedin, cüzdanlarınızı başka bir yere aktarmak istediğinizde ihtiyacınız olacak!

Kurulumu tamamladıktan sonra cüzdanınızı Phantom'da görebileceksiniz:

<img width="377" alt="5" src="https://github.com/Yusufcihan1/Solana-Pay-Marketplace-Uygulamasi/assets/50721899/75fb9ddf-0ea2-43dd-b886-371da3ddd3d0">

Başka bir şey yapmadan önce Devnet'e geçelim. Devnet'te tüm jetonlar sahtedir ve gerçek dünyada hiçbir değeri yoktur, bu yüzden öğrenmek için harikadır! Kendimize ücretsiz olarak Solana da gönderebiliriz ki bu kullanışlıdır!
Phantom'da Ayarlar'a gidin (sağ alttaki dişli simgesi), "Ağı Değiştir"i seçin ve "Devnet"i seçin.

Devnet SOL alalım
--------------------

Tamam, "0 SOL" olayı oldukça sıkıcı, biraz Solana ile oynamak için biraz SOL edinelim! https://solfaucet.com/ adresine gidin ve adresinizi girin. Phantom'da adresiniz üst kısımda kırpılmış olarak gösterilir ve tümünü kopyalamak için tıklayabilirsiniz:

<img width="361" alt="6" src="https://github.com/Yusufcihan1/Solana-Pay-Marketplace-Uygulamasi/assets/50721899/c3f23e8a-49ab-4a47-af4b-7a94aa5abe03">

Adresinizi solfaucet'e yapıştırın ve Devnet'e tıklayın:

<img width="970" alt="7" src="https://github.com/Yusufcihan1/Solana-Pay-Marketplace-Uygulamasi/assets/50721899/c742ef73-ae74-41f9-a7d9-9b4dba274e4e">

Bu arada,her airdrop için geçerli limit 2 SOL'dir. Bu eğitim için fazlasıyla yeterli olmalı :)
Hemen bir başarı mesajı aldığınızı fark edeceksiniz:

<img width="397" alt="8" src="https://github.com/Yusufcihan1/Solana-Pay-Marketplace-Uygulamasi/assets/50721899/0e0c1818-cb1b-4325-95ff-9e7573cf9765">

Solana'nın hızlı olduğundan bahsetmiş miydim? 🚀
Phantom'u kontrol edin ve bakiyenizin artık 1 SOL olduğunu göreceksiniz! Güzel!

İkinci bir cüzdan (hesap) ekleme
----------------------------------

Ödemelerle uğraşırken iki hesaba ihtiyacımız var: biri alıcı, diğeri satıcı için. Alıcı satıcıya öder! Şimdiye kadar bir hesap oluşturduk ve ona bir şeyler satın almak için kullanabileceği bir miktar SOL verdik. Şimdi satıcı hesabımızı yapalım.
Phantom'da sol üstteki menüyü açabilir ve yeni bir cüzdan ekleyebilirsiniz:

<img width="360" alt="9" src="https://github.com/Yusufcihan1/Solana-Pay-Marketplace-Uygulamasi/assets/50721899/42c4ae26-2163-4925-b827-17fb50200fd7">

Bir parola vermenizin istenmeyeceğini veya bir Gizli Kurtarma İfadesi gösterilmeyeceğini unutmayın. Parolanın Phantom uzantısı için olduğunu (tüm cüzdanların kilidini açar) ve Gizli Kurtarma İfadesinin de tüm cüzdanlar için olduğunu unutmayın!
Son bir şey, Phantom'da (ve çoğu cüzdan uygulamasında) cüzdanlarınızı tanımlamayı kolaylaştırmak için adlandırabilirsiniz. Bu, Ayarlar altındadır:

<img width="365" alt="10" src="https://github.com/Yusufcihan1/Solana-Pay-Marketplace-Uygulamasi/assets/50721899/16d09d71-1196-41b7-b422-78d315a70a0d">

İlk cüzdanı (SOL'lu olan) "Alıcı" ve ikincisini "Mağaza" olarak adlandırmanızı tavsiye ederim. Bu isimlerin sadece size ait olduğunu, blok zincirine hiçbir şekilde yansımayacağını unutmayın. Ama Phantom'u kullanmayı çok daha güzel hale getirecekler!

Başlangıç Kodunu İndirin
----------------------------
Bu öğretici Solana Pay ile ilgili olduğu için Html,Css ve Javascript kullanarak oluşturulan template kodunu hazır olarak çekiyoruz.

$ git clone -b start https://github.com/Yusufcihan1/Solana-Pay-Tutorial

Bu bir NextJS uygulamasıdır. npm ile çalıştırabilirsiniz:  
```
$ npm install
$ npm run dev
```
Varsayılan olarak localhost:3000 üzerinde çalışır. Çalışırken tarayıcınızda açın ve şöyle bir şey görmelisiniz:

![11](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/47859b46-98e0-4343-a889-c717f4d85bf7)

Başlangıç kodu size bazı ürünleri seçip sipariş verebileceğimiz basit bir e-ticaret arayüzü sunar!Bu ödeme sayfası şu anda biraz çıplak görünüyor.

KODUMUZU ÖZELLEŞTİRELİM
--------------------------
Görüntülenen ürünler lib/products.ts 'dedir, tanımlama bilgileri dışında bir şey satmak istiyorsanız bunları değiştirmekten çekinmeyin!

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

Renklerin, yazı tiplerinin hayranı değilseniz, bu sizin uygulamanız! İstediğinizi değiştirmekte özgürsünüz :)

SATIŞ MANTIĞI
------------------------
Solana Pay ile ödemeleri almak için bir satış noktası uygulaması oluşturmaya göz atmadan önce, uygulamamızın basit bir e-ticaret mağazası gibi çalışmasını sağlayalım.Kullanıcıların siparişleri için tarayıcı cüzdanlarında SOL kullanarak ödeme yapmasına izin verelim. Bu bize Solana işlemlerinin nasıl çalıştığı (daha fazlasını ileride göreceğiz!) ve Solana Pay'in perde arkasında ne yaptığı hakkında bir fikir verecektir.

Bazı bağımlılıkları yükleyerek başlayalım. Bunlar Solana tarafından sağlanır ve güzel bir kullanıcı arayüzü ve React entegrasyonu ile cüzdan bağlantısını yönetir:

```
$ npm install @solana/web3.js @solana/wallet-adapter-react @solana/wallet-adapter-react-ui @solana/wallet-adapter-base @solana/wallet-adapter-wallets
```
Daha sonra bileşen hiyerarşimizin en üstüne Solana bağlantısını ve bağlı cüzdanı işlemek için kod eklememiz gerekiyor. Blok zincirine istekte bulunmak için bir Solana bağlantısını ve kullanıcıdan ödeme yapmasını istemek için bağlı cüzdanı kullanacağız. Pages/ app.tsx'i aşağıdaki gibi görünecek şekilde güncelleyin:

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
Burada pek çok yenilik var! Devnet Solana ağına bağlantı oluşturuyoruz. Ayrıca uygulamamıza bağlanmasına izin vermek istediğimiz cüzdanları da tanımlıyoruz. Burada Phantom ve Solflare kullandım, ancak bir sürü cüzdan için adaptör var, bu yüzden istediğiniz cüzdanları eklemekten çekinmeyin! Uç noktayı ve cüzdanları tanımladıktan sonra, uygulamamızdaki her sayfadan Solana bağlantısına ve bağlı herhangi bir cüzdana erişebilmemiz için uygulamamızı bazı içerik sağlayıcılara bağlıyoruz. Bu kod, bu Solana kitaplıklarını kullanan herhangi bir uygulamada hemen hemen aynıdır.
Ana sayfamıza cüzdan bağlama özelliğini ekleyelim. 
Pages/index.tsx'i aşağıdaki şekilde güncelleyin:

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
Ufak bir isim değişikliği ile dükkanımı kurabiye dükkanı haline getirdim.Siz istediğinizi yapmakta özgürsünüz :D
Şimdi sayfa şöyle görünmelidir:

![13](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/13799aea-8767-4dcf-821e-e08b00b5c164)

"Cüzdan Seç" düğmesini tıklarsanız, cüzdanınızı seçmek için bir mod görmelisiniz:

![14](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/d1d2d747-b3ba-4378-bf0c-a336e2b6dc72)

Phantom'a tıklayın (alıcı cüzdanını bağladığınızdan emin olun) ve bağlantıyı onaylayın. Sayfa şimdi şöyle görünmelidir:

![15](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/fc0db40f-ef39-4ed8-908d-6f77f637968a)

Güzel! Cüzdanı bağlayıp kontrol edebiliriz. Ödeme sayfamız henüz bir şey yapmıyor, bu yüzden bir sonraki işimiz bu.

```
Gerçekte, bir e-ticaret satın alımı için alıcının adı ve siparişlerin nereye teslim edilmesini istedikleri gibi daha fazla bilgi toplamamız gerekir. Bunu sadece Solana yapılarını anlamak için kullandığımız için, onu burada atlayacağız.
```

İŞLEM OLUŞTURMA
----------------------
İşlemi ön uçta oluşturabilir ve kullanıcının cüzdanına gönderebiliriz. Bunu yapan, örneğin NFT satın alan uygulamalar görmüş olabilirsiniz. Ancak bir e-ticaret kullanım durumunda, işlemi oluşturmak için bir API yolu kullanmak daha mantıklıdır çünkü bu bize beklenen işlemleri güvenilir bir şekilde kaydetme yeteneği verir. Ön uçta çalıştırdığımız herhangi bir kodun müşteri tarafından değiştirilebileceğini unutmayın!

İhtiyacımız olan ilk şey mağaza adresi. Bunu öğretici boyunca birkaç farklı yerde kullanacağız, o yüzden yeni bir lib/addresses.ts dosyası oluşturalım:

```
import { PublicKey } from "@solana/web3.js"

// Your shop wallet address
export const shopAddress = new PublicKey('...') 
```
Mağaza adresinizi,üç noktanın içine yazdığınızdan emin olun ('...') . Genel anahtarın adres için kullandığımız başka bir terim olduğunu unutmayın, bu nedenle adresi burada sadece Solana kitaplıklarının beklediği şekilde saklıyoruz.

Tamam, API rotamızı oluşturalım. Yeni bir dosya oluşturalım (page/api/makeTransaction.ts ). Belirli bir ödeme için bir işlem oluşturmak için bunu kullanacağız ve ardından ön uç, kullanıcıdan bu işlemi onaylamasını isteyecektir.Bu arada, tüm bunları anlamadıysanız endişelenmeyin, aşağıda gözden geçireceğim. İşte bunun için kod:

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
Yazdığımız kodları biraz açıklayalım ve sonra devam edelim.
API, girdi olarak bir JSON nesnesi {"account": "public-key"} alır ve şunu döndürür:

```
{
  "transaction": "base-64 encoded transaction",
  "message": "Thanks for your order! 🍪"
}
```
Ayrıca istek sorgusunda girdi alır:
Ana sayfadaki formda seçilen öğeler, örneğin kullanıcı 2 kutu çerez satın aldıysa ?box-of-cookies=2. Bunun nasıl göründüğünü biraz daha görmek isterseniz, ana sayfada bazı ürünleri seçip kontrol etmeyi deneyin. Ödeme URL'sinin şöyle göründüğünü göreceksiniz: http://localhost:3000/checkout?box-of-cookies=2&basket-of-cookies=1. Şu anda ödeme sayfasında toplam fiyatı görüntülemek için URL'deki bu sorgu parametrelerini kullanıyoruz, ancak ücretlendirilecek fiyatı da hesaplayabilmesi için bunları API'mize ileteceğiz.

Referans: const {referans} = req.query. Bu, ödeme sayfasında oluşturacağımız yeni bir Solana genel anahtarıdır. Bunu birazdan biraz daha açıklayacağım.
API'mizin nasıl çalıştığına ve ne yaptığına biraz daha ayrıntılı olarak göz atalım.

```
const network = WalletAdapterNetwork.Devnet
const endpoint = clusterApiUrl(network)
const connection = new Connection(endpoint)
```
Bu, _app.tsx'te sahip olduğumuz türden bir kod, Solana'nın devnet ağına bir bağlantı başlatıyoruz.

```
// Get a recent blockhash to include in the transaction
const { blockhash } = await (connection.getLatestBlockhash('finalized'))
```
Bir işlem yalnızca kısa bir süre için geçerli olmalıdır. Şimdiye kadar ağda görülen en son bloğu dahil ediyoruz ve işlem çok eskiyse reddedilebilir.

```
const transaction = new Transaction({
  recentBlockhash: blockhash,
  // The buyer pays the transaction fee
  feePayer: buyerPublicKey,
})
```
Burada yeni bir Solana işlemi oluşturuyoruz. Yeni aldığımız Blockhash'i az önce getirdiğimiz bloğa ayarlıyoruz. Ayrıca alıcımızı işlem için ücret ödeyen kişi olarak belirliyoruz. Bu, alıcının işlemi ağ tarafından işlenmeden önce imzalaması ve devam etmesi için yetki vermesi gerektiği anlamına gelir.

```
// Create the instruction to send SOL from the buyer to the shop
const transferInstruction = SystemProgram.transfer({
  fromPubkey: buyerPublicKey,
  lamports: amount.multipliedBy(LAMPORTS_PER_SOL).toNumber(),
  toPubkey: shopPublicKey,
})
```
Bir Solana işlemi bir dizi talimat içerebilir ve atomiktir - ya hepsi başarılı olur ya da işlem hiçbir değişiklik olmaksızın başarısız olur. Bu durumda, işlemimizin tek bir talimatı vardır: alıcıdan mağazaya SOL gönderin. Mağazamızın şu anda SOL cinsinden fiyatlandırıldığını, ancak transfer talimatının lamport cinsinden numara verilmesini beklediğini unutmayın. 1 SOL'de 1 milyar (10^9) lamport vardır, ancak aralarında dönüştürme yaparken her zaman LAMPORTS_PER_SOL sabitini kullanmak en iyisidir.

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

Her talimatın kendisiyle ilişkilendirilmiş bir dizi anahtarı vardır. İşlem, bu anahtarlardan herhangi biri tarafından aranabilir. Her anahtar bir imzalayıcı olabilir ve yazılabilir. Bizim durumumuzda, transfer işlevi bazı varsayılan tuşlarla bir talimat oluşturuyor:

Alıcı ortak anahtarı: imzalayandır, çünkü SOL'lerini aktarıyorlar ve yetkilerini vermeleri gerekiyor. Yazılabilir, çünkü SOL bakiyeleri değişecektir.

Mağaza genel anahtarı: yazılabilir, çünkü SOL bakiyeleri değişecektir. İmzalayan değil, SOL almak için yetki vermesine gerek yok.

Yukarıdaki koda ek bir anahtar ekliyoruz:Referans. Bunun, belirli ödeme oturumuna özgü, API'mize girdi olarak iletilen bir genel anahtar olduğunu unutmayın. İmzalayan veya yazılabilir olması gerekmez, çünkü gerçek SOL aktarımına dahil değildir. Ancak talimatımıza ekleyerek, bu referansı kullanarak işlemi arayabiliriz. Bu, ödeme sayfamızın bir ödeme yapıldığını algılamasını sağlar!

Ekstra anahtarı ekledikten sonra transfer talimatını işleme ekliyoruz. İşlemimizin artık bir talimatı var.

```
// Serialize the transaction and convert to base64 to return it
const serializedTransaction = transaction.serialize({
  // We will need the buyer to sign this transaction after it's returned to them
  requireAllSignatures: false
})
const base64 = serializedTransaction.toString('base64')
```

İşlemi serileştiriyoruz ve ardından base-64'e dönüştürüyoruz. Bu, onu API'den döndürmemize ve /checkout sayfasında tüketmemize izin verecektir. İşlemimiz alıcının imzasını gerektirdiğinden ve henüz buna sahip olmadığımızdan serileştirdiğimizde requestAllSignatures: false değerini iletmeliyiz. /checkout sayfasındaki bağlı cüzdanlarından talep edeceğiz.

```
Devam etmeden önce son bir şey: Gerçekte bu işlemi API çağrısının bir parçası olarak bir veritabanına kaydetmek isteyeceksiniz. Bu, daha sonra ücretli işlemin doğru olduğunu doğrulamamıza olanak tanır. Yine burada Solana yapılarına odaklandığımız için bu eğitimde onu atladım.
```

İşlemin talep edilmesi
----------------------

Öncelikle, bu API'yi çağırabileceğimizden ve döndürülen işlemin serisini kaldırabileceğimizden emin olalım.

pages/checkout.tsx'i aşağıdaki şekilde güncelleyin:

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

Burada oldukça fazla yenilik var! Adım adım ilerleyelim:

```
const { publicKey } = useWallet();
```
Bu sadece bağlı cüzdanı ana sayfadan okur. Bağlı cüzdan yoksa boş olacaktır.
```
// State to hold API response fields
const [transaction, setTransaction] = useState<Transaction | null>(null);
const [message, setMessage] = useState<string | null>(null);
```
API'miz bir işlem + bir mesaj döndürür, bu yüzden bunları aldığımızda yanıttan ayarlayacağız.
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
Sadece sorgu parametrelerini bir URLSearchParams nesnesine dönüştürdük. Bununla çalışmak, Next.js'in bize sorgu parametreleri için verdiğinden daha kolaydır! Seçilen ürünlerin sorgu parametrelerinde olduğunu ve bunları API'mize aktarmamız gerektiğini unutmayın.

```
// Generate the unique reference which will be used for this transaction
const reference = useMemo(() => Keypair.generate().publicKey, []);

// Add it to the params we'll pass to the API
searchParams.append('reference', reference.toString());
```

Bu, API'de döndürdüğümüz referanstır. Bu sayfada üretiyoruz ve geçmekte olduğumuz parametrelere ekliyoruz. Bunu kısa süre sonra işlemi tespit etmek için kullanabileceğiz.
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

/api/makeTransaction'ımıza bir API çağrısı yapıyoruz ve bunu sorgu parametrelerimiz + hesap gövdesi iletiyoruz. Base64'ten gelen yanıtın kodunu çözüyoruz ve seriyi kaldırıp bir Transaction nesnesine geri döndürüyoruz.

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

Renderimiz şimdi biraz daha ilginç! İlk önce bir publicKey'in olmadığı durumu ele alıyoruz - bu olmadan işlemi oluşturamayız. Sadece cüzdan bağlan düğmesini gösteriyoruz ve kullanıcıya bağlanması gerektiğini bildiriyoruz.

Aksi takdirde, işlemi getirirken önce küçük bir yükleme göstergesi gösteririz. Elimize geçtikten sonra, API tarafından döndürülen mesajı gösteririz. Sayfayı yenilerseniz, getirilen ve günlüğe kaydedilen işlemi ve gösterilen mesajı görmelisiniz:

![16](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/d40d14cf-0a46-4801-94da-41cdc630796b)

İşlemin gönderilmesi
----------------------
Tamam güzel, API'mizden bir işlem aldık! Şimdi bunu kullanıcının cüzdanına göndermek ve onaylamasını istemek için sayfayı güncelleyelim.

Öncelikle, kancaları kullanarak biraz daha bağlam yakalamamız gerekiyor:
```
import { useConnection, useWallet } from "@solana/wallet-adapter-react";

export default function Checkout() {
  const router = useRouter();
  const { connection } = useConnection();
  const { publicKey, sendTransaction } = useWallet();

  // unchanged below here
```

Solana bağlantısını alıyoruz ve ayrıca bağlı cüzdandan sendTransaction alıyoruz. Bu, bağlı cüzdanı kullanarak işlem göndermek için kullanabileceğimiz bir işlevdir.

Şimdi getTransaction ve onun useEffect kancasından sonra, başka bir fonksiyon ve kanca eklememiz gerekiyor:

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

Yeni kodu bu şekilde yerleştirmek biraz kafa karıştırıcı olabilir, kaybolursanız kodun tam hali (pages/checkout.tsx) :
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

İşlem durumu güncellendiğinde (setTransaction'ı çağırdığımızda bunu yaparız), sendTransaction'ı kullanarak bu işlemi kullanıcının cüzdanına göndeririz.

Ödeme sayfasını şimdi yenilerseniz, Phantom sizden işlemi onaylamanızı isteyecektir:

<img width="1399" alt="17" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/9e964970-2f08-43b0-ad6f-ff965932e2f0">

Bu arada ilk açıldığında SOL fiyatını göstermeden önce “İşlem onaylanamayabilir” gibi bir şey yazabilir. Bu normal. Orada gerçekte olan şey, cüzdanın Solana ağından işlemi simüle etmesini istemesidir, böylece onaylarsanız ne olacağını size bildirebilir - bu durumda sizden 0,05 SOL ücretlendirilir. İşlemi bir süre onaysız bırakırsanız da olmayabilir. Bunun nedeni, daha önce bahsettiğimiz son blok hash işlemidir, işlem eskir ve yeniden oluşturulması gerekir.

Yine de onaylarsanız, ilk Solana işleminizi göndereceksiniz! Güzel!

Kullanıcı arayüzümüz henüz ödeme yaptığınızı bilmeyecek, dolayısıyla orada hiçbir şey olmayacak. Sıradaki işimiz bu! Ancak hesabınızı Phantom'da kontrol ederseniz, işlemi orada göreceksiniz:

<img width="358" alt="18" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/718a9db4-f3d8-4e5c-aa27-0fee3ccb9c10">

Ve bir işlem göndermek için tek yapmamız gereken bu!

ÖDEMENİN TESPİT EDİLMESİ
----------------------------

Şimdiye kadarki kullanıcı deneyimi biraz sınırlı, işlemi sunduğumuzda kullanıcının ödeme yapıp yapmadığını görmek için kendi cüzdanını kontrol etmesi gerekiyor. Bundan çok daha iyisini yapabiliriz!

Teknik olarak bunu Solana Pay olmadan yapabiliriz, ancak bunu gerçekten kolaylaştıracak süper kullanışlı bir işlevi var. Öyleyse şimdi yükleyelim:

```
npm install @solana/pay@0.2.0
```

Bu bağımlılığı, yalnızca bu öğreticide kullanılan API'lerin biz onu güncelleme fırsatı bulamadan değişmeyeceğinden emin olmak için sürümlendiriyoruz.

pages/checkout.tsx'e bir tane daha useEffect ekleyeceğiz:
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
Yine ihtiyacınız varsa, kodun tamamı :
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
Referansımızı kullanan herhangi bir işlem olup olmadığını görmek için her 0,5 saniyede bir kontrol eden bir aralık ekledik. Eğer yoksa, o zaman findReference, yakaladığımız ve yok saydığımız bir FindReferenceError atar. Artık ödeme sayfamız, kullanıcının ödeme yapıp yapmadığını görmek için arka planda oylamaya devam edecek.

```
findReference çağrısı, gizli olmayan referansımızı kullanan herhangi bir işlemi bulacaktır. Doğru işlemin yapıldığını garanti etmez. Bu durumda sorun yok çünkü biz sadece kullanıcıya geri bildirim gösteriyoruz. Eğitimin ilerleyen kısımlarında, burada güvenliği iyileştirmenin yollarını göreceğiz.
```

İşlemi yeniler ve onaylarsanız, ödendiğini belirten bir günlük mesajı görmelisiniz:

<img width="1144" alt="19" src="https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/3fd1d88c-99ae-4786-81d8-c3a5ab8adf51">

Şimdi kullanıcıya ödemesini aldığımızı bildirmemiz gerekiyor!

ONAY SAYFASI EKLEME
-------------------------
Kullanıcıya ödemesinin kabul edildiğini bildirmek için yeni bir sayfa ekleyeceğiz.

Size benimkini nasıl yaptığımı göstereceğim ama başka bir şey yapmak isterseniz çekinmeyin! Uygulama sizin 🙂

İlk olarak, yeni bir bağımlılık var:
```
npm install react-circular-progressbar
```
Bu, gerçekten güzel göründüğünü düşündüğüm dairesel bir ilerleme çubuğuna animasyon ekliyor :

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

İlerleme çubuğu kütüphanesinin dahili bir animasyonu vardır, ancak yalnızca durum değişikliklerinde animasyon yapar - yani eğer yalnızca %100 ilerlemeye sahip bir ilerleme çubuğu oluşturursak, animasyon gerçekleşmez.Bu yüzden onu %0 ile oluşturup, ardından %100'e animasyonla hareket ettiriyoruz.

React ilerleme çubuğu hakkında detaylı bilgiye https://www.npmjs.com/package/react-circular-progressbar sitesinden ulaşabilirsiniz.

Ve bu bileşeni görüntülemek için bir sayfa ekleyelim:
pages/confirmed.tsx dosyasını oluşturuyoruz.

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

Ve son olarak, ödemeyi gördüğümüz anda bu sayfaya yönlendirmek için ödeme sayfamızdaki useEffect'i güncelleyebiliriz!
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
Az önce console.log satırını router.push('/confirmed') olacak şekilde düzenledim.
Ve şimdi geçerli bir ödeme aldığımızda yeni onaylanan ekranı görüntüleyeceğiz:

![tutorial__7clC2VD3oSsgx8mbh6Ak](https://github.com/Yusufcihan1/Solana-Pay-Tutorial/assets/50721899/11c7d3a9-4ba4-4551-a3da-35cf8b290951)

Bu noktada Solana kullanarak sitemizde çerez satabiliriz!

Ancak çerez dükkanımıza gelen pek çok kişi bir SOL'un değerinin ne olduğunu bilmiyor olabilir. Bunun yerine onları dolar olarak alabilseydik iyi olurdu!Sıradaki keşfedeceğimiz şey bu !

