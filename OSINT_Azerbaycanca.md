# OSINT (Açıq Mənbə Kəşfiyyatı) — Tam Bələdçi

---

## Mündəricat

1. [Giriş — OSINT nədir?](#1-giriş--osint-nədir)
2. [OSINT Dövrü](#2-osint-dövrü)
3. [Əsas Anlayışlar](#3-əsas-anlayışlar)
4. [Google Dork ilə Məlumat Toplama](#4-google-dork-ilə-məlumat-toplama)
5. [Sosial Media və Şəkillərdən Məlumat Toplama](#5-sosial-media-və-şəkillərdən-məlumat-toplama)
6. [Veb Tətbiqləri və DNS-dən Məlumat Toplama](#6-veb-tətbiqləri-və-dns-dən-məlumat-toplama)
7. [İnternet Axtarış Mühərrikləri — Shodan və Censys](#7-i̇nternet-axtarış-mühərrikləri--shodan-və-censys)
8. [Sızdırılmış Məlumatlar, Dark Web və Deep Web Alətləri](#8-sızdırılmış-məlumatlar-dark-web-və-deep-web-alətləri)
9. [OSINT Framework](#9-osint-framework)

---

## 1. Giriş — OSINT nədir?

**OSINT** (Open Source Intelligence — Açıq Mənbə Kəşfiyyatı) — ictimaiyyətə açıq mənbələrdən məlumat toplamaq, təhlil etmək və istifadə etmək prosesidir.

Ənənəvi kəşfiyyat metodlarından fərqli olaraq, OSINT yalnız **açıq mənbələrdən** — yəni hər kəsin əldə edə biləcəyi məlumatlardan istifadə edir. İnternetdəki saytlar, sosial media platformaları, xəbər mənbələri, açıq verilənlər bazaları və digər onlayn resurslar OSINT üçün potensial mənbədir.

### OSINT-in Əhəmiyyəti və Tətbiq Sahələri

Rəqəmsal dövrdə məlumata çıxışın asanlaşması ilə OSINT-in əhəmiyyəti gündən-günə artır. OSINT bir çox sahədə strateji qərar qəbulunun əsas hissəsinə çevrilib:

- **Kibertəhlükəsizlik:** Təcavüzkarlar hücumdan əvvəl zəiflikləri aşkar etmək və kəşfiyyat toplamaq üçün OSINT-dən istifadə edir.
- **Brend reputasiyasının idarəsi**
- **Rəqib analizi**
- **Şəxsi məxfilik qorunması**

### OSINT Alətləri və Texnikaları

OSINT alətləri və texnikaları daim inkişaf edir. Tədqiqatçılar məlumat toplamaq üçün müxtəlif metodlardan istifadə edir:

- Veb scraping (məlumat yığımı)
- Data mining (verilənlərin çıxarılması)
- Sosial media analizi
- Açıq mənbəli kod analizi
- Avtomatlaşdırılmış məlumat toplama

> Ən çox istifadə edilən OSINT alətlərinə misal: **Shodan**, **Maltego**, **Recon-ng**

### Etik və Hüquqi Mülahizələr

OSINT fəaliyyəti zamanı etik və hüquqi cəhətlərə riayət etmək vacibdir:

- Məxfiliyə hörmət etmək
- Qanunlara riayət etmək
- İcazəsiz şəxsi məlumat toplamaq **qeyri-qanuni və etikasızdır**
- Toplanmış məlumat pis niyyətlə və ya şəxslərin məxfiliyini pozmaq üçün istifadə edilməməlidir

---

## 2. OSINT Dövrü

OSINT dövrü — açıq mənbə kəşfiyyatı prosesini **dairəvi model** şəklində təmsil edir. Bu model prosesin davamlı xarakter daşıdığını vurğulayır. OSINT dövrü ümumiyyətlə **5 əsas mərhələdən** ibarətdir:

```
İstiqamət → Toplama → Təhlil → Qiymətləndirmə → Yayım
     ↑                                                  |
     └──────────────────────────────────────────────────┘
```

### 1️⃣ İstiqamət (Direction)

OSINT dövrünün ilk addımı — hədəfin müəyyənləşdirilməsi və əməliyyatın məqsədinin təsviridir.

- Əməliyyatın məqsədləri, əhatəsi və prioritetləri aydınlaşdırılır
- Məqsədlər adətən müəyyən bir təşkilat, şəxs, hadisə və ya mövzu ilə bağlıdır

### 2️⃣ Toplama (Collection)

İstiqamət mərhələsində müəyyən edilmiş hədəflərə doğru məlumat toplama prosesidir.

- İnternetdəki saytlar, sosial media, xəbər mənbələri, açıq verilənlər bazaları istifadə olunur

### 3️⃣ Təhlil (Analysis)

Toplanmış məlumatların ətraflı şəkildə araşdırılması və analiz edilməsi mərhələsidir.

- Məlumatın dəqiqliyi, etibarlılığı və əhəmiyyəti qiymətləndirilir
- Məlumatlar sistemləşdirilir, əlaqəli məlumatlar bir-birinə bağlanır və mənalı nəticələrə çevrilir

### 4️⃣ Qiymətləndirmə (Evaluation)

Analiz prosesi başa çatdıqdan sonra tapıntıların qiymətləndirilməsi və şərh edilməsi mərhələsidir.

- Analiz edilmiş məlumatın mənası, əhəmiyyəti və təsiri müəyyən edilir
- Əməliyyatın məqsədlərinə nail olub-olmadığı qiymətləndirilir

### 5️⃣ Yayım (Dissemination)

Tapıntıların və hesabatların istifadəçilərlə paylaşılması mərhələsidir.

- Nəticələr uyğun formatlarda hazırlanmış hesabatlar vasitəsilə paylaşılır
- Hesabatlar əməliyyatın məqsədinə və hədəf auditoriyanın tələblərinə uyğun hazırlanır

> ⚠️ Hər mərhələdə etik və hüquqi prinsiplərə riayət etmək vacibdir.

---

## 3. Əsas Anlayışlar

### 📂 Açıq Mənbə (Open Source)

İctimaiyyətə açıq və ya əldə edilə bilən istənilən məlumatdır. İnternetdəki saytlar, sosial media platformaları, açıq verilənlər bazaları OSINT üçün potensial mənbədir.

### ✅ Doğrulama (Verification)

OSINT fəaliyyəti zamanı toplanmış məlumatın dəqiqliyini yoxlamaq vacibdir.

- Bir neçə mənbədən çarpaz yoxlama dəqiqliyi artırır
- Saxta və ya yanlış məlumatların yayıldığı internet mühitində doğrulama **həyati əhəmiyyət** daşıyır

### ⛏️ Data Mining (Verilənlərin Çıxarılması)

Böyük verilənlər dəstlərini təhlil edərək mənalı məlumatları çıxarma prosesidir. OSINT kontekstində data mining texnikası internetdəki verilənlər dəstlərini skan etmək və vacib məlumatları aşkar etmək üçün istifadə olunur.

### 🧑‍💼 HUMINT (İnsan Kəşfiyyatı)

Human Intelligence — OSINT ilə yanaşı kəşfiyyat toplama prosesinin bir komponentidir. İnsan mənbələrindən toplanan kəşfiyyatı bildirir. OSINT fəaliyyətlərində insan mənbələri ilə qarşılıqlı əlaqə qurularaq dəyərli məlumatlar əldə edilə bilər.

### 🔍 Metadata Analizi

Fayllarda və ya sənədlərdə gizli və ya vacib məlumatları aşkar etmək məqsədilə aparılan analiz prosesidir. Metadata — məlumat haqqında məlumatdır və OSINT fəaliyyətlərində mühüm rol oynayır.

---

## 4. Google Dork ilə Məlumat Toplama

**Google Dorking** — Google-da xüsusi açar sözlər, operatorlar və simvollardan istifadə edərək qabaqcıl axtarışlar aparmaq metodudur. Bu metodla adətən tapmaq çətin olan və ya gizlənmiş məlumatlara çıxış əldə etmək mümkündür.

### Google Hacking Database (GHDB)

**GHDB** (Google Hacking Database) — kibertəhlükəsizlik mütəxəssisləri və etik hakerlər üçün mühüm resursdur. 2000-ci illərin əvvəlində **Johnny Long** tərəfindən yaradılan GHDB, Google dork-ları və digər axtarış mühərriki sorğularından istifadə edərək sistemlərdəki təhlükəsizlik zəifliklərini tapmağı hədəfləyir.

Verilənlər bazası aşkar edə biləcək məlumatlar:
- Açıq qovluqlar (open directories)
- Səhv konfiqurasiyalar
- Gizli fayllar
- Digər potensial təhlükəsizlik problemləri

> 🔗 Rəsmi GHDB səhifəsi: [exploit-db.com/google-hacking-database](https://exploit-db.com/google-hacking-database)

---

### Ən Çox İstifadə Edilən Google Dork-lar

| # | Dork | Açıqlama | İstifadə Nümunəsi |
|---|------|----------|-------------------|
| 1 | `site:` | Müəyyən sayt daxilində axtarış edir | `site:example.com` |
| 2 | `filetype:` | Müəyyən fayl növünü axtarır | `filetype:pdf` |
| 3 | `intitle:` | Başlıqda müəyyən sözlər olan səhifələri axtarır | `intitle:"login"` |
| 4 | `inurl:` | URL-də müəyyən sözlər olan səhifələri axtarır | `inurl:admin` |
| 5 | `cache:` | Google-un keşindəki səhifələri göstərir | `cache:example.com` |
| 6 | `link:` | Müəyyən səhifəyə keçid verən səhifələri tapır | `link:example.com` |
| 7 | `related:` | Müəyyən sayta oxşar saytları tapır | `related:example.com` |
| 8 | `intext:` | Səhifə mətni daxilindəki sözləri axtarır | `intext:"password"` |
| 9 | `allintitle:` | Başlıqda bütün göstərilən sözlər olan səhifələri axtarır | `allintitle:login admin` |
| 10 | `allinurl:` | URL-də bütün göstərilən sözlər olan səhifələri axtarır | `allinurl:admin login` |
| 11 | `allintext:` | Mətn daxilindəki bütün göstərilən sözləri axtarır | `allintext:username password` |
| 12 | `define:` | Müəyyən sözün tərifi üçün axtarış edir | `define:OSINT` |
| 13 | `"açar söz"` | Dəqiq ifadəni axtarır | `"admin login"` |
| 14 | `-açar söz` | Müəyyən söz olan səhifələri nəticədən çıxarır | `password -example` |
| 15 | `OR` | İki sözdən birini ehtiva edən səhifələri axtarır | `login OR signup` |
| 16 | `*` | İstənilən söz üçün joker simvol kimi işləyir | `intitle:"admin *"` |
| 17 | `..` | Rəqəm aralığı üçün axtarış edir | `filetype:pdf 2020..2022` |
| 18 | `info:` | Müəyyən sayt haqqında məlumat göstərir | `info:example.com` |
| 19 | `maps:` | Müəyyən yerin xəritəsini göstərir | `maps:New York` |
| 20 | `stocks:` | Müəyyən şirkətin səhm məlumatlarını göstərir | `stocks:GOOG` |

---

### Google Dork İstifadə Nümunələri

#### 1. Müəyyən Sayt Daxilində Axtarış

Saytda xüsusi məlumat axtarmaq üçün. Məsələn, bir saytda əlaqə məlumatı tapmaq:

```
site:example.com "contact information"
```

#### 2. Müəyyən Fayl Növü Axtarışı

PDF formatında gizli sənədlər tapmaq üçün:

```
filetype:pdf "confidential"
```

#### 3. Açıq Qovluqlar və Faylları Tapmaq

```
intitle:"index of /"
```

#### 4. Admin Panellərini Tapmaq

URL-də "admin" olan səhifələri axtarmaq üçün:

```
inurl:admin
```

#### 5. Google Keşindəki Səhifələri Göstərmək

Saytın köhnə versiyalarını görmək üçün:

```
cache:example.com
```

#### 6. Müəyyən Səhifəyə Keçid Verən Saytları Tapmaq

```
link:example.com
```

#### 7. Oxşar Saytları Tapmaq

```
related:example.com
```

#### 8. Səhifə Mətni Daxilindəki Xüsusi Sözləri Axtarmaq

Şifrə kimi kritik məlumatlar tapmaq üçün:

```
intext:"password"
```

#### 9. Başlıqda Göstərilən Sözlər Olan Səhifələri Axtarmaq

Login və admin səhifələrini tapmaq üçün:

```
allintitle:login admin
```

#### 10. URL-də Göstərilən Sözlər Olan Səhifələri Axtarmaq

```
allinurl:admin login
```

#### 11. Səhifə Mətni Daxilindəki Göstərilən Sözləri Axtarmaq

İstifadəçi adı və şifrə ehtiva edən səhifələri tapmaq üçün:

```
allintext:username password
```

#### 12. Müəyyən Sözün Tərifi Üçün Axtarış

Phishing-in tərifi üçün:

```
define:phishing
```

#### 13. Dəqiq İfadə Axtarışı

Gizli sənədlər tapmaq üçün:

```
"confidential document"
```

#### 14. Müəyyən Söz Olmayan Səhifələri Axtarmaq

"password" olan amma "example" olmayan səhifələr:

```
password -example
```

#### 15. İki Sözdən Birini Ehtiva Edən Səhifələr

```
admin OR user
```

#### 16. Joker Simvol İstifadəsi

"admin" ilə başlayan və arxasında istənilən söz olan başlıqları tapmaq:

```
intitle:"admin *"
```

#### 17. Rəqəm Aralığı Axtarışı

2020-2023 illər arasındakı PDF faylları:

```
filetype:pdf 2020..2023
```

#### 18. Sayt Haqqında Məlumat Göstərmək

```
info:google.com
```

#### 19. Açıq Qovluqlar və Onların Məzmunu

```
intitle:"Index of" -inurl:(jsp|pl|php|html|aspx|htm|cf|shtml)
```

#### 20. Açıq Veb Kameralar Tapmaq

Canlı yayım edən vebkameraları tapmaq:

```
inurl:"viewerframe?mode=motion"
```

#### 21. E-poçt Siyahıları Tapmaq

```
filetype:txt @gmail.com OR @yahoo.com
```

#### 22. Zəifliyi Olan Veb Serverləri Tapmaq

Köhnə Windows 2000 serverləri tapmaq:

```
intitle:"Welcome to Windows 2000 Internet Services"
```

#### 23. SQL İnjeksiya Zəifliklərini Tapmaq

```
inurl:index.php?id=
```

#### 24. Şifrə Ehtiva Edən Faylları Tapmaq

```
intitle:"Index of" password.txt
```

#### 25. Admin Giriş Səhifələrini Tapmaq

```
inurl:admin/login
```

#### 26. Açıq phpMyAdmin Panellərini Tapmaq

```
intext:"phpMyAdmin" "running on" inurl:"main.php"
```

#### 27. Açıq FTP Serverlərini Tapmaq

```
intitle:"index of" inurl:ftp
```

#### 28. Açıq Konfiqurasiya Fayllarını Tapmaq

```
intitle:"index of" config.yml
```

#### 29. Açıq Git Repozitoriyaları Tapmaq

```
intitle:index of .git
```

#### 30. Zəifliyi Olan Apache Tomcat Serverləri Tapmaq

```
intitle:"Apache Tomcat" intext:"If you're seeing this, you've successfully"
```

---

## 5. Sosial Media və Şəkillərdən Məlumat Toplama

Sosial media platformaları və şəkil analiz alətləri OSINT proseslərində mühüm rol oynayır.

### 📱 Sosial Media Analizi

#### İstifadəçi Adı ilə Məlumat Toplama

Müxtəlif tətbiqlərdə istifadə edilən istifadəçi adları xüsusi alətlər vasitəsilə aşkar edilə bilər.

**instantusername.com** — istifadəçi adının müxtəlif tətbiqlərdə istifadə edilib-edilmədiyini göstərən saytdır. Şəxslər haqqında araşdırma aparmaq və ya CTF yarışmalarında populyardır.

```
https://instantusername.com/?q=hacker
```

---

#### Sherlock ilə Məlumat Toplama

**Sherlock** — istifadəçinin müxtəlif sosial media və digər platformalardakı istifadəçi adlarını tapmaq üçün istifadə edilən populyar OSINT alətidir. İstifadəçi adlarını müəyyən etməklə hədəfin onlayn mövcudluğuna geniş baxış imkanı verir.

> 🔗 GitHub: [github.com/sherlock-project/sherlock](https://github.com/sherlock-project/sherlock)

---

#### Şəxslər Haqqında Məlumat Toplama

**RocketReach** (rocketreach.co) — şəxslərin peşəkar və əlaqə məlumatlarını tapmaq üçün istifadə edilən bir alətdir. Adətən aşağıdakı məlumatları təqdim edir:

- E-poçt ünvanları
- Telefon nömrələri
- Sosial media profillər

Şirkət və ya şəxsin əlaqə məlumatlarını tapmaq üçün RocketReach-dən istifadə əlaqə qurmağı asanlaşdırır. LinkedIn profilləri işçilərin e-poçt ünvanlarını və digər əlaqə məlumatlarını aşkar etmək üçün istifadə edilə bilər.

---

### 🖼️ Şəkil Analizi

Şəkillər OSINT fəaliyyətləri üçün mühüm məlumat mənbəyidir.

#### Tərs Şəkil Axtarışı (Reverse Image Search)

**Google Images** (images.google.com):
- Şəklin mənbəyini tapmaq
- Eyni şəklin müxtəlif versiyalarını tapmaq
- Şəklin harada istifadə edildiyini öyrənmək
- Profil şəklinin internet üzərindəki istifadə yerlərini aşkar etmək

**TinEye** (tineye.com):
- Şəklin internet tarixçəsini izləmək
- Oxşar şəkilləri tapmaq
- Reklam və ya xəbər şəklinin orijinal mənbəyini müəyyən etmək

**PimEyes** (pimeyes.com):
- Üz tanıma texnologiyasından istifadə edərək şəkillərdəki üzləri aşkar etmək
- Şəxsin şəklini yükləyərək internetdəki eyni şəxsi ehtiva edən digər şəkilləri tapmaq
- Profil şəklinin müxtəlif veb saytlarda istifadə edildiyini müəyyən etmək

---

#### Metadata Analizi — ExifTool

**ExifTool** — şəkil və videoların metadata-sını çıxarmaq və analiz etmək üçün istifadə edilən güclü bir alətdir.

Fotoşəkilin Exif məlumatlarını yoxlayaraq aşağıdakıları öyrənmək mümkündür:
- Şəkili çəkən cihaz
- Çəkilmə tarixi
- GPS koordinatları (yer məlumatı)

**Quraşdırma:**

```bash
sudo apt-get install exiftool
```

**Şəkilin metadata-sını çıxarmaq:**

```bash
exiftool IMG_8153.JPG
```

**Nümunə Çıxış:**

```
ExifTool Version Number         : 12.42
File Name                       : IMG_8153.JPG
File Size                       : 4.2 MB
File Modification Date/Time     : 2024:05:18 14:43:23+03:00
File Type                       : JPEG
Make                            : Apple
Camera Model Name               : iPhone 14 Pro
Software                        : 16.3.1
Modify Date                     : 2023:04:12 17:15:58
ISO                             : 80
Date/Time Original              : 2023:04:12 17:15:58
Focal Length In 35mm Format     : 24 mm
Lens Model                      : iPhone 14 Pro back triple camera 6.86mm f/1.78
Image Size                      : 4032x3024
GPS Altitude                    : 47.2 m Above Sea Level
GPS Latitude                    : 50 deg 50' 30.71" N
GPS Longitude                   : 4 deg 21' 14.96" E
GPS Position                    : 50 deg 50' 30.71" N, 4 deg 21' 14.96" E
```

> 💡 **İzahat:** Bu nümunədə şəkilin **iPhone 14 Pro** ilə 2023-cü il aprelin 12-də çəkildiyini, GPS koordinatlarından isə Belçikanın Brüssel şəhərinin yaxınlığında olduğunu müəyyən etmək mümkündür!

---

## 6. Veb Tətbiqləri və DNS-dən Məlumat Toplama

Veb tətbiqləri və DNS-dən məlumat toplama, kibertəhlükəsizlik və penetrasiya testlərində mühüm bir texnikadır. Bu proses hədəf sistemlər haqqında ətraflı məlumat əldə etmək və potensial zəiflikləri aşkar etmək üçün istifadə olunur.

**Passiv məlumat toplama** — hədəf sistemlə birbaşa əlaqə qurmadan məlumat toplamaq
**Aktiv məlumat toplama** — məlumat əldə etmək üçün hədəfə birbaşa sorğular göndərmək

### 🌐 Əsas Terminlər

**Web (World Wide Web):**
İstifadəçilərə veb brauzerləri vasitəsilə mətn, şəkil, video və digər multimedia məzmununa çıxış imkanı verən internet üzərindən əlçatımlı məlumat sistemidir. HTML (HyperText Markup Language) ilə yaradılmış səhifələrdən ibarətdir və HTTP/HTTPS protokolları vasitəsilə serverlər və müştərilər arasında əlaqə qurur.

**DNS (Domain Name System):**
İnternetdəki cihazların və xidmətlərin adlarını IP ünvanlarına çevirən iyerarxik və paylanmış verilənlər bazası sistemidir. İstifadəçi `www.example.com` yazanda DNS bu domen adını müvafiq IP ünvanına çevirir.

---

### 🔍 Whois

**Whois** — bir veb sayt və ya IP ünvanı haqqında vacib məlumatları toplamağa imkan verən sorğu və cavab protokoludur.

Whois sorğuları aşağıdakıları aşkar edə bilər:
- Domenin sahibi
- Əlaqə məlumatları
- Domenin qeydiyyat tarixi
- Son istifadə tarixi
- Xidmət təminatçısı

Whois sorğuları veb-əsaslı onlayn alətlər və ya komanda xətti vasitəsilə həyata keçirilə bilər. Məşhur saytlar: **ICANN Whois**, **whois.com**, **DomainTools**

**Komanda xətti ilə Whois sorğusu:**

```bash
whois google.com
```

**Nümunə Çıxış:**

```
% IANA WHOIS server
domain:       COM
organisation: VeriSign Global Registry Services
address:      12061 Bluemont Way, Reston VA 20190, United States

contact:      administrative
name:         Registry Customer Service
phone:        +1 703 925-6999
e-mail:       info@verisign-grs.com

nserver:      A.GTLD-SERVERS.NET 192.5.6.30
created:      1985-01-01
changed:      2023-12-07
source:       IANA
```

---

### 🕰️ Internet Archive — Wayback Machine

**Wayback Machine** — internetin rəqəmsal zaman kapsulasıdır. 1996-cı ildən bəri veb səhifələrin arxivlənmiş nüsxələrini saxlayır və istifadəçilərə keçmiş versiyalara çıxış imkanı verir.

> 🔗 Link: [https://web.archive.org/](https://web.archive.org/)

---

### 🛠️ Veb Saytlarda İstifadə Edilən Texnologiyalar

**Brauzer Genişlənmələri:**

- **Wappalyzer** — ziyarət edilən veb saytlarda istifadə edilən texnologiyalar haqqında ani məlumat verir
- **WhatRuns** — oxşar funksionallığa malik genişlənmə

**Komanda Xətti Alətləri:**

`curl` — veb serverlərdən HTTP başlıqlarını sorğulamaq üçün istifadə edilir. Bu başlıqlar server proqramı, CMS sistemi və bəzən proqramlaşdırma dili haqqında ipucu verə bilər.

```bash
curl --head https://wordpress.org
```

**Nümunə Çıxış:**

```
HTTP/2 200 
server: nginx
date: Sat, 18 May 2024 12:47:05 GMT
content-type: text/html; charset=UTF-8
x-frame-options: SAMEORIGIN
```

> 💡 Bu nəticə `wordpress.org` saytının **nginx** veb serverində işlədiyini göstərir.

---

### 🤖 robots.txt

İnternetdəki saytlar robotların, axtarış mühərriklərinin və avtomatlaşdırılmış proseslərin saytın müəyyən hissələrinə necə daxil olması lazım olduğunu **robots.txt** faylı vasitəsilə bildirir. Bu fayl saytın kök qovluğunda yerləşir.

```bash
curl --get https://www.youtube.com/robots.txt
```

**Nümunə Çıxış:**

```
# robots.txt file for YouTube
User-agent: *
Disallow: /comment
Disallow: /feeds/videos.xml
Disallow: /live_chat
Disallow: /login
Disallow: /results
Disallow: /signup
Sitemap: https://www.youtube.com/sitemaps/sitemap.xml
```

> 💡 `Disallow` — robotların daxil olmasının qadağan edildiyi yolları göstərir.

---

### 🌐 DNS Enumeration (DNS Sayımı)

**DNS Enumeration** — müəyyən bir hədəf sistemin hücum səthi haqqında daha yaxşı anlayış əldə etmək üçün istifadə edilən kəşfiyyat texnikasıdır. Bu texnika DNS yazı növlərini, host adlarını, IP ünvanlarını əldə etməyi hədəfləyir.

#### DNSdumpster

**DNSdumpster.com** — kibertəhlükəsizlik mütəxəssisləri arasında populyar onlayn alətdir. Müəyyən bir domen üçün ətraflı DNS məlumatı və domen xəritəsi imkanları təqdim edir.

> 🔗 Link: [https://dnsdumpster.com/](https://dnsdumpster.com/)

---

#### `host` Komutu

DNS sorğuları üçün sadə, lakin güclü alətdir. Domen adlarını IP ünvanlarına çevirir, MX (mail) qeydlərini sorğulayır, NS (Name Server) qeydlərini tapır.

```bash
host youtube.com
```

**Çıxış:**

```
youtube.com has address 142.250.187.110
youtube.com has IPv6 address 2a00:1450:4017:810::200e
youtube.com mail is handled by 0 smtp.google.com.
```

---

#### `dig` Komutu

**dig** (Domain Information Groper) — DNS sorğuları üçün daha təkmil alətdir. Qabaqcıl sorğu seçimləri və çıxış formatlama xüsusiyyətləri təqdim edir.

```bash
dig youtube.com
```

**Çıxış:**

```
; <<>> DiG 9.10.6 <<>> youtube.com
;; QUESTION SECTION:
;youtube.com.           IN  A

;; ANSWER SECTION:
youtube.com.    300     IN  A   172.217.17.110

;; Query time: 66 msec
;; SERVER: 8.8.8.8#53(8.8.8.8)
;; WHEN: Sat May 18 15:54:50 +03 2024
```

---

## 7. İnternet Axtarış Mühərrikləri — Shodan və Censys

İnternet axtarış mühərrikləri kibertəhlükəsizlik mütəxəssisləri və penetrasiya testçiləri üçün dəyərli alətlərdir. Bu mühərriklər internetə qoşulmuş cihazların, sistemlərin və xidmətlərin vəziyyətini təhlil etməyə və izləməyə kömək edir.

---

### 🔴 Shodan

**Shodan** — "İnternetin axtarış mühərriki" olaraq tanınan, kibertəhlükəsizlik mütəxəssisləri üçün kritik bir alətdir. Shodan internetə qoşulmuş cihazları və xidmətləri skan edərək onların təhlükəsizlik vəziyyətlərini və zəifliklərini müəyyən etməyə kömək edir.

Hədəf cihazlar:
- IoT (Əşyaların İnterneti) cihazları
- Sənaye idarəetmə sistemləri
- Şəbəkə avadanlığı

> 🔗 Sayt: [shodan.io](https://shodan.io)
> 📖 Bütün filtrlər üçün bələdçi: [shodan.io/search/filters](https://shodan.io/search/filters)

#### Shodan İstifadə Nümunələri

**Cihaz və Xidmətlər Axtarmaq:**
```
apache
```

**Ölkə Koduna Görə Axtarış:**
```
country:DE
```

**Şəhərə Görə Axtarış:**
```
city:San Francisco
```

**ƏS və Xidmət Versiyalarını Müəyyən Etmək:**
```
os:Windows
```

**Port Nömrəsinə Görə Axtarış:**
```
port:22
```

**Xidmət Növünə Görə Axtarış:**
```
service:ssh
```

**Məhsula Görə Axtarış:**
```
product:"Rockwell Automation"
```

**Müəyyən Təşkilata Aid Cihazları Tapmaq:**
```
org:Google
```

**HTTP Başlıqlarına Görə Axtarış:**
```
http.title:"Login"
```

**Zəifliyə Görə Axtarış:**
```
vuln:heartbleed
```

---

### 🔵 Censys

**Censys** — internetin və qoşulmuş cihazların vəziyyətini təhlil etmək və izləmək üçün istifadə edilən güclü axtarış mühərrikidir. İnternetdə fəal xidmət göstərən cihazların və sistemlərin ətraflı inventarını təqdim edir.

> 🔗 Sayt: [search.censys.io](https://search.censys.io)

#### Censys İstifadə Nümunələri

**Açıq Portları Tapmaq:**
```
ip:192.168.1.1
```

**SSL/TLS Sertifikatlarını Yoxlamaq:**
```
domain:google.com and tags:443/https
```

**Xidmət Versiyalarını Müəyyən Etmək:**
```
ip:192.168.1.1 and tags:version
```

**Müəyyən Ölkədəki Cihazları Axtarmaq:**
```
location.country_code:US
```

**Müəyyən Təşkilata Aid Cihazları Tapmaq:**
```
autonomous_system.asn:AS12345
```

**Təhlükəsizlik Zəifliyinə Görə Axtarış:**
```
443.https.tls.cipher_suite: "TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256"
```

**Xidmətə Görə Axtarış (FTP):**
```
services.service_name: "ftp"
```

**Əməliyyat Sisteminə Görə Axtarış:**
```
services.software.product: "Windows"
```

**Yenilənməmiş Versiyaları Tapmaq:**
```
services.software.version: "OpenSSH_7.2p2"
```

**Veb Tətbiqinin Versiyasını Müəyyən Etmək:**
```
services.software.product: "nginx" and services.software.version: "1.14.0"
```

---

## 8. Sızdırılmış Məlumatlar, Dark Web və Deep Web Alətləri

Kibertəhlükəsizlik mütəxəssisləri, penetrasiya testçiləri və tədqiqatçılar üçün sızdırılmış məlumatlarla, dark web və deep web ilə əlaqəli alətlər kritik əhəmiyyət daşıyır.

---

### 🔓 Sızdırılmış Məlumat Alətləri

Bu alətlər sızdırılmış verilənlər bazalarını, istifadəçi məlumatlarını və həssas dataları aşkar etmək üçün istifadə olunur.

**Have I Been Pwned** — istifadəçilərə e-poçt ünvanlarının məlumat sızıntılarına məruz qalıb-qalmadığını yoxlamağa imkan verir. Böyük miqyaslı məlumat sızıntılarına məruz qalan hesabları müəyyən edir.
> 🔗 [haveibeenpwned.com](https://haveibeenpwned.com/)

**Hunter.io** — e-poçt ünvanlarını tapmaq və yoxlamaq üçün istifadə edilən bir alətdir. Xüsusilə şirkətlər daxilindəki işçilərin e-poçt ünvanlarını müəyyən etmək üçün faydalıdır.
> 🔗 [hunter.io](https://hunter.io/)

**Email Verifier** — e-poçt ünvanlarının etibarlılığını və dəqiqliyini yoxlamaq üçün istifadə olunur, phishing və spam hücumlarına qarşı müdafiə təmin edir.
> 🔗 [email-checker.net](https://email-checker.net/)

---

### 🌑 Dark Web Alətləri

**Tor** — internetə anonim şəkildə çıxmaq və dark web saytlarına qoşulmaq üçün istifadə edilən brauzerdir. İstifadəçilərin kimliyini gizlədərək interneti təhlükəsiz gəzməyə imkan verir.
> 🔗 [torproject.org](https://www.torproject.org/)

**Onion Saytları** — dark webdə `.onion` uzantısına malik saytlardır, tez-tez anonim ünsiyyət və ticarət üçün istifadə olunur. Tor brauzeri ilə əlçatımlıdır.

**Ahmia** — Tor şəbəkəsindəki `.onion` saytlarını tapmaq üçün istifadə edilən axtarış mühərrikidir, istifadəçilərə dark web məzmununu kəşf etməyə kömək edir.
> 🔗 [ahmia.fi](https://ahmia.fi/)

---

### 🕳️ Deep Web Alətləri

**DuckDuckGo** — məxfiliyə fokuslanmış axtarış mühərrikidir, deep web-ə çıxış imkanı verir və istifadəçiləri izləmir. Tor şəbəkəsində də istifadə edilə bilər.
> 🔗 [duckduckgo.com](https://duckduckgo.com/)

**Not Evil** — deep web və dark webdə məlumat axtarmaq üçün istifadə edilən axtarış mühərrikidir, Tor şəbəkəsi vasitəsilə əlçatımlıdır.

**Deep Web Technologies** — deep webdəki verilənlər bazalarını və akademik resursları axtarmaq üçün istifadə edilən platformadır, tədqiqatçılar üçün dəyərli məlumat təqdim edir.
> 🔗 [deepwebtech.com](http://www.deepwebtech.com/)

---

### 📋 İstifadə Ssenariləri

**1. Təhlükəsizlik Zəifliyi Aşkarlanması:**
Sızdırılmış məlumatları yoxlamaqla potensial təhlükəsizlik zəiflikləri müəyyən edilə və preventiv tədbirlər görülə bilər.

**2. Anonimlik və Məxfilik:**
Dark web alətləri anonim ünsiyyət və əməliyyatlar üçün istifadə olunur; həm müdafiə, həm də tədqiqat məqsədləri üçün vacibdir.

**3. Dərindən Araşdırma:**
Deep web alətləri standart axtarış mühərriklərinin əldə edə bilmədiyi məlumatlara çıxış imkanı verir; xüsusi məlumat və akademik tədqiqatlar üçün faydalıdır.

**4. Təhlükə Kəşfiyyatı:**
Kiber təhlükə aktorlarının fəaliyyəti dark web və deep webdə izlənilə bilər, proaktiv təhlükəsizlik tədbirlərinin görülməsinə imkan verir.

---

## 9. OSINT Framework

**OSINT Framework** — açıq mənbələrdən məlumat toplama prosesini asanlaşdırmaq üçün hazırlanmış hərtərəfli alət dəstidir. Bu framework kibertəhlükəsizlik mütəxəssisləri, tədqiqatçılar, jurnalistlər və məlumat təhlükəsizliyi mütəxəssisləri üçün faydalıdır.

OSINT Framework müxtəlif onlayn mənbələrdən məlumat toplama və analiz etmə tapşırığını sistematik şəkildə sadələşdirir.

---

### ⭐ Əsas Xüsusiyyətlər

**1. Hərtərəfli Mənbə Siyahısı:**
OSINT Framework yüzlərlə müxtəlif veb sayt və aləti əhatə edən geniş resurs spektri təklif edir:
- E-poçt axtarışı
- Sosial media analizi
- Dark web araşdırmaları
- və daha çox

**2. Kateqoriyalara Bölünmüş Alətlər:**
Framework alətlər və resursları kateqoriyalara ayırır, istifadəçilərin lazım olan məlumata sürətlə çıxışını təmin edir:
- Domen axtarışı
- IP ünvanı izləmə
- Şəxs və sosial media axtarışları

**3. İstifadəçi Dostu İnterfeys:**
Web-əsaslı interfeys istifadəçilərə asanlıqla naviqasiya imkanı verir. Hər alət və ya resursun yanında keçid və qısa açıqlama mövcuddur.

**4. Davamlı Yenilənən Məzmun:**
OSINT Framework yeni mənbələr əlavə olunduqca daim yenilənir. Bu, istifadəçilərin ən müasir və effektiv məlumat toplama alətlərinə çıxışını təmin edir.

---

### 🎯 İstifadə Halları

**Kibertəhlükəsizlik:**
Potensial təhdidləri müəyyən etmək, təhlükəsizlik zəifliklərini aşkar etmək və hədəflənmiş hücumları araşdırmaq üçün istifadə olunur.

**Penetrasiya Testi:**
Hədəf haqqında məlumat toplamaq və potensial zəiflikləri kəşf etmək üçün tətbiq olunur.

**Tədqiqatçılar və Jurnalistlər:**
Müəyyən şəxslər, təşkilatlar və ya mövzular haqqında dərindən araşdırma aparmaq üçün istifadə olunur.

**Rəqəmsal Kriminalistika:**
Araşdırmalarda rəqəmsal sübut toplamaq və rəqəmsal izləri izləmək üçün istifadə olunur.

---

### 🧰 Nümunə Mənbələr və Alətlər

| Kateqoriya | Alətlər |
|------------|---------|
| E-poçt Axtarışı | Hunter.io, Have I Been Pwned |
| Sosial Media Araşdırması | Social-Searcher, Twitter Advanced Search |
| Domen və IP İzləmə | Whois, IPinfo |
| Dark Web və Deep Web | Tor, Ahmia |

OSINT Framework istifadəçilərə geniş məlumat hovuzundan effektiv şəkildə məlumat toplamasına və analiz etməsinə imkan verir. Bu, daha məlumatlı qərarlar qəbul etməyi və daha hərtərəfli araşdırmalar aparmağı mümkün edir.

---

## 📚 Ümumi Xülasə

| Mövzu | Əsas Alətlər |
|-------|-------------|
| OSINT Əsasları | OSINT Cycle, Verification |
| Google Dorking | GHDB, Google Dorks |
| Sosial Media Analizi | Sherlock, RocketReach, instantusername.com |
| Şəkil Analizi | Google Images, TinEye, PimEyes, ExifTool |
| DNS & Web | Whois, dig, host, DNSdumpster, Wayback Machine |
| İnternet Axtarışı | Shodan, Censys |
| Sızdırılmış Məlumatlar | Have I Been Pwned, Hunter.io |
| Dark/Deep Web | Tor, Ahmia, DuckDuckGo |
| Framework | OSINT Framework |

---

> ⚠️ **Xəbərdarlıq:** Bu materialda göstərilən bütün alət və texnikalar yalnız etik məqsədlər üçün — öz sistemlərinizin təhlükəsizliyini yoxlamaq, təhsil almaq və icazəli penetrasiya testləri üçün istifadə edilməlidir. İcazəsiz sistemlərə daxil olmaq **qeyri-qanuni** və **cinayət məsuliyyəti** doğura bilər.
