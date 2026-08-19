# Kompüter Şəbəkələri — Tam Kurs Materialı (Azərbaycan dilində)

---

## 1. Giriş

**Şəbəkə nədir?**
Şəbəkələr müxtəlif cihazların (kompüterlər, serverlər, mobil cihazlar) bir-biri ilə əlaqə qurub məlumat mübadiləsi etməsini təmin edən rəqəmsal strukturlardır. İnternetin özü milyardlarla cihazı birləşdirən ən böyük şəbəkə nümunəsidir.

---

### Şəbəkə Standartları və Protokolları

Şəbəkədəki cihazlar məlumat göndərərkən və qəbul edərkən eyni prosedurlardan istifadə etməlidir. Bu prosedurlar **protokol** adlanır. TCP/IP, Ethernet, WiFi, HTTP, DNS, DHCP kimi protokollar şəbəkə kommunikasiyasını idarə edir.

---

### Şəbəkə Standartlarını Hazırlayan Qurumlar

| Qurum | Tam adı | Əsas fəaliyyəti |
|-------|---------|-----------------|
| **IEEE** | Institute of Electrical and Electronics Engineers | Elektrik, elektronika və kompüter mühəndisliyi sahəsində standartlar hazırlayır. LAN və MAN üçün IEEE 802 standartı Wi-Fi və Ethernet-in əsasını təşkil edir. |
| **IETF** | Internet Engineering Task Force | İnternetin arxitekturası, işləməsi və inkişafı ilə bağlı standartları müəyyənləşdirir. TCP/IP protokolu üzərində işləyir. Standartları RFC (Request for Comments) sənədləri vasitəsilə nəşr edir. |
| **ISO** | International Organization for Standardization | Beynəlxalq standartlar hazırlayan müstəqil qeyri-hökumət təşkilatı. ISO/IEC 27000 seriyası informasiya təhlükəsizliyi idarəetmə standartlarını əhatə edir. |
| **ITU** | International Telecommunication Union | BMT-nin telekommunikasiya və radio tezliyi idarəetməsi üzrə beynəlxalq standartlar hazırlayan agentliyi. ITU-T texniki standartlar, ITU-R isə radio tezlikləri üzrə standartlar hazırlayır. |
| **ANSI** | American National Standards Institute | ABŞ-da standartlar hazırlayan qurum. Amerika standartlarının beynəlxalq standartlarla uyğunluğunu təmin edir. |
| **W3C** | World Wide Web Consortium | World Wide Web üçün standartlar hazırlayan konsorsium. HTML, CSS, XML kimi veb texnologiyaların standartlarını müəyyənləşdirir. |

---

## 2. Şəbəkə Növləri

Şəbəkələr istifadə sahəsinə və ölçüsünə görə kateqoriyalara bölünür. Əsas üç növ mövcuddur: **LAN**, **MAN** və **WAN**. Aralarındakı ən əhəmiyyətli fərq əhatə etdikləri coğrafi ərazidir.

---

### LAN — Lokal Sahə Şəbəkəsi (Local Area Network)

LAN coğrafi cəhətdən məhdud bir ərazini əhatə edən kompüter şəbəkəsidir. Adətən ev, ofis və ya bina daxilindəki cihazları birləşdirmək üçün istifadə olunur.

**Xüsusiyyətlər:**
- Kiçik ərazini əhatə edir, yüksək sürətli məlumat ötürülməsini təmin edir
- Tipik olaraq Gbps (Gigabit/saniyə) sürətində məlumat ötürür
- Şəbəkədəki cihazlar printer, fayllar kimi ortaq resursları paylaşa bilir
- Şəbəkədəki məlumatların qorunması üçün təhlükəsizlik protokolları tətbiq edilir

---

### WAN — Geniş Sahə Şəbəkəsi (Wide Area Network)

WAN böyük coğrafi ərazilərdə yayılmış kompüter və şəbəkələri birləşdirən şəbəkə növüdür. Şəhərlər, ölkələr və hətta qitələr arasında kommunikasiya imkanı yaradır. İnternetin özü WAN növü hesab olunur.

**Xüsusiyyətlər:**
- LAN-dan fərqli olaraq çox böyük coğrafi əraziləri əhatə edir
- Fiber optik kabellər, peyk əlaqəsi və telefon xətlərindən istifadə olunur
- Qurulma və texniki xidməti adətən bahalıdır
- Məsafənin uzunluğuna görə LAN-dan daha aşağı sürət təklif edir
- Qlobal kommunikasiya və resurs paylaşımını mümkün edir

---

### MAN — Metropolitan Sahə Şəbəkəsi (Metropolitan Area Network)

MAN şəhər miqyasında coğrafi ərazidə yayılmış kompüter şəbəkəsi və cihazları birləşdirən şəbəkə növüdür. WAN ilə LAN arasında yerləşir.

**Xüsusiyyətlər:**
- Adətən bir şəhər qədər böyük ərazini əhatə edir (kilometrlərlə)
- Yüksək bant genişliyi və sürətli məlumat ötürülməsini təmin edir
- Müxtəlif təşkilatlar şəbəkə üzərindən resursları paylaşa bilir
- Spesifik ehtiyaclara uyğun genişləndirilə bilir
- Şəhər idarələri, ictimai təhlükəsizlik, səhiyyə, təhsil qurumları tərəfindən istifadə olunur
- Qurulması və idarəsi İnternet Xidmət Provayderi (İXP) və ya böyük təşkilatların İT departamentləri tərəfindən həyata keçirilir

---

### İnternet və İntranet

**İnternet** — dünya üzrə milyardlarla cihazı birləşdirən nəhəng şəbəkədir. Məlumat mübadiləsi, ünsiyyət və onlayn əməliyyatlar üçün qlobal infrastrukturu təmin edir.

**İntranet** — bir təşkilat daxilindəki məhdud istifadəçi qrupu üçün nəzərdə tutulmuş xüsusi şəbəkədir. Şirkət məlumatlarına, əməkdaş resurslarına və daxili kommunikasiya vasitələrinə giriş üçün istifadə olunur. İnternetdən fərqli olaraq İntranet ictimaiyyətə qapalıdır.

---

## 3. Şəbəkə Cihazları

### Şəbəkə İnterfeys Kartı (NIC — Network Interface Card)

NIC kompüterin şəbəkəyə qoşulmasını təmin edən fiziki hardware komponentidir. Hər NIC-in dünyada bənzərsiz olan, istehsalçı tərəfindən verilmiş **MAC ünvanı** mövcuddur.

**NIC növləri:**

- **Kabel NIC (Wired NIC):** Ethernet kabeli vasitəsilə şəbəkəyə qoşulur. RJ-45 konnektor və ya fiber optik kabel istifadə edə bilər. Daha stabil və təhlükəsiz məlumat ötürülməsi təmin edir.
- **Simsiz NIC (Wireless NIC):** Wi-Fi texnologiyası vasitəsilə simsiz şəbəkəyə qoşulur. Noutbuk, smartfon və planşetlərdə geniş istifadə olunur.

