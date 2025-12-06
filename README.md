C# Konsol Çok Dilli Sözlük Uygulaması

Bu proje, bir konsol tabanlı çok dilli sözlük ve çeviri uygulamasıdır. Tüm sözlük verileri sozluk.json dosyasında saklanır ve uygulama kapanıp açılsa bile kaybolmaz. Kullanıcıya kelime arama, yeni kelime ekleme ve kelime silme işlemleri sunar.

✨ Özellikler

Çok Dilli Çeviri
Kaynak dil, hedef dil ve kelimeye göre tam eşleşmeli arama yapar.

Kalıcı Veri Depolama
Tüm veriler otomatik olarak sozluk.json dosyasında tutulur.

CRUD İşlemleri
Yeni kelime ekleme ve mevcut kelimeyi silme imkanı.

Konforlu Konsol Arayüzü
Basit ve kullanıcı dostu bir metin tabanlı menüye sahiptir.

⚙️ Kurulum ve Çalıştırma
1. Projeyi Açma

cokdillisozluk.sln dosyasını Visual Studio’da açın.

Program.cs ve SozlukGirdisi.cs dosyalarının projede bulunduğundan emin olun.

2. sozluk.json Dosyasını Hazırlama (Önemli!)

Uygulamanın çalışması için sozluk.json dosyasının doğru ayarlanmış olması gerekir.

Yapmanız gereken:

sozluk.json dosyasını projenin ana dizinine ekleyin.

Visual Studio’da dosyaya sağ tıklayın → Properties (Özellikler)

Şu ayarları yapın:

Özellik	Değer
Build Action	Content
Copy to Output Directory	Copy if newer
3. Uygulamayı Başlatma

Visual Studio’da:

F5’e basarak
veya

"Start" tuşuna tıklayarak

uygulamayı çalıştırabilirsiniz.

🧭 Kullanım

Uygulama açıldığında aşağıdaki menü gelir:

-----------------------------------------
Yapmak istediğiniz işlemi seçin:
1: Kelime Arama/Çevirme
2: Yeni Kelime Ekleme (ve Kaydetme)
3: Kelime Silme
exit: Çıkış
Seçiminiz:

1. Kelime Arama / Çevirme

Kullanıcıdan sırasıyla:

Kaynak dil kodu (Örn: en)

Hedef dil kodu (Örn: tr)

Çevrilecek kelime

alınır.

Örnek kullanım:

Kaynak Dil: en
Hedef Dil: tr
Kelime: hello
Çeviri Sonucu: merhaba

2. Yeni Kelime Ekleme

Sözlüğe yeni bir çeviri eklemek için:

Kaynak Dil

Kaynak Kelime

Hedef Dil

Hedef Kelime

bilgileri girilir ve kayıt anında JSON dosyasına yazılır.

3. Kelime Silme

Belirli bir kelime çevirisini silmek için:

Kaynak Dil

Hedef Dil

Kelime

bilgileri istenir. Eşleşen kayıt JSON’dan kaldırılır.

💾 JSON Veri Yapısı

sozluk.json dosyası aşağıdaki formatı kullanır:

[
  {
    "KaynakKelime": "hello",
    "HedefKelime": "merhaba",
    "KaynakDil": "en",
    "HedefDil": "tr"
  }
]

🛠 Kullanılan Teknolojiler
Bileşen	Teknoloji
Programlama Dili	C#
Platform	.NET Console App
Veri Depolama	JSON (System.Text.Json)
Dosya İşlemleri	System.IO
Arama Motoru	LINQ (FirstOrDefault)
📁 Proje Dosya Yapısı
📂 Proje
 ├── Program.cs
 ├── SozlukGirdisi.cs
 ├── sozluk.json
 └── cokdillisozluk.sln

