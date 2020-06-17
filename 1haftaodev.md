				|Software Development is not Jenga Game|

![](https://i0.wp.com/www.hasanaytac.net/wp-content/uploads/2019/02/1qfk6AFv4OF1GRd1WZJc25A.jpeg?fit=740%2C300)


 
***\*SOLİD PRENSİPLERİ\****

***\*“Yazılımda sürdürebilirliği sağlayan kurallar bütünü”\****

 

***\*Nedir S\**** ***\*O L I D\**** ***\*?\****

 

SOLİD, projemizin sürdürebilirliğinin olması,yeni teknolojilere ve eklentilere açık olması,yapılacak değişikliğe farklı yerleri etkilemeyip,geliştirmelere açık olmasıdır.

Robert Cecil Martin nam-ı diğer Uncle Bob’un “***\*Yazılımda Kötü Mimari Tasarımı Sorununa Çözüm\****” olarak ortaya çıkan *\*Bağımlılık Yönetimi\**dir. (Dependency Managament)

 

***\*Bağımlılık Yönetimi;\**** 

 

Kötü oluşturulmuş bir projede,***\*genişletilebilirliğin\**** neredeyse mümkün olmaması ***\*sabit\****(immobility:geliştirilen modüllerin tekrar kullanıma uygun olmaması) ve ***\*kırılgan\**** (fragility: yapılacak olan bir değişikliğin,başka bölümleri etkilememesi) bir yapının olmasından dolayı projemizin sürdürülebilirliğinin olmaması durumudur.

 

Her bileşenin kendi sorumluluk alanına sahip olması,başka bir bileşen ile sıkı sıkıya bağlı olmaması bağımlılık yönetiminin en önemli özelliğidir.

 

Bağımlılıklarının azaltılması ve görevlerin teklileştirilmesi,yazılımın bakımını ve genişletilmesini kolaylaştırır.

 

-Solid prensiplerini açıklamadan önce değinmemiz gereken bir kaç kavram var.



 

***\*Refactoring\****; yazılımı daha basit,daha anlaşılır,değiştirilmesi daha kolay bir hale getirmek amacıyla iç yapısında yapılan ve yazılımın dış davranışlarını etkilemeyen değişkenlerdir.

 

 

![](https://miro.medium.com/max/2554/1*ufqp4eDLabgkKTxqi168yA.png) 



***\*Code Smell\**** 

— What? How can code "smell"??
— Well it doesn't have a nose... but it definitely can stink!

 

Yeniden yapılandırılmaya ihtiyaç duyulan kodlar için kodun kötü koktuğu söylenir. Kokular,koddaki temel tasarım ilkelerinin ihlali sonucu ortaya çıkar.Bir kaç ihlal durumu;

 

l Bir çok işten sorumlu üst sınıflar

l Koplaya yapıştır yöntemiyle oluşmuş kod tekrarları

l Iç içe geçmiş karmaşık (if-else,for,while)yapılar

l Bir gün lazım olur düşüncesiyle yazılmış kodlar

l Sınıf olmayı haketmeyen sınıflar

 

 

Bütün bunlara dikkat etmek her yazılımcının ana görevi.

Gelelim prensiplere!



***\*Single Responsibiliyt Principle\****

 

Bir class veya function’a sadece ***\*tek bir sorumluluğu\**** yerine getirilmesine dayanmaktadır.Birden fazla sorumluluk tek bir class/function’a yüklendiği zaman kod büyür ve karmaşık bir yapı halini alır. Karmaşık ve aşırı bir kodun yönetimi zordur ve bu yüzden ***\*kırılganlığı\**** ortaya çıkar. Aynı zamanda ***\*esnekliği\**** bir o kadar da azdır.

Bu prensip göz ardı edildiğinde,kendisi ile ilgili sorumlulukları yerine getiremediği gibi,uyapılan herhangi bir değişiklikte başka bir yer etkilenebilir ve yeniden kullanılabilirliği düşürülmüş olur.

 

***\*Basit bir örnekle\**** açıklamak istersek alanında yapması gerekenden daha fazlası yapılması istediği taktirde bir noktada alanında da hatalara neden olması. 

 

![](https://miro.medium.com/max/516/1*tiSg1rGku05uT1w_DaJEiQ.png) 

 
 

***\*Open/Closed Principle\****



Projemizde kullandığımız varlıkların(class,function,methot) gelişime açık değişime kapalı olma prensibidir. Bir varlığın davranışını değiştirmeden onu genişletmeye dayalıdır. 

Bu prensip;sürdürülebilir ve tekrar kullanılabilir yapıda kod yazmanın temelini oluşturur. 

***\*Open\**** varlık için yeni davranışlar eklenilmesini sağlar. Gereksinimler değiştiğinde,yeni gereksinimlerin karşılanabilmesi için bir varlığa yeni veya farklı davranışlar eklenebilir olmasıdır.

***\*Closed\**** bir varlığın temel özelliklerinin değişime kapalı olmasıdır.

 

 

​       ![](https://image.slidesharecdn.com/openclosedprinciplekata-130915060011-phpapp01/95/open-closed-principle-kata-7-638.jpg?cb=1379225200)

***\*Basit Bir Örnekle\****

 

Herkesin kendine göre çalışma alanları olduğunu varsayalım. Herkes kendi alanında uzman bir şekilde çalışıyor. Günümüz şartları ve gelişim açısından her gün yeni bir bilgiye maruz kalıp bu yönde kendimizi geliştirmemiz gerekiyor. 	Eğer kendimizi geliştirmezsek rekabetin bir adım arasında kalabiliriz. Eğer kendimizi geliştirme yolunda alanımızı da değiştirirsek,farklı alanlara doğru yol alabiliriz. Gelişime açık olup, değişime kapalı olmalıyız. 

 

 

 

***\*Liskov ‘s Substitution Principle\****

 

Kodlarımızda herhangi bir değişiklik yapmaya gerek duymadan alt sınıfları,türetildikleri sınıfların yerine kullanabilmeliyiz.

Türeyen sınıf (alt sınıflar) ana (üst) sınıfın tüm özelliklerini ve methotlarını aynı işlevi gösterecek şekilde kullanabilme ve kendine ait yeni özellikler barındırabilmelidir.

 

 

​    ![](https://stackify.com/wp-content/uploads/2018/04/SOLID-Principles-Liskov-Substitution-1-1280x720.png)

 

***\*Basit Bir Örnekle\****

 

Eğitim-Öğretim yılları içerisinde belirli bir müfredat dahilinde Öğretmen-Öğrenci ilişkisiyle eğitim verilmektedir.Öğretmen’i üst sınıf olarak düşünürsek kendi bünyesinde barındırdığı bilgileri bir alt sınıf olan Öğrenci’ye aktarmakla görevlidir. Bir öğretmenin bir konu üzerinde ki bilgi birikimini öğrencisiyle paylaştığı düşünülürse,öğretmenin tüm özellikleri öğrenciye geçecektir.

 



 

***\*İnterface Segregation Principle\****

 

Sorumlulukların hepsini tek bir arayüze toplamak yerine daha özelleştirilmiş birden fazla arayüz oluşturmayı tercih etmemizi açıklayan prensiptir.

 

 

![](data:image/jpeg;base64,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) 

 

***\*Basit Bir Örnekle\****

 

Bir proje ortaya çıkarmak için ekip oluşturulmuştur. Öncelikle projenin planlanmasıyla başlayıp ekip üyelerine bu şekilde yapılması gereken görevler verilir. Bir kişinin bütün projeyi yapmasını beklemek yerine,görev dağılımı ile iş bölümünü sağlayıp hem zamandan tasarruf edebilir hem projemizi daha kolay bir şekilde bitirebiliriz.

 

 

***\*Dependency Inversion Principle\****

 

Bir sınıfın,metodun ya da özelliğin,onu kullanan diğer sınıflara karşı bağımlılığı en aza indirgenmelidir.Bir alt sınıfta yapılan değişiklik üst sınıfı etkilememelidir. 

 

![img](file:///C:\Users\hp\AppData\Local\Temp\ksohtml8304\wps9.jpg) 

 

 

***\*Basit Bir Örnekle\****

 

Buzdolabımızın kapağının bozulduğunu varsayalım. Teknik servis çağırdığımızda buzdolabı kapağımızın değişimini talep etmek istiyoruz fakat buzdolabı kapağının bu dolaba ait olduğunu ve yerini değiştirebileceğimiz başka kapak olmadığı cevabını alıyoruz. Bu yüzden kapağı değiştirmek isterken buzdolabını da değiştirmek zorunda kalıyoruz.

 

   

 

***\*Microsoft Build 2020 Yenilikleri\****

 ***\*AZURE YENİLİKLERİ\****

 

Microsoft, Azure ARC özellikli Kubernetes’in herkese açık önizlemeisini müşterilerin Kubernetes kümelerini Open Shıft’te dahil olmak üzere Azure Stack hublarında ölçeklendirebilmelerini,organize edebilmelerini ve yönetebilmelerini sağlıyor.

Mıcrosoft ve SUSE Linux Enterprise Server’ı Azure ARC özellikli bir sunucu olarak destekleyerek müşterilerin kolalaştırmasına olanak sağlıyor.

Yeni Azure Stack Hub güncellemeleri filo ve kaynak yönetimini basitleştirecek hale geldi.

Azure Stack Hub Filo Yönetimi, müşterilere tüm Azure Stack Hub dağıtımları için Azure’da tek bir görünüm ve yönetim sağlıyor. 

ManageIQ bulut operatörlerini artık Azure Stack hubdaki kaynakların yönetmelerine ve Azure Stack Hub’ı yönetmek için Redhat teknik araçlarını kullanmalarına izin veriyor.

ManageIQ,Ibm ve Redhat tarafından desteklenen bir platform.

Azure Stack’te Aks Kaynak Sağlayıcısı,müşterilerin Azure Stack Hub’da Kubernetes kümelerini otomatik olarak oluşturmaları için sağlanan bir hizmettir.

Microsoft herhangi bir ölçek için Apılere sahip hızlı NoSQL veritabnı olan Azure Cosmos DB için eklentileri var.Bu eklentilrt müşterilere benzersiz ihtiyaçlarına uygun fiyatlandırma modelleri sağlamak,uygulama geliştirme döngüsünü kısaltmak ve iş yüklerini etkili bir şekilde yönetmek için tasarlanmıştır.

 

 

***\*.NET\****

.Net 5 sürümü için mobil,web,masaüstü,yapay zeka,makine öğrenimi,büyük veri ve loT ile proje geliştirebiliyoruz. Daha az bellek kullanan,daha küçük,daha hızlı çeşitli bulut ve web uygulamalarına sahip olacaktır. 
	Geliştiricilerin JAvaScript yerine c# ile etkileşimli web UI’leri oluşturmasına izin veren ASPçNET Blazor,artık WebAssembly’ı de destekliyor.

 

 

 

***\*Takip Edilmesi Gereken Kişiler\****

 

 ***\*Fatih Kadir Akın\**** 

 

Toolio şirketinde Senior Software 

JavaScript hakkında kitabı var



github.com/f

 

***\*Engin Demiroğ\****

 

Udemy’de en çok oy alan eğitmen

Java,Python,C#,Html,Flutter alanında uzman

 

github.com/engindemirog

  

  

 

***\*HACKATHON\****


***\*Flutter Hackathon\****

27-28th June 2020

 


***\*United Game Jam\****

\#evdekal Oyun Geliştir, 5-7 Haziran 

 

Game Jam’ler oyun geliştirme amaçlı yapılan 48 saat süren bir oyun geliştirme etkinliğidir. United Game Jam’de tüm oyun geliştiriciler online olarak bir araya gelir,ekiptler kurar ve oyun geliştirirler. 

​    

***\*MİCROSOFT BUİLD ETKİNLİKLERİ\****

 

### ***\*C# Today & Tomorrow - Live\****

## ***\*Speakers\**** ***\*:\**** Mads Torgersen

### Program Manager-Microsoft

Mads is the lead designer of the C# language and a program manager at Microsoft.

#### C# 8.0 incelemesi yapılıyor ve C# 9 hakkında düşüncelerini belirtiyorlar.

 

 

### ***\*Create DevOps workspaces in Teams\****

#### ***\*Speakers\**** ***\*:\**** Sid Uppal

### Engineering Manager-Microsoft

Sid is one of the founding members of Microsoft Teams and currently the Engineering Manager responsible for Bots, Message Extensions, Cards, and Connectors support in Teams

 

DevOps ekipleri kurulumu hakkında bilgi veriyor.

 

  

 

***\*DevlerAzure’Da Etkinlikleri\****

 

***\*Yapay Zeka ve Microsoft Azure Cognitive Services\****

***\*Halil Aksu\****

 

Dijital Dönüşüm ve Yapay Zeka

 

Fluid Enterprise ile iş akışından bahsediyor. ***\*Her şey internete bağlanacak\**** görüşünü savunuyor. Amaçlara göre hareket edilmesi gerektiğine vurgu yapıyor. Dijitalleşmenin önemi hakkında bilgi veriyor.

 

***\*DevOps Kültürü ve Azure DevOps\****

***\*Mehmet Kut\****

 

DevOps Kültürü ve Azure DevOps hk.

 

DevOps öncesi bu işin nasıl yapıldığı hakkında,tarihçesi,ne olduğu ve Azure DevOps platformundan bahsedip bir uygulama yapıyor.

 

 

 