---

### Hub

Hub şəbəkədəki bir neçə cihazı birləşdirmək üçün istifadə olunan şəbəkə cihazıdır. Gələn məlumatı bağlı olan **bütün portlara** göndərir; məlumatın sahibi olan cihaz qəbul edir. Bu seçici olmayan xüsusiyyəti gereksiz şəbəkə sıxıntısına və təhlükəsizlik zəifliklərinə gətirib çıxarır. Kiçik, sadə ev şəbəkələrində istifadə olunur.

---

### Switch (Kommutator)

Switch şəbəkədəki cihazlar arasında məlumat ötürülməsini idarə edən şəbəkə cihazıdır. Məlumatı **yalnız təyinat alıcısına** göndərir. MAC ünvanları əsasında işləyir.

**Üstünlükləri:**
- Hər porta MAC ünvanı təyin edir
- Yalnız lazımi portlara məlumat göndərərək şəbəkə trafikini azaldır
- VLAN dəstəyi, QoS parametrləri kimi xüsusiyyətlər şəbəkə idarəsini asanlaşdırır

**Switch növləri:**

| Növ | Xüsusiyyət | İstifadə sahəsi |
|-----|-----------|-----------------|
| **Unmanaged Switch** | Sadə plug-and-play dizayn, əlavə konfiqurasiya yoxdur | Kiçik şəbəkələr |
| **Managed Switch** | VLAN, QoS, link aggregation kimi qabaqcıl konfiqurasiya imkanları | Böyük, mürəkkəb şəbəkələr |
| **Smart Switch** | Managed switch kimi qabaqcıl xüsusiyyətlər, amma daha asan qurulma | Orta ölçülü şəbəkələr |

---

### Router (Marşrutlaşdırıcı)

Router müxtəlif şəbəkələri birləşdirən və məlumat paketlərini təyinatlarına yönləndirən cihazıdır. **IP ünvanları** əsasında məlumat paketlərini yönləndirir.

- Evdə və ofisdə birdən çox cihazın internet bağlantısını paylaşmasına imkan verir
- Müxtəlif şəbəkələr arasında məlumat axınını idarə edərək təhlükəsizlik təmin edir

---

### Modem

Modem "modulator-demodulator" sözündən yaranıb. İnternet xidmət provayderindən gələn analoq siqnalları rəqəmsal məlumata çevirir (və əksinə). Yeni nəsil modemlər çox vaxt switch və router xüsusiyyətlərini özündə birləşdirir.

**Modem növləri:**

| Növ | Xüsusiyyət |
|-----|-----------|
| **Dial-Up** | Telefon xətti üzərindən, maksimum 56 kbps sürət |
| **DSL** | Telefon xətti üzərindən, daha yüksək sürət (ADSL, VDSL) |
| **Kabel Modem** | TV kabel infrastrukturu üzərindən, DSL-dən yüksək sürət |
| **Fiber Optik** | Fiber optik kabel ilə çox yüksək sürət |
| **Simsiz Modem** | Mobil şəbəkə texnologiyaları (3G, 4G/LTE, 5G) ilə internet |

---

### Giriş Nöqtəsi (AP — Access Point)

AP simsiz cihazların kabel şəbəkəsinə qoşulmasına imkan verir. Wi-Fi siqnallarını qəbul edib Ethernet üzərindən router və ya switch-ə ötürür. Ofis və ictimai yerlərdə geniş ərazili Wi-Fi təmin etmək üçün istifadə olunur.

---

### Firewall (Təhlükəsizlik Divarı)

Firewall əvvəlcədən müəyyən edilmiş təhlükəsizlik qaydaları əsasında giriş-çıxış trafikini izləyən və idarə edən şəbəkə təhlükəsizlik cihazıdır.

**Firewall növləri:**

| Növ | Xüsusiyyət |
|-----|-----------|
| **Paket Filtrasiyası** | IP ünvanı, port nömrəsi və protokola əsasən filtrasiya edir |
| **Stateful Inspection** | Əlaqənin vəziyyətini izləyir, daha dinamik qoruma təmin edir |
| **Application Layer (Proxy)** | Trafiki tətbiq səviyyəsində idarə edir, daha dərin qoruma |
| **Next-Generation (NGFW)** | Ənənəvi firewall + təhdid qarşısının alınması + IPS + dərin paket yoxlaması |

---

### Şəbəkə Kabel Növləri

#### Koaksial Kabel

Köhnə texnologiya; indiki şəbəkə bağlantılarında nadir istifadə olunur (modem bağlantıları istisna). Metal qabığı elektromaqnit müdaxilədən qoruyur.

**Kateqoriyaları (RG):**
- **RG-6:** Müasir kabel TV və geniş zolaqlı kabel modemlər üçün
- **RG-8:** Erkən 10Base5 "Thicknet" Ethernet-də istifadə edilib
- **RG-58:** Erkən 10Base2 "Thinnet" Ethernet-də istifadə edilib
- **RG-59:** CCTV sistemlərində qısa məsafəli video ötürülməsi üçün

**Konnektor növləri:**
- **BNC Connector:** Təhlükəsizlik kameraları, video avadanlıqlar
- **F-Connector:** Kabel TV, peyk qəbuledicilər, modemlər

---

#### Bükülmüş Cüt Kabel (Twisted Pair Cable)

Bükülmüş mis tel cütlərindən ibarət kabel; analoq və rəqəmsal məlumat ötürülməsi üçün geniş istifadə olunur. LAN qurulmasında əsas seçimdir.

**Növləri:**
- **UTP (Unshielded Twisted Pair):** Əlavə qalxan yoxdur; ofis binalarında və evlərdə geniş istifadə olunur
- **STP (Shielded Twisted Pair):** Hər bükülmüş cütün ətrafında metal qalxan var; yüksək elektromaqnit müdaxilə olan sənaye mühitlərində istifadə olunur

**Standartlar (Kateqoriyalar):**

| Kateqoriya | Xüsusiyyətlər |
|-----------|--------------|
| Cat 5 | 100 Mbps, 100 MHz |
| Cat 5e | 1 Gbps, 100 MHz |
| Cat 6 | 1 Gbps (55m-ə qədər 10 Gbps), 250 MHz |
| Cat 6a | 10 Gbps, 500 MHz |
| Cat 7 | 10 Gbps, 600 MHz, ekranlı |

**Konnektor növləri:**
- **RJ-11:** 4 pinli, telefon bağlantıları üçün
- **RJ-45:** 8 pinli, kompüter şəbəkəsi və Ethernet bağlantıları üçün
- **DB-9:** 9 pinli, şəbəkə cihazlarında serial bağlantılar üçün

**TIA/EIA 568A və 568B Standartları:**
- RJ-45 konnektor üçün pin konfiqurasiyasını müəyyənləşdirən sənaye standartları
- **568B** daha yeni və tövsiyə olunan standartdır
- Rəngli tellər müvafiq ardıcıllıqla pinlənir

