# Kriptologiya — Tam Bələdçi (Azərbaycanca)

---

## Mündəricat

1. [Giriş — Kriptologiya nədir?](#1-giriş--kriptologiya-nədir)
2. [Kriptoqrafiya və Kriptanaliz](#2-kriptoqrafiya-və-kriptanaliz)
3. [Simmetrik Şifrələmə](#3-simmetrik-şifrələmə)
4. [Asimmetrik Şifrələmə](#4-asimmetrik-şifrələmə)
5. [Həş Funksiyaları və Həş Alqoritmləri](#5-həş-funksiyaları-və-həş-alqoritmləri)
6. [Rəqəmsal İmzalar](#6-rəqəmsal-i̇mzalar)
7. [Kriptoqrafik Protokollar](#7-kriptoqrafik-protokollar)
8. [Kriptanaliz Texnikaları](#8-kriptanaliz-texnikaları)

---

## 1. Giriş — Kriptologiya nədir?

**Kriptologiya** — məlumatın məxfiliyini, bütövlüyünü və həqiqiliyini qorumaq üçün riyazi texnikalardan istifadə edən bir elmdir. Kriptologiya iki əsas sahəyə bölünür:

| Sahə | İzah |
|------|------|
| **Kriptoqrafiya** | Məlumatın şifrələnməsi və deşifrə edilməsi texnikalarına fokuslanır |
| **Kriptanaliz** | Şifrələnmiş məlumatın qırılması metodlarını öyrənir |

---

### 1.1 Kriptologiyanın Tarixi

| Dövr | Hadisə |
|------|--------|
| **Qədim Misir** | Heroqliflər məlumat gizlətmə üçün istifadə edilirdi |
| **Roma dövrü** | Sezar şifrəsi kimi sadə şifrələmə metodları istifadə edilirdi |
| **20-ci əsr** | Müasir kriptologiyanın əsasları qoyuldu |
| **II Dünya Müharibəsi** | Enigma maşını və Alan Turinqin işləri — əhəmiyyətli inkişaf |
| **Bugün** | Kriptologiya rəqəmsal dünyanın təhlükəsizliyinin əvəzolunmaz texnologiyasıdır |

---

### 1.2 Kriptologiyanın Əhəmiyyəti və Tətbiqləri

Kriptologiya bu gün informasiya təhlükəsizliyinin onurğa sütununu təşkil edir:

| Sahə | İzah |
|------|------|
| **Kommunikasiya Təhlükəsizliyi** | Bütün internet kommunikasiyalarının məxfiliyi və bütövlüyü kriptoqrafiya vasitəsilə təmin edilir |
| **Məlumat Saxlama Təhlükəsizliyi** | Həssas məlumatın təhlükəsiz saxlanılması üçün şifrələmə texnikaları istifadə edilir |
| **Autentifikasiya** | Kriptoqrafik metodlara əsaslanan rəqəmsal imzalar və sertifikatlar kimlikləri doğrulamaq üçün istifadə edilir |
| **Maliyyə Əməliyyatları** | Onlayn bank və e-ticarət əməliyyatlarının təhlükəsizliyi kriptologiyaya əsaslanır |
| **Hökumət və Hərbi Tətbiqlər** | Gizli və həssas məlumatı qorumaq üçün kriptoqrafiyadan istifadə edilir |

---

### 1.3 Əsas Kriptoqrafik Terminlər

**Şifrələmə və Deşifrə Etmə:**

| Termin | İzah |
|--------|------|
| **Şifrələmə (Encryption)** | Məlumatı oxunmaz formaya çevirmə prosesi. Məlumat alqoritm və açar vasitəsilə şifrələnir. |
| **Deşifrə Etmə (Decryption)** | Şifrələnmiş məlumatı orijinal formasına geri çevirmə prosesi. Bu proses də adətən alqoritm və açardan istifadə edir. |

**Açar və Açar İdarəetməsi:**

| Termin | İzah |
|--------|------|
| **Açar (Key)** | Şifrələmə və deşifrə etmə proseslərində istifadə edilən gizli məlumat. Açar kriptoqrafik alqoritmlərin işləməsi üçün vacibdir. |
| **Açar İdarəetməsi (Key Management)** | Açarların yaradılması, paylanması, saxlanması və məhv edilməsi proseslərini əhatə edir. Təhlükəsiz açar idarəetməsi kriptoqrafiyanın təhlükəsizliyini qorumaq üçün kritikdir. |

**Açıq Açar və Şəxsi Açar:**

| Termin | İzah |
|--------|------|
| **Açıq Açar (Public Key)** | İctimaiyyətə açıq olan və asimmetrik şifrələmə alqoritmlərində istifadə edilən açar |
| **Şəxsi Açar (Private Key)** | Yalnız sahibi tərəfindən bilinən və qorunan açar. Təhlükəsiz kommunikasiyanı təmin etmək üçün açıq açarla birgə istifadə edilir. |

**Kriptoqrafik Alqoritmlər və Protokollar:**

| Termin | Nümunələr |
|--------|-----------|
| **Kriptoqrafik Alqoritmlər** | Şifrələmə və deşifrə etmə üçün istifadə edilən riyazi metodlar: AES, RSA, DES |
| **Kriptoqrafik Protokollar** | Kriptoqrafik alqoritmlərin təhlükəsiz istifadəsini təmin edən qayda dəstləri: SSL/TLS, SSH, IPsec |

---

## 2. Kriptoqrafiya və Kriptanaliz

### 2.1 Kriptoqrafiya nədir?

**Kriptoqrafiya** — məlumatı təhlükəsiz şəkildə ötürmək və saxlamaq üçün riyazi metodlar və alqoritmlər istifadə edən elmdir.

Kriptoqrafiyanın əsas məqsədləri:

| Məqsəd | İzah |
|--------|------|
| **Məxfilik (Confidentiality)** | Məlumatın yalnız səlahiyyətli şəxslər tərəfindən oxuna bilməsini təmin etmək |
| **Bütövlük (Integrity)** | Məlumatı icazəsiz dəyişikliklərdən qorumaq |
| **Autentifikasiya (Authentication)** | Məlumatın mənbəyini doğrulamaq |
| **İnkar Edilməzlik (Non-repudiation)** | Göndərənin məlumatı göndərdiyini inkar edə bilməməsini təmin etmək |

---

### 2.2 Kriptoqrafiya Növləri

| Növ | İzah |
|-----|------|
| **Simmetrik Kriptoqrafiya** | Həm şifrələmə, həm də deşifrə etmə üçün eyni açardan istifadə edilir |
| **Asimmetrik Kriptoqrafiya** | Şifrələmə və deşifrə etmə üçün fərqli, lakin riyazi olaraq əlaqəli açarlardan (açıq açar və şəxsi açar) istifadə edilir |

---

### 2.3 Kriptanaliz nədir?

**Kriptanaliz** — kriptoqrafik sistemlərdəki zəiflikləri aşkar etmək və onları qırmaq üçün istifadə edilən metodların məcmusudur. Kriptanalizin məqsədi şifrələnmiş məlumatı icazəsiz şəkildə deşifrə etməkdir.

---

### 2.4 Kriptanaliz Növləri

| Növ | İzah |
|-----|------|
| **Qırma Hücumları** | Şifrəmətni deşifrə etmək üçün şifrəmətni və ya açarı əldə etməyə yönəlmiş hücumlar |
| **Analiz Hücumları** | Şifrələmə alqoritmi və ya protokolunun zəifliklərini araşdıran hücumlar |

---

### 2.5 Kriptoqrafiya və Kriptanaliz Arasındakı Fərqlər

| | Kriptoqrafiya | Kriptanaliz |
|-|--------------|------------|
| **Məqsəd** | Məlumatı qorumaq | Qorunan məlumatı əldə etmək |
| **İstifadəçilər** | Məlumatı qorumaq istəyənlər | Qorunan məlumatı deşifrə etməyə çalışanlar |
| **Metodlar** | Riyazi alqoritmlər və protokollar | Bu alqoritm və protokollardakı zəifliklərdən istifadə |

---

### 2.6 Kriptoqrafiyanın Fundamental Prinsipləri

**1. Kerckhoffs Prinsipi:**
> Kriptosisteminin təhlükəsizliyi alqoritmin deyil, açarın gizliliyindən asılı olmalıdır.

**2. Şenonun Qeyri-müəyyənlik Nəzəriyyəsi:**
> Şifrəmətn mənalı statistik strukturlar ehtiva etməməli və təsadüfi görünməlidir.

---

### 2.7 Kriptanaliz Texnikaları (Ümumi Baxış)

| Texnika | İzah |
|---------|------|
| **Kobud Güc Hücumları (Brute Force)** | Düzgün açarı tapmaq üçün bütün mümkün açarları sınamaq |
| **Lüğət Hücumları (Dictionary)** | Tez-tez istifadə olunan söz və şifrələri sınamaq |
| **Yan Kanal Hücumları (Side-Channel)** | Şifrələmə cihazının aldığı vaxt, istifadə etdiyi enerji kimi köməkçi məlumatlardan istifadə |
| **Statistik Hücumlar** | Şifrəmətinin statistik xüsusiyyətlərindən istifadə edərək deşifrə etmək |

---

## 3. Simmetrik Şifrələmə

**Simmetrik şifrələmə** — həm şifrələmə, həm də deşifrə etmə üçün eyni açarın istifadə edildiyi bir şifrələmə üsuludur. Bu üsulda həm göndərən, həm də qəbul edən gizli açarı paylaşır. Simmetrik şifrələmə sürətli və effektivdir, lakin açar paylanması və idarəetməsi sahəsində çətinliklərlə üzləşə bilər.

---

### 3.1 Simmetrik Şifrələmə Alqoritmləri

Simmetrik şifrələmə alqoritmləri iki əsas növə bölünür: **blok şifrələri** və **axın şifrələri**.

#### Blok Şifrələri (Block Ciphers)

Blok şifrələri məlumatı sabit ölçülü bloklarda emal edir, hər blok üzərində müəyyən bir alqoritm və açar istifadə edərək şifrələmə və deşifrə etmə əməliyyatları həyata keçirir.

**1. DES (Data Encryption Standard)**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **İnkişaf etdirən** | IBM, 1970-ci illər |
| **Standart** | 1977-ci ildə ABŞ hökuməti tərəfindən qəbul edildi |
| **Açar uzunluğu** | 56 bit |
| **Vəziyyət** | Kifayətsiz təhlükəsizlik səbəbindən artıq geniş istifadə edilmir |

**2. 3DES (Triple DES)**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **Məqsəd** | DES-in təhlükəsizlik zəifliklərini aradan qaldırmaq üçün inkişaf etdirildi |
| **Prinsip** | DES-dən üç dəfə (şifrələ-deşifrə et-şifrələ) istifadə edir |
| **Açar uzunluğu** | 168 bit |

**3. AES (Advanced Encryption Standard)**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **Standart** | 2001-ci ildə NIST tərəfindən qəbul edildi |
| **Açar uzunluqları** | 128, 192 və 256 bit |
| **Vəziyyət** | Təhlükəsizliyi və sürəti sayəsində geniş istifadə edilir |

---

#### Axın Şifrələri (Stream Ciphers)

Axın şifrələri məlumatı bit və ya bayt axını kimi emal edir. Bu üsul xüsusilə məlumat axınlarının şifrələnməsi üçün uyğundur.

**1. RC4 (Rivest Cipher 4)**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **İnkişaf etdirən** | Ron Rivest, 1987 |
| **Açar uzunluğu** | Dəyişkən |
| **Vəziyyət** | Sürətli və sadədir, lakin bəzi təhlükəsizlik zəifliklərinə malikdir |

**2. Salsa20 və ChaCha20**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **Xüsusiyyət** | Təhlükəsiz və sürətli axın şifrələri |
| **İstifadə** | Mobil və IoT cihazları kimi aşağı güc istehlakı tələb edən mühitlərdə üstünlük verilir |

---

### 3.2 Simmetrik Şifrələmənin Üstünlükləri və Çatışmazlıqları

| | Üstünlüklər | Çatışmazlıqlar |
|-|------------|----------------|
| **Sürət** | Asimmetrik şifrələmə alqoritmlərindən çox daha sürətlidir | — |
| **Effektivlik** | Daha az hesablama resursu tələb edir | — |
| **Sadəlik** | Alqoritmlər və tətbiqlər ümumiyyətlə daha sadədir | — |
| **Açar Paylanması** | — | Açarı təhlükəsiz paylaşmaq və yaymaq çətin ola bilər |
| **Açar İdarəetməsi** | — | Böyük şəbəkələrdə çox sayda açarın idarə edilməsi mürəkkəb ola bilər |
| **Təhlükəsizlik** | — | Açar ələ keçirildikdə bütün şifrələnmiş məlumatlar riskdədir |

---

### 3.3 Blok Şifrəsinin İşləmə Rejimleri

Blok şifrələri təhlükəsizlik və performansı artırmaq üçün fərqli rejimlərda işlədilə bilər:

| Rejim | Tam Adı | İzah |
|-------|---------|------|
| **ECB** | Electronic Codebook | Hər blok müstəqil şəkildə şifrələnir. Eyni açıq mətn blokları eyni şifrəmətn blokları yaradır. Nümunə təkrarı riskləri səbəbindən təhlükəsiz deyil. |
| **CBC** | Cipher Block Chaining | Hər blok şifrələmədən əvvəl əvvəlki şifrəmətn bloku ilə XOR edilir. Birinci blok üçün başlanğıc vektoru (IV) istifadə edilir. Nümunələri aradan qaldıraraq daha təhlükəsizdir. |
| **CFB** | Cipher Feedback | Şifrələmə alqoritmi axın şifrəsi kimi işləyir. Açıq mətn blokları şifrəmətnlə XOR edilir. |
| **OFB** | Output Feedback | Şifrələmə alqoritmi axın şifrəsi kimi işləyir. Şifrəmətn blokları açıq mətn blokları ilə XOR edilir. |
| **CTR** | Counter | Hər blokun şifrələnməsi üçün sayğac dəyəri istifadə edilir. Bloklar paralel emal edilə bilər, bu da performansı artırır. |

---

### 3.4 Simmetrik Şifrələmənin Tətbiqləri

| Sahə | İzah |
|------|------|
| **Məlumat Saxlama** | Fayl və disk şifrələmə |
| **Kommunikasiya** | VPN və SSL/TLS protokolları |
| **Autentifikasiya** | Açar idarəetmə sistemləri |

---

## 4. Asimmetrik Şifrələmə

**Asimmetrik şifrələmə** — şifrələmə və deşifrə etmə prosesləri üçün iki fərqli açarın istifadə edildiyi bir şifrələmə üsuludur. Bu açarlar **açıq açar** və **şəxsi açar** kimi tanınır. Açıq açar hər kəsə əlçatandır, şəxsi açar isə yalnız sahibi tərəfindən bilinir və qorunur. Asimmetrik şifrələmə simmetrik şifrələmə ilə müqayisədə daha təhlükəsizdir, lakin daha yavaşdır.

---

### 4.1 Asimmetrik Şifrələmə Alqoritmləri

**1. RSA (Rivest-Shamir-Adleman)**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **İnkişaf etdirən** | Ron Rivest, Adi Shamir, Leonard Adleman, 1977 |
| **İstifadə** | Həm şifrələmə, həm də rəqəmsal imzalar üçün |
| **Açar uzunluqları** | 1024, 2048 və 4096 bit |
| **Təhlükəsizlik əsası** | Böyük əsas ədədlərin çarpanlara ayrılmasının çətinliyi |

**2. ECC (Elliptic Curve Cryptography — Elliptik Əyri Kriptoqrafiyası)**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **Əsas** | Elliptik əyri nəzəriyyəsi |
| **Müqayisə** | RSA ilə oxşar təhlükəsizlik, lakin daha qısa açar uzunluqları ilə (məsələn, 256 bitlik ECC açarı 2048 bitlik RSA açarına ekvivalent təhlükəsizlik təqdim edir) |
| **İstifadə** | Mobil və IoT cihazları üçün ideal — az hesablama gücü tələb edir |

**3. ElGamal**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **İnkişaf etdirən** | Taher Elgamal, 1985 |
| **İstifadə** | Şifrələmə və rəqəmsal imzalar üçün istifadə oluna bilər |
| **Təhlükəsizlik əsası** | Diskret logaritm probleminin həllinin çətinliyi |

**4. DSA (Digital Signature Algorithm — Rəqəmsal İmza Alqoritmi)**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **Standart** | 1991-ci ildə NIST tərəfindən rəqəmsal imzalar üçün standartlaşdırıldı |
| **İstifadə** | Yalnız rəqəmsal imzaların yaradılması və yoxlanması üçün |
| **Təhlükəsizlik əsası** | Diskret logaritm probleminin həllinin çətinliyi |

---

### 4.2 Asimmetrik Şifrələmənin Üstünlükləri və Çatışmazlıqları

| | Üstünlüklər | Çatışmazlıqlar |
|-|------------|----------------|
| **Açar Paylanması** | Simmetrik şifrələmənin açar paylanması problemləri həll edilir. Açıq açar hər kəslə paylaşıla bilər, şəxsi açar isə sahibinin yanında qalır. | — |
| **Təhlükəsizlik** | İki açarın istifadəsi sistemin təhlükəsizliyini artırır | — |
| **Autentifikasiya** | Rəqəmsal imzalar və sertifikatlar vasitəsilə autentifikasiya təmin edilir | — |
| **Performans** | — | Asimmetrik şifrələmə alqoritmləri simmetrik şifrələmə alqoritmlərindən daha yavaşdır |
| **Hesablama Gücü** | — | Daha çox hesablama resursu tələb edir |

---

### 4.3 İctimai Açar İnfrastrukturu (PKI — Public Key Infrastructure)

**PKI** açıq açarları təhlükəsiz şəkildə yaymaq və idarə etmək üçün rəqəmsal sertifikatlardan və sertifikat orqanlarından (CA) istifadə edir.

**PKI-nin Əsas Komponentləri:**

| Komponent | İzah |
|-----------|------|
| **Sertifikat Orqanları (CA)** | Açıq açarları rəqəmsal sertifikatlarla doğrulayan və təhlükəsizliyini təmin edən təşkilatlar. Sertifikat imzalama və ləğvetmə həyata keçirir. |
| **Qeydiyyat Orqanları (RA)** | Sertifikat orqanları adından autentifikasiya və qeydiyyat proseslərini həyata keçirən təşkilatlar |
| **Rəqəmsal Sertifikatlar** | İstifadəçinin və ya cihazın açıq açarını və kimlik məlumatlarını ehtiva edən rəqəmsal sənədlər. Sertifikat orqanı tərəfindən imzalanır və doğrulanır. |
| **Sertifikat Depozitarları** | Rəqəmsal sertifikatların saxlandığı və idarə edildiyi verilənlər bazaları |

---

### 4.4 Asimmetrik Şifrələmənin Tətbiqləri

| Sahə | İzah |
|------|------|
| **SSL/TLS** | Veb brauzerlər və serverlər arasındakı kommunikasiyanı təhlükəsizləşdirmək üçün istifadə edilir |
| **E-poçt Təhlükəsizliyi** | PGP və S/MIME kimi protokollar vasitəsilə e-poçtların şifrələnməsi və rəqəmsal imzalanması |
| **VPN** | Uzaq şəbəkələr arasında təhlükəsiz kommunikasiya təmin edir |
| **Rəqəmsal Sertifikatlar və Autentifikasiya** | E-ticarət, bank və digər rəqəmsal xidmətlərdə istifadəçi autentifikasiyası üçün istifadə edilir |
| **Fayl və Məlumat Şifrələmə** | Həssas məlumatın təhlükəsiz saxlanması və ötürülməsini təmin edir |

---

## 5. Həş Funksiyaları və Həş Alqoritmləri

**Həş funksiyası** — istənilən uzunluqda giriş götürən və sabit uzunluqda çıxış istehsal edən riyazi bir funksiyadır. Bu çıxış **həş dəyəri** və ya **xülasə (digest)** adlanır.

Həş funksiyalarının əsas xüsusiyyətləri:

| Xüsusiyyət | İzah |
|-----------|------|
| **Deterministik** | Eyni giriş üçün hər dəfə eyni çıxışı istehsal edir |
| **Effektiv** | Girişin ölçüsündən asılı olmayaraq həş dəyərini sürətlə yaradır |
| **Proqnozlaşdırıla bilməz** | Girişdəki kiçik bir dəyişiklik tamamilə fərqli bir həş dəyəri yaradır |
| **Toqquşmaya Davamlı** | İki fərqli girişin eyni həş dəyərini yaratma ehtimalı çox aşağıdır |

---

### 5.1 Həş Funksiyalarının İstifadəsi

| İstifadə | İzah |
|---------|------|
| **Məlumat Bütövlüyünün Yoxlanması** | Faylların və məlumatların bütövlüyünü yoxlamaq üçün istifadə edilir. Məsələn, yüklənmiş faylın orijinalla uyğun olduğunu yoxlamaq üçün həş dəyərləri müqayisə edilir. |
| **Rəqəmsal İmzalar** | Rəqəmsal imzaların yaradılmasında və yoxlanılmasında istifadə edilir |
| **Şifrə Saxlama** | Şifrələri təhlükəsiz saxlamaq üçün istifadə edilir. Şifrələr həş dəyərlərinə çevrilib saxlanılır. |
| **Verilənlər Bazası İndeksləməsi** | Verilənlər bazasında məlumatların indeksləşdirilməsi və sürətli axtarışın asanlaşdırılması üçün istifadə edilir |

---

### 5.2 Həş Alqoritmləri

**1. MD5 (Message Digest Algorithm 5)**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **İnkişaf etdirən** | Ronald Rivest, 1991 |
| **Həş dəyəri** | 128 bit (16 bayt) |
| **Vəziyyət** | Geniş istifadə edilib, lakin təhlükəsizlik zəiflikləri səbəbindən artıq tövsiyə edilmir |
| **Zəiflik** | Zəif toqquşma davamlılığı — fərqli girişlər eyni həş dəyərini yarada bilər |

**2. SHA-1 (Secure Hash Algorithm 1)**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **İnkişaf etdirən** | NSA, 1993 |
| **Həş dəyəri** | 160 bit (20 bayt) |
| **Vəziyyət** | Təhlükəsizlik zəiflikləri səbəbindən tövsiyə edilmir |
| **Zəiflik** | Toqquşma davamlılığı zəiflədi; 2017-ci ildə Google tərəfindən toqquşma tapıldı |

**3. SHA-2 (Secure Hash Algorithm 2)**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **İnkişaf etdirən** | NSA, 2001 |
| **Həş dəyərləri** | SHA-224, SHA-256, SHA-384, SHA-512 (224, 256, 384, 512 bit) |
| **Vəziyyət** | Təhlükəsiz və geniş istifadə edilir |

**4. SHA-3 (Secure Hash Algorithm 3)**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **İnkişaf etdirən** | NIST, 2015 |
| **Həş dəyərləri** | Fərqli uzunluqlar |
| **Xüsusiyyət** | Tamamilə fərqli riyazi struktur istifadə edir (Keccak alqoritmi) |

**5. RIPEMD-160**

| Xüsusiyyət | Dəyər |
|-----------|-------|
| **İnkişaf etdirən** | Leuven Katolik Universiteti, 1996 |
| **Həş dəyəri** | 160 bit |
| **İstifadə** | Alternativ həş alqoritmi kimi istifadə edilir |

---

### 5.3 Həş Funksiyalarının Xüsusiyyətləri

| Xüsusiyyət | İzah |
|-----------|------|
| **Tərsinə Çevrilməzlik (One-Way Property)** | Həş dəyərini orijinal girişə qaytarmaq mümkün olmamalıdır |
| **Toqquşma Davamlılığı (Collision Resistance)** | İki fərqli girişin eyni həş dəyərini yaratması son dərəcə ehtimalsız olmalıdır |
| **Çağlama Effekti (Avalanche Effect)** | Girişdəki kiçik bir dəyişiklik həş dəyərində əhəmiyyətli dəyişikliyə səbəb olmalıdır |
| **Sürət və Effektivlik** | Həş funksiyaları sürətli və effektiv şəkildə işləməlidir |

---

### 5.4 Həş Funksiyalarına Hücum Texnikaları

| Hücum Növü | İzah |
|-----------|------|
| **Toqquşma Hücumları (Collision Attacks)** | Eyni həş dəyərini istehsal edən iki fərqli giriş tapmağı hədəfləyir |
| **Ön şəkil Hücumları (Preimage Attacks)** | Verilmiş həş dəyərinə uyğun bir giriş tapmağı hədəfləyir |
| **İkinci Ön şəkil Hücumları (Second Preimage Attacks)** | Verilmiş girişlə eyni həş dəyərini yaradan fərqli bir giriş tapmağı hədəfləyir |
| **Göy qurşağı Cədvəli Hücumları (Rainbow Table Attacks)** | Şifrələri sındırmaq üçün əvvəlcədən hesablanmış həş dəyərlərindən istifadə edir |

---

## 6. Rəqəmsal İmzalar

**Rəqəmsal imza** — bir sənədin və ya mesajın göndərəninin kimliyini doğrulamaq və məzmunun dəyişdirilmədiyini təmin etmək üçün istifadə edilən kriptoqrafik bir texnikadır. Rəqəmsal imzalar elektron sənədlər və kommunikasiya üçün təhlükəsizliyi təmin etmək üçün asimmetrik şifrələmə alqoritmlərindən istifadə edir.

---

### 6.1 Rəqəmsal İmzaların Məqsədləri

| Məqsəd | İzah |
|--------|------|
| **Autentifikasiya** | Sənədi imzalayan şəxsin kimliyini doğrulamaq |
| **Bütövlük** | Sənədin imzalandıqdan sonra dəyişdirilmədiyini təmin etmək |
| **İnkar Edilməzlik** | Sənədi imzalayan şəxsin onu imzaladığını inkar edə bilməməsini təmin etmək |

---

### 6.2 Rəqəmsal İmzanın İşləmə Prinsipi

**Rəqəmsal İmzanın Yaradılması:**

```
1. Sənədin həş dəyəri hesablanır (SHA-256 kimi təhlükəsiz həş funksiyası ilə)
2. Hesablanmış həş dəyəri göndərənin şəxsi açarı ilə şifrələnir
3. Bu şifrələnmiş həş dəyəri rəqəmsal imza olur
4. Rəqəmsal imza sənədə əlavə edilir və ya onunla birlikdə göndərilir
```

**Rəqəmsal İmzanın Yoxlanması:**

```
1. Qəbul edən həmin həş funksiyasını istifadə edərək sənədin həş dəyərini yenidən hesablayır
2. Qəbul edən göndərənin açıq açarından istifadə edərək rəqəmsal imzanı deşifrə edir
3. Əldə edilən həş dəyəri yenidən hesablanmış həş dəyəri ilə müqayisə edilir
4. İki həş dəyəri uyğun gəlirsə, sənədin bütövlüyü təsdiqlənir və göndərənin kimliyi doğrulanır
```

---

### 6.3 Rəqəmsal İmza Alqoritmləri

| Alqoritm | İzah |
|---------|------|
| **RSA** | Həm şifrələmə, həm də rəqəmsal imza prosesləri üçün istifadə edilir. İmza yaratmaq və yoxlamaq üçün etibarlı alqoritm. |
| **DSA** | 1991-ci ildə NIST tərəfindən rəqəmsal imzalar üçün standartlaşdırıldı. Yalnız rəqəmsal imzaların yaradılması və yoxlanması üçün istifadə edilir. RSA ilə müqayisədə daha sürətli imza yaradır, lakin yoxlama daha yavaşdır. |
| **ECDSA** | Elliptik əyri kriptoqrafiyasına əsaslanır. Daha qısa açar uzunluqları ilə yüksək təhlükəsizlik təmin edir. Mobil və IoT cihazları kimi aşağı güc istehlakı tələb edən mühitlərdə geniş istifadə edilir. |

---

### 6.4 Rəqəmsal Sertifikatlar və PKI

**Rəqəmsal Sertifikatlar** — istifadəçinin və ya cihazın açıq açarını və kimlik məlumatlarını ehtiva edən rəqəmsal sənədlər:
- Sertifikat orqanı (CA) tərəfindən imzalanır və doğrulanır
- X.509 standartına görə strukturlaşdırılmışdır

**Sertifikat Orqanları (CA)** — rəqəmsal sertifikatları imzalayan və doğrulayan etibarlı qurumlar:
- Sertifikat imzalama və ləğvetmə həyata keçirir

**Sertifikat Ləğvetmə Siyahıları (CRL)** — ləğv edilmiş rəqəmsal sertifikatların siyahıları:
- Sertifikat orqanları tərəfindən idarə edilir və dövri olaraq yenilənir

---

### 6.5 Rəqəmsal İmzaların Tətbiqləri

| Sahə | İzah |
|------|------|
| **E-poçt Təhlükəsizliyi** | E-poçt mesajlarının həqiqiliyini və bütövlüyünü yoxlamaq üçün istifadə edilir (PGP, S/MIME) |
| **Elektron Müqavilələr** | Elektron sənəd və müqavilələrin hüquqi bağlayıcılığını təmin edir |
| **Proqram və Fayl Yoxlaması** | Proqram yeniləmələrinin və faylların bütövlüyünü və həqiqiliyini təmin edir |
| **Maliyyə Əməliyyatları** | Elektron bank və maliyyə əməliyyatlarında təhlükəsizlik və autentifikasiya təmin edir |
| **E-hökumət və E-ticarət** | E-hökumət xidmətlərində və elektron ticarət əməliyyatlarında autentifikasiya və məlumat bütövlüyünü təmin edir |

---

### 6.6 Rəqəmsal İmzaların Təhlükəsizliyi

Rəqəmsal imzaların təhlükəsizliyi əsas asimmetrik şifrələmə alqoritminin və həş funksiyasının təhlükəsizliyindən asılıdır:

- **Güclü Kriptoqrafik Alqoritmlər:** RSA, DSA, ECDSA kimi etibarlı alqoritmlər
- **Təhlükəsiz Həş Funksiyaları:** SHA-256 və SHA-3 kimi funksiyalar
- **Açar İdarəetməsi:** Şəxsi açarların təhlükəsiz saxlanması
- **Sertifikat İdarəetməsi:** Rəqəmsal sertifikatların və CRL-lərin müntəzəm yenilənməsi

---

## 7. Kriptoqrafik Protokollar

**Kriptoqrafik protokol** — iki və ya daha çox tərəf arasında kommunikasiyanı təhlükəsizləşdirmək, kimlikləri doğrulamaq, məlumatın bütövlüyünü qorumaq və məxfiliyi təmin etmək üçün nəzərdə tutulmuş qayda və alqoritmlər dəstidir. Bu protokollar kriptoqrafik alqoritm və texnikalarının düzgün və təhlükəsiz tətbiqini təmin edir.

---

### 7.1 Mühüm Kriptoqrafik Protokollar

**1. SSL/TLS (Secure Sockets Layer / Transport Layer Security)**

| Aspekt | Dəyər |
|--------|-------|
| **Məqsəd** | İnternet üzərindəki kommunikasiyaların təhlükəsizliyini təmin etmək |
| **Tətbiqlər** | Veb brauzerlər və serverlər arasında təhlükəsiz kommunikasiya (HTTPS) |

İşləmə Prinsipi:
- **Əl Sıxışma (Handshake):** Tərəflər arasında sessiya açarı qurulur və autentifikasiya həyata keçirilir
- **Şifrələnmiş Kommunikasiya:** Məlumatları şifrələmək və ötürmək üçün sessiya açarından istifadə edilir

Əsas Komponentlər: Asimmetrik şifrələmə, simmetrik şifrələmə, rəqəmsal sertifikatlar, həş funksiyaları

---

**2. IPsec (Internet Protocol Security)**

| Aspekt | Dəyər |
|--------|-------|
| **Məqsəd** | IP paketlərini təhlükəsizləşdirmək |
| **Tətbiqlər** | VPN-lər və şəbəkələrarası təhlükəsiz kommunikasiya |

İşləmə Prinsipi:
- **ESP (Encapsulating Security Payload):** Məlumat məxfiliyini, bütövlüyünü və autentifikasiyanı təmin edir
- **AH (Authentication Header):** Məlumat bütövlüyünü və autentifikasiyanı təmin edir
- **IKE (Internet Key Exchange):** Açar mübadiləsi və təhlükəsizlik assosiasiyalarını idarə edir

---

**3. SSH (Secure Shell)**

| Aspekt | Dəyər |
|--------|-------|
| **Məqsəd** | Təhlükəsiz uzaqdan giriş və idarəetmə təmin etmək |
| **Tətbiqlər** | Serverlərə, routerlərə və digər şəbəkə cihazlarına təhlükəsiz giriş |

İşləmə Prinsipi:
- **Əl Sıxışma:** Təhlükəsiz sessiya başladılır və açar mübadiləsi həyata keçirilir
- **Autentifikasiya:** İstifadəçi autentifikasiyası həyata keçirilir (şifrə, açar əsaslı)
- **Şifrələnmiş Kommunikasiya:** Məlumatları şifrələmək üçün sessiya açarından istifadə edilir

---

**4. PGP (Pretty Good Privacy)**

| Aspekt | Dəyər |
|--------|-------|
| **Məqsəd** | E-poçt kommunikasiyasını təhlükəsizləşdirmək |
| **Tətbiqlər** | E-poçt mesajlarının şifrələnməsi və rəqəmsal imzalanması |

İşləmə Prinsipi:
- **Açar İdarəetməsi:** İstifadəçilər arasında açıq açarlar paylaşılır
- **Şifrələmə:** Mesaj simmetrik şifrələmə ilə şifrələnir, sessiya açarı alıcının açıq açarı ilə şifrələnir
- **Rəqəmsal İmza:** Mesajın həş dəyəri göndərənin şəxsi açarı ilə imzalanır

---

**5. Kerberos**

| Aspekt | Dəyər |
|--------|-------|
| **Məqsəd** | Şəbəkə üzərindən təhlükəsiz autentifikasiya təmin etmək |
| **Tətbiqlər** | Müəssisə şəbəkələrində istifadəçi və xidmət autentifikasiyası |

İşləmə Prinsipi:
- **TGS (Ticket Granting Server):** İstifadəçiyə sessiya açarı və bilet verir
- **Xidmət Bileti:** İstifadəçi xidmətlərə daxil olmaq üçün xidmət biletindən istifadə edir

---

**6. OAuth**

| Aspekt | Dəyər |
|--------|-------|
| **Məqsəd** | Üçüncü tərəf tətbiqlərə avtorizasiya vermək |
| **Tətbiqlər** | Veb tətbiqlər və mobil tətbiqlər |

İşləmə Prinsipi:
- **Avtorizasiya Kodu:** İstifadəçidən avtorizasiya kodu vasitəsilə giriş tokenləri əldə edilir
- **Giriş Tokeni:** Üçüncü tərəf tətbiqləri müəyyən resurslara daxil olmaq üçün giriş tokenindən istifadə edir

---

### 7.2 Kriptoqrafik Protokolların Müqayisəsi

| Protokol | Məqsəd | Əsas İstifadə |
|---------|--------|--------------|
| **SSL/TLS** | İnternet kommunikasiya təhlükəsizliyi | HTTPS, veb trafiyi |
| **IPsec** | IP paket təhlükəsizliyi | VPN, şəbəkələrarası |
| **SSH** | Uzaqdan idarəetmə | Server girişi |
| **PGP** | E-poçt təhlükəsizliyi | Şifrəli e-poçt |
| **Kerberos** | Şəbəkə autentifikasiyası | Müəssisə şəbəkələri |
| **OAuth** | Üçüncü tərəf avtorizasiyası | Veb/mobil tətbiqlər |

---

### 7.3 Kriptoqrafik Protokolların Təhlükəsizliyi

Kriptoqrafik protokolların təhlükəsizliyi aşağıdakı amillərdən asılıdır:

- **Güclü Kriptoqrafik Alqoritmlər:** Təhlükəsiz və müasir şifrələmə alqoritmlərindən istifadə edilməlidir (AES, RSA, SHA-256)
- **Açar İdarəetməsi:** Açarlar təhlükəsiz yaradılmalı, saxlanılmalı və rotasiya edilməlidir
- **Yeniləmələr və Yamaqlar:** Protokol proqramları müntəzəm yenilənməli, zəifliklər aradan qaldırılmalıdır
- **Düzgün Tətbiq:** Protokollar düzgün və standartlara uyğun tətbiq edilməlidir

---

## 8. Kriptanaliz Texnikaları

**Kriptanaliz** — şifrələnmiş məlumatı qırmaq və ya şifrələmə sistemlərindəki zəiflikləri tapmaq elmidir. Kriptanalizin məqsədi şifrələmə metodlarının təhlükəsizliyini yoxlamaq və potensial zəiflikləri müəyyənləşdirməkdir.

---

### 8.1 Kriptanaliz Növləri

**1. Kobud Güc Hücumları (Brute Force Attacks)**

| Aspekt | Dəyər |
|--------|-------|
| **Təsvir** | Düzgün açarı tapmaq üçün bütün mümkün açar kombinasiyalarını sınamaq |
| **Xüsusiyyətlər** | Açar uzunluğundan asılı olaraq çox vaxt və resurs tələb edir |
| **Müdafiə** | Uzun və güclü açarlardan istifadə etmək |

**2. Lüğət Hücumları (Dictionary Attacks)**

| Aspekt | Dəyər |
|--------|-------|
| **Təsvir** | Tez-tez istifadə olunan söz və şifrələri sınamaqla şifrələri sındırmaq |
| **Xüsusiyyətlər** | Şifrə sındırma prosesini sürətləndirmək üçün əvvəlcədən hazırlanmış lüğət faylından istifadə edir |
| **Müdafiə** | Mürəkkəb və təxmin edilməsi çətin şifrələrdən istifadə etmək |

**3. Yan Kanal Hücumları (Side-Channel Attacks)**

| Aspekt | Dəyər |
|--------|-------|
| **Təsvir** | Məlumatı deşifrə etmək üçün kriptosisteminin fiziki xüsusiyyətlərindən (güc istehlakı, zamanlama məlumatları, elektromaqnit sızması kimi) istifadə edir |
| **Xüsusiyyətlər** | Kriptosisteminin mühit məlumatlarını analiz edir. Məsələn, güc istehlakındakı dəyişikliklər açar məlumatı haqqında ipucları verə bilər. |
| **Müdafiə** | Yan kanal hücumlarına qarşı hardware və software təhlükəsizlik tədbirləri tətbiq etmək |

**4. Məlum Açıq Mətn Hücumları (Known Plaintext Attacks)**

| Aspekt | Dəyər |
|--------|-------|
| **Təsvir** | Məlumatı deşifrə etmək üçün şifrəmətni və məlum açıq mətnləri analiz edir |
| **Xüsusiyyətlər** | Şifrəmətndən açıq mətn çıxarmaq üçün şifrələmə alqoritminin zəifliklərindən istifadə edir |
| **Müdafiə** | Güclü və təhlükəsiz şifrələmə alqoritmlərindən istifadə etmək |

**5. Tezlik Analizi (Frequency Analysis)**

| Aspekt | Dəyər |
|--------|-------|
| **Təsvir** | Açıq mətni çıxarmaq üçün şifrəmətindəki simvolların və ya blokların tezliyini analiz edir |
| **Xüsusiyyətlər** | Sezar şifrəsi və Vigenère şifrəsi kimi sadə şifrələmə metodlarına qarşı effektivdir |
| **Müdafiə** | Tezlik analizinə davamlı müasir kriptoqrafik alqoritm və metodlardan istifadə etmək |

**6. Diferensial Kriptanaliz (Differential Cryptanalysis)**

| Aspekt | Dəyər |
|--------|-------|
| **Təsvir** | Şifrələməni qırmaq üçün fərqli girişlərdən yaranan çıxış fərqlərini analiz edir |
| **Xüsusiyyətlər** | Şifrələmə alqoritminin daxili strukturunu və zəifliklərini hədəf alır. Blok şifrələrinə qarşı effektivdir. |
| **Müdafiə** | Diferensial kriptanalizə davamlı olmaq üçün nəzərdə tutulmuş şifrələmə alqoritmlərindən istifadə etmək |

**7. Xətti Kriptanaliz (Linear Cryptanalysis)**

| Aspekt | Dəyər |
|--------|-------|
| **Təsvir** | Şifrələməni qırmaq üçün şifrələmə alqoritminin xətti kombinasiyalarını analiz edir |
| **Xüsusiyyətlər** | Diferensial kriptanalizə bənzər, şifrələmə alqoritminin daxili strukturunu hədəf alır |
| **Müdafiə** | Xətti kriptanalizə davamlı olmaq üçün nəzərdə tutulmuş şifrələmə alqoritmlərindən istifadə etmək |

**8. Ortadakı Adam Hücumları (Man-in-the-Middle — MitM Attacks)**

| Aspekt | Dəyər |
|--------|-------|
| **Təsvir** | Məlumatı deşifrə etmək üçün iki tərəf arasındakı kommunikasiyanı dinləyir və ya dəyişdirir |
| **Xüsusiyyətlər** | Kommunikasiya kanalı üzərində nəzarət tələb edir |
| **Müdafiə** | Təhlükəsiz açar mübadiləsi protokolları və uçdan-uca şifrələmədən istifadə etmək |

---

### 8.2 Kriptanaliz Texnikalarının Müqayisəsi

| Texnika | Hədəf | Effektiv Olduğu Yer | Müdafiə |
|---------|-------|---------------------|---------|
| **Kobud Güc** | Açar | Qısa açarlar | Uzun açarlar |
| **Lüğət** | Şifrə | Sadə şifrələr | Mürəkkəb şifrələr |
| **Yan Kanal** | Fiziki məlumat | Hardware tətbiqləri | Hardware müdafiəsi |
| **Məlum Açıq Mətn** | Alqoritm | Zəif alqoritmlər | Güclü alqoritmlər |
| **Tezlik Analizi** | Nümunələr | Klassik şifrələr | Müasir alqoritmlər |
| **Diferensial** | Alqoritm | Blok şifrələri | Davamlı dizayn |
| **Xətti** | Alqoritm | Blok şifrələri | Davamlı dizayn |
| **MitM** | Kanal | Zəif açar mübadiləsi | E2E şifrələmə |

---

### 8.3 Kriptanaliz Texnikalarının Tətbiqləri

Kriptanaliz texnikaları həm təhlükəsizlik qiymətləndirilməsi, həm də hücum məqsədləri üçün istifadə oluna bilər:

| Sahə | İzah |
|------|------|
| **Təhlükəsizlik Qiymətləndirilməsi** | Şifrələmə sistemlərindəki zəiflikləri müəyyənləşdirmək və onları gücləndirmək |
| **Rəqəmsal Məhkəmə (Digital Forensics)** | Rəqəmsal sübutları deşifrə etmək və analiz etmək |
| **Hərbi və Kəşfiyyat** | Düşmən kommunikasiyalarını deşifrə etmək və analiz etmək |
| **Kiber Hücumlar** | Şifrələmə sistemlərini qırmaq |

---

*© Kriptologiya — Azərbaycanca Tam Bələdçi | Kibertəhlükəsizlik Laboratoriyası üçün hazırlanmışdır*
