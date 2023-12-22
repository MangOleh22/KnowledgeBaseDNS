---
title: Genel Bakış
sidebar_position: 1
---

:::info

AdGuard DNS ile, DNS isteklerini çözümlemek ve reklamları, izleyicileri ve kötü amaçlı alan adlarını cihazınıza ulaşmadan önce engellemek için özel DNS sunucularınızı ayarlayabilirsiniz

Hızlı bağlantı: [AdGuard DNS'i dene](https://agrd.io/download-dns)

:::

![Özel AdGuard DNS pano esas](https://cdn.adtidy.org/public/Adguard/Blog/private_adguard_dns/main.png)

## Genel

<iframe width="560" height="315" class="youtube-video" src="https://www.youtube-nocookie.com/embed/ME3_Ms9LO8M" title="YouTube video oynatıcı" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Özel AdGuard DNS, trafik şifreleme ve alan adı engel listeleri de dahil olmak üzere genel bir AdGuard DNS sunucusunun tüm avantajlarını sunar. Ayrıca esnek özelleştirme, DNS istatistikleri ve Ebeveyn denetimi gibi ek özellikler de sunar. Tüm bu seçeneklere kullanıcı dostu bir gösterge pano aracılığıyla kolayca erişilebilir ve yönetilebilir.

### Özel AdGuard DNS'e neden ihtiyacınız var

Bugün internete her şeyi bağlayabilirsiniz: TV'ler, buzdolapları, akıllı ampuller veya hoparlörler. Ancak inkar edilemez kolaylıkların yanı sıra izleyiciler ve reklamlar elde edersiniz. Basit bir tarayıcı tabanlı reklam engelleyici bu durumda sizi korumayacaktır, ancak trafiği filtrelemek, içeriği ve izleyicileri engellemek için ayarlayabileceğiniz AdGuard DNS, sistem genelinde bir etkiye sahiptir.

Bir zamanlar, AdGuard ürün grubu yalnızca [genel AdGuard DNS](../public-dns/overview.md) ve [AdGuard Home](https://github.com/AdguardTeam/AdGuardHome) içeriyordu. Bu çözümler bazı kullanıcılar için iyi çalışıyor, ancak diğerleri için genel AdGuard DNS yapılandırma esnekliğinden yoksunken AdGuard Home basitlikten yoksun. İşte bu noktada özel AdGuard DNS devreye giriyor. Her iki dünyanın da en iyisine sahiptir: özelleştirilebilirlik, kontrol ve bilgi sunar - tümü basit, kullanımı kolay bir pano aracılığıyla.

### Özel ve genel AdGuard DNS arasındaki fark

Burada genel ve özel AdGuard DNS'de bulunan özelliklerin basit bir karşılaştırmasını bulabilirsiniz.

| Genel AdGuard DNS                            | Özel AdGuard DNS                                                                                      |
| -------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| DNS trafik şifreleme                         | DNS trafik şifreleme                                                                                  |
| Önceden belirlenmiş alan adı engel listeleri | Özelleştirilebilir alan adı engel listeleri                                                           |
| -                                            | İçe ve dışa aktarma özelliğine sahip özel DNS filtreleme kuralları                                    |
| -                                            | İstek istatistikleri (DNS isteklerinizin nereye gittiğini görün: hangi ülkeler, hangi şirketler, vb.) |
| -                                            | Ayrıntılı sorgu günlüğü                                                                               |
| -                                            | Ebeveyn denetimi                                                                                      |

## Özel AdGuard DNS nasıl kurulur

### DoH, DoT ve DoQ'yu destekleyen cihazlar için

1. [AdGuard DNS panonuza](https://agrd.io/download-dns) gidin (giriş yapmadıysanız AdGuard hesabınızı kullanarak giriş yapın)
1. *Cihazı bağla* öğesine tıklayın ve ekrandaki talimatları takip edin

:::note Desteklenen platformlar:

- Android
- iOS
- Windows
- Mac
- Linux
- Yönlendiriciler
- Oyun konsolları
- Akıllı TV'ler

:::

AdGuard DNS paneline eklediğiniz her cihazın, modern şifreli DNS protokollerini (DoH, DoT ve DoQ) desteklemesi durumunda kullanılabilecek kendi benzersiz adresi vardır.

### DoH, DoT ve DoQ'yu desteklemeyen cihazlar için

Cihaz şifrelenmiş DNS'i desteklemiyorsa ve düz DNS kullanmanız gerekiyorsa, AdGuard DNS'nin cihazı tanımasına izin vermenin iki yolu daha vardır — özel IP adresleri kullanın veya cihazın IP adresini bağlayın.

:::not

Yalnızca başka seçeneğiniz yoksa düz DNS adreslerini kullanın: bu, DNS isteklerinin güvenliğini azaltır. Düz DNS kullanmaya karar verirseniz, özel IP adresleri seçmenizi öneririz.

:::

#### Özel IP adresleri

AdGuard DNS'e bağladığınız her cihaz için, cihaz ayarlarınıza girebileceğiniz iki özel IPv6 adresi sunulacaktır. Her iki IPv6 adresini kullanmak zorunlu değildir, ancak genellikle cihazlar sizden iki IPv6 adresi girmenizi isteyebilir.

Bunlara bağlandığınızda, AdGuard DNS hangi cihazın DNS istekleri gönderdiğini belirleyebilecek ve bunun için istatistikleri görüntüleyebilecektir. Ve DNS kurallarını özellikle bu cihaz için yapılandırabileceksiniz.

Ne yazık ki, tüm servis sağlayıcılar IPv6 desteği sunmaz ve tüm cihazlar IPv6 adreslerini yapılandırmanıza izin vermez. Eğer durumunuz buysa, Bağlı IP yöntemine güvenmeniz gerekebilir.

#### Bağlı IP

Cihazınızı Bağlı IP üzerinden AdGuard DNS'e bağlarsanız, hizmet bu IP adresinden gelen tüm düz DNS isteklerini bu "cihaza" doğru sayar. Bu bağlantı yöntemiyle, cihazın IP'si her değiştiğinde, yani her yeniden başlatmanın ardından elle veya özel bir program aracılığıyla yeniden bağlanmanız gerekir.

IP bağlamak için tek gereksinim **konut IP adresi olmasıdır**.

:::not

Konut IP adresi, bir konut İSS'sine bağlı bir cihaza atanan IP adresidir. Tipik olarak fiziksel bir konumla ilişkilendirilir ve bireysel evlere veya dairelere atanır. Konut IP adresleri, normal internet kullanıcıları tarafından web'de gezinme, sosyal medya platformlarına erişim, e-posta gönderme veya içerik canlı yayın akışı gibi günlük çevrimiçi etkinlikleri için kullanılır.

:::

Bir konut IP adresini bağlamaya çalışıyorsanız ve AdGuard DNS buna izin vermiyorsa, lütfen support@adguard.com adresinden destek ekibimizle iletişime geçin.

## Özel AdGuard DNS özellikleri

### İstatistikler

*İstatistikler* sekmesinde Özel AdGuard DNS'inize bağlı cihazlar tarafından yapılan DNS sorgularına ilişkin tüm özet istatistikleri görebilirsiniz. İsteklerin toplam sayısını ve coğrafyasını, engellenen isteklerin sayısını, isteklerin yönlendirildiği şirketlerin listesini, istek türlerini ve başlıca istenen alan adlarını gösterir.

![Özel AdGuard DNS panosu istatistikler](https://cdn.adtidy.org/public/Adguard/Blog/private_adguard_dns/statistics.png)

### Trafik istikameti

Bu özellik, cihazlarınız tarafından gönderilen DNS isteklerinin nereye gittiğini gösterir. İstek istikametlerinin haritasını görmenin yanı sıra bilgileri tarihe, cihaza ve ülkeye göre filtreleyebilirsiniz.

![Özel AdGuard DNS panosu trafik](https://cdn.adtidy.org/public/Adguard/Blog/private_adguard_dns/traffic_destination.png)

### Şirketler

Bu sekme, hangi şirketlerin en çok istek gönderdiğini ve hangi şirketlerin en çok engellenen istekleri olduğunu hızlı bir şekilde kontrol etmenizi sağlar.

![Özel AdGuard DNS panosu şirketler](https://cdn.adtidy.org/public/Adguard/Blog/private_adguard_dns/companies.png)

### Sorgu günlüğü

Bu, her bir istekle ilgili bilgileri kontrol edebileceğiniz ve ayrıca istekleri duruma, türe, şirkete, cihaza, zamana, ülkeye göre sıralayabileceğiniz ayrıntılı bir günlüktür.

![Özel AdGuard DNS panosu sorgu günlüğü](https://cdn.adtidy.org/public/Adguard/Blog/private_adguard_dns/query_log.png)

## Sunucu ayarları

Bu bölümde, özel AdGuard DNS'nin çalışmasını özelleştirmenize olanak tanıyan ve internetin tam istediğiniz gibi çalışmasını sağlayan bir dizi ayar bulunur.

### Engel listeleri yönetimi

*Engel listeleri* özelliği, hangi alan adlarını engellemek istediğinizi ve hangilerini istemediğinizi belirtmenize olanak tanır. Farklı amaçlara yönelik çeşitli engel listeleri arasından seçim yapın.

![Özel AdGuard DNS panosu engel listeleri](https://cdn.adtidy.org/public/Adguard/Blog/private_adguard_dns/blocklists.png)

### Güvenlik ayarları

Çevrimiçi dolandırıcıların kullandığı tüm yöntemlerin farkında olsanız bile, yanlışlıkla kötü amaçlı bir bağlantıya tıklama ihtimaliniz her zaman vardır. Kendinizi bu tür durumlardan korumak için *Güvenlik ayarları* öğesine gidin ve burada listelenen seçeneklerin yanındaki kutuları işaretleyin.

*Kötü amaçlı, kimlik avı ve dolandırıcılık alan adlarını engelle* özelliği, özel veri tabanında bulunan alan adlarını engeller. Ve *Yeni kaydedilen alan adlarını engelle* 30 günden daha kısa bir süre önce kaydedilen ve genellikle çevrimiçi gizliliğiniz açısından riskli olduğu düşünülen tüm alan adlarını eneller.

### Ebeveyn denetimi

Çocuğunuzu uygunsuz bulduğunuz çevrimiçi içerikten korumak için *Ebeveyn denetimi* seçeneğini ayarlayın ve etkinleştirin. "Yetişkinlere yönelik içerik" engelleme ve güvenli arama gibi seçeneklere ek olarak, engelleme için etki alanlarını manuel olarak belirleme ve *Ebeveyn kontrolü*'nün buna göre çalışması için bir zamanlama ayarlama olanağı ekledik.

![Ebeveyn denetimi](https://cdn.adtidy.org/public/Adguard/Blog/private_adguard_dns/parental_control.png)

### Kullanıcı kuralları

Binlerce kurala sahip önceden yüklenmiş engel listelerinin yeterli olmadığı durumlar için *Kullanıcı kuralları* adı verilen kullanışlı bir özelliğimiz var. Burada belirli bir alan adını engellemek/engelini kaldırmak için elle özel kurallar ekleyebilir veya özel kural listelerini içe aktarabilirsiniz (bkz. [DNS filtreleme kuralları söz dizimi](../general/dns-filtering-syntax.md)). Listeleri dışa aktarabilirsiniz.

![Özel AdGuard DNS panosu kullanıcı kuralları](https://cdn.adtidy.org/public/Adguard/Blog/private_adguard_dns/import.png)

## Advanced

Here you can set the way AdGuard DNS must respond to blocked domains:

- Default — zero IP address
- NXDOMAIN — the domain does not exist
- REFUSED — the server has refused to process the request
- Custom IP — you can manually specify an IP address

Additionally, you can adjust the *Time to live* (TTL) setting. This parameter defines the time period (in seconds) that a client device caches the response to a DNS request. A higher TTL means that even if a previously blocked domain is unblocked, it may still appear as blocked for a while. A TTL of 0 indicates that the device does not cache responses.

In the Advanced section, there are three options that can be customized:

- Block access to iCloud Private Relay. Devices that use iCloud Private Relay may ignore DNS settings. Enabling this option ensures that AdGuard DNS can effectively protect your device.
- Block Firefox canary domain. This setting prevents Firefox from automatically switching to its DoH resolver when AdGuard DNS is set as the system-wide DNS service.
- Log IP addresses. If this option is enabled, IP addresses associated with incoming DNS requests will be recorded and displayed in the Query log.

### Access settings

Here you can manage an access to your DNS server by configuring the following settings:

- Allowed clients. Specify which clients are permitted to use your DNS server
- Disallowed clients. List clients that are denied to use your DNS server
- Disallowed domains. Specify domain names that will be denied access to your DNS server. Wildcards and DNS filtering rules can also be listed here

By setting up these options, you can control who uses your DNS server and prevent potential DDoS attacks. Requests that are not allowed will not appear in your Query log, and they are free of charge.