**Düz və Çarpaz Kabellər:**

| Növ | İstifadə sahəsi |
|-----|----------------|
| **Düz (Straight-Through)** | Kompüterdən switch/router-ə, router-dən switch-ə, hub-dan switch-ə qoşulmaq üçün |
| **Çarpaz (Crossover)** | İki kompüteri birbaşa birləşdirmək, iki switch/hub birləşdirmək, router-to-router bağlantısı üçün |

> **Qeyd:** Müasir şəbəkə cihazlarının əksəriyyəti **Auto-MDIX** xüsusiyyəti ilə avtomatik tənzimləmə edir; kabel növündən asılılıq azalmışdır.

---

#### Fiber Optik Kabel

Fiber optik kabel işıq siqnalları vasitəsilə məlumatı yüksək sürətlə ötürən kommunikasiya vasitəsidir. Elektromaqnit müdaxiləyə qarşı immunitetlidir.

**Növləri:**

| Növ | Məsafə | İstifadə sahəsi |
|-----|--------|----------------|
| **MMF (Multimode Fiber)** | 2 km-ə qədər | LAN, bina-dan binaya |
| **SMF (Singlemode Fiber)** | 200 km-ə qədər | WAN, şəhər miqyasında |

> *Qeyd: 9 mikron SMF 400 Gbps sürətlə 75 mil (120 km) məsafəni keçə bilər.*

**Fiber Optik Konnektor növləri:**
- **LC (Lucent Connector):** MMF və SMF gigabit/10-gigabit Ethernet şəbəkələrində geniş istifadə olunur
- **SC (Subscriber Connector):** MMF və SMF gigabit Ethernet şəbəkələrində istifadə olunur
- **MTRJ (Mechanical Transfer-Registered Jack):** İki fiber optik kabeli yerləşdirir; MMF şəbəkələri üçün nəzərdə tutulub

---

## 4. Şəbəkə Topologiyaları

Şəbəkə topologiyası cihazların (kompüterlər, printerlər, serverlər) şəbəkədə necə birləşdirildiyini və bir-biri ilə necə əlaqə qurduğunu müəyyənləşdirir. Həm fiziki bağlantıları (kabellər, Wi-Fi), həm də məntiqi strukturları (məlumat axını, siqnal yolları) əhatə edir.

---

### Ulduz Topologiyası (Star Topology)

Bütün cihazlar mərkəzi bir nöqtəyə (adətən hub və ya switch) qoşulur.

**Üstünlükləri:**
- Yeni cihaz əlavə etmək və ya nasaz cihazı silmək asandır, qalanlarına təsir etmir
- Tək bir cihazın xarab olması bütün şəbəkəyə təsir etmir

**Çatışmazlıqları:**
- Mərkəzi cihaz xarab olarsa, bütün şəbəkə işdən çıxır

**İstifadə sahəsi:** Ev şəbəkələri, kiçik ofislər

---

### Halqa Topologiyası (Ring Topology)

Hər cihaz dəqiq iki başqa cihaza qoşulur və məlumat tək istiqamətdə dairəvi yol üzrə hərəkət edir.

**Üstünlükləri:**
- Məlumat paketlərinin müəyyən istiqamətdə hərəkəti kolliziyaları azaldır
- Hər cihaz üçün yalnız iki bağlantı tələb olunur

**Çatışmazlıqları:**
- Tək bir xəta bütün şəbəkəni etkiləyə bilər
- Şəbəkənin genişləndirilməsi halqanı qırmağı tələb edir

**İstifadə sahəsi:** MAN-lar və bəzi LAN-lar

---

### Avtobus Topologiyası (Bus Topology)

Bütün cihazlar tək ötürücü xətt (adətən koaksial kabel) paylaşır. Məlumat hər iki istiqamətdə hərəkət edə bilir.

**Üstünlükləri:**
- Tək ötürücü xətt sayəsində kabel xərcləri azdır

**Çatışmazlıqları:**
- Kabel zədələnərsə, xətanı tapmaq çətindir

**İstifadə sahəsi:** Kiçik, müvəqqəti və ya sadə şəbəkə qurulmaları

---

### Ağac Topologiyası (Tree Topology)

Ağac topologiyası ulduz topologiyalarını ierarxik bir tərtipdə birləşdirir; mərkəzi köklü budaqlara bölünən alt-şəbəkələr yaradır.

**Üstünlükləri:**
- Yeni budaqların əlavə edilməsi asandır
- İerarxik quruluş sayəsində alt-şəbəkələrin idarəsi asanlaşır

**Çatışmazlıqları:**
- Yüksək səviyyəli cihazların xarab olması alt-şəbəkələrə təsir edir
- Şəbəkə böyüdükcə kabel tələbatı artır

**İstifadə sahəsi:** Böyük korporativ şəbəkələr, geniş kampus şəbəkələri

---

### Mesh Topologiyası

Cihazlar arasında birdən çox yol mövcuddur. **Tam mesh**-də hər cihaz birbaşa hər digər cihaza qoşulur. **Qismən mesh**-də isə bəzi cihazlar çoxlu bağlantıya malikdir.

**Üstünlükləri:**
- Çoxlu yollar tək xəta nöqtəsinin şəbəkəyə təsirini önləyir
- Məlumat ən səmərəli yolu seçir

**Çatışmazlıqları:**
- Çoxlu bağlantılar kabel və cihaz xərclərini artırır

**İstifadə sahəsi:** Kritik kommunikasiya şəbəkələri, məlumat mərkəzləri

---

### Peer-to-Peer (P2P) Topologiyası

Hər cihaz bərabər statusa malikdir; mərkəzi serverə ehtiyac olmadan birbaşa əlaqə qurulur.

**Üstünlükləri:**
- Yeni cihazlar asanlıqla əlavə edilib inteqrasiya oluna bilər
- Mərkəzi server və ya xüsusi hardware tələb olunmur

**Çatışmazlıqları:**
- Böyük şəbəkələrdə təhlükəsizlik və idarəetmə çətinləşir
- Resurs bölgüsü çətin ola bilər

**İstifadə sahəsi:** Fayl paylaşımı, blockchain texnologiyaları, bəzi paylanmış tətbiqlər

---

### Hibrid Topologiya (Hybrid Topology)

İki və ya daha çox müxtəlif topologiyanın birləşməsidir; hər birinin üstünlüklərindən faydalanır.

**Üstünlükləri:**
- Müxtəlif topologiyaların güclü cəhətlərini birləşdirir
- Tələblərə uyğun asanlıqla genişləndirilə bilər

**Çatışmazlıqları:**
- Müxtəlif topologiyaların inteqrasiyası idarəni çətinləşdirir
- Mürəkkəblik səbəbindən adətən daha bahalıdır

**İstifadə sahəsi:** Böyük korporativ şəbəkələr, mürəkkəb şəbəkə tələbləri olan qurumlar

---

## 5. Kommunikasiya Rejimləri və Növləri

