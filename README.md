# Staj_Proje_1 - Hava Durumu Botu

Bu proje, UiPath Studio kullanılarak hazırlanmış bir RPA öğrenci projesidir. Belirtilen il ve ilçeye ait 5 günlük hava durumu tahminlerini Meteoroloji Genel Müdürlüğü (MGM) web sitesinden çekerek masaüstüne bir Excel dosyası olarak kaydeder.

## Projenin Çalışma Mantığı

Süreç üç temel adımdan oluşmaktadır:

1. Kullanıcı Girişi (001_UserInput.xaml): Ekrana gelen diyalog pencereleri ile kullanıcıdan hava durumu istenen il ve ilçe bilgileri alınır.
2. Veri Çekme (002_Browser.xaml): Tarayıcı üzerinden mgm.gov.tr adresine gidilerek, girilen konuma ait 5 günlük (Tarih, En Düşük Sıcaklık, En Yüksek Sıcaklık) veriler okunur.
3. Excel'e Kaydetme (003_ExcelOperations.xaml): Elde edilen veriler masaüstünde bir Excel dosyası oluşturularak tablo halinde kaydedilir. Örneğin, il olarak "Bursa" ve ilçe olarak "İnegöl" girildiğinde bot bu bölgenin verilerini çekerek "Bursa 5 Günlük Hava Durumu.xlsx" adında bir dosya oluşturur.

## Kullanılan Paketler

Projenin çalışması için `project.json` içerisinde tanımlı olan bağımlılıklar:
* UiPath.Excel.Activities
* UiPath.System.Activities
* UiPath.UIAutomation.Activities

## Kurulum ve Kullanım

1. Proje dosyalarını bilgisayarınıza indirin.
2. Klasör içerisindeki `project.json` dosyasını UiPath Studio ile açın.
3. Proje açıldıktan sonra `Main.xaml` dosyasını çalıştırarak süreci başlatın.
