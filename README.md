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