### Kommunikasiya Rejimləri

Ötürücü rejimlər üç kateqoriyaya bölünür:

| Rejim | İzah | Nümunə |
|-------|------|--------|
| **Simplex** | Məlumat yalnız bir istiqamətdə axır. Göndərici daim göndərir, qəbuledici yalnız qəbul edir. | Klaviatura → monitor |
| **Half Duplex** | Məlumat hər iki istiqamətdə ötürülə bilər, lakin eyni anda deyil. | Walkie-talkie |
| **Full Duplex** | Məlumat eyni anda hər iki istiqamətdə axır. Ən səmərəli rejim. | Telefon danışığı, canlı internet söhbəti |

---

### Kommunikasiya Növləri

**Unicast (Tək Alıcıya):**
- Tək göndəricidən tək qəbulediciyə məlumat göndərilməsi
- Şəbəkədəki ən geniş istifadə olunan ötürücü rejim
- Nümunə: Veb serverdən kompüterinizə veb səhifənin yüklənməsi

**Multicast (Qrup Alıcılarına):**
- Tək göndəricidən müəyyən alıcılar qrupuna məlumat göndərilməsi
- Eyni məlumatın birdən çox alıcıya çatdırılması lazım olduqda səmərəli üsul
- Nümunə: Canlı video yayımı eyni anda çoxlu izləyiciyə çatır

**Broadcast (Bütün Alıcılara):**
- Tək göndəricidən şəbəkədəki bütün qəbuledicilərə məlumat göndərilməsi
- Məlumatın şəbəkədəki hər cihaza çatması lazım olduqda istifadə olunur
- Nümunə: DHCP tələbi — bu sorğu şəbəkədəki bütün cihazlara çatmalıdır

---

## 6. Kompüter Şəbəkəsi Modelləri

Kompüter şəbəkəsi modelləri kompüterlərin bir-biri ilə necə əlaqə qurduğunu və məlumat mübadiləsi etdiyini müəyyənləşdirən qaydalar və protokollar toplusudur. Şəbəkəni müxtəlif qatlarla təşkil edərək hər funksiyani müstəqil şəkildə araşdırmağa imkan verir.

**Şəbəkənin əsas komponentləri:**

- **Şəbəkə Cihazları:** Şəbəkə kartları, modemlər, switch-lər, router-lar məlumat ötürülməsi və marşrutlaşdırma funksiyalarını həyata keçirir
- **Ötürücü Mühit:** Mis kabellər, fiber optik kabellər, simsiz bağlantılar məlumat ötürülməsini təmin edir
- **Protokollar:** TCP/IP, HTTP, FTP, SMTP kimi protokollar şəbəkə üzərindən məlumat ötürülməsi qaydalarını müəyyənləşdirir
- **Şəbəkə Proqram Təminatı:** Əməliyyat sistemləri və şəbəkə idarəetmə proqramları cihazlar arasındakı əlaqəni idarə edir

---

### OSI Modeli

ISO tərəfindən hazırlanmış **OSI (Open Systems Interconnection)** modeli müxtəlif sistemlərin bir-biri ilə problemsiz kommunikasiyasını təmin edir. 7 qatdan ibarətdir:

1. Fiziki Qat (Physical Layer)
2. Məlumat Əlaqəsi Qatı (Data Link Layer)
3. Şəbəkə Qatı (Network Layer)
4. Nəqliyyat Qatı (Transport Layer)
5. Sessiya Qatı (Session Layer)
6. Təqdimat Qatı (Presentation Layer)
7. Tətbiq Qatı (Application Layer)

---

### TCP/IP Modeli

**TCP/IP** modeli internetin əsasını təşkil edir. OSI modeli ilə müqayisədə daha sadə quruluşa malikdir: 4 qatdan ibarətdir.

1. Şəbəkə İnterfeysi Qatı (Network Interface Layer)
2. İnternet Qatı (Internet Layer)
3. Nəqliyyat Qatı (Transport Layer)
4. Tətbiq Qatı (Application Layer)

Hər iki model şəbəkə dizaynı üçün əsas prinsiplər təmin edir. Lakin **TCP/IP** modeli praktikada daha geniş istifadə olunur. **OSI** modeli isə nəzəri şəbəkə konsepsiyalarını başa düşmək üçün faydalıdır.

---

## 7. OSI Modeli (Ətraflı)

OSI modeli ISO tərəfindən 1984-cü ildə hazırlanmış və kompüterlər arasındakı kommunikasiyanın memarlıq modeli hesab olunur. Məlumat ötürülməsi prosesini 7 qata bölür.

**Yuxarı Qatlar:** İstifadəçilər və proqramlar arasındakı kommunikasiyanı idarə edir (proqram təminatı). Tətbiq, Təqdimat və Sessiya qatları yuxarı qatlardır.

**Aşağı Qatlar:** Məlumatın necə ötürüldüyü ilə məşğuldur. Fiziki, Məlumat Əlaqəsi, Şəbəkə və Nəqliyyat qatları aşağı qatlardır.

---

### Qat 1 — Fiziki Qat (Physical Layer)

- Məlumatı bit şəklində fiziki kommunikasiya mühiti üzərindən ötürmək üçün lazım olan funksiyaları əhatə edir
- OSI modelinin ən aşağı qatıdır
- Kabellər, konnektor standartları bu qatın bir hissəsidir (UTP, RJ45, RS-232C, V.35)
- İki və ya daha çox cihazın fiziki olaraq necə qoşulacağını müəyyənləşdirir
- İki cihaz arasındakı ötürücü rejimi (simplex, half-duplex, full-duplex) müəyyənləşdirir
- Hardware nümunələri: şəbəkə adapterləri, repeterlər, hub-lar

---

### Qat 2 — Məlumat Əlaqəsi Qatı (Data Link Layer)

Kompüterlər və ya şəbəkə cihazları arasında etibarlı məlumat ötürülməsini təmin edir. Məlumatı çərçivələrə (frames) bölür, MAC ünvanları ilə ünvanlandırır və ötürmə xətalarını aşkar edir.

**Əsas funksiyalar:**
- **Çərçivələmə (Framing):** Məlumatı çərçivələrə qablaşdırır; qəbuledici məlumatın başlanğıcını və sonunu aşkar edə bilir
- **Ünvanlama (Addressing):** Hər şəbəkə cihazının unikal MAC ünvanı var; bu ünvanlar məlumatın düzgün cihaza çatmasını təmin edir
- **Xəta Yoxlama (Error Checking):** Ötürülmüş çərçivələrdəki xətaları aşkar edir
- **Axın İdarəsi (Flow Control):** Qəbuledicinin həddindən artıq məlumatla yüklənməsinin qarşısını alır

---

### Qat 3 — Şəbəkə Qatı (Network Layer)

Müxtəlif şəbəkələr arasında məlumat ötürülməsini idarə edir. Məntiqi ünvanlama (IP ünvanları), marşrutlaşdırma və paket yönləndirilməsi bu qatın əsas məsuliyyətidir.

