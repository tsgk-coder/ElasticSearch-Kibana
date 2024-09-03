# Event Code Example

[Ultimate Windows Security](https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/default.aspx)


# Kibana Query Language

``event.provider:"Microsoft-Windows-Sysmon"``

``event.code:"1"`` 

``agent.type :"endpoint"``  

``process.entity_id :* ``

``host.name:"desktop-xxxxxxx"`` 

``process.name :"rundll32.exe"`` 

``process.args:"MiniDump"``

``process.command_line:*HKLM*``

``message:"Invoke"``  


# Windows Powershell Event Code 

```
4104  
4103
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
