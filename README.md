# Ece-ogrenci-ders-yonetim-sistemi
Bu proje, bir öğrenci ve ders yönetim sistemi oluşturmayı amaçlamaktadır. Sistem, öğrenci ve ders bilgilerini yönetmek için sınıflar, nesneler ve veri dosyaları kullanmaktadır. Veriler, XML veya JSON formatlarında saklanır ve gerektiğinde okunur. Projede kullanılan temel özellikler arasında serileştirme (serialization), polimorfizm (çok biçimlilik) ve interface kullanımı yer almaktadır.

Proje Özeti
Bu yazılım, öğrenci, öğretim görevlisi ve ders bilgilerini yönetmek için bir yönetim paneli sağlar. Kullanıcılar dersleri tanımlayabilir, öğretim görevlilerini ve öğrencileri ilişkilendirebilir. Ayrıca, derslerin adları, kredileri, öğretim görevlisi ve kayıtlı öğrenciler gibi bilgileri görüntüleyebilirler.

Temel Bileşenler
Ogrenci (Öğrenci) Sınıfı
Öğrencilerin temel bilgilerini (ID, ad, soyad, numara gibi) saklayan bir sınıftır. Öğrenciler, belirli derslere kayıt olabilir ve derslerle ilişkili bilgiler saklanabilir.

OgretimGorevlisi (Öğretim Görevlisi) Sınıfı
Öğretim görevlisinin temel bilgilerini (ID, ad, soyad, departman gibi) saklayan bir sınıftır. Her öğretim görevlisinin verdiği dersler de bu sınıf içerisinde tutulur.

Ders Sınıfı
Derslerin temel bilgilerini (ad, kredi, öğretim görevlisi gibi) saklayan sınıftır. Derslere öğrenciler kayıt olabilir.

BasePerson Sınıfı
Öğrenci ve öğretim görevlisi sınıflarının ortak özelliklerini ve metotlarını içerir. Bu sınıf, ID, Ad, Soyad gibi temel bilgileri içerir.

Kullanılan Teknolojiler ve Yaklaşımlar
XML ve JSON Veri Depolama

Veriler, XML veya JSON dosyaları aracılığıyla saklanır.
Verileri saklamak ve okumak için XmlSerializer ve JsonConvert sınıfları kullanılmıştır.
XML veya JSON dosyalarına veri yazma ve okuma işlemleri yapılır.
Polimorfizm

Temel sınıfta tanımlanan BilgiGoster() metodu, türetilmiş sınıflarda özelleştirilerek kullanılmıştır.
Interface Kullanımı

Sistemde IPerson veya ILogin gibi bir interface kullanılmış ve bu interface’in zorunlu kıldığı metotlar sınıflarda uygulanmıştır.
Kullanıcı Arayüzü
Sistem, kullanıcıya aşağıdaki işlemleri sunmaktadır:

Öğrenci Kaydı: Öğrenciler sisteme eklenebilir.
Öğretim Görevlisi Kaydı: Öğretim görevlileri sisteme eklenebilir.
Ders Tanımlama: Dersler tanımlanabilir, dersin adı, kredisi ve öğretim görevlisi bilgileri sisteme kaydedilebilir.
Ders Kayıtları: Öğrenciler, derslere kayıt olabilir.
Listeleme ve Görüntüleme: Öğrenciler ve dersler listelenebilir.
Uygulama Akışı
Öğrenci Ekleme: Öğrenciler, kimlik, ad, soyad ve numara gibi bilgilerle sisteme eklenir.
Öğretim Görevlisi Ekleme: Öğretim görevlileri, kimlik, ad, soyad ve departman bilgileriyle sisteme eklenir.
Ders Tanımlama: Dersler, adı, kredisi ve hangi öğretim görevlisinin verdiği bilgileriyle sisteme eklenir.
Ders Kayıtları: Öğrenciler derslere kaydolabilir ve dersin öğretim görevlisi atanır.
Veri Kaydetme ve Okuma: XML veya JSON dosyaları kullanılarak veriler kaydedilir ve okunur.
Projenin Faydaları
Veri Yönetimi: Öğrenciler ve dersler kolaylıkla yönetilebilir.
Veri Güvenliği: Veriler, XML veya JSON dosyalarıyla güvenli bir şekilde saklanır.
Kullanıcı Dostu: Basit bir kullanıcı arayüzü ile işlemler hızlı bir şekilde yapılabilir.
