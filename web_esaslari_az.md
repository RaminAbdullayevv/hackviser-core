# Web Əsasları — Tam Bələdçi (Azərbaycanca)

---

## Mündəricat

1. [Giriş — World Wide Web (WWW)](#1-giriş--world-wide-web-www)
2. [İnternet və Web Fərqi](#2-i̇nternet-və-web-fərqi)
3. [Müştəri və Server Modeli](#3-müştəri-və-server-modeli)
4. [Domen Ad Sistemi (DNS)](#4-domen-ad-sistemi-dns)
5. [HTTP Protokolu](#5-http-protokolu)

---

## 1. Giriş — World Wide Web (WWW)

### WWW nədir?

**World Wide Web (WWW)** — internetdə fəaliyyət göstərən, hipermətn sənədlər şəklində təşkil edilmiş nəhəng bir məlumat sistemidir. **Hipermətn (Hypertext)** sənədlərin keçidlər vasitəsilə bir-birinə inteqrasiyasına imkan verir. Bu keçidlər istifadəçilərə bir sənəddən digərinə asanlıqla və sürətlə keçməyə imkan verir.

Yaxşı bir nümunə: Veb səhifədə rastlaşdığınız bir termin və ya mövzu haqqında ətraflı məlumat almaq üçün bir keçidə kliklədiyinizdə, sizi digər əlaqəli səhifəyə yönləndirməsidir.

---

### 1.1 WWW-nin İxtirası

World Wide Web **1989-cu ildə** britaniyalı alim **Tim Berners-Lee** tərəfindən ixtira edildi — bu, inqilabi bir inkişaf idi.

| Detal | Məlumat |
|-------|---------|
| **İxtiraçı** | Tim Berners-Lee |
| **İl** | 1989 |
| **Yer** | CERN (Avropa Nüvə Tədqiqatları Təşkilatı) |
| **Əsas Məqsəd** | Dünya üzrə alimlər arasında avtomatik məlumat mübadiləsini asanlaşdırmaq |

O vaxt Berners-Lee CERN-də kompüter mühəndisi kimi çalışırdı. CERN — 100-dən çox ölkədən 1700-dən çox alimin bir araya gəldiyi beynəlxalq bir tədqiqat icmasıdır. Bu alimlər vaxtlarının bir hissəsini CERN-də, qalanını isə öz ölkələrindəki universitetlərdə və milli laboratoriyalarda keçirirlər. Bu səbəbdən məlumat mübadiləsi üçün etibarlı kommunikasiya vasitələrinə ehtiyac duyurdular.

O dövrdə internet və hipermətn texnologiyaları mövcud idi, lakin heç kim internetdən sənədləri necə əlaqələndirmək və ya paylaşmaq barədə konkret addımlar atmamışdı.

---

### 1.2 WWW-nin Əsas Texnologiyaları

Tim Berners-Lee kompüterlərin bir-birini başa düşməsinə imkan verəcək **üç əsas texnologiyaya** fokuslandı:

| Texnologiya | Tam Adı | Rolu |
|------------|---------|------|
| **HTML** | HyperText Markup Language | Veb səhifələrin strukturunu müəyyən edir |
| **URL** | Uniform Resource Locator | İnternetdəki resursların unikal ünvanını təyin edir |
| **HTTP** | HyperText Transfer Protocol | Məlumatın server ilə müştəri arasında ötürülməsini idarə edir |

Beləliklə, WWW-nin ixtirası arxasındakı fundamental məqsəd mövcud kompüter texnologiyalarını, məlumat şəbəkələrini və hipermətn texnologiyasını istifadəçi dostu və effektiv qlobal bir məlumat sisteminə birləşdirmək idi.

---

## 2. İnternet və Web Fərqi

İnternet və World Wide Web (Web) tez-tez bir-biri ilə qarışdırılır, lakin əslində fərqli anlayışlardır.

---

### 2.1 Müqayisə Cədvəli

| | **İnternet** | **World Wide Web (Web)** |
|-|-------------|------------------------|
| **Tərif** | Dünya üzrə milyonlarla kompüteri birləşdirən nəhəng şəbəkə | İnternetdə fəaliyyət göstərən, məlumatı hipermətn sənədlər vasitəsilə təqdim edən məlumat paylaşım sistemi |
| **Başlanğıc** | 1960-cı illərin sonu (ARPANET layihəsi) | 1989-cu il (Tim Berners-Lee) |
| **Rol** | İnfrastruktur | İnfrastruktur üzərində işləyən tətbiq |
| **Xidmətlər** | E-poçt, fayl köçürmə, ani mesajlaşma, onlayn oyunlar, Web və s. | HTML səhifələri, URL-lər, HTTP protokolu |

---

### 2.2 Əsas Fərq

> **Qısaca:** İnternet müxtəlif kompüterləri birləşdirən geniş bir şəbəkədir, Web isə həmin şəbəkə üzərində işləyən bir xidmətdir — istifadəçilərin məlumata çıxışını asanlaşdırır.

Web bugün o qədər geniş istifadə edilir ki, bəzən İnternetlə sinonim kimi qəbul edilir. Lakin texniki baxımdan, **İnternet infrastrukturu**, **Web isə həmin infrastruktur üzərindəki tətbiqlərdən biridir**.

---

## 3. Müştəri və Server Modeli (Client-Server Model)

İnternet dünyasında **müştəri (client)** və **server** terminləri tez-tez qarşılaşılır. Bu iki termin internetin fundamental prinsipi olan **müştəri-server modelini** müəyyən edir.

---

### 3.1 Model Necə İşləyir?

Bu modeldə:

- **Müştəri (Client)** — serverə məlumat və ya xidmət sorğusu göndərir.
- **Server** — bu sorğunu emal edir və lazımi cavabı müştəriyə göndərir.

Bu qarşılıqlı təsir webin əsasını təşkil edir.

> **Müştəri-server modeli** bütün məlumatları bir yerdə mərkəzləşdirərək əhəmiyyətli xərc üstünlüyü təklif edir, resursların yalnız lazım olduqda istifadə edilməsini təmin edir.

---

### 3.2 Serverlər

Veb saytlar internetdəki serverlərda yerləşdirilir. Bu serverlərin evdə və ya işdə istifadə etdiyimiz kompüterlərdən yeganə fərqi **24/7 işləmək üçün xüsusi olaraq dizayn edilmələridir**. İnternetə qoşulmuş istənilən kompüter də internetdə veb səhifə yayımlaya bilər.

---

### 3.3 Müştərilər (Clients)

Müştərilər — veb saytları göstərə bilən və serverlərlə qarşılıqlı əlaqə qura bilən cihazlardır:

- Fərdi kompüterlər
- Smartfonlar
- Planşetlər

Müştərilər istifadəçilərə veb brauzerlər (məsələn, Google Chrome, Mozilla Firefox, Safari) vasitəsilə veb səhifələrlə qarşılıqlı əlaqə qurmağa imkan verir.

---

### 3.4 Proses Necə Baş Verir?

Bir veb saytı görmək istədiyinizdə:

1. Müştəri serverə **sorğu göndərir**.
2. Bu sorğu ilə veb səhifənin bir **nüsxəsi serverdən yüklənir**.
3. Məzmun veb brauzerdə **göstərilir**.

---

## 4. Domen Ad Sistemi (DNS)

**Domen Ad Sistemi (DNS — Domain Name System)** — istifadəçiləri World Wide Web-dəki veb saytlara, xidmətlərə və resurslara qoşmaqda mühüm rol oynayan İnternet infrastrukturunun kritik bir komponentidir.

Əsas etibarı ilə **DNS — internetin "telefon kitabıdır"**: İstifadəçi dostu domen adlarını (www.example.com kimi) kompüterlərin və şəbəkə cihazlarının bir-birini internetdə tapmaq üçün istifadə etdiyi rəqəmsal IP ünvanlarına (192.0.2.1 kimi) çevirir.

---

### 4.1 DNS-in Tarixi

DNS-in inkişafı ARPANET kimi tanınan internetin ilk günlərində başladı.

| Dövr | Hadisə |
|------|--------|
| **1980-ci illərin əvvəli** | ARPANET host adlarını IP ünvanlarına uyğunlaşdırmaq üçün mərkəzi idarə edilən `hosts.txt` faylından istifadə edirdi |
| **İnternet böyüdükcə** | Bu yanaşma idarəolunmaz hala gəldi |
| **1983** | Paul Mockapetris və Jon Postel RFC 882 və RFC 883 vasitəsilə bugün bildiyimiz DNS-i təqdim etdi — domen adı həlli üçün paylanmış və iyerarxik sistem |

---

### 4.2 Domen Adı Strukturu

Domen adı internetdəki müəyyən bir yeri və ya resursu təmsil edən insan tərəfindən oxuna bilən bir etiketdir. Domen adları nöqtələrlə ayrılmış iyerarxik strukturda qurulur.

Məsələn, `www.example.com` domen adı üç hissədən ibarətdir:

```
www        .    example    .    com
 ↑                ↑              ↑
Alt domen    İkinci səviyyəli   Üst səviyyəli
(Subdomain)      domen           domen (TLD)
```

---

### 4.3 Üst Səviyyəli Domen (TLD — Top-Level Domain)

TLD domen adları iyerarxiyasında ən yüksək səviyyədə yerləşir. Domen adının son hissəsidir.

| TLD | İstifadə |
|-----|---------|
| `.com` | Kommersiya qurumları üçün |
| `.org` | Qeyri-kommersiya təşkilatları üçün |
| `.gov` | Dövlət qurumları üçün |
| `.edu` | Təhsil qurumları üçün |
| `.uk` | Birləşmiş Krallıq (ölkə kodu TLD — ccTLD) |
| `.de` | Almaniya (ölkə kodu TLD — ccTLD) |
| `.photography`, `.guru`, `.tech` | Xüsusi maraqları, sənayeləri hədəfləyən ümumi TLD-lər (gTLD) |

İnternetin ilk günlərində TLD-lər sayca məhdud idi. İnternetin böyüməsi ilə daha çox TLD-nin yaradılmasına ehtiyac yarandı. Bu genişlənmə domen adı sistemini daha çevik və müxtəlif etdi.

---

### 4.4 DNS Server Növləri

DNS sistemi bir domen adını sorğulayarkən 3 əsas oyunçu var:

**1. Səlahiyyətli Ad Serveri (Authoritative Name Server)**

Bu server müəyyən bir domen üçün rəsmi məlumat mənbəyidir. Hər domenin ən azı bir səlahiyyətli ad serveri var:

- Domenin IP ünvanı
- Poçt serverləri (MX qeydləri)
- Alt domenlər (CNAME qeydləri)
- və digər DNS qeydlərini saxlayır

DNS sorğu prosesinin sonunda bu serverə çatılarsa, tələb olunan məlumat birbaşa və qəti olaraq buradan əldə edilir.

**2. Rekursiv Resolver (Recursive Resolver)**

İstifadəçi veb sayta daxil olmaq istədikdə, bu sorğu əvvəlcə rekursiv resolverə gedir. Rekursiv resolver istifadəçi adından lazımi sorğu prosesini həyata keçirir:

- Kök serverlərdən başlayaraq ümumi istinadla başlayır
- İstənilən məlumat tapılana qədər müxtəlif DNS serverləri arasında addım-addım irəliləyir
- Lazımi DNS qeydlərini keşləyərək gələcək sorğuları sürətləndirir

**3. Kök Ad Serverləri (Root Name Servers)**

Bu serverlər internetin DNS iyerarxiyasının zirvəsindədir və bütün TLD-lər üçün ünvan məlumatlarını saxlayır (`.com`, `.net`, `.org` kimi).

Rekursiv resolver bir ünvan üçün hansı TLD serverinə müraciət edəcəyini bilmirsə, əvvəlcə kök ad serverlərinə müraciət edir. Kök ad serverləri sorğunu düzgün TLD serverinə yönləndirmək üçün lazımi ilkin istinad məlumatını təqdim edir.

---

### 4.5 DNS Həlli Prosesi — 7 Addımda

**Addım 1: İstifadəçi kompüterindən DNS Sorğusu**

İstifadəçi brauzerin ünvan çubuğuna `www.example.com` kimi bir URL daxil edir. Bu, müştərinin DNS həlli üçün sorğu yaratmasına səbəb olur. Sorğu əvvəlcə istifadəçinin İnternet Xidmət Provayderinin (ISP) rekursiv resolverinə göndərilir.

**Addım 2: ISP-nin Rekursiv Resolverinə Sorğu**

Rekursiv resolver bu sorğunu alır və əvvəlcə öz keşini bu sorğunun qeydi üçün yoxlayır:
- Uyğun qeyd **tapılarsa** → həll prosesi burada bitir, IP ünvanı birbaşa istifadəçiyə qaytarılır.
- Uyğun qeyd **tapılmazsa** → rekursiv resolver sorğunu həll etmək üçün bir sıra addımlar həyata keçirir.

**Addım 3: Kök DNS Serverinə Sorğu**

Keşdə uyğun qeyd tapılmazsa, rekursiv resolver sorğunu DNS iyerarxiyasının zirvəsindəki Kök Ad Serverinə yönləndirir. Kök server sorğunun hansı Üst Səviyyəli Domen (TLD) DNS Serverinə (məsələn, `.com` üçün) getməli olduğu barədə məlumat verir.

**Addım 4: TLD DNS Serverinə Sorğu**

Kök DNS Serverindən alınan istinad məlumatı ilə rekursiv resolver sorğunu müvafiq TLD DNS Serverinə (məsələn, `.com` üçün) yönləndirir. TLD serveri istənilən domen üçün Səlahiyyətli Ad Serverinin ünvanını verir (məsələn, `example.com`).

**Addım 5: Səlahiyyətli Ad Serverinə Sorğu**

Rekursiv resolver əldə edilmiş məlumatla birbaşa domenin Səlahiyyətli Ad Serverinə sorğu göndərir. Səlahiyyətli server `www.example.com` üçün A qeydi (domenin IP ünvanı) kimi lazımi DNS qeydini saxlayır.

**Addım 6: DNS Qeydi Müştəriyə Qaytarılır**

Səlahiyyətli ad serveri tələb olunan DNS qeydini (IP ünvanını) rekursiv resolverə göndərir. Rekursiv resolver bu məlumatı istifadəçinin kompüterinə ötürür, bu da istifadəçiyə brauzer vasitəsilə istənilən veb sayta daxil olmağa imkan verir.

**Addım 7: Veb Sayta Qoşulma**

İstifadəçinin kompüteri əldə edilmiş IP ünvanından istifadə edərək birbaşa veb saytın serverinə HTTP sorğusu göndərir və veb saytın məzmunu istifadəçiyə təqdim edilir.

```
İstifadəçi → Rekursiv Resolver → Kök Server → TLD Serveri → Səlahiyyətli Server
                                                                      ↓
İstifadəçi ← Rekursiv Resolver ←─────────────────────────── IP Ünvanı
```

---

## 5. HTTP Protokolu

**Hipermətn Ötürmə Protokolu (HTTP — Hypertext Transfer Protocol)** — internetdə məlumat mübadiləsini mümkün edən fundamental bir protokoldur. Veb saytların serverlərdən müştərilərə (adətən veb brauzerlərə) şəbəkə üzərindən ötürülməsinə imkan verir.

Tim Berners-Lee tərəfindən 1990-cı illərin əvvəlində ixtira edilən HTTP, World Wide Web-in əsas dayaqlarından biridir.

HTTP **müştəri-server modelindən** istifadə edir:
- **Müştəri** (istifadəçinin brauzeri) serverə sorğu göndərir.
- **Server** (veb saytı yerləşdirən server) bu sorğuya cavab verir.

Bu sorğu-cavab mexanizmi internetdə veb səhifələrin, şəkillərin, videoların və digər məzmunun ötürülməsinə imkan verir.

---

### 5.1 HTTP Sorğuları (HTTP Requests)

HTTP sorğuları dörd əsas komponentdən ibarətdir:

| Komponent | İzah |
|-----------|------|
| **URL** | Sorğunun göndərildiyi resursun ünvanı |
| **Metod** | Serverin nə etməli olduğunu bildirən əmr |
| **Başlıqlar (Headers)** | Əlavə məlumat və kontekst |
| **Sorğu Gövdəsi (Request Body)** | Serverə göndərilən məlumat (ixtiyari) |

**Nümunə HTTP Sorğusu:**

```http
GET /index.html HTTP/1.1
Host: www.example.com
Cookie: SESSIONID=badb655ebd99ed6c8e58c0a1aab44eb9
```

| Sətir | İzah |
|-------|------|
| `GET /index.html HTTP/1.1` | HTTP Metodu (`GET`), sorğu yolu (`/index.html`) və HTTP versiyası (`HTTP/1.1`) |
| `Host: www.example.com` | Hədəf serverin ünvanı (domen adı və ya IP ünvanı ilə göstərilə bilər) |
| `Cookie: SESSIONID=...` | Müştəri tərəfli məlumat saxlama üçün istifadə edilən cookie başlığı. Veb saytlarda giriş prosesləri çox vaxt cookie-lər vasitəsilə idarə edilir. |

---

### 5.2 HTTP Sorğu Metodları

HTTP sorğu metodları serverə müştərinin serverdən hansı növ əməliyyatı yerinə yetirməsini istədiyini bildirir:

| HTTP Metodu | Təsvir |
|------------|--------|
| **GET** | Resursu əldə etmək üçün istifadə edilir; URL ilə göstərilən resursun məzmununu qaytarır |
| **POST** | Serverə məlumat göndərmək üçün istifadə edilir; adətən forma məlumatlarını göndərmək üçün istifadə edilir |
| **PUT** | Müəyyən bir resursu yaratmaq və ya yeniləmək üçün istifadə edilir |
| **DELETE** | Müəyyən bir resursu silmək üçün istifadə edilir |
| **HEAD** | GET-ə bənzər, lakin resursun özü əvəzinə yalnız başlıqları qaytarır |
| **OPTIONS** | Bir resurs tərəfindən dəstəklənən mövcud HTTP metodlarını sorğulamaq üçün istifadə edilir |
| **PATCH** | Müəyyən bir resursu qismən yeniləmək üçün istifadə edilir |
| **CONNECT** | Müştəri ilə server arasında tunel qurmaq üçün istifadə edilir |
| **TRACE** | Sorğu yolu boyunca mesaj döngüsü-geri testi aparmaq üçün istifadə edilir |

---

### 5.3 HTTP Sorğu Başlıqları (Request Headers)

HTTP sorğu başlıqları HTTP sorğusunun bir hissəsi kimi serverə göndərilən əlavə məlumatı ehtiva edir. Bu başlıqlar sorğunun necə işlənməli olduğu, müştərinin üstünlükləri, göndərilən məzmunun növü və s. haqqında kontekst və əlavə göstərişlər verir.

Başlıqlar `AD=DƏYƏR` formatında yazılır:

```
NAME=VALUE
```

**Nümunə HTTP Başlıqları:**

```http
GET /api/info HTTP/1.1
Host: example.com
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/89.0.4389.82 Safari/537.36
Accept: application/json
Accept-Language: en-US,en;q=0.5
Authorization: Token secret123
Cache-Control: no-cache
Connection: keep-alive
Referer: https://www.google.com/
Pragma: no-cache
```

| Başlıq Adı | Təsvir |
|-----------|--------|
| **Host** | Müştərinin qoşulmağa çalışdığı serverin host adını göstərir |
| **User-Agent** | Sorğu edən müştəri haqqında məlumat verir (bu nümunədə Chrome brauzeri olduğunu göstərir) |
| **Accept** | Müştərinin cavabda qəbul etməyə hazır olduğu MIME növlərini göstərir |
| **Accept-Language** | Cavab üçün üstünlük verilən dil(lər)i göstərir |
| **Authorization** | Autentifikasiya məqsədi ilə giriş tokeni təqdim edir |
| **Cache-Control** | Həm sorğu, həm də cavab üçün keşləmə direktivlərini göstərir |
| **Connection** | Müştəri ilə server arasındakı bağlantını idarə etmək üçün seçimləri göstərir |
| **Referer** | Cari sorğu səhifəsinə istinad edən URL-i göstərir |
| **Pragma** | Sorğu-cavab zənciri boyunca istənilən agentə tətbiq oluna bilən tətbiqə xas direktvlər verir |
| **Content-Type** | Sorğu gövdəsindəki məlumatın MIME növünü göstərir (bu nümunədə GET sorğusu olduğu üçün istifadə edilmir) |

---

### 5.4 HTTP Sorğu Gövdəsi (Request Body)

HTTP sorğu gövdəsi müştəridən serverə göndərilmək üçün paketlənmiş məlumatı ehtiva edir. Adətən `POST`, `PUT`, `PATCH` və oxşar metodlarda istifadə edilir.

Göndərilə bilən məlumat növləri:
- Forma məlumatları
- Fayllar
- JSON və ya XML kimi strukturlaşdırılmış məlumatlar

HTTP sorğu gövdəsinin məzmunu və formatı **Content-Type** başlığı ilə müəyyən edilir. Bu, serverin göndərilən məlumatı necə emal etməli olduğunu başa düşməsinə kömək edir.

**Nümunə — Foto Yükləmə Sorğusu:**

```http
POST /v1/photos/upload HTTP/1.1
Host: api.myphotos.com
x-api-key: API_KEY
Content-Length: 232
Content-Type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW

------WebKitFormBoundary7MA4YWxkTrZu0gW
Content-Disposition: form-data; name="file"; filename="/C:/Users/John/Photos/my_photo.jpg"
Content-Type: image/jpeg

(data)
------WebKitFormBoundary7MA4YWxkTrZu0gW--
```

> Yuxarıdakı sorğuda `C:/Users/John/Photos/my_photo.jpg` yerli kompüterdəki bir foto `POST` metodu ilə `api.myphotos.com` serverindəki `/v1/photos/upload` API endpoint-inə yüklənir. Server bu sorğunu aldıqda, sorğu gövdəsini analiz edəcək və foto verilənlər bazasında yeni bir giriş yaratmaq üçün istifadə edəcək.

---

### 5.5 HTTP Cavabları (HTTP Responses)

HTTP cavabı — müştərinin HTTP sorğusuna veb serverinin verdiyi cavabdır. Bu cavab tələb olunan resursun statusunu, server haqqında məlumatı və ixtiyari olaraq tələb olunan resursu ehtiva edir.

**Nümunə HTTP Cavabı:**

```http
HTTP/1.1 200 OK
Date: Sun, 28 Mar 2023 10:15:00 GMT
Content-Type: application/json
Server: Apache/2.4.39 (Unix) OpenSSL/1.1.1c PHP/7.3.6
Content-Length: 1024

{
    "name": "John Doe",
    "email": "johndoe@example.com"
}
```

İlk sətir (**status sətri**) HTTP versiyasını və sorğunun nəticəsini bildirən status kodunu göstərir.

**Ən Çox İstifadə Edilən Status Kodları:**

| Status Kodu | Məna |
|------------|------|
| **100** | Continue (Davam et) |
| **101** | Switching Protocols (Protokolları dəyiş) |
| **200** | OK (Uğurlu) |
| **201** | Created (Yaradıldı) |
| **202** | Accepted (Qəbul edildi) |
| **203** | Non-Authoritative Information (Qeyri-səlahiyyətli məlumat) |
| **301** | Moved Permanently — Tələb olunan resurs yeni URL-ə daimi köçürülüb |
| **404** | Not Found — Tələb olunan resurs serverdə tapılmadı |
| **500** | Internal Server Error — Server sorğunu emal edərkən xəta baş verdi |

> Nümunədəki `Content-Type: application/json` başlığından cavabın gövdəsinin JSON formatında olduğunu anlaya bilərik. Cavab John Doe adlı istifadəçinin məlumatlarının sorğu nəticəsində qaytarıldığını göstərir.

---

### 5.6 Addım-addım: Veb Sayta Daxil Olmaq

Öyrəndiklərimizi ümumiləşdirərək, bir veb sayta daxil olarkən baş verən addımlara baxaq:

**Addım 1: Veb Brauzeri Açmaq və URL Daxil Etmək**

İnternetə baxmağa başlamaq üçün əvvəlcə veb brauzeri açarsınız və ziyarət etmək istədiyiniz saytın ünvanını — URL (Uniform Resource Locator) — daxil edirsiniz.

```
https://google.com
```

**Addım 2: DNS Sorğusu**

Daxil etdiyiniz URL xatırlamaq asan olan insan tərəfindən oxuna bilən bir ünvandır. Lakin internet şəbəkələri və kompüterlər bu adlar əvəzinə rəqəmsal IP ünvanlarından istifadə edir. Bu səbəbdən brauzeriniz URL-i veb saytı yerləşdirən serverin IP ünvanına çevirmək üçün **DNS sorğusu** həyata keçirir.

**Addım 3: Serverə Sorğu Göndərmək**

DNS sorğusundan əldə edilən IP ünvanı ilə brauzeriniz veb saytı yerləşdirən serverə **HTTP sorğusu** göndərir. Bu sorğu serverdən müəyyən bir səhifənin məzmununu istəyir.

**Addım 4: Serverdən Cavab Almaq**

Veb server brauzerinizin sorğusunu alır və emal edir, tələb olunan veb səhifənin məzmununu **HTTP cavabında** qaytarır. Bu cavab adətən səhifənin necə görünməli olduğunu müəyyən edən **HTML** (Hypertext Markup Language) kodundan ibarətdir.

**Addım 5: Veb Səhifəni Göstərmək**

Brauzeriniz serverdən alınan HTML məzmununu emal edir və onu istifadəçiyə vizual veb səhifə kimi təqdim edir. Bu mərhələdə səhifənin düzgün göstərilməsini təmin etmək üçün əlavə resurslar (şəkillər, CSS faylları, JavaScript faylları və s.) da serverdən tələb oluna bilər.

**Addım 6: Bağlantının Sonlandırılması**

Veb səhifə uğurla yüklənəndən sonra müştəri ilə server arasındakı bağlantı HTTP/1.1-də `keep-alive` xüsusiyyəti istifadə edilmirsə avtomatik olaraq sonlandırılır. İstifadəçi başqa bir keçidə kliklədikdə və ya yeni səhifə sorğusu etdikdə bu proses yenidən başlayır — yeni bir bağlantı qurulur.

```
Brauzer → DNS Sorğusu → IP Ünvanı əldə edilir
    ↓
HTTP Sorğusu → Server
    ↓
HTTP Cavabı (HTML, CSS, JS, şəkillər)
    ↓
Brauzer məzmunu render edir → Veb Səhifə görünür
```

---

*© Web Əsasları — Azərbaycanca Tam Bələdçi | Kibertəhlükəsizlik Laboratoriyası üçün hazırlanmışdır*