**Əsas funksiyalar:**
- **Marşrutlaşdırma (Routing):** Məlumat paketlərinin mənbədən təyinata ən yaxşı yolu müəyyənləşdirir
- **Ünvanlama (Addressing):** IP ünvanları vasitəsilə məlumat paketlərini düzgün təyinata yönləndirir
- **Paketləmə (Packetization):** Məlumatı paketlərə bölür; hər paketin başlığında təyinat ünvanı var
- **Xəta Aşkarlanması:** Paket itkisi və ya yanlış ötürülmə hallarını aşkarlayır

> **Qeyd:** Router-lər 3-cü qat cihazlarıdır.

---

### Qat 4 — Nəqliyyat Qatı (Transport Layer)

Etibarlı, dəqiq və səmərəli uçdan-uca məlumat ötürülməsini təmin edir.

**Əsas funksiyalar:**
- **Seqmentasiya və Yenidən Yığım:** Yuxarı qatdan gələn mesajı seqmentlərə bölür, hər seqmentə unikal sıra nömrəsi verir; təyinatda sıra nömrələrinə əsasən yenidən yığır
- **Bağlantı İdarəsi:** İki növ xidmət: bağlantı yönümlü (connection-oriented) və bağlantısız (connectionless)
- **Xəta İdarəsi:** Uçdan-uca xəta düzəltməsini həyata keçirir

**Nəqliyyat Qatı Protokolları:**

| Protokol | Xüsusiyyət | İstifadə sahəsi |
|----------|-----------|-----------------|
| **TCP** | Etibarlı kommunikasiya; paketlerin itirilmədən çatdırılmasını təmin edir. İnternet kommunikasiyası üçün standart protokol. | Veb, e-poçt, fayl ötürülməsi |
| **UDP** | Sürətli lakin etibarsız kommunikasiya. TCP-dən az resurs istehlak edir, lakin məlumatın doğru sıra ilə çatacağını təmin etmir. | Video yayımı, oyunlar |

---

### Qat 5 — Sessiya Qatı (Session Layer)

Tətbiqlər arasında kommunikasiya sessiyalarını idarə etməkdən məsuldur. Sessiyaların başlanması, idarə edilməsi və sonlandırılmasını həyata keçirir.

---

### Qat 6 — Təqdimat Qatı (Presentation Layer)

Məlumatı başqa formata çevirən əməliyyat sistemi qatıdır.

**Əsas funksiyalar:**
- **Məlumat Formatlaşdırma:** Sistemlər arasında uyğunluq üçün məlumatı çevirir
- **Məlumat Sıxışdırma:** Şəbəkə trafikini azaltmaq üçün məlumatı sıxışdırır
- **Şifrələmə və Təhlükəsizlik:** SSL kimi protokollar vasitəsilə məlumatın təhlükəsiz ötürülməsini təmin edir
- **Kodlaşdırma:** Məlumatı hədəf sistem tərəfindən düzgün başa düşülən formata kodlaşdırır

---

### Qat 7 — Tətbiq Qatı (Application Layer)

İstifadəçilərin şəbəkə tətbiqləri ilə qarşılıqlı əlaqə qurması üçün lazım olan protokollar və interfeysləri ehtiva edir. E-poçt, fayl ötürülməsi, uzaqdan giriş, veb brauzer kimi tətbiqlərə birbaşa xidmət edir.

**Protokollar:**

| Protokol | Funksiya |
|----------|---------|
| **HTTP** | Veb səhifələrin ötürülməsi |
| **FTP** | Fayl ötürülməsi |
| **SMTP** | E-poçt göndərilməsi |
| **POP3 / IMAP** | E-poçt qəbul edilməsi |

---

### Məlumat Paketinin Mənbədən Təyinata Gedişi

```
İstifadəçi → [Tətbiq Qatı (7)] → [Təqdimat Qatı (6)] → [Sessiya Qatı (5)]
           → [Nəqliyyat Qatı (4)] → [Şəbəkə Qatı (3)] → [Məlumat Əlaqəsi Qatı (2)]
           → [Fiziki Qat (1)] → Fiziki Mühit (kabel, fiber, simsiz)
```

| Qat | Proses |
|-----|--------|
| **Tətbiq (7)** | İstifadəçi veb səhifə tələb edir; HTTP/FTP işə düşür |
| **Təqdimat (6)** | Məlumat şifrələnir/sıxışdırılır |
| **Sessiya (5)** | Mənbə və təyinat arasında sessiya qurulur |
| **Nəqliyyat (4)** | Məlumat seqmentlərə bölünür; TCP hər seqmentin çatmasını təmin edir |
| **Şəbəkə (3)** | Seqmentlər paketlərə bölünür; IP ünvanı əlavə edilir |
| **Məlumat Əlaqəsi (2)** | Paketlər çərçivəyə salınır; MAC ünvanı əlavə edilir |
| **Fiziki (1)** | Məlumat elektrik, optik və ya radio siqnallarına çevrilir |

---

## 8. TCP/IP Modeli (Ətraflı)

TCP/IP modeli şəbəkə kommunikasiyası üçün fundamental çərçivə təmin edir və internetin əsasını təşkil edir. "Transmission Control Protocol / Internet Protocol" deməkdir. OSI modelindən əvvəl hazırlanmışdır; 4 qatdan ibarətdir.

---

### Tətbiq Qatı (Application Layer)

TCP/IP modelinin ən yuxarı qatıdır. Son istifadəçilərin şəbəkə tətbiqləri ilə qarşılıqlı əlaqəsi üçün lazım olan interfeysləri və protokolları təmin edir.

**Tətbiq Qatında İstifadə Olunan Protokollar:**

| Protokol | Port | İzah |
|----------|------|------|
| **HTTP/HTTPS** | 80 / 443 | Veb brauzerlər və serverlər arasındakı kommunikasiyanın əsası |
| **SNMP** | 161 | Şəbəkə cihazlarının (router, switch) idarəedilməsi |
| **SMTP** | 25 | E-poçt mesajlarının göndərilməsi |
| **DNS** | 53 | Domen adlarını IP ünvanlarına çevirir |
| **TELNET** | 23 | Uzaq kompüterə terminal bağlantısı (təhlükəsiz deyil) |
| **SSH** | 22 | Şifrəli, təhlükəsiz şəbəkə giriş protokolu |
| **FTP** | 20, 21 | Kompüterlər arasında fayl ötürülməsi |

---

### Nəqliyyat Qatı (Transport Layer)

Uçdan-uca kommunikasiya üçün məsuldur. Məlumat axınını idarə edir, paketlərin sıra ilə ötürülməsini təmin edir.

**TCP Seqmentin Formatı:**

