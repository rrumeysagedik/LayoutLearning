LAYOUT 
Constrait Layout:
ConstraintLayout, Android uygulamalarda kullanabileceğimiz yeni bir layout tipidir. API 9 ve üstündeki tüm API’lerde kullanılabilir bir yapıdır. Constraint Layout karmaşık tasarımları birbirine bağımlı layout’lar olmadan kolay bir şekilde tasarlamamıza imkan sağlar. View’lar birbirine göre konumlandırıldığında herhangi bir view’ın konumu değiştirildiğinde diğer view’da konumunu değiştiriyor. Diğer bir yandan ConstraintLayout ile birlikte iç içe bağımlı layout’lara gerek olmadığı için ekstra performans artışı sağlamaktadır.

Constrait layout kullanımı :android studio’da design ekranını split ettiğimiz zaman
xml formatı karışımıza gelir.  <androidx.constraintlayout.widget.ConstraintLayout xmlns:
buradaki kırmızı yer ile işaretli yer layoutun türünü belli eder.

MANUAL CONSTRAIT 
mesela bir buttonun manual constraitini ayarlamak  istiyorsak butonların sağ sol alt ve üstlerde içi boş daireler var. Oradan sayfadaki duruşunu ayarlayabiliriz.

blue design’da tırtıklı oklar layoutu ayarlamayı sağlıyor.

DEĞİŞİK SIZELAR

wrap-content: içeriğe bak ve ona göre boyutu ayarla demek.
köşelerden çekiştirerek boyutlarla oynadığımız zaman dp formatına geçer.
dp:dencity pixel

kendimiz bir boyut verip her boyuttaki telefona ayarlamamız gerektiğinde yani düzgün gözükmesini sağlamamız gerektiğinde
avd managerdan farklı emülatorlerle test edeibilrim.
pixelden seçebiliriz.
LAYOUT VALİDATİON KULLANABİLİRİM.  layout validation>pixel devices.
Bir ConstraintLayout'ta herhangi bir görünüm için match_parent kullanamazsınız. Bunun yerine 'eşleşme kısıtlamaları' (0dp) kullanın.

match-constrait : diğer constraite göre karar veriyor Mesela biri image’i buttonun diğer kenarlardan uzaklığına göre ayarlayacağım. mesela buttona 300px veriyorum image daha büyk duruyor buttona 400px veriyorum, image daha küçük gözüküyor. 


dp boyut türünü px yaparsak, px farklı boyutlarda kendini iyi ayarlayamıyor yani (adjust) edemiyor. dp kendini her boyuta göre daha iyi dizayn ediyor.

match-parent: boyutu px vermek yerine match-parent verseydik mesela width’i match parent yapsaydık yatayda sağdan sola yayacaktı.



LAYOUT ÇEŞİTLERİ

Linear Layout: En çok kullanılan ve genelde daha çok lazım olan layout çeşididir.Bu layout yapısını ayarladığımızda constrait layout gibi flexible bir yapısı yok. Linear elemanları sıra sıra yerleştirilmesi için üretilmiş.
split edip xml koda geçince android:orientation yazınca bir horizontal çıkar birde vertical çıkar. vertical seçersek mesela image ekledikten sonra buton ekle onu image’ın altına atar butondan sonra text ekle onu da butonun altına atar yani hepsini alt alta ekler.


FRAME LAYOUT

içerisinde kocaman tek bir image yada içerisinde tek bir textview olan görselde kullanılan layout çeşididir. Çokda farklı bir özelliği yoktur.

					RELATİVE LAYOUT
Birbirine bağlı olarak haraket edebilen görünümleri oluşturmaya yarıyor.
mesela iki tane button var biri diğerinin solunda dursun istiyoruz o zaman above ve below parametreleri geliyor below dersek seçtiğimiz butona diğerinin aşağısında duracak. Aşağısına sağına soluna gibi işlemlerde kullanılıyor.
GRİD LAYOUT
XML’den çalışması çok daha rahat bir layout çeşididir. Adından da anlaşılacağı üzere gridlere bölüyor. Sıra ve sütun değerlerine sahipler.
