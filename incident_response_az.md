# Hadisəyə Müdaxilə (Incident Response) — Tam Bələdçi (Azərbaycanca)

---

## Mündəricat

1. [Giriş](#1-giriş)
2. [Hadisəyə Müdaxilə Çərçivələri](#2-hadisəyə-müdaxilə-çərçivələri)
3. [Hazırlıq Mərhələsi](#3-hazırlıq-mərhələsi)
4. [Aşkarlama və Analiz Mərhələsi](#4-aşkarlama-və-analiz-mərhələsi)
5. [Məhdudlaşdırma Strategiyaları](#5-məhdudlaşdırma-strategiyaları)
6. [Aradan Qaldırma Mərhələsi](#6-aradan-qaldırma-mərhələsi)
7. [Bərpa Mərhələsi](#7-bərpa-mərhələsi)
8. [Hadisə Sonrası Fəaliyyət](#8-hadisə-sonrası-fəaliyyət)
9. [Hadisəyə Müdaxilə Playbook-ları](#9-hadisəyə-müdaxilə-playbook-ları)
10. [Hüquqi və Kommunikasiya Məsələləri](#10-hüquqi-və-kommunikasiya-məsələləri)

---

## 1. Giriş

### Hadisəyə Müdaxilə nədir?

Kibertəhlükəsizlik dünyasında "Sındırıla bilməyən sistem yoxdur, yalnız hələ sındırılmamış sistemlər var" kəlamı ümumi bir reallığı əks etdirir. Təşkilatların aldığı təhlükəsizlik tədbirləri nə qədər güclü olsa da, kiber hücumçular həmişə bir zəiflik tapmaq potensialına malikdirlər. Məhz bu nöqtədə **Hadisəyə Müdaxilə (Incident Response / IR)** devreye girer.

**Hadisəyə Müdaxilə**, bir təşkilatda baş verən kibertəhlükəsizlik hadisələrinin (pozuntular, kiber hücumlar, məlumat sızmaları və s.) aşkarlanması, analiz edilməsi, məhdudlaşdırılması və nəticələrinin idarə edilməsi prosesidir. Əsas məqsəd hücumun vurduğu zərəri minimuma endirmək, Bərpa Müddətini (Recovery Time) qısaltmaq və xərcləri azaltmaqdır.

Peşəkar bir Hadisəyə Müdaxilə prosesi aşağıdakıları təmin edir:

- **Sürətli Müdaxilə:** Hadisəni dərhal fərq etmək və tədbirə başlamaq.
- **Strukturlaşdırılmış Yanaşma:** Çaxnaşmaq əvəzinə əvvəlcədən müəyyən edilmiş prosedurları tətbiq etmək.
- **Məlumatın Bütövlüyü:** Hüquqi proseslərə uyğun şəkildə sübut toplamaq.
- **Daimi Təkmilləşdirmə:** Hadisədən öyrənərək təhlükəsizlik vəziyyətini gücləndirmək.

---

### 1.1 Əsas Anlayışlar

**1. Hadisə (Event) vs. Təhlükəsizlik Hadisəsi (Incident)**

Bu iki termin tez-tez qarışdırılır, lakin aralarında əhəmiyyətli fərq var:

| Termin | İzah | Nümunə |
|--------|------|--------|
| **Event (Hadisə)** | Sistemdə və ya şəbəkədə baş verən hər hansı müşahidə oluna bilən hadisə | İstifadəçinin fayl paylaşımına qoşulması, serverin yenidən başlaması, gələn veb sorğusu |
| **Incident (Təhlükəsizlik Hadisəsi)** | Təhlükəsizlik siyasətinin pozulması və ya təhlükəsizlik riski yaradan hadisə | İcazəsiz istifadəçinin verilənlər bazasına daxil olmağa cəhd etməsi, Ransomware-in sistemə yoluxması, DDoS hücumu |

> Hər Incident bir Event-dir, lakin hər Event bir Incident deyil.

**2. CSIRT, CERT və SOC**

| Abbreviatura | Tam Adı | Rolu |
|-------------|---------|------|
| **CSIRT** | Computer Security Incident Response Team | Birbaşa hadisəyə müdaxiləyə fokuslanır. Hadisəni analiz edir, müdaxilə edir və hesabat verir. |
| **CERT** | Computer Emergency Response Team | Çox vaxt CSIRT ilə sinonim kimi istifadə edilir, lakin bəzən ölkə və ya sektor miqyasında koordinasiya mərkəzlərinə istinad edir (məsələn, US-CERT). |
| **SOC** | Security Operations Center | 24/7 monitorinq həyata keçirən, alarmları ilk alan və analiz edən mərkəz. SOC analitikləri adətən "Tier 1" səviyyəsində ilk müdaxiləni həyata keçirir, lazım gəldikdə vəziyyəti CSIRT komandasına (Tier 2/3) eskalasiya edir. |

---

### 1.2 Niyə Hadisəyə Müdaxilə Lazımdır?

Yaxşı strukturlaşdırılmış IR prosesi olmayan təşkilatlar hücum zamanı aşağıdakı problemlərlə üzləşir:

1. **Çaxnaşma və Xaos:** Kimin nə etməli olduğu barədə qeyri-müəyyənlik.
2. **Sübut İtkisi:** Sistemlərin təsadüfən söndürülməsi və ya logların silinməsi səbəbindən hücumun mənbəyini tapa bilməmək.
3. **Uzanan Proses:** Hücumçunun şəbəkədə günlər, hətta aylar boyu qalması (Dwell Time — Qalma Müddəti).
4. **Nüfuz İtkisi:** Müştərilərə və ictimaiyyətə yanlış və ya gecikmiş məlumat vermək.

---

### 1.3 Hadisəyə Müdaxilə Dövrü

Hadisəyə müdaxilə düz bir xətt deyil, bir **dövrdür**. Bir hadisə bitdikdə proses tamamlanmır; əldə edilən təcrübə ilə "Hazırlıq" mərhələsi gücləndirilir.

Bu bələdçidə sənayedə ən qəbul görmüş modellərə (NIST və SANS) əsaslanaraq bu dövrün hər addımını ən incə texniki detallarla araşdıracağıq.

---

## 2. Hadisəyə Müdaxilə Çərçivələri

Hadisəyə müdaxilə proseslərini standartlaşdırmaq üçün dünya miqyasında qəbul edilmiş iki əsas çərçivə var: **NIST** və **SANS Institute** modelləri.

> Kibertəhlükəsizlik Analitiki kimi bu addımları əzbərləmək deyil, məntiqi başa düşmək və bir hadisə zamanı harada olduğunuzu bilmək ("Mən hazırda Məhdudlaşdırma mərhələsindəyəm") həyati əhəmiyyət daşıyır.

---

### 2.1 NIST SP 800-61 Rev. 2 (NIST Modeli)

NIST-in "Kompüter Təhlükəsizliyi Hadisəsinin İdarə Edilməsi Bələdçisi" sənədində müəyyən edilmiş model prosesi **4 əsas başlıq** altında qruplaşdırır:

| # | Mərhələ | İzah |
|---|---------|------|
| 1 | **Hazırlıq** (Preparation) | Hadisədən əvvəl görülən bütün işlər |
| 2 | **Aşkarlama və Analiz** (Detection & Analysis) | Hadisəni fərqetmə və doğrulama prosesi |
| 3 | **Məhdudlaşdırma, Aradan Qaldırma və Bərpa** (Containment, Eradication & Recovery) | Hücumu dayandırmaq, təmizləmək və sistemi bərpa etmək (NIST bu üç addımı tez-tez üst-üstə düşdükləri üçün tək faza kimi qruplaşdırır) |
| 4 | **Hadisə Sonrası Fəaliyyət** (Post-Incident Activity) | Öyrənilənlər və hesabat |

---

### 2.2 SANS PICERL Modeli

SANS Institute prosesi **6 daha ətraflı addıma** bölür (PICERL abbreviaturası ilə tanınır):

| Hərf | Mərhələ |
|------|---------|
| **P** | Preparation (Hazırlıq) |
| **I** | Identification (Müəyyənləşdirmə) |
| **C** | Containment (Məhdudlaşdırma) |
| **E** | Eradication (Aradan Qaldırma) |
| **R** | Recovery (Bərpa) |
| **L** | Lessons Learned (Öyrənilənlər) |

---

### 2.3 Müqayisə Cədvəli

| NIST Mərhələsi | SANS Mərhələsi | Təsvir |
|----------------|----------------|--------|
| Hazırlıq | Preparation | Komanda qurulması, alət hazırlığı, siyasət yaradılması |
| Aşkarlama və Analiz | Identification | Hadisənin mövcudluğunun təsdiqlənməsi, əhatə dairəsinin müəyyənləşdirilməsi |
| Məhdudlaşdırma, Aradan Qaldırma və Bərpa | Containment | Hücumun yayılmasının qarşısının alınması (Şəbəkədən izolyasiya və s.) |
| Məhdudlaşdırma, Aradan Qaldırma və Bərpa | Eradication | Kök Səbəbin Aradan Qaldırılması (Zərərli proqramın silinməsi, yamaq tətbiqi) |
| Məhdudlaşdırma, Aradan Qaldırma və Bərpa | Recovery | Sistemlərin normal əməliyyata qaytarılması və monitorinq |
| Hadisə Sonrası Fəaliyyət | Lessons Learned | "Nə səhv getdi? Nə yaxşı edildi?" suallarına cavab vermək |

---

### 2.4 Hansı Modeldən İstifadə Etməli?

Sənayedə **SANS PICERL modeli** əməliyyat proseslərində (Playbook-lar hazırlayarkən) daha tez-tez istinad edilir, çünki addımları daha aydın şəkildə ayırır. Lakin rəsmi hesabat və uyğunluq prosesləri çox vaxt NIST standartlarına istinad edir.

Bu bələdçidə mövzunu ən ətraflı və anlaşılan şəkildə əhatə etmək üçün **SANS PICERL modelinin 6 mərhələsinə** əsaslanaraq irəliləyəcəyik.

---

### 2.5 "Qızıl Saat" Konsepsiyası

İstifadə etdiyiniz çərçivədən asılı olmayaraq, hadisəyə müdaxilədə **vaxt** ən kritik amildir. Tibbdə olduğu kimi, kibertəhlükəsizlikdə də "Qızıl Saat" konsepsiyası var. Hücum aşkarlandıqdan sonrakı ilk saatlar hücumçunun izini sürmək və zərəri məhdudlaşdırmaq üçün ən kritik vaxtdır.

> Hücumçular çox vaxt aşkarlanmamaq üçün logları silməyə və ya digər sistemlərə yan tərəfdən keçməyə çalışır.

Düzgün IR çərçivəsini tətbiq etmək bu kritik saatlarda çaxnaşmanın qarşısını alır və analitikə "İndi nə etməliyəm?" sualına dərhal cavab tapmasını təmin edir.

---

## 3. Hazırlıq Mərhələsi

Hadisəyə Müdaxilə dövrünün ən vacib, lakin çox vaxt ən çox laqeyd edilən mərhələsi **Hazırlıq** mərhələsidir. Yanğın söndürmə briqadasının yanğın başlayanda şlanqlarının işləmədiyini və ya suları olmadığını anlaması fəlakətdir. Kibertəhlükəsizlikdə hücum zamanı logların saxlanılmadığını və ya yedəkləmələrin işləmədiyini anlamaq eyni effekti yaradır.

Hazırlıq mərhələsi iki əsas kateqoriyaya bölünür:

1. **İnsanlar və Proses:** Siyasət, təlim və təşkilat.
2. **Texnologiya və Məlumat:** Alətlər, loglama, baselining.

---

### 3.1 İnsanlar və Proses

**Komanda Strukturu və Kommunikasiya**

Hadisə zamanı kimi çağırmaq lazım olduğu aydın olmalıdır. Kommunikasiya siyahısı (Call Tree — Zəng Ağacı) hazırlanmalı və aktual saxlanılmalıdır:

- **Əsas Əlaqə:** Hadisəni texniki olaraq idarə edəcək şəxs.
- **Eskalasiya:** Hadisənin miqyası böyüdükdə xəbər veriləcək rəhbərlər (CISO, CTO).
- **Hüquq və PR:** Hüquq şöbəsi və ictimaiyyətlə əlaqələr (lazım gəldikdə).

**Siyasətlər və Prosedurlar**

Təşkilatın "Hadisəyə Müdaxilə Siyasəti" yazılmış olmalıdır. "Hadisə" nəyi təşkil edir, kimin nə səlahiyyəti var (məsələn, serverin şəbəkə kabelini kim çıxara bilər?) əvvəlcədən müəyyən edilməlidir.

**Təlimlər və Simulyasiyalar**

Komanda real hücumdan əvvəl ssenariləri məşq etməlidir (Masa Üstü Məşqlər — Tabletop Exercises).

> **Nümunə Ssenari:** "Bazar ertəsi səhər CEO-dan gələn bir e-poçt vasitəsilə Ransomware bütün şirkəti yoluxdurdu. Nə edirsiniz?"

---

### 3.2 Texnologiya və Məlumat Hazırlığı

Texniki hazırlıq analitikə hadisə zamanı "görməyə" imkan verir. Loglar yoxdursa, analiz aparıla bilməz.

**Log İdarəetməsi və Görünürlük**

Hadisə zamanı aşağıdakı mənbələrdən logların toplanması və mərkəzi bir yerdə (SIEM) saxlanması şərtdir:

| Log Mənbəyi | Detallar |
|-------------|----------|
| **Endpoint Logları** | Əməliyyat sistemi logları. Windows üçün `Sysmon` kimi qabaqcıl loglama alətləri quraşdırılmalıdır. Standart Windows Event Logları (Security, System, Application) çox vaxt kifayətsizdir. **Nümunə:** PowerShell əmrlərinin loglanması (Script Block Logging) aktiv edilməlidir. |
| **Şəbəkə Logları** | Firewall, Proxy, DNS logları |
| **Tətbiq Logları** | Veb server (IIS, Nginx, Apache) giriş və xəta logları |

**Baselining (Əsas Xətt Müəyyənləşdirməsi)**

Sistemlərinizin "normal" davranışını bilmirsinizsə, "anormal" olanı aşkarlaya bilməzsiniz:

- **Şəbəkə Trafiki:** Serverləriniz normal olaraq hansı ölkələrə qoşulur? Günlük məlumat çıxışı MB-la nə qədərdir?
- **Proseslər:** Serverlərdə hansı `service account`-lar normal olaraq işləyir?

> **Nümunə:** Mühasibat serveri normal olaraq yalnız 08:00-18:00 arasında trafik yaradırsa və gecə saat 03:00-da 5 GB məlumat yükləyirsə, bu bir anomaliyadır. Bunu bilmək üçün əvvəlcədən "normal"i (baseline) qeydə almış olmalısınız.

**Aktiv İdarəetmə (Asset Management)**

Nəyi qoruduğunuzu bilməlisiniz. Təşkilatın "Tac Cəvahirləri" (Ən dəyərli aktivlər) hansılardır?

- Müştəri verilənlər bazası
- Mənbə kodu deposu (Source code repository)
- Active Directory serveri

Bu aktivlər hadisə zamanı prioritet olaraq qorunacaq və bərpa ediləcək sistemlərdir.

**Hadisəyə Müdaxilə Alət Dəsti (IR Toolkit)**

Hadisə zamanı internetə girişiniz olmaya bilər və ya sistemlərə güvənə bilməzsiniz. Bu səbəbdən təmiz bir "Müdaxilə Dəsti" (rəqəmsal və ya fiziki) hazır olmalıdır:

| Alət | İzah |
|------|------|
| **Təmiz Laptop** | Zərərli proqram analizi və ya təhlükəsiz kommunikasiya üçün izolyasiya edilmiş, təmiz kompüter |
| **Açıla bilən USB-lər** | Şəkil almaq və ya sistemi təmiz şəkildə açmaq üçün (məsələn, CAINE, SIFT Workstation kimi Forensics distribusiyaları) |
| **Forensics Proqramları** | FTK Imager, KAPE, Volatility, Eric Zimmerman Tools |
| **Yedəkləmələr** | Kritik sistemlərin və konfiqurasiya fayllarının oflayn yedəkləmələri |

---

### 3.3 Hazırlıq Yoxlama Siyahısı (Checklist)

- [ ] Hadisəyə Müdaxilə Planı yazılıbmı?
- [ ] Kommunikasiya siyahısı aktualdırmı?
- [ ] Kritik loglar SIEM-ə və ya Log serverinə axırmı?
- [ ] Kritik sistemlərin yedəkləməsi varmı və bərpa testi aparılıbmı?
- [ ] Komandanın əsas analiz alətləri (Forensics alətləri) varmı və onlardan istifadə etməyi bilirlərmi?

---

## 4. Aşkarlama və Analiz Mərhələsi

Bu mərhələ Hadisəyə Müdaxilə prosesinin ən texniki və çətin hissəsidir. Bir hadisənin mövcudluğunu müəyyənləşdirmək (Aşkarlama) və onun nə olduğunu başa düşmək (Analiz) bu mərhələdə baş verir. Hücumçular gizlənmək üçün əllərindən gələni edirlər, analitikın vəzifəsi isə bu gizliliyi aşkara çıxarmaqdır.

---

### 4.1 Aşkarlama Mənbələri

Bir hadisə adətən iki üsulla aşkarlanır:

**Avtomatik Aşkarlamalar (Alarmlar):**

| Sistem | Nümunə |
|--------|--------|
| **SIEM** | Korrelyasiya Qaydaları tərəfindən yaradılan alarmlar. Nümunə: "1 dəqiqə ərzində eyni IP ünvanından 10 uğursuz giriş cəhdi." |
| **EDR** | Endpoint-lərdə şübhəli proses fəaliyyətləri |
| **IDS/IPS** | Şəbəkə trafikindəki imza əsaslı müdaxilə aşkarlamaları |
| **Antivirus** | Məlum zərərli proqram imzaları |

**Manuel Aşkarlamalar və Bildirişlər:**

- **İstifadəçi Bildirişləri:** "Kompüterim çox yavaşladı", "Qəribə bir pop-up çıxdı", "Siçan öz-özünə hərəkət edir".
- **Threat Hunting:** Analitikın sistemdəki anomaliyaları proaktiv olaraq axtarması.
- **Üçüncü Tərəf Bildirişləri:** İnternet Xidmət Provayderi (ISP) və ya milli CERT komandasından "IP ünvanınızdan Botnet trafiki gəlir" xəbərdarlığı.

---

### 4.2 Aşkarlama Üsulları: İmza vs. Anomaliya

| | İmza Əsaslı Aşkarlama | Anomaliya/Davranış Əsaslı Aşkarlama |
|-|----------------------|-------------------------------------|
| **Məntiqi** | Məlum təhdidlərin "barmaq izini" axtarır | Normadan kənarlaşmaları axtarır |
| **Üstünlük** | Aşağı Yanlış Müsbət (False Positive) dərəcəsi | Naməlum hücumları tuta bilər |
| **Çatışmazlıq** | Yalnız məlum olanı tapır. Yeni (Zero-day) hücumları əldən verir | Yüksək Yanlış Müsbət dərəcəsi |
| **Nümunə** | Faylın həş dəyərini (MD5/SHA256) məlum virus siyahısında (VirusTotal) axtarmaq | Word sənədinin (winword.exe) powershell.exe işlətməsi — texniki olaraq mümkündür, lakin normal istifadəçi davranışı deyil |

---

### 4.3 Doğrulama və Triage (Prioritizasiya)

Hər alarm bir hadisə deyil. Analitikın ilk vəzifəsi "Triage" həyata keçirməkdir. Bu prosesdə aşağıdakı suallar verilir:

- **Real midirmi?** Yanlış Müsbət (False Positive) mi, yoxsa Doğru Müsbət (True Positive) mi?
- **Əhatə dairəsi nədir?** Neçə sistem təsirlənib? Yalnız bir laptop mu, yoxsa bütün server şəbəkəsi mi?
- **Təsir nədir?** Hansı məlumatlar riskdədir? Məxfilik, Bütövlük və ya Əlçatımlılıq itkisi varmı?

**Yanlış Müsbət (False Positive) Nümunəsi:**

Şəbəkəni taran bir təhlükəsizlik skaneri (Nessus, OpenVAS) IDS sistemində minlərlə "Port Taraması" alarması yaradır. Bu hücum deyil, planlaşdırılmış bir testdir. Bu, Yanlış Müsbət vəziyyətidir (Alarm var, təhdid yoxdur).

**Doğru Müsbət (True Positive) Nümunəsi:**

Veb serverinin loglarında URL parametrlərindəki SQL əmrlərini (UNION SELECT) görmək və serverin verilənlər bazası xətası əvəzinə böyük ölçülü məlumatla cavab verməsi (200 OK və böyük Content-Length). Bu real bir SQL Injection hücumudur.

---

### 4.4 Hadisə Ciddilik Səviyyələri

| Səviyyə | Nümunə |
|---------|--------|
| **Aşağı** | Fərdi virus yoluxması (AV tərəfindən təmizləndi), uğursuz tarama cəhdləri |
| **Orta** | Siyasətin pozulması, qeyri-kritik sistemlər təsirləndi |
| **Yüksək** | Kritik serverlərə giriş, məlumat sızması şübhəsi, aktiv Ransomware |
| **Kritik** | İş davamlılığının dayanması, geniş miqyaslı məlumat itkisi, korporativ nüfuzun sarsılması |

---

### 4.5 Araşdırma Texnikaları (Texniki Analiz)

**A. Veb Hücum Analizi (Log Əsaslı)**

Veb hücumlar adətən veb server (Apache, Nginx, IIS) giriş loglarında iz qoyur. Analitik HTTP sorğularını oxuya bilməli və onların içindəki payload-ları tanıya bilməlidir.

**Ssenari: SQL Injection**

Hücumçu bir e-ticarət saytının axtarış qutusundan verilənlər bazasından məlumat çıxarmaq üçün istifadə edir.

Normal Sorğu (Payload yoxdur) — İstifadəçi "iphone" sözünü axtarır:

```http
GET /search.php?q=iphone HTTP/1.1
Host: vulnerable-shop.com
User-Agent: Mozilla/5.0...
```

Cavab: `200 OK` (Məhsul siyahısı gəlir).

Hücum Sorğusu (Payload ilə — SQL Injection) — Hücumçu verilənlər bazası versiyasını öyrənmək üçün payload göndərir:

```http
GET /search.php?q=iphone' UNION SELECT 1,@@version-- HTTP/1.1
Host: vulnerable-shop.com
User-Agent: Mozilla/5.0...
```

| Payload Elementi | İzah |
|-----------------|------|
| `'` (Tək dırnaq) | SQL sorğusunu qırmaq üçün |
| `UNION SELECT` | İkinci sorğunu birləşdirmək üçün |
| `@@version` | Verilənlər bazası versiyasını qaytaran əmr |
| `--` | Sorğunun qalanını şərh etmək üçün |

Gözlənilən Cavab (Zəiflik varsa):

```
HTTP Status: 200 OK
Content: "iphone" məhsullarının yanında verilənlər bazası versiyası (məsələn, 5.7.33-log) görünür.
```

> **Analitik Qeydi:** Qaytarılan cavabın ölçüsü (Content-Length) normal sorğudan əhəmiyyətli dərəcədə fərqlidirsə, injection uğurlu olmuş ola bilər.

**Ssenari: Əmr İnjeksiyası (Command Injection)**

Hücumçu sistemdə əmrlər icra etməyə çalışır:

```http
POST /ping.php HTTP/1.1
Host: target-server.com
Content-Type: application/x-www-form-urlencoded

ip=127.0.0.1; cat /etc/passwd
```

| Payload Elementi | İzah |
|-----------------|------|
| `;` (Nöqtəli vergül) | Linux-da əmr ayırıcısı. Birinci əmr bitdikdən sonra ikinci əmri icra edir. |
| `cat /etc/passwd` | İstifadəçi siyahısını oxuyan əmr |

Cavab: Cavab gövdəsində `root:x:0:0:...` kimi sətirlər görünsə, hücum uğurludur.

---

**B. Windows Sistem Analizi (Endpoint)**

Bir Windows maşının ələ keçirildiyindən şübhələnirsinizsə, aşağıdakı sahələri yoxlamalısınız:

**1. Şübhəli Proseslər**

Proses ağacı Task Manager və ya Process Hacker / Process Explorer kimi daha qabaqcıl alətlərlə yoxlanılır.

Anomaliya nümunələri:
- `svchost.exe`-nin `C:\Windows\System32` xaricindəki bir yerdən işləməsi (məsələn, `C:\Users\Admin\AppData\Temp`)
- `lsass.exe` prosesinin `winword.exe`-dən başqa bir valideyn prosesi olması
- Yazılış səhvləri: `scvhost.exe` (svchost.exe-nin imitasiyası), `chorme.exe`

**2. Davamlılıq Elementləri**

Hücumçular sistemi yenidən başlatdığınızda belə içəridə qalmaq üçün "Davamlılıq" (Persistence) təmin edirlər:

Registry:
```
HKCU\Software\Microsoft\Windows\CurrentVersion\Run
HKLM\Software\Microsoft\Windows\CurrentVersion\Run
```

Planlaşdırılmış Tapşırıqlar (Terminal əmri):
```cmd
schtasks /query /fo LIST /v
```

Başlanğıc Qovluğu:
```
C:\Users\[İstifadəçi]\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup
```

**3. PowerShell Logları**

Hücumçular çox vaxt faylsız hücumlar (fileless attacks) üçün PowerShell-dən istifadə edirlər.

- **Event ID 4104 (Script Block Logging):** İcra edilmiş PowerShell kodunun məzmununu göstərir. Base64 ilə kodlanmış (`-EncodedCommand`) əmrlərin burada deşifrə edilmiş halını görə bilərsiniz.

---

**C. Yaddaş (RAM) Analizi Əsasları**

Diskdəki faylları silsəniz belə, işləyən zərərli proqram RAM-da izlər qoyur. RAM şəkli Volatility kimi alətlərlə analiz edilir.

Nə tapıla bilər:
- Gizli proseslər
- Açıq şəbəkə bağlantıları (netstat çıxışı kimi)
- Əmr sətri tarixi (cmd history)
- Kopyalanmış şifrələr və ya həşlər

---

### 4.6 Analiz Alət Dəsti

| Alət | İstifadə |
|------|---------|
| **Wireshark** | Şəbəkə trafiki (PCAP) analizi |
| **Sysinternals Suite** | Windows sistem analizi (Process Explorer, Autoruns) |
| **Volatility** | Yaddaş forensikası |
| **CyberChef** | Məlumat deşifrəsi üçün "İsveçrə Çakısı" (Base64, Hex deşifrəsi) |

> Analiz nəticəsində "Bəli, hadisə var, əhatə dairəsi budur və o sistemlər təsirlənib" deyə bilsəniz, artıq Məhdudlaşdırma mərhələsinə keçməyə hazırsınız.

---

## 5. Məhdudlaşdırma Strategiyaları (Containment)

Hücum aşkarlandıqda və analiz/doğrulandıqda, növbəti prioritet "qanaxmanı dayandırmaqdır". **Məhdudlaşdırma** mərhələsi hücumçunun şəbəkə daxilində daha da yayılmasının (Lateral Movement) və məlumat oğurlamasının qarşısını almaq üçün həyata keçirilir.

Məhdudlaşdırma adətən iki mərhələdə tətbiq edilir:

---

### 5.1 Qısamüddətli Məhdudlaşdırma (Short-Term Containment)

Məqsəd hücumun təsirini dərhal dayandırmaqdır. Bu mərhələdə "kök səbəb" analizi hələ tamamlanmamış ola bilər, lakin dərhal müdaxilə tələb olunur.

| Tədbirlər | İzah |
|-----------|------|
| **İzolyasiya** | Təsirlənmiş serverin və ya kompüterin şəbəkə kabelini çıxarmaq, ya da virtual maşındırsa vNIC (Virtual Şəbəkə İnterfeys Kartı) bağlantısını kəsmək |
| **IP Bloklanması** | Hücumçunun C2 (Komanda & İdarəetmə) serverinə məxsus IP ünvanını Firewall vasitəsilə blok etmək |
| **Hesabın Kilidlənməsi** | Ələ keçirildiyi güman edilən istifadəçi hesabını deaktiv etmək (məsələn, Active Directory-də) |

---

### 5.2 Uzunmüddətli Məhdudlaşdırma (Long-Term Containment)

Məqsəd sistemləri təmizləmək və bərpa etməzdən əvvəl təhlükəsizliyi gücləndirməkdir.

| Tədbirlər | İzah |
|-----------|------|
| **Müvəqqəti Düzəltmələr** | Zəif tətbiqə "Virtual Yamaq" tətbiq etmək və ya WAF (Veb Tətbiq Firewallı) qaydası yazmaq |
| **Seqmentasiya** | Təsirlənmiş alt şəbəkəni (VLAN) digər təhlükəsiz şəbəkələrdən tamamilə ayırmaq |
| **Şifrə Sıfırlama** | Bütün administrator şifrələrini dəyişdirmək (Golden Ticket hücumu şübhəlidirsə, `krbtgt` hesabının şifrəsini iki dəfə dəyişdirmək) |

---

### 5.3 Ümumi Səhvlər: "Kabeli Çəkmək" Həmişə Doğrudurmu?

Əksər insanlar hack vəziyyətində dərhal "kabeli çəkməyi" (sistemi söndürməyi) düşünür. Lakin bu həmişə doğru deyil.

**Niyə Söndürməməlisiniz?**

1. **RAM-dakı Sübutlar İtirilir:** Yaddaşdakı zərərli proqram izləri, şifrə açarları və açıq şəbəkə bağlantıları kompüter söndürüldükdə silinir (Volatile Data — Uçucu Məlumat).
2. **Hücumçunu Oyandıra Bilərsiniz:** Bəzi hücumçular bağlantıları kəsildiqdə avtomatik olaraq məlumatları silən (wiper) və ya şifrələyən (ransomware) "Dead Man's Switch" mexanizmləri qura bilərlər.

> **Doğru Yanaşma:** Məlumat itkisi riski çox yüksək deyilsə, əvvəlcə RAM şəkli alınmalı, sonra şəbəkə bağlantısı kəsilməli (sistem işləməyə davam edərkən) və analiz aparılmalıdır. Lakin aktiv Ransomware şifrələyirsə, sistemi dərhal söndürmək məlumatları bərpa etmək üçün ən yaxşı seçim ola bilər.

---

### 5.4 Seqmentasiya və VLAN İstifadəsi

Məhdudlaşdırma mərhələsindəki ən effektiv üsullardan biri şəbəkə seqmentasiyasıdır.

> **Nümunə:** Mühasibat departamentindəki bir kompüter virusa yoluxubsa, bütün mühasibat VLAN-ının server VLAN-ına girişi müvəqqəti olaraq məhdudlaşdırıla bilər. Beləliklə, virus serverlərə keçə bilmir.

---

### 5.5 Sübutların Qorunması

Məhdudlaşdırma həyata keçirərkən sübutları məhv etməmək üçün diqqətli olmaq lazımdır:

- Hüquqi prosesin mümkünlüyü varsa, disklərin "Forensik Şəkli" (dəqiq nüsxəsi) alınmalıdır.
- Alınan şəklin Həş dəyəri (MD5/SHA256) hesablanmalı və qeyd edilməlidir. Bu, sübutun dəyişmədiyini sübut edir (**Sübut Zənciri** — Chain of Custody).

---

## 6. Aradan Qaldırma Mərhələsi (Eradication)

Hücum məhdudlaşdırıldıqdan sonra təhdid sistemlərdən tamamilə təmizlənməlidir. **Aradan Qaldırma** kök səbəbin aradan qaldırıldığı və hücumçunun yenidən daxil olmasının qarşısını almaq üçün tədbirlərin görüldüyü mərhələdir.

Bu mərhələdə həyata keçirilən əməliyyatlar "yamaq tətbiq etməkdən" daha irəliyə gedir; sistemin sterilizasiyasından söhbət gedir.

---

### 6.1 Kök Səbəbin Müəyyənləşdirilməsi və Aradan Qaldırılması

Yalnız virusu silmək kifayət deyil; virusun necə daxil olduğunu tapmalı və o yolu bağlamalısınız. Əks halda, hücumçu eyni qapıdan yenidən girəcək.

| Kök Səbəb | Tədbirlər |
|-----------|-----------|
| **Zəiflik** | Hücumçu Exploit istifadə edərək giriblər (məsələn, EternalBlue) — müvafiq sistem üçün yamaq quraşdırılmalıdır |
| **Zəif Şifrə** | Hücumçu RDP-yə Brute Force ilə giribsə — şifrə siyasəti gücləndirilməli və MFA (Çoxfaktorlu Autentifikasiya) aktiv edilməlidir |
| **Phishing** | İstifadəçi keçidə klikləyibsə — E-poçt Gateway qaydaları sərtləşdirilməli və istifadəçi təlimi planlaşdırılmalıdır |

---

### 6.2 Zərərli Proqramın Silinməsi

Bütün aşkarlanan zərərli fayllar, arxa qapılar və hücumçunun yaratdığı alətlər silinməlidir:

- **Antivirus/EDR Taraması:** Tam sistem taraması həyata keçirilməlidir.
- **Manuel Təmizlənmə:** Avtomatik alətlərin tapa bilmədikləri davamlılıq mexanizmləri (Registry girişləri, planlaşdırılmış tapşırıqlar) əl ilə silinməlidir.

---

### 6.3 Yenidən Quraşdırma (Re-imaging) vs. Təmizləmə

Kibertəhlükəsizlikdə qızıl bir qayda var: **"Bir sistem bir dəfə ələ keçirilsə, ona 100% güvənə bilməzsiniz."**

Bu səbəbdən peşəkar yanaşma adətən virusu təmizləmək əvəzinə sistemi sıfırdan yenidən quraşdırmaqdır (Re-imaging):

- **Niyə?** Rootkit-lər kimi qabaqcıl zərərli proqramlar özlərini əməliyyat sistemi kernelində və ya BIOS/UEFI-də gizlədə bilər. Antiviruslar onları görməyə bilər.
- **Tövsiyyə:** Məlumatları ehtiyata götürün (yalnız məlumatları, icra edilə bilən faylları deyil!), diski formatlayın və təmiz şəkildən (Golden Image) quraşdırın.

---

### 6.4 Etimad məlumatlarının Yenilənməsi (Renewing Credentials)

Hücumçunun sistemdə olduğu müddət ərzində həşlər oğurlaya bilər (Dump LSASS) və ya Keylogger istifadə etmiş ola bilər:

- Bütün təsirlənmiş istifadəçilərin şifrələri dəyişdirilməlidir.
- Xidmət Hesabları (Service Accounts) və verilənlər bazası bağlantı şifrələri yenilənməlidir.
- SSH açarları və API token-ləri ləğv edilməli və yenilər yaradılmalıdır.

---

### 6.5 Təhlükəsizlik Təkmilləşdirmələri

Sistemi əvvəlkindən daha təhlükəsiz edin:

- Lazımsız portları bağlayın.
- Tətbiqləri Ən Az İmtiyaz (Least Privilege) prinsipi ilə işlədin.
- Loglamanı artırın.

---

## 7. Bərpa Mərhələsi (Recovery)

Aradan qaldırma prosesi tamamlandıqdan sonra sistemlər və xidmətlər normal fəaliyyətə qaytarılmalıdır. Lakin bu "bir düyməyə basıb yandırmaq" qədər sadə deyil. **Bərpa** mərhələsi sistemin yenidən yoluxmayacağını təmin etmək və tədricən keçidi sağlamaq üçün diqqətlə həyata keçirilməlidir.

---

### 7.1 Bərpa etmə və Doğrulama

Təmizlənmiş və ya yenidən quraşdırılmış sistemlər istehsal mühitinə alınmazdan əvvəl test edilməlidir:

| Addım | İzah |
|-------|------|
| **Yedəkləmədən Bərpa** | Təmiz yedəkləmədən bərpa edirsinizsə, yedəkləmənin alındığı tarihin hücumdan əvvəl olduğundan əmin olun. Əks halda, yedəkləmənin içindəki zərərli proqram (time-bomb) da ola bilər. |
| **Funksional Testlər** | Sistem gözlənilən performansda işləyirmi? Verilənlər bazası bağlantısı düzgündürmü? |
| **Təhlükəsizlik Taraması** | Sistem canlıya keçməzdən əvvəl son dəfə zəiflik taramasından keçməlidir. |

---

### 7.2 Mərhələli Yanaşma

Bütün sistemləri eyni anda açmaq riskli ola bilər. Tədricən bir yanaşma izlənməlidir:

1. Əvvəlcə kritik infrastruktur serverləri (DNS, DC).
2. Sonra iş tətbiqləri.
3. Nəhayət, son istifadəçi girişi.

Bu proses ərzində hər açılan sistemin davranışı yaxından izlənir.

---

### 7.3 Gücləndirilmiş Monitorinq

Sistem açıldığında "xəstə hələ reanimasiyadadır". Hücumçunun geri dönməsi ehtimalına qarşı monitorinq səviyyəsi artırılmalıdır:

| Tədbirlər | İzah |
|-----------|------|
| **Log Səviyyələri** | Log səviyyəsi müvəqqəti müddət üçün `Verbose` və ya `Debug` rejiminə keçirilə bilər |
| **Alarm Həddləri** | SIEM qaydaları daha həssas edilə bilər. Məsələn, normal olaraq 10 uğursuz girişdə alarm verirsə, bu proses ərzində 3 uğursuz girişdə alarm vermək üçün tənzimlənə bilər |
| **Xüsusi Alarmlar** | Hücumda istifadə edilmiş xüsusi IOC-lar (Kompromis Göstəriciləri — IP ünvanları, fayl adları) üçün xüsusi alarmlar müəyyən edilməlidir |

---

### 7.4 "Nə Vaxt Bitti?" Qərarı

Rəhbərlik və texniki komanda (CSIRT Lideri) adətən birlikdə əməliyyatların nə zaman normala qayıdacağına qərar verir. Bərpa aşağıdakı meyarlar yerinə yetirildikdə tamamlanmış sayılır:

- Bütün təsirlənmiş sistemlər təmizlənib və yamaqlanıb.
- İş prosesləri fasiləsiz işləyir.
- Müəyyən bir müddət üçün (məsələn, 48 saat) şübhəli fəaliyyət və ya yenidən yoluxma görülməyib.

---

## 8. Hadisə Sonrası Fəaliyyət (Post-Incident Activity)

Böhran keçdi, adrenalin düşdü və hamı normal işlərinə qayıtdı. Adətən bu nöqtədə fayl bağlanır. Lakin bu, Hadisəyə Müdaxilə dövrünün ən dəyərli hissəsidir: **Öyrənilənlər (Lessons Learned)**.

Bu mərhələ hadisəni analiz edərək təşkilatı daha davamlı etməyi və IR prosesinin özünü təkmilləşdirməyi hədəfləyir.

---

### 8.1 Öyrənilənlər Görüşü (Post-Mortem)

Hadisə bağlandıqdan sonra (adətən ilk 2 həftə içərisində) hadisəyə müdaxilə edən bütün komandalar bir araya gəlməlidir. Bu görüş "günahkar axtarma sessiyası" deyil, konstruktiv bir analiz prosesidir.

Görüşdə aşağıdakı suallara dürüst cavablar axtarılır:

- Tam olaraq nə baş verdi və nə vaxt?
- Hadisəni aşkarlayana qədər nə qədər vaxt keçdi? (MTTD — Mean Time To Detect / Orta Aşkarlama Müddəti)
- Hadisəni həll edənə qədər nə qədər vaxt keçdi? (MTTR — Mean Time To Respond / Orta Müdaxilə Müddəti)
- Hansı prosedurlar işlədi, hansılar işləmədi?
- Hansı alətlər çatışmırdı və ya qeyri-kafi idi?
- Kommunikasiya kəsintiyi oldumu?

---

### 8.2 Hadisə Hesabatı

Rəhbərliyə, hüquq şöbəsinə və ya (lazım gəldikdə) auditorlara təqdim edilmək üçün rəsmi hesabat hazırlanmalıdır. Bu hesabat texniki detallarla yanaşı icraçı xülasəsini də ehtiva etməlidir.

**Nümunə Hadisə Hesabatı Şablonu:**

```markdown
# Hadisəyə Müdaxilə Hesabatı

**Hadisə ID:** IR-2023-001
**Tarix:** 25 Oktyabr 2023
**Hazırlayan:** CSIRT Lideri
**Hadisə Növü:** Ransomware / Məlumat Sızması
**Ciddilik Səviyyəsi:** Kritik

## 1. İcraçı Xülasəsi
23 Oktyabr 2023-cü il tarixdə saat 09:15-də Maliyyə departamentindəki bir serverdə Ransomware fəaliyyəti aşkarlandı. Hadisə istifadəçinin phishing e-poçtunu açması ilə başladı. Müdaxilə komandası hadisəni 15 dəqiqə ərzində aşkarladı və serveri 45 dəqiqə ərzində izolyasiya etdi. Məlumat itkisi baş vermədi, sistemlər yedəkləmədən bərpa edildi və 6 saat ərzində xidmətə qaytarıldı.

## 2. Hadisə Zaman Cədvəli
- **23 Oktyabr, 08:30:** Hücumçu `accounting@company.com` ünvanına zərərli əlavəli e-poçt göndərdi.
- **23 Oktyabr, 08:45:** İstifadəçi əlavəni açdı, zərərli proqram (Emotet) işlədi.
- **23 Oktyabr, 09:00:** C2 serveri ilə əlaqə quruldu və Ransomware yükləndi.
- **23 Oktyabr, 09:15:** SIEM "Yüksək sayda fayl adı dəyişikliyi" alarması yaratdı (Aşkarlama).
- **23 Oktyabr, 09:30:** CSIRT hadisəni təsdiqlədi və serverin şəbəkə bağlantısını kəsdi (Məhdudlaşdırma).
- **...**

## 3. Texniki Analiz və Kök Səbəb
Hadisənin kök səbəbi istifadəçinin zərərli makro ehtiva edən Excel faylını icra etməsidir.
Antivirus proqramı imza əsaslı olduğu üçün yeni variantı aşkarlaya bilmədi.

**IOC-lar (Kompromis Göstəriciləri):**
- Zərərli Proqram Həşi: `a1b2c3d4...`
- C2 IP: `192.0.2.55`

## 4. Görülmüş Tədbirlər
- Təsirlənmiş server formatlandı.
- İstifadəçi şifrələri dəyişdirildi.
- C2 IP Firewall-da blok edildi.

## 5. Tövsiyyələr
- [ ] E-poçt Gateway qaydaları sərtləşdirilməlidir.
- [ ] İstifadəçilərə phishing simulyasiya təlimi verilməlidir.
- [ ] Endpoint-lərdə "Makro icrasına" GPO vasitəsilə qadağa qoyulmalıdır.
```

---

### 8.3 Metriklər və KPI-lar

| Metrik | İzah |
|--------|------|
| **Yanlış Müsbət Dərəcəsi** | Alarmların neçə faizi yanlış idi? |
| **Aşkarlama Müddəti** | Hücum başladıqdan nə qədər sonra fərq etdik? |
| **Məhdudlaşdırma Müddəti** | Fərq etdikdən nə qədər sonra hücumçunu dayandırdıq? |

---

### 8.4 Dövrü Tamamlamaq

"Tövsiyyələr" bölməsindəki elementlər tətbiq ediləndə, Hazırlıq mərhələsi yenilənir və dövr daha güclü şəkildə başa çatır. Növbəti hadisədə daha sürətli və effektiv olacaqsınız.

---

## 9. Hadisəyə Müdaxilə Playbook-ları

Hər hadisə unikaldır, lakin hadisə növləri (Phishing, Zərərli Proqram, DDoS) çox vaxt oxşar nümunələri izləyir. Böhran zamanı təkərləri yenidən kəşf etməmək üçün hər hadisə növü üçün addım-addım nə etməli olduğunu izah edən bələdçilərə **Playbook-lar** (və ya Runbook-lar) deyilir.

---

### 9.1 Ssenari 1: Phishing Analiz Playbook-u

**Məqsəd:** Şübhəli e-poçtun zərərli olub-olmadığını müəyyənləşdirmək və istifadəçiləri qorumaq.

**Tetikləyici:**
- Mənbə: İstifadəçi bildirişi ("PhishAlarm" düyməsi) və ya E-poçt Gateway alarması.
- Alətlər: Sandbox (Cuckoo, Joe Sandbox), Header Analyzer, URL Skaneri.

**Analiz Addımları:**

1. **Header Analizi:**
   - `Return-Path` və `From` ünvanları uyğun gəlirmi?
   - SPF/DKIM/DMARC qeydləri `PASS` mı, yoxsa `FAIL` mi?
   - Nümunə: Göndərən `admin@paypal-support.com` (saxta domen), lakin göstərici ad "PayPal Support"dur.

2. **Məzmun və Keçid Analizi:**
   - E-poçtdakı keçidlər üzərindən klikləmədən real URL-i yoxlayın.
   - URL-i `VirusTotal` və ya `URLScan.io`-da skan edin.
   - Payload: URL `http://bit.ly/55f...` kimi qısaldılıbmı?

3. **Əlavə Analizi:**
   - Faylı izolyasiya edilmiş mühitdə (Sandbox) işlədin.
   - Həş dəyərini alın və Threat Intelligence mənbələrində sorğulayın.

**Məhdudlaşdırma və Aradan Qaldırma (Zərərlidirsə):**

- E-poçtu bütün istifadəçilər üçün serverdən (Exchange/Office 365) silin (Purge).
- Göndərən domenini və IP-ni qara siyahıya alın.
- Keçidə kliklayan istifadəçiləri müəyyənləşdirin (Proxy loglarından).
- Kliklayan istifadəçilərin şifrələrini sıfırlayın və kompüterlərini skan edin.

---

### 9.2 Ssenari 2: Ransomware Playbook-u

**Məqsəd:** Ransomware-in yayılmasını dayandırmaq və məlumatları bərpa etmək.

**Tetikləyici:**
- İstifadəçi ekranında fidyə notunun görünməsi.
- Fayl uzantılarının dəyişməsi (məsələn, `.locked`, `.enc`).
- SIEM-dən "Yüksək Tezlikli Fayl Dəyişikliyi" alarması.

**Məhdudlaşdırma — Çox Kritik!**

1. **Şəbəkə Bağlantısını Kəsin:** Təsirlənmiş cihazın LAN kabelini çıxarın və ya Wi-Fi-ni söndürün. **(Sistemi söndürməyin! RAM analizi üçün lazım ola bilər.)**
2. **Lateral Movement-in Qarşısını Alın:** Switch və ya Firewall vasitəsilə müvafiq VLAN-ı izolyasiya edin.
3. **Paylaşımları Bağlayın:** Fayl Serverlerindəki paylaşımları müvəqqəti olaraq dayandırın və ya Yalnız Oxuma (Read-Only) rejiminə keçirin.

**Analiz:**

1. **Variant Aşkarlanması:** Hansı ransomware-dir? (WannaCry, Ryuk, Conti?). Fidyə notunu və ya şifrələnmiş faylı `ID Ransomware` kimi saytlara yükləyərək aşkarlayın.
2. **Giriş Nöqtəsi:** Necə girdi? (RDP, Phishing, Zəiflik?). Bunu tapmasanız, təmizlədikdən sonra yenidən girəcəklər.
3. **Deşifrə Yoxlaması:** `No More Ransom` layihəsində bu variant üçün pulsuz deşifrə aləti varmı?

**Bərpa:**

1. **Sistemi Sıfırlayın:** Diski tamamilə formatlayın (Wipe). Heç vaxt təmizləyib istifadə etməyə çalışmayın.
2. **Yedəkləmədən Bərpa Edin:** Hücum tarixindən əvvəlki təmiz yedəkləmədən məlumatları yükləyin.
3. **Yedəkləməni Skan Edin:** Bərpa edilmiş məlumatları aktual antivirus ilə skan edin.

> Bu playbook-lar hadisə zamanı çaxnaşmanın qarşısını alır və standart keyfiyyəti təmin edir. Bu addımları təşkilatınızın strukturuna uyğun olaraq fərdiləşdirməlisiniz.

---

## 10. Hüquqi və Kommunikasiya Məsələləri

Hadisəyə müdaxilə yalnız texniki bir proses deyil; həm də hüquqi və kommunikativ bir böhran idarəetməsidir. Yanlış kommunikasiya texniki zərərdən daha böyük nüfuz itkisinə yol aça bilər. Sübutların düzgün toplanmaması hücumçunun məhkəmədə cəzalandırılmasının qarşısını ala bilər.

---

### 10.1 Sübut Zənciri (Chain of Custody)

Kompüter forensikasında bir sübutun (sabit disk, log faylı, USB) cinayət yerindən götürüldüyü andan məhkəməyə təqdim edilənə qədər kimin əlindən keçdiyi, harada saxlandığı və bütövlüyünün pozulmadığını qeyd etmək prosesi **Sübut Zənciri (Chain of Custody — CoC)** adlanır.

Bu zəncir qırılarsa (məsələn, sübut kilidlənməmiş bir otaqda buraxılarsa), məhkəmə bu sübutu "etibarsız" sayır və rədd edir.

**CoC Formasında Nə Olmalıdır?**

| Sahə | İzah |
|------|------|
| **Case ID** | Hadisə nömrəsi |
| **Item Description** | Sübutun təsviri (Marka, Model, Seriya №) |
| **Original Hash** | Sübut alındığı anda həş dəyəri (MD5/SHA256) |
| **Timestamp** | Tarix və Saat |
| **From / To** | Kimdən kimə təhvil verildi? (İmza ilə) |

---

### 10.2 Məlumatların Qorunması və Bildiriş Öhdəlikləri

Qlobal kibertəhlükəsizlik ekosistemində şəxsi məlumatların pozulmasından sonra hüquq-mühafizə orqanlarını və təsirlənmiş şəxsləri xəbərdar etmək əksər yurisdiksiyalarda qanuni tələbdir.

| Standart | Tələblər |
|----------|----------|
| **GDPR (Qlobal Standart)** | Pozuntundan xəbərdar olduqdan sonra 72 saat içərisində müvafiq nəzarət orqanına bildiriş edilməlidir |
| **Digər Regionlar** | ABŞ, Asiya-Sakit Okean regionu və s.-də hadisənin ciddiliyindən asılı olaraq oxşar ciddi bildiriş müddətləri və ağır maliyyə sanksiyaları tətbiq edilir |

> Bu proseslər zamanla yarışdığı üçün Hadisəyə Müdaxilə (IR) komandası Hüquq və Uyğunluq şöbələri ilə daimi və real vaxt rejimli əlaqədə olmalıdır.

"Sızan məlumatlar arasında şəxsi müəyyənedici məlumatlar (PII) varmı?" sualına aydın və dərhal cavab verə bilmək, hüquqi öhdəliklərin tetiklənib-tetiklənmədiyini müəyyən edən həyati amildir.

---

### 10.3 Böhran Kommunikasiyası

Hadisə zamanı kimin kiminlə necə danışacağı əvvəlcədən müəyyən edilməlidir.

**Daxili Kommunikasiya:**

- İşçilərə nə deyiləcək? ("Sistemlərdə texniki xidmət var" yoxsa "Hücum altındayıq"?)
- Adətən "bilgiye ihtiyaç duyma" (need-to-know) prinsipi tətbiq edilir. Çaxnaşma yaratmamaq üçün detallar yalnız müvafiq texniki komanda ilə paylaşılır.

**Xarici Kommunikasiya:**

| Hədəf Kütlə | Yanaşma |
|-------------|---------|
| **Müştərilər** | Şəffaflıq vasitəsilə etibar yaratmaq, lakin vəziyyəti texniki detallara boğmadan izah etmək |
| **Mətbuat** | Yalnız təyin edilmiş sözcü danışmalıdır |
| **Hüquq Orqanları** | Prokurorluq və ya kiber cinayətkarlıqla mübarizə komandaları ilə əməkdaşlıq |

**Nümunə Kommunikasiya Səhvləri:**

- **Erkən Danışmaq:** "Heç bir məlumat oğurlanmadı" demək, sonra 2 gün sonra "Bağışlayın, hər şey oğurlandı" demək. **(Əmin olmadan danışmayın.)**
- **Sükut:** Müştərilər hadisəni Twitter-dən (X) öyrənirlərsə, etibarı itirirsiniz.

> Peşəkar hadisəyə müdaxilə prosesi texniki bacarıqlar qədər hüquqi uyğunluq və düzgün kommunikasiya tələb edir.

---

*© Hadisəyə Müdaxilə (Incident Response) — Azərbaycanca Tam Bələdçi | Kibertəhlükəsizlik Laboratoriyası üçün hazırlanmışdır*