| Sahə | İzah |
|------|------|
| **Mənbə Portu** | Kommunikasiyanı başladan müştərinin port nömrəsi |
| **Təyinat Portu** | Hədəf kompüterin port nömrəsi |
| **Sıra Nömrəsi** | Məlumatın düzgün sıra ilə yenidən yığılmasını təmin edir |
| **Təsdiq Nömrəsi** | Məlumatın qəbulunu təsdiqləyir |
| **Başlıq Uzunluğu** | Başlığın uzunluğunu göstərir |
| **Bayraqlar** | Bağlantının idarəsi üçün idarəetmə siqnalları (SYN, ACK, FIN) |
| **Pəncərə Ölçüsü** | Təsdiq olmadan qəbul edilə biləcək məlumat miqdarı |
| **Yoxlama Cəmi** | Məlumat bütövlüyünü təmin edir |

**TCP Üçlü Əl Sıxışması (Three-Way Handshake):**

TCP/IP protokolu vasitəsilə iki cihaz arasında etibarlı bağlantı qurmaq üçün üçlü əl sıxışması istifadə olunur:

1. **SYN** — Müştəri serverə SYN paketi göndərir (başlanğıc sıra nömrəsini bildirir)
2. **SYN-ACK** — Server SYN-ACK paketi ilə cavab verir (serverın sıra nömrəsi + müştərinin sıra nömrəsinin təsdiqi)
3. **ACK** — Müştəri serverın sıra nömrəsini təsdiqləyən ACK paketi ilə cavab verir

**UDP Seqmentinin Formatı:**

| Sahə | İzah |
|------|------|
| **Mənbə Portu** | Müştərinin port nömrəsi |
| **Təyinat Portu** | Hədəf kompüterin port nömrəsi |
| **Uzunluq** | Başlıq və məlumatdakı ümumi bayt sayı |
| **Yoxlama Cəmi** | İxtiyari xəta yoxlaması |

> UDP bağlantı qurmadan məlumat göndərir; çatdırılmanı təmin etmir. Sürət vacib olduqda (video yayımı, oyunlar) istifadə olunur.

---

### İnternet Qatı (Internet Layer)

İnternetin onurğasını təşkil edir və qlobal məlumat ötürülməsini mümkün edir. Bu qatın ən mühüm protokolu **IP (Internet Protocol)**-dir.

**IP-nin funksiyaları:**
- Şəbəkədəki hər cihazı unikal IP ünvanı ilə müəyyənləşdirir
- RIP, OSPF, BGP kimi marşrutlaşdırma protokollarından istifadə edərək məlumat paketlərini yönləndirir
- Nəqliyyat qatından gələn seqmentləri IP başlığı ilə qablaşdırır
- Böyük dataqramları kiçik fraqmentlərə bölür (Fraqmentasiya); hədəfdə yenidən yığır

**IP Dataqram Formatı:**

| Sahə | İzah |
|------|------|
| **Version** | IP versiyası (IPv4, IPv6) |
| **IHL** | Dataqram başlığının faktiki uzunluğu |
| **TOS** | Paketlər şəbəkədə necə prioritetləşdirilir |
| **Total Length** | Dataqramın baytla ümumi uzunluğu |
| **Identification** | Məlumat fraqmentləri üçün 16-bitlik dəyər |
| **Flags** | DF (fraqmentasiya etmə), MF (daha fraqment var) |
| **Fragment Offset** | Fraqmentin ümumi mesaj daxilindəki mövqeyi |
| **TTL** | Dataqramın şəbəkədə nə qədər mövcud ola biləcəyi; hər router 1 azaldır |
| **Protocol** | Yuxarı qat protokolu (TCP, UDP, ICMP) |
| **Header Checksum** | Başlığın bütövlüyünü yoxlayır |
| **Source Address** | Göndərici cihazın IP ünvanı |
| **Destination Address** | Qəbuledicinin IP ünvanı |
| **Data** | Yuxarı qatdan gələn faydalı məlumat |

**ICMP (Internet Control Message Protocol):**

- İdarəetmə protokoludur; IP protokolu vasitəsilə göndərilir
- Cihaz aktiv deyilsə və ya şəbəkə sıxlığı varsa, məlumat vahidinin çatdırıla bilmədiyini göndəriciyə bildirir
- **ICMP Echo Request:** Hədəfin əlçatan olub olmadığını yoxlamaq üçün istifadə olunur
- **ICMP Echo Reply:** Hədəf cihazın cavab verib-vermədiyini yoxlamaq üçün istifadə olunur
- `ping` əmri IP ünvanı və ya domen adını yoxlamaq üçün istifadə olunur
- ICMP problemləri **bildirmək** üçündür, həll etmək üçün deyil

**ARP (Address Resolution Protocol):**

- IP ünvanından fiziki ünvanı (MAC) tapmaq üçün istifadə olunan şəbəkə qatı protokolu
- **ARP Request:** Göndərici IP ünvanı ilə əlaqəli fiziki ünvanı öyrənmək üçün göndərir
- **ARP Reply:** Uyğun IP ünvanına malik cihaz fiziki ünvanı ilə cavab verir
- `arp -a` əmri ilə ARP cədvəlini görmək olar

---

### Şəbəkə Giriş Qatı (Network Access Layer)

OSI modelindəki Fiziki və Məlumat Əlaqəsi qatlarını özündə birləşdirir. Məlumatın şəbəkə üzərindən fiziki olaraq necə ötürüldüyünü müəyyənləşdirir.

**Funksiyalar:**
- IP dataqramlarını çərçivələrə qablaşdırır
- IP ünvanlarını fiziki ünvanlarla (MAC) uyğunlaşdırır
- Hardware Ünvanlama: Hər şəbəkə cihazı MAC ünvanı ilə müəyyənləşdirilir
- Məlumat Çərçivələmə: İnternet qatından gələn paketlərə fiziki ötürülmə məlumatı əlavə edir

**Bu qatda istifadə olunan protokollar:** Ethernet, Token Ring, FDDI, X.25, Frame Relay

---

## 9. Protokollar və Portlar

### Protokollar

Kompüterlər şəbəkə protokolları vasitəsilə bir-biri ilə əlaqə qurur. Protokollar maşınlar arasında məlumat mübadiləsinin qaydalarını müəyyənləşdirir.

### Port

- Port nömrəsi protokol prosesi və ya xidməti ilə əlaqəli məntiqi konstruksiyadır
- Kompüterlər çox tapşırıqlı şəbəkə tətbiqləri üçün portlara ehtiyac duyur
- Kompüterin yalnız bir IP ünvanı ola bildiyi üçün portlar müxtəlif şəbəkə protokolları və xidmətlərini fərqləndirir
- TCP/IP-nin **65,536** portu var
- **0–1023** arası portlar "məşhur portlar" adlanır; IANA (Internet Assigned Numbers Authority) tərəfindən idarə olunur

---

### Əsas Port Cədvəli

