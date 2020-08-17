# Soket_Programlama

if we talk about socket programing now, we can understandm that we pass basic level of programing stuff and so forth.
it is a good thing.In here, we will learn how to cominucate tools each other in network.

Socket programing provides a channel for two different tool in network using TCP/IP protocol via  IP and port number.

*******

Bu haberleşmede bir socket(uç cihaz node) belirlenen IP ve port üzerinden kanalı dinlerken diğer socket(uç cihaz node) aynı kanal üzerinden diğer uca erişmeye çalışır.

Bu bağlantıda server kanalı dinleyen uç, client ise server a ulaşmaya çalışan uçtur.
Socket programlamanın mantığını anladıktan sonra Pyhton ile socket programlamaya başlayabiliriz.
Bunun için ilk olarak server tarafını hazırlayalım ve server.py dosyamızı hazırlayalım.Dosyamıza socket kütüphanesini dahil edelim.
Ardından server bilgileri için IP ve port numaralarını belirleyelim.Bu örnekte hem server hemde client çalışma yerimiz pc olacağı için server adresi
127.0.0.1 yani local host olacaktır.

host="127.0.0.1"
port=12345

Şimdi bu bilgilerle socketi oluşturalım.

s=socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.bind((host,port))

Bu noktada socket(family, type) yapısındaki socket fonksiyonunda geçirdiğimiz iki parametreyide açıklayalım.
family parametresi:
AF_UNIX:unıx domain protocolleri
AF_INET:TCP ve UDP için IPv4 protocolleri 
AF_INET6:TCP ve UDP için IPv6 protocolleri

değişkenlerini alabilir.


type parametresi SOCK_STREAM, SOCK_DGRAM, SOCK_RAW bağlantı tipleridir.

Biz bu örneğimizde en çok TCP bağlantı tipini ve IPv4 adresleme seçeneğini 


