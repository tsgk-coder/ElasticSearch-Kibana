# Kibana Query Language


``agent.type :"endpoint"``  

``process.entity_id :* ``

``host.name:"desktop-8f3jgrb"`` 

``process.name :"rundll32.exe"`` 

``process.args:"MiniDump"``

``event.code:"1"`` 

``process.command_line:*HKLM*``

``message:"Invoke"``  

``event.provider``


``Powershell Aktiviteleri Takibi``
``Host Bazlı Güvenlik Önlemi``
``Powershell & Sysmon  & EDR``

# Windows Security Event Code 

```
4104
4103
```

# Sysmon Event Code 

```
Event ID 1 – Process Creation: Yeni bir süreç oluşturulduğunda kaydedilir. Sürecin adı, işlem kimliği, komut satırı parametreleri gibi bilgileri içerir.

Event ID 2 – File Creation Time Changed: Bir dosyanın oluşturulma zamanında bir değişiklik yapıldığında kaydedilir. Bu, dosyanın zaman damgasının değiştiğini gösterir.

Event ID 3 – Network Connection: Bir ağ bağlantısı yapıldığında (TCP/UDP) kaydedilir. Bağlantı bilgileri, IP adresleri ve portlar gibi detayları içerir.

Event ID 4 – Sysmon Service State Changed: Sysmon hizmetinin durumu değiştiğinde kaydedilir. Hizmetin başlatılması veya durdurulması gibi durumları içerir.

Event ID 5 – Process Terminated: Bir sürecin sonlandığı durumları kaydeder. Sürecin kimliği ve sonlanma kodu gibi bilgileri içerir.

Event ID 6 – Driver Load: Bir sürücünün yüklendiği durumlarda kaydedilir. Sürücünün yolu ve dosya adı gibi bilgileri içerir.

Event ID 7 – Image Load: Bir yürütülebilir dosya veya dinamik bağlantı kitaplığı (DLL) yüklendiğinde kaydedilir. Yüklenen dosyanın yolu gibi bilgileri içerir.

Event ID 8 – CreateRemoteThread: Bir süreçten diğer bir sürece uzaktan bir iş parçacığı oluşturulduğunda kaydedilir. Bu, genellikle kötü niyetli aktivitelerin bir göstergesidir.

Event ID 9 – Raw Access Read: Bir dosyanın ham okuma erişimi sağlandığında kaydedilir. Bu, dosyaya doğrudan erişim sağlandığını gösterir.

Event ID 10 – Process Access: Bir sürecin diğer bir süreç tarafından erişildiği durumlarda kaydedilir. Erişim türü ve sürecin kimliği gibi bilgileri içerir.

Event ID 11 – File Create: Bir dosya oluşturulduğunda kaydedilir. Dosyanın yolu ve oluşturulma zamanı gibi bilgileri içerir.

Event ID 12 – Registry Event: Kayıt defteri (registry) üzerinde yapılan değişiklikleri kaydeder. Anahtarlar ve değerler üzerindeki değişiklikleri içerir.

Event ID 13 – Registry Value Set: Kayıt defterinde bir değerin ayarlandığı durumlarda kaydedilir. Yeni veya değiştirilen değerleri içerir.

Event ID 14 – Registry Key Deleted: Bir kayıt defteri anahtarının silindiği durumlarda kaydedilir. Silinen anahtarın yolu gibi bilgileri içerir.

Event ID 15 – File Delete: Bir dosyanın silindiği durumlarda kaydedilir. Silinen dosyanın yolu ve diğer detayları içerir.

Event ID 16 – File Rename: Bir dosyanın yeniden adlandırıldığı durumlarda kaydedilir. Yeni ve eski dosya adları gibi bilgileri içerir.
```


Antivirus & EDR arasındaki farklar ? 
   --

```
*  Antivirus malware imza tabanlı.
   Gelişmiş Antivirüs
   Makine öğrenmesi ile çağrılan patern Match yapıyor.

*  EDR (Endpoint Detection Response)
   Yapılan aktivitenin tüm ağacını çıkartır.
   Kural, korelasyon yapar.
   Olay sonrası kısmı daha güçlü.
   Oluşan bütün eventleri, çalışan makroları sistem dosyalarına hangi process e 
   erişilmiş ise hepsini getirir. Bütün olayı atar.
   Network aktiviteleri de takip edilir.
   Process takip, life sykel, yaşam döngüsü.
   Uzaktan komut çalıştır ve sonuçların yaşam döngüsünü bana logla.

   XDR
   Farklı endpoint de çalışan olayları birleştirir.
   Korelasyon yapar binevi.
   Ajan olmayan makinalardan gelen trafikleri gördüğü için
   bu makinalarında da alarm üretir

   MDR

   Farklı process id ile işleme devam edersen bu ürünleri atlatabilirsin
```


[UltimateWindowsSecurity](https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/default.aspx)