| Xidmət / Protokol | Port Nömrəsi | TCP/UDP |
|-------------------|-------------|---------|
| FTP (Fayl Ötürmə Protokolu) | 20, 21 | TCP |
| SFTP (Təhlükəsiz FTP) | 22 | TCP |
| SSH (Secure Shell) | 22 | TCP |
| Telnet | 23 | TCP |
| SMTP (E-poçt göndərmə) | 25 | TCP |
| DNS (Domen Adı Sistemi) | 53 | UDP |
| DHCP | 67, 68 | UDP |
| TFTP | 69 | UDP |
| HTTP | 80 | TCP |
| POP3 | 110 | TCP |
| NTP (Şəbəkə Vaxt Protokolu) | 123 | UDP |
| IMAP4 | 143 | TCP |
| SNMP | 161 | UDP |
| LDAP | 389 | TCP |
| HTTPS | 443 | TCP |
| SMB | 445 | TCP |
| LDAPS | 636 | TCP |
| RDP (Uzaq Masa Üstü) | 3389 | TCP |
| H.323 | 1720 | TCP |
| SIP | 5060, 5061 | TCP |

---

### Əsas Protokolların İzahı

**DNS (Domain Name System):**
- Domen adını uyğun IP ünvanına çevirən protokol
- Nümunə: `hackviser.com → 162.0.232.236`
- Defolt olaraq UDP port 53-dən istifadə edir (zona köçürmələri üçün TCP port 53)
- `nslookup` aləti ilə DNS sorğuları həyata keçirilə bilər

**SNMP (Simple Network Management Protocol):**
- Şəbəkə cihazlarını izləmək və idarə etmək üçün protokol
- Administratorlara cihaz vəziyyəti, yaddaş, CPU, bant genişliyi istifadəsini izləməyə imkan verir
- Defolt olaraq TCP port 161

**LDAP (Lightweight Directory Access Protocol):**
- İstifadəçi adları, parollar, kompüter hesabları kimi kataloq xidmət sistemlərinə giriş və sorğu vasitələri
- Defolt olaraq TCP port 389

**LDAPS:** LDAP-ın SSL ilə şifrələnmiş versiyası; TCP port 636

**SMB (Server Message Block):**
- Microsoft mühitlərində geniş istifadə olunan şəbəkə fayl paylaşımı protokolu
- Fayl və printerlərin digər sistemlərlə paylaşılmasına imkan verir
- TCP port 445

**Telnet:**
- Uzaq hostla "təhlükəsiz olmayan" əlaqə üçün köhnə protokol
- Məlumatlar açıq mətndə ötürülür — təhlükəsiz deyil
- TCP port 23

**SSH (Secure Shell):**
- Uzaq hosta təhlükəsiz giriş üçün kriptoqrafik protokol
- PKI (Public Key Infrastructure) ilə şifrələnir
- TCP port 22

**RDP (Remote Desktop Protocol):**
- Microsoft-un uzaqdan idarəetmə protokolu; Windows masa üstünə uzaqdan giriş imkanı verir
- TCP port 3389

**FTP (File Transfer Protocol):**
- Kompüterlər arasında fayl ötürülməsi protokolu
- İstifadəçi adı/parol və ya anonim girişlə istifadə olunur
- Məlumatlar açıq mətndə — təhlükəsiz deyil
- Port 20 (məlumat ötürülməsi), Port 21 (idarəetmə)

**SFTP:** SSH üzərindən şifrəli fayl ötürülməsi; TCP port 22

**SMTP:** E-poçt müştərisindən hədəf e-poçt serverinə e-poçt göndərmə protokolu; TCP port 25

**POP3:** E-poçt serverdən e-poçt qəbuledicisi protokolu; TCP port 110

**IMAP:** POP3-ün əvəzedicisi; e-poçtlara server üzərindən oxuma imkanı; TCP port 143

**HTTP:** World Wide Web-in gözdən keçirilməsi üçün protokol; məlumat açıq mətndə ötürülür; TCP port 80

**HTTPS:** HTTP-nin SSL/TLS ilə şifrəli versiyası; TCP port 443

---

## 10. IP və MAC Ünvanları

### MAC Ünvanı (Media Access Control)

- Şəbəkə interfeysinin fiziki ünvanıdır və bənzərsizdir
- 6 baytdan (48 bitdən) ibarətdir
- İlk 3 bayt (24 bit) IEEE tərəfindən istehsalçıya verilir; istehsalçı MAC ünvanından müəyyən edilə bilər
- Nümunə: `00:21:70:6F:06:F2`
- `FF:FF:FF:FF:FF:FF` ünvanı bütün cihazlara broadcast üçün istifadə olunur

---

### İnternet Protokolu (IP)

IP ünvanı şəbəkədəki cihazı unikal şəkildə müəyyənləşdirmək üçün istifadə olunan məntiqi ünvandır. İki versiya mövcuddur: **IPv4** və **IPv6**.

---

### IPv4

- 32 bitlik ikili ədəddən ibarətdir; 4 okteta bölünür
- Hər oktet onluq ədədə çevrilir, nöqtə ilə ayrılır: `192.168.1.10`
- Hər oktet 8 bitdən ibarətdir

**İkili-Onluq Çevirmə nümunəsi (192):**

| 2⁷=128 | 2⁶=64 | 2⁵=32 | 2⁴=16 | 2³=8 | 2²=4 | 2¹=2 | 2⁰=1 |
|--------|-------|-------|-------|------|------|------|------|
| 1 | 1 | 0 | 0 | 0 | 0 | 0 | 0 |

128 + 64 = **192**

**IP Ünvanının Komponentləri:**

Hər şəbəkə cihazına aşağıdakılar verilir:
- **IP Ünvanı:** Şəbəkədəki hər cihaza verilən unikal məntiqi ünvan
- **Alt Şəbəkə Maskası (Subnet Mask):** IP ünvanının hansı alt şəbəkəyə aid olduğunu müəyyənləşdirir. Məsələn, `255.255.255.0` son 8 bitin cihazı, ilk 24 bitin şəbəkəni müəyyənləşdirdiyini göstərir.
- **Defolt Keçid (Default Gateway):** Yerli şəbəkə cihazlarının digər şəbəkələrdəki cihazlarla əlaqə qurmasına imkan verən router-in IP ünvanı

> Windows-da `ipconfig`, Linux-da `ifconfig` əmri IP ünvanı, subnet mask və default gateway məlumatlarını göstərir.

---

### IPv4 Ünvan Sinifləri

| Sinif | Şəbəkə Bitləri | Host Bitləri | Ünvan Aralığı |
|-------|---------------|-------------|---------------|
| **A** | 8 | 24 | 1.0.0.0 – 126.255.255.255 |
| **B** | 16 | 16 | 128.0.0.0 – 191.255.255.255 |
| **C** | 24 | 8 | 192.0.0.0 – 223.255.255.255 |

---

### Alt Şəbəkələr (Subnets)

Alt şəbəkələr böyük bir şəbəkəni daha kiçik, idarə edilə bilən hissələrə bölmək üçün istifadə olunan şəbəkə dizayn konsepsiyasıdır. Şəbəkə trafikini azaldır, şəbəkə idarəsini asanlaşdırır və şəbəkə təhlükəsizliyini artırır.

**CIDR (Classless Inter-Domain Routing) Notasiyası:**

