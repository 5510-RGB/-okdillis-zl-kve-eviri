📚 C# Konsol Çok Dilli Sözlük UygulamasıBu proje, bir masaüstü konsol uygulaması olarak geliştirilmiş basit bir çok dilli sözlük ve çeviri aracıdır. Uygulama, verileri kalıcı olarak bir sozluk.json dosyası üzerinde saklar ve CRUD (Oluşturma, Okuma, Silme) işlemlerini destekler.✨ ÖzelliklerÇok Dilli Arama: Kaynak dil, hedef dil ve kelime kriterlerine göre tam eşleşmeli arama yapar.Kalıcı Veri Depolama: Tüm sözlük verileri, uygulamanın yeniden başlatılması durumunda kaybolmaması için JSON dosyası (sozluk.json) içinde saklanır.Dinamik Yönetim: Kullanıcıya yeni kelime ekleme ve mevcut kelime kayıtlarını silme imkanı sunar.Konsol Tabanlı Arayüz: Kullanımı basit, metin tabanlı etkileşim.⚙️ Kurulum ve ÇalıştırmaProjeyi Visual Studio'da çalıştırmak için aşağıdaki adımları izleyin.1. Visual Studio'da Açmaçokdillisözlük.sln dosyasını Visual Studio'da açın.Gereken tüm C# dosyalarının (Program.cs, SozlukGirdisi.cs) projeye dahil edildiğinden emin olun.2. Veri Dosyası (sozluk.json) Kurulumu (Çok Önemli!)Uygulamanın çalışabilmesi için sozluk.json dosyasının uygulamanın çalıştırıldığı klasörde bulunması gerekir.sozluk.json dosyasını projenizin ana dizinine yerleştirin.Visual Studio'da, sozluk.json dosyasına tıklayın ve Özellikler penceresinde aşağıdaki ayarları yapın:Yapı Eylemi (Build Action): İçerik (Content)Çıktı Dizinine Kopyala (Copy to Output Directory): Daha Yeniyse Kopyala (Copy if newer)3. ÇalıştırmaVisual Studio'da F5 tuşuna basarak veya üst menüden Başlat'a tıklayarak uygulamayı çalıştırın.💡 Kullanım KılavuzuUygulama başladığında, aşağıdaki ana menü ile karşılaşırsınız:-----------------------------------------
Yapmak istediğiniz işlemi seçin:
1: Kelime Arama/Çevirme
2: Yeni Kelime Ekleme (ve Kaydetme)
3: Kelime Silme
exit: Çıkış
Seçiminiz:
1. Kelime Arama/ÇevirmeKullanıcıdan sırasıyla Kaynak Dil Kodu (en, de, tr vb.), Hedef Dil Kodu ve çevrilecek kelimeyi alır.Örnek Giriş: en $\rightarrow$ tr $\rightarrow$ helloBeklenen Çıktı: Çeviri Sonucu: **merhaba**2. Yeni Kelime EklemeSözlüğe kalıcı olarak yeni bir kayıt eklemek için kullanılır. Eklenen kayıt hemen sozluk.json dosyasına kaydedilir.Gerekenler: Kaynak Dil, Kaynak Kelime, Hedef Dil, Hedef Kelime (Çeviri).3. Kelime SilmeBelirli bir kelime kaydını sözlükten kaldırmak için kullanılır. Silme işlemi için kelimenin yanı sıra hem kaynak hem de hedef dil kodlarını girmeniz istenir, bu sayede doğru kayıt silinir.💾 Veri Yapısı (sozluk.json)Uygulama, tüm verileri aşağıdaki JSON formatında saklar:[
  { 
    "KaynakKelime": "hello", 
    "HedefKelime": "merhaba", 
    "KaynakDil": "en", 
    "HedefDil": "tr" 
  },
  // ... diğer kayıtlar
]
💻 Proje Kodlama ÖzellikleriDil: C#Platform: .NET Console ApplicationVeri Yönetimi: System.Text.Json (Serileştirme/Deserileştirme) ve System.IO (Dosya Okuma/Yazma)Arama Algoritması: C#'ın güçlü LINQ (Language Integrated Query) özelliği ile bellek üzerinde hızlı ve kesin eşleşmeli sorgulama (FirstOrDefault).