CIDR notasiyası subnet maskasını daha qısa şəkildə ifadə edir.

- `192.168.1.0/24` → IP ünvanı `192.168.1.0`, subnet maskası `255.255.255.0`
- `/24` = `11111111.11111111.11111111.00000000`

**Host sayının hesablanması:**

Formulası: `2^(host bit sayı) - 2`

Nümunə: `192.168.1.0/24` üçün:
- Host bitləri: 8 bit
- `2^8 - 2 = 254 host`

---

### İctimai və Xüsusi IP Ünvanları

**İctimai IP Ünvanları:**
- İnternet Xidmət Provayderləri (İXP) tərəfindən verilən, qlobal miqyasda bənzərsiz ünvanlar
- İnternet üzərindən istənilən cihaz tərəfindən əlçatan
- İctimai serverlər, vebsaytlar, e-poçt serverləri üçün istifadə olunur

**Xüsusi IP Ünvanları:**
- Yerli şəbəkələrdə istifadə olunur; internетdə marşrutlaşdırıla bilmir
- RFC 1918 tərəfindən müəyyənləşdirilmiş aralıqlardan verilir
- İnternet ilə əlaqə üçün NAT (Network Address Translation) tələb olunur

| Növ | Başlanğıc IP | Son IP |
|-----|-------------|--------|
| **Xüsusi** | 10.0.0.0 | 10.255.255.255 |
| **Xüsusi** | 172.16.0.0 | 172.31.255.255 |
| **Xüsusi** | 192.168.0.0 | 192.168.255.255 |
| **APIPA** | 169.254.0.0 | 169.254.255.255 |

**Loopback Ünvanı:**
- `127.0.0.1` — kompüterə məlumatı özünə qaytaran xüsusi IP ünvanı
- Şəbəkə tətbiqlərini test etmək üçün istifadə olunur
- Brauzerə `http://127.0.0.1` və ya `http://localhost` yazaraq yerli veb serverə daxil olmaq olar

---

## 11. IP Alt Şəbəkə Bölgüsü (IP Subnetting)

IP subnetting IP ünvanını daha kiçik alt şəbəkələrə bölmə prosesidir. Şəbəkə administratorlarına IP ünvanlarını daha səmərəli bölüşdürmək və şəbəkə trafikini idarə etmək imkanı verir.

- Host bitlərini borc alaraq yeni alt şəbəkələr yaradılır
- Hər alt şəbəkənin öz IP ünvanları aralığı və subnet maskası var
- Alt şəbəkənin ilk ünvanı — **şəbəkə ünvanı**; son ünvanı — **broadcast ünvanı**; istifadə oluna bilən IP aralığı isə bu ikisi arasındadır

---

### FLSM (Fixed Length Subnet Masking — Sabit Uzunluqlu Alt Şəbəkə Maskalama)

FLSM IP ünvan məkanını **eyni ölçülü** alt şəbəkələrə bölməkdir. Sadədir, amma IP ünvanlarının səmərəsiz istifadəsinə gətirib çıxara bilər.

**Nümunə: `192.168.1.0/24` şəbəkəsini 4 bərabər alt şəbəkəyə bölmək:**

**Addım 1 — Subnet Maskasının Müəyyənləşdirilməsi:**
- 4 alt şəbəkə üçün 2 bit borc alınır (`2^2 = 4`)
- Yeni CIDR: `/26`
- Yeni Subnet Mask: `255.255.255.192`

**Addım 2 — Şəbəkə Ünvanlarının Hesablanması:**

| Alt Şəbəkə | Şəbəkə Ünvanı | İstifadə oluna bilən Host Aralığı | Broadcast Ünvanı |
|-----------|--------------|----------------------------------|----------------|
| 1 | 192.168.1.0/26 | 192.168.1.1 – 192.168.1.62 | 192.168.1.63 |
| 2 | 192.168.1.64/26 | 192.168.1.65 – 192.168.1.126 | 192.168.1.127 |
| 3 | 192.168.1.128/26 | 192.168.1.129 – 192.168.1.190 | 192.168.1.191 |
| 4 | 192.168.1.192/26 | 192.168.1.193 – 192.168.1.254 | 192.168.1.255 |

---

### VLSM (Variable Length Subnet Masking — Dəyişkən Uzunluqlu Alt Şəbəkə Maskalama)

VLSM IP ünvan məkanını **müxtəlif ölçülü** alt şəbəkələrə bölməyə imkan verir. Cihaz sayına uyğun alt şəbəkə ölçüsü seçildiyi üçün IP ünvanlarından daha səmərəli istifadə edilir.

**Nümunə: `192.168.1.0/24` şəbəkəsini aşağıdakı tələblərə görə bölmək:**

- Alt Şəbəkə 1: 50 cihaz
- Alt Şəbəkə 2: 30 cihaz
- Alt Şəbəkə 3: 10 cihaz
- Alt Şəbəkə 4: 2 cihaz

**Addım 1 — Subnet Maskalarının Müəyyənləşdirilməsi:**

| Alt Şəbəkə | Cihaz Sayı | Hesablama | Host Bitləri | Subnet Mask |
|-----------|-----------|-----------|-------------|-------------|
| 1 | 50 | 2⁶ - 2 = 62 | 6 bit | 255.255.255.192 (/26) |
| 2 | 30 | 2⁵ - 2 = 30 | 5 bit | 255.255.255.224 (/27) |
| 3 | 10 | 2⁴ - 2 = 14 | 4 bit | 255.255.255.240 (/28) |
| 4 | 2 | 2² - 2 = 2 | 2 bit | 255.255.255.252 (/30) |

**Addım 2 — Şəbəkə Ünvanlarının Hesablanması:**

VLSM-də alt şəbəkələr ən böyükdən ən kiçiyə doğru sıralanır; ünvanlar buna uyğun bölüşdürülür.

| Alt Şəbəkə | Şəbəkə Ünvanı | Cihaz Sayı |
|-----------|--------------|-----------|
| 1 | 192.168.1.0 /26 | 50 cihaz |
| 2 | 192.168.1.64 /27 | 30 cihaz |
| 3 | 192.168.1.96 /28 | 10 cihaz |
| 4 | 192.168.1.112 /30 | 2 cihaz |

---

## Kurs Bölmələrinin Xülasəsi

| № | Mövzu |
|---|-------|
| 1 | Giriş |
| 2 | Şəbəkə Növləri |
| 3 | Şəbəkə Cihazları |
| 4 | Şəbəkə Topologiyaları |
| 5 | Kommunikasiya Rejimləri və Növləri |
| 6 | Kompüter Şəbəkəsi Modelləri |
| 7 | OSI Modeli |
| 8 | TCP/IP Modeli |
| 9 | Protokollar və Portlar |
| 10 | IP və MAC Ünvanları |
| 11 | IP Alt Şəbəkə Bölgüsü |

> Bütün bölmələri tamamladıqdan sonra imtahana girə bilərsiniz.
