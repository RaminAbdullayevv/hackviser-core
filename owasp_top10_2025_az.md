# OWASP Top 10 (2025) — Tam Bələdçi (Azərbaycanca)

---

## Mündəricat

1. [Giriş — OWASP nədir?](#1-giriş--owasp-nədir)
2. [OWASP Top 10:2025 Ümumi Baxış](#2-owasp-top-102025-ümumi-baxış)
3. [A01:2025 — Qırıq Giriş Nəzarəti (Broken Access Control)](#3-a012025--qırıq-giriş-nəzarəti-broken-access-control)
4. [A02:2025 — Təhlükəsizlik Yanlış Konfiqurasiyası (Security Misconfiguration)](#4-a022025--təhlükəsizlik-yanlış-konfiqurasiyası-security-misconfiguration)
5. [A03:2025 — Proqram Təchizat Zənciri Uğursuzluqları (Software Supply Chain Failures)](#5-a032025--proqram-təchizat-zənciri-uğursuzluqları-software-supply-chain-failures)
6. [A04:2025 — Kriptoqrafik Uğursuzluqlar (Cryptographic Failures)](#6-a042025--kriptoqrafik-uğursuzluqlar-cryptographic-failures)
7. [A05:2025 — İnjeksiya (Injection)](#7-a052025--i̇njeksiya-injection)
8. [A06:2025 — Təhlükəsiz Olmayan Dizayn (Insecure Design)](#8-a062025--təhlükəsiz-olmayan-dizayn-insecure-design)
9. [A07:2025 — Autentifikasiya Uğursuzluqları (Authentication Failures)](#9-a072025--autentifikasiya-uğursuzluqları-authentication-failures)
10. [A08:2025 — Proqram və ya Məlumat Bütövlüyü Uğursuzluqları (Software or Data Integrity Failures)](#10-a082025--proqram-və-ya-məlumat-bütövlüyü-uğursuzluqları-software-or-data-integrity-failures)
11. [A09:2025 — Təhlükəsizlik Loglama və Xəbərdarlıq Uğursuzluqları (Security Logging and Alerting Failures)](#11-a092025--təhlükəsizlik-loglama-və-xəbərdarlıq-uğursuzluqları-security-logging-and-alerting-failures)
12. [A10:2025 — İstisna Halların Yanlış İdarə Edilməsi (Mishandling of Exceptional Conditions)](#12-a102025--i̇stisna-halların-yanlış-i̇darə-edilməsi-mishandling-of-exceptional-conditions)

---

## 1. Giriş — OWASP nədir?

### OWASP Top 10 haqqında

**OWASP Top 10** — kritik veb tətbiq təhlükəsizliyi risklərini başa düşmək üçün ən geniş istifadə edilən istinadlardan biridir. Bu siyahı tam test metodologiyası, hüquqi uyğunluq standartı və ya ətraflı təhlükəsizlik yoxlama siyahısı deyil. Düzgün istifadə edildikdə, o, developerlərə, təhlükəsizlik komandalarına və menecerlərə ümumi bir risk dili verir: zəifliyin yalnız texniki adını deyil, kök səbəbini və necə prioritetləşdirilməli olduğunu izah etməyə kömək edir.

---

### 1.1 OWASP nədir?

**OWASP** (**Open Worldwide Application Security Project**) — proqram təhlükəsizliyini yaxşılaşdırmağa yönəlmiş açıq, icma tərəfindən idarə olunan bir təhlükəsizlik ekosistemidir. OWASP Fondu developerlər, təhlükəsizlik tədqiqatçıları, auditorlar, müəllimlər və təşkilatların töhfələri vasitəsilə pulsuz sənədlər, standartlar, alətlər və tədris resursları istehsal edir. Ümumi missiyası tətbiq təhlükəsizliyini daha görünən, anlaşılan və praktik etməkdir.

> OWASP adı uzun müddət **Open Web Application Security Project** kimi tanınırdı. Zamanla OWASP ekosistemi klassik veb tətbiqlərin hüdudlarını aşaraq API-ləri, mobil tətbiqləri, proqram təchizat zənciri təhlükəsizliyini, bulud-doğma sistemləri, LLM tətbiqləri və geniş tətbiq təhlükəsizliyi praktikalarını əhatə etdi.

---

### 1.2 Digər Mühüm OWASP Layihələri

| Layihə | İzah |
|--------|------|
| **OWASP ASVS** | Müasir veb tətbiqlər və xidmətlər üçün doğrulanabilir təhlükəsizlik tələbləri |
| **OWASP SAMM** | Təşkilatların proqram təhlükəsizliyi yetkinliyini ölçməyə kömək edir |
| **OWASP Cheat Sheet Series** | Developerlər və müdafiəçilər üçün praktik təhlükəsiz kodlaşdırma bələdçisi |

**Açıq Mənbə Alətlər:**

| Alət | İstifadə |
|------|---------|
| **OWASP ZAP** | Veb tətbiqlərin proksi əsaslı dinamik təhlükəsizlik testi |
| **OWASP Dependency-Check** | Məlum zəiflikləri olan komponentləri müəyyənləşdirmək |
| **OWASP Amass** | Hücum səthi və aktiv kəşfi |
| **OWASP WebGoat / Juice Shop** | Təhlükəsizlik təlimi üçün qəsdən zəif tətbiqlər |
| **OWASP CycloneDX** | Proqram materialları siyahısı (SBOM) və təchizat zənciri görünürlüğü üçün standart |

---

### 1.3 OWASP Top 10-un Qısa Tarixi

| İl | Hadisə |
|----|--------|
| **2003** | OWASP Top 10 ilk dəfə tətbiq təhlükəsizliyi riskləri üçün praktik başlanğıc nöqtəsi kimi meydana çıxdı |
| **2017** | Əhəmiyyətli yeniləmə |
| **2021** | Növbəti böyük buraxılış |
| **2025** | Cari buraxılış — 2 yeni kateqoriya, 1 birləşdirmə |

> Top 10 müntəzəm olaraq yenilənir, lakin sərt bir təqvim üzrə deyil. Yeni buraxılış yalnız "ən geniş yayılmış zəifliklər"i saymır. O, töhfə edilmiş məlumatlardan, CVE/CWE uyğunlaşdırmalarından, istismar edilə bilmə və təsir qiymətləndirilməsindən istifadə edir.

---

### 1.4 OWASP Top 10:2025-i Necə Oxumalı

OWASP Top 10 kateqoriyaları adətən oxşar kök səbəbləri olan zəiflik ailələrini təmsil edir, tək bir zəifliyi deyil.

**Nümunə:**
- `A05:2025 Injection` — yalnız SQL Injection deyil; OS əmr injeksiyası, NoSQL injeksiyası, LDAP injeksiyası, XSS və oxşar interpretator əsaslı məsələləri də əhatə edir.
- `A01:2025 Broken Access Control` — IDOR, imtiyaz artırımı, CORS səhvləri, SSRF və API avtorizasiya çatışmazlıqları kimi üzə çıxa bilər.

**Yüksək keyfiyyətli təhlükəsizlik tapıntısı bunları əhatə etməlidir:**

- Təsirlənmiş endpoint və HTTP metodu
- Tələb olunan imtiyaz səviyyəsi və hücumçunun ön şərti
- Uğurlu və uğursuz sorğu müqayisəsi
- Məlumat təsiri: oxu, dəyişdirmə, silmə, maliyyə əməliyyatı, hesab ələ keçirilməsi
- Çatışmayan müdafiə: yoxluq nəzarəti, yanlış nəzarət yeri, yanlış etibar sərhədi
- Yenidən istehsal edilə bilmə və iş təsiri

---

### 1.5 Əsas Anlayışlar

| Anlayış | İzah |
|---------|------|
| **Etibar Sərhədi (Trust Boundary)** | Etibar edilən və edilməyən zonalar arasındakı məntiqi sərhəd. Brauzer, mobil tətbiq, əks proxy, backend xidməti, verilənlər bazası fərqli etibar sərhədlərində yerləşə bilər. |
| **Server Tərəfi Tətbiq (Server-side enforcement)** | Təhlükəsizlik qərarının hücumçunun dəyişdirə bilmədiyi etibarlı server tərəfi kodunda verilməsi. Bir düyməni gizlətmək, marşrutu gizlətmək və ya icazələri yalnız JavaScript-də yoxlamaq təhlükəsizlik nəzarəti deyil. |
| **Bağlı Uğursuzluq (Fail Closed)** | Xəta baş verdikdə sistemin daha təhlükəsiz standarta keçməsi. Avtorizasiya xidməti əlçatmaz olarsa, əməliyyatı rədd etmək fail closed-dir; onu qəbul etmək isə fail open-dir. |
| **Müsbət Doğrulama (Positive Validation)** | İcazə verilən formatı açıq şəkildə müəyyənləşdirmək. Tətbiqin nəyi qəbul etdiyini bildirdiyi üçün təhlükəli simvolları blok etməyə çalışmaqdan daha etibarlıdır. |

---

## 2. OWASP Top 10:2025 Ümumi Baxış

### 2.1 Tam Kateqoriya Siyahısı

| Kod | Kateqoriya | Qısa Məna |
|-----|-----------|-----------|
| **A01:2025** | Broken Access Control | İstifadəçilər nəzərdə tutulan icazələri xaricindəki məlumatlara və ya funksiyalara daxil ola bilir |
| **A02:2025** | Security Misconfiguration | Tətbiq, framework, bulud, server və ya təhlükəsizlik başlıqlarında təhlükəsiz olmayan konfiqurasiya |
| **A03:2025** | Software Supply Chain Failures | Asılılıqlar, build-lər, artifact-lar, CI/CD və ya paylama infrastrukturunda etibar uğursuzluqları |
| **A04:2025** | Cryptographic Failures | Həssas məlumatlar zəif, çatışmayan və ya yanlış kriptoqrafiya ilə qorunur |
| **A05:2025** | Injection | Etibar edilməyən giriş interpretator tərəfindən əmr və ya sorğu kimi icra edilir |
| **A06:2025** | Insecure Design | Dizayn səviyyəsində təhlükəsizlik nəzarətləri çatışmır və ya effektiv deyil |
| **A07:2025** | Authentication Failures | Autentifikasiya, etimad məlumatı bərpası, MFA və ya sessiya idarəetməsindəki qüsurlar |
| **A08:2025** | Software or Data Integrity Failures | Kod, yeniləmələr, seriallaşdırılmış məlumatlar və ya kritik məlumatlar bütövlük yoxlaması olmadan etibar edilir |
| **A09:2025** | Security Logging and Alerting Failures | Təhlükəsizlik hadisələri effektiv şəkildə loglanmır, izlənilmir, xəbərdarlıq edilmir |
| **A10:2025** | Mishandling of Exceptional Conditions | Xəta idarəetməsi, anormal vəziyyət, fail open və istisna idarəetmə qüsurları |

---

### 2.2 2025 Versiyasında Nə Dəyişdi?

- **A03:2025 Software Supply Chain Failures** — köhnə "Vulnerable and Outdated Components" əhatə dairəsini genişləndirdi: asılılıqlar, build pipeline-ları, artifact depozitarları, paket qeydiyyatçıları və paylama infrastrukturunu əhatə edir.
- **A10:2025 Mishandling of Exceptional Conditions** — yanlış istisna idarəetməsi, fail open, məntiq xətaları və anormal vəziyyət idarəetməsini ayrı kateqoriya kimi təqdim edir.
- **Server-Side Request Forgery (SSRF)** — artıq müstəqil 2021 kateqoriyası deyil; indi **A01:2025 Broken Access Control** altında əhatə edilir.
- **A09:2025** — yalnız log yaratmağı deyil, həm də əməli xəbərdarlıq və hadisəyə müdaxilə iş axınlarını vurğulayır.

---

## 3. A01:2025 — Qırıq Giriş Nəzarəti (Broken Access Control)

**A01:2025 Broken Access Control** — OWASP Top 10:2025-in birinci kateqoriyasıdır. Rəsmi OWASP A01:2025 səhifəsi onu istifadəçilərin nəzərdə tutulan icazələri xaricində fəaliyyət göstərməsi kimi təsvir edir.

Bu kateqoriya veb tətbiqlərdə kritikdir, çünki müasir sistemlər məlumatları API endpoint-ləri, obyekt ID-ləri, tenant sərhədləri, rol yoxlamaları və xidmətdən xidmətə sorğular vasitəsilə qoruyur. Sistemə daxil olan istifadəçi avtomatik olaraq hər resurs üçün avtorizasiya edilmiş sayılmır; əsl təhlükəsizlik qərarı serverin həmin xüsusi resursa həmin istifadəçinin hansı əməliyyatı edə biləcəyini yoxlayıb-yoxlamamasıdır.

2025 buraxılışında **SSRF** da bu kateqoriya altında əhatə edilir, çünki bir çox SSRF halları hücumçuya server vasitəsilə daxili resurslara giriş imkanı verir.

---

### 3.1 Kök Səbəb

Giriş nəzarəti hansı istifadəçinin hansı resursda hansı əməliyyatı edə biləcəyini müəyyən edən siyasətdir. Bu nəzarət müştəridə deyil, etibarlı server tərəfi kodunda tətbiq edilməlidir.

Broken access control adətən bunlarda meydana gəlir:

- Endpoint girişi yoxlayır, lakin avtorizasiyanı yoxlamır
- İstifadəçi tərəfindən idarə olunan `id`, `account_id`, `tenant_id` və ya `file_id` dəyərləri qəbul edilir
- Admin funksiyaları yalnız UI-da gizlənib
- API metodları ardıcıl olmayan avtorizasiya yoxlamaları istifadə edir
- JWT-lərdən, cookie-lərdən, gizli sahələrdən gələn rol məlumatı doğrulanmadan etibar edilir
- Çox kirayəçili (multi-tenant) tətbiqlər tenant izolyasiyasını tətbiq etmir

---

### 3.2 Tipik Hücum Ssenarisi (IDOR)

İstifadəçi öz sifarişini görür:

```http
GET /api/orders/1001 HTTP/1.1
Host: vulnerable-app.example
Cookie: session=user_a_session
```

Hücumçu eyni endpoint-də fərqli sifariş nömrəsini sınayır:

```http
GET /api/orders/1002 HTTP/1.1
Host: vulnerable-app.example
Cookie: session=user_a_session
```

> Tətbiq `1002` sifarişinin `user_a`-ya aid olub-olmadığını yoxlamadan qaytararsa, bu **IDOR (Insecure Direct Object Reference)** nümunəsidir.

---

### 3.3 Zəif Kod vs. Müdafiə Olunan Kod

**Zəif Kod** — yalnız `order_id` ilə qeyd alır, sessiya istifadəçisi ilə qeyd sahibi arasındakı əlaqəni doğrulamır:

```python
@app.get("/api/orders/<order_id>")
def get_order(order_id):
    order = db.query("SELECT * FROM orders WHERE id = ?", [order_id])
    return jsonify(order)
```

**Müdafiə Olunan Kod** — həm `order_id`, həm də autentifikasiya edilmiş istifadəçinin ID-si ilə filtrləyir:

```python
@app.get("/api/orders/<order_id>")
def get_order(order_id):
    user = current_user()
    order = db.query(
        "SELECT * FROM orders WHERE id = ? AND owner_id = ?",
        [order_id, user.id]
    )
    if not order:
        abort(404)
    return jsonify(order)
```

---

### 3.4 Test Yanaşması

Giriş nəzarəti testi birdən çox istifadəçi tələb edir. Minimum olaraq fərqli imtiyaz səviyyələrinə sahib hesablardan istifadə edin:

- Anonim istifadəçi
- Standart istifadəçi
- Fərqli standart istifadəçi
- İmtiyazlı istifadəçi
- Admin və ya tenant sahibi

Eyni endpoint-ləri hər rolun sessiyası ilə müqayisə edin. `GET`, `POST`, `PUT`, `PATCH` və `DELETE`-i ayrı-ayrılıqda test edin. Tətbiq `GET` üçün avtorizasiyanı tətbiq edib, `DELETE` üçün unutmuş ola bilər.

---

### 3.5 Müdafiə Nəzarətləri

- **Varsayılan olaraq rədd et (deny-by-default)** prinsipindən istifadə edin.
- Avtorizasiyanı mərkəzi middleware və ya siyasət vasitəsilə tətbiq edin.
- Resurs mülkiyyəti yoxlamalarını domain modelində məcburi edin.
- Verilənlər bazası sorğularında və xidmət məntiğində tenant izolyasiyasını tətbiq edin.
- Müştəri tərəfindəki rol, qiymət, limit və ya sahiblik məlumatına etibar etməyin.
- CORS-u etibarlı mənşələrlə məhdudlaşdırın.
- Giriş nəzarəti uğursuzluqlarını loglayın və təkrarlanan cəhdlər üçün xəbərdarlıq edin.

---

### 3.6 Hesabat Qeydi

Yaxşı giriş nəzarəti hesabatı yalnız "başqa istifadəçinin məlumatı görünür" demir. O, hansı rolun hansı resursa daxil olduğunu, gözlənilən davranışı, faktiki cavabı, təsirlənmiş məlumat növünü və tövsiyə olunan server tərəfi mülkiyyəti nəzarətini göstərir.

---

## 4. A02:2025 — Təhlükəsizlik Yanlış Konfiqurasiyası (Security Misconfiguration)

**A02:2025 Security Misconfiguration** — tətbiq, framework, server, konteyner, bulud xidməti, verilənlər bazası və ya təhlükəsizlik başlığında təhlükəsiz olmayan konfiqurasiya deməkdir.

Bu risk əhəmiyyətlidir, çünki bugünkü veb tətbiqlər yalnız tətbiq kodundan ibarət deyil. Əks proxylər, API gateway-lər, obyekt saxlaması, konteyner runtime-ları, Kubernetes manifestləri, framework parametrləri, sirr idarəetməsi, HTTP təhlükəsizlik başlıqları və bulud IAM siyasətləri hamısı təhlükəsizlik səthini təşkil edir.

---

### 4.1 Kök Səbəb

Təhlükəsizlik yanlış konfiqurasiyası çox vaxt kod səhvindən deyil, **təhlükəsiz varsayılanların olmamasından** qaynaqlanır:

- İstehsalatda debug rejimi aktiv saxlanılıb
- Standart admin hesabları və ya standart şifrələr
- Lazımsız xidmətlər, portlar, endpoint-lər və ya nümunə tətbiqlər
- Qovluq siyahısı aktiv
- Çatışmayan və ya təhlükəsiz olmayan təhlükəsizlik başlıqları
- Açıq bulud saxlama bucketləri
- XXE-yə icazə verən şəkildə konfiqurasiya edilmiş XML parserlər
- Stack trace-ləri, yolları və ya sirləri ifşa edən xəta mesajları

---

### 4.2 HTTP Başlıq Nümunəsi

**Təhlükəsiz olmayan cavab** — server versiyasını və texnologiya stackini ifşa edir:

```http
HTTP/1.1 200 OK
Server: Apache/2.4.49
X-Powered-By: Express
Content-Type: text/html
```

**Daha təhlükəsiz cavab** — texnoloji məlumat gizlənib, təhlükəsizlik başlıqları əlavə edilib:

```http
HTTP/1.1 200 OK
Content-Type: text/html; charset=utf-8
Strict-Transport-Security: max-age=31536000; includeSubDomains
X-Content-Type-Options: nosniff
Content-Security-Policy: default-src 'self'
Referrer-Policy: no-referrer
Permissions-Policy: geolocation=()
```

> Bu başlıqlar tətbiqi özlüyündə təhlükəsiz etmir, lakin brauzer tərəfli riski azaldır və daha təhlükəsiz varsayılanlar yaradır.

---

### 4.3 Debug Rejimi Ssenarisi

**Zəif davranış:**

```http
GET /api/profile?debug=true HTTP/1.1
Host: vulnerable-app.example

HTTP/1.1 500 Internal Server Error
Traceback (most recent call last):
  File "/srv/app/profile.py", line 42, in get_profile
DatabaseError: relation "users_private" does not exist
DB_HOST=10.0.2.15
DB_USER=app_readonly
```

> Bu cavab hücumçuya texnologiya stack-i, daxili IP-lər, fayl yolları və məlumat strukturu haqqında məlumat verir. Bu məlumat sonrakı injeksiya və ya giriş nəzarəti testini asanlaşdıra bilər.

---

### 4.4 Təhlükəsiz Konfiqurasiya Yanaşması

Konfiqurasiya təhlükəsizliyi yalnız manuel yoxlama siyahısına görə deyil:

- Infrastructure as Code faylları kod icmalından keçir
- İstehsal və staging eyni təhlükəsizlik əsas xəttindən istifadə edir
- Sirlər depozitarlarda və ya şəkillərdə saxlanılmır
- Konteyner şəkilləri yalnız minimal paketlər ehtiva edir
- Standart hesablar və nümunə tətbiqlər silinir
- Təhlükəsizlik başlıqları əks proxy və ya tətbiq qatında mərkəzi olaraq tətbiq edilir
- Konfiqurasiya sürüşməsi (drift) avtomatik yoxlanılır

---

### 4.5 Müdafiə Nəzarətləri

- Hər mühit üçün təkrarlana bilən bərkidilmə prosesi yaradın.
- Lazımsız funksiyaları, xidmətləri, paketləri və nümunə faylları silin.
- Avtomatlaşdırma vasitəsilə təhlükəsiz əsas xətti tətbiq edin və yoxlayın.
- İstehsal debug çıxışını deaktiv edin.
- Mərkəzləşdirilmiş xəta idarəetməsindən istifadə edin.
- Sirlər üçün platforma sirr menecerindən və ya vault-dan istifadə edin.
- Bulud IAM-ı və bucket siyasətlərini ən az imtiyaz ilə məhdudlaşdırın.

> Təhlükəsizlik yanlış konfiqurasiyası kiçik bir parametr kimi görünə bilər, lakin çox vaxt hücumçunun kəşf və imtiyaz artırma zəncirindəki ilk addım olur.

---

## 5. A03:2025 — Proqram Təchizat Zənciri Uğursuzluqları (Software Supply Chain Failures)

**A03:2025 Software Supply Chain Failures** — 2025 buraxılışındakı ən mühüm genişlənmələrdən biridir. Rəsmi OWASP A03:2025 səhifəsi qeyd edir ki, bu risk yalnız zəif komponentlərdən istifadə etməklə məhdudlaşmır; asılılıqları, build sistemlərini, CI/CD pipeline-larını, artifact depozitarlarını, developer alətlərini və paylama infrastrukturunu da əhatə edir.

Müasir veb tətbiqlər çox vaxt tətbiq komandası tərəfindən birbaşa yazılan koddan daha çox üçüncü tərəf kodu, paketlər, konteyner şəkilləri və build alətlərindən asılıdır. Bu səbəbdən hücumçunun hədəfi istehsal endpoint-i olmaya bilər; npm paketi, GitHub Action, CI runner, konteyner qeydiyyatçısı, IDE uzantısı və ya vendor yeniləmə mexanizmi ola bilər.

---

### 5.1 Kök Səbəb

Müasir veb tətbiqlər minlərlə birbaşa və tranzitiv asılılıqdan istifadə edə bilər. Tətbiq təhlükəsizliyi yalnız öz kodunuzdan deyil, həm də bunlardan asılıdır:

| Komponent | Risk |
|-----------|------|
| **Paket qeydiyyatçısı** | Zərərli paket yüklənməsi |
| **Açıq mənbə kitabxanası** | Məlum zəifliklər |
| **Build aləti** | Zərərli kod injeksiyası |
| **CI/CD runner** | Sirr ifşası |
| **Konteyner şəkli** | Kompromis edilmiş əsas şəkil |
| **IDE uzantısı** | Developer iş stansiyası kompromisi |
| **Deployment skripti** | İcazəsiz dəyişiklik |

---

### 5.2 Tipik Risklər

- Zəif və köhnəlmiş asılılıqlar
- Dəstəklənməyən paketlər
- Tranzitiv asılılıq görünürlüğünün olmaması
- Paket qarışıqlığı və ya typosquatting
- CI/CD sirr ifşası
- İmzalanmamış build artifact-ları
- Developer iş stansiyası və ya IDE uzantısı kompromisi
- SBOM olmaması
- Nəzarətsiz vendor yeniləmələri

---

### 5.3 Zəif Asılılıq Axını Nümunəsi

```
Developer laptopу
  -> npm install unknown-helper
  -> paket postinstall skriptini işlədilir
  -> CI tokeni mühit dəyişənindən oxunur
  -> zərərli paket dəyişdirilmiş build artifact-ı yayımlayır
  -> istehsal kompromis edilmiş artifact-ı deploy edir
```

> Tətbiq kodunda klassik SQL Injection olmaya bilər. Zərərli kod istehsala çatdığı üçün təsir hələ də daha böyük ola bilər.

---

### 5.4 SBOM və Asılılıq Nəzarəti

**SBOM (Software Bill of Materials — Proqram Materialları Siyahısı)** — tətbiqi təşkil edən komponentlərin inventarıdır. SBOM özlüyündə müdafiə deyil, lakin zəiflik idarəetməsi, lisenziya nəzarəti, hadisəyə müdaxilə və təchizat zənciri görünürlüğü üçün zəruridir.

Nümunə asılılıq yoxlamaları:

```bash
npm audit --production
pip-audit
osv-scanner --recursive .
```

> Əmr çıxışı son qərar deyil. CVE-nin istismar edilə bilən olub-olmadığı istifadə olunan versiyadan, əlçatımlı funksiyalardan, ifşa edilmiş endpoint-lərdən asılıdır.

---

### 5.5 Təhlükəsiz CI/CD Prinsipləri

- Şaquli qorunma və məcburi kod icmalı istifadə edin.
- CI/CD sirlərini mühitə görə əhatə edin.
- Build və deploy icazələrini ayırın.
- Hər mühit üçün yenidən qurmaq əvəzinə imzalanmış artifact-ları irəli aparın.
- Paket kilit fayllarını nəzərdən keçirin.
- Build loglarında sirləri maskalayın.
- Asılılıq yeniləmələrini mərhələli şəkildə həyata keçirin.
- Konteyner şəkillərini müntəzəm skan edin və minimal əsas şəkillərdən istifadə edin.

---

### 5.6 Müdafiə Nəzarətləri

- SBOM-lar yaradın və mərkəzi olaraq izləyin.
- Etibar edilən paket qeydiyyatçılarından və sabitlənmiş versiyalardan istifadə edin.
- Asılılıq yeniləmələrini risk əsaslı proses vasitəsilə həyata keçirin.
- CI/CD pipeline-ını istehsal qədər kritik kimi qəbul edin.
- Build artifact-larını imzalayın və deploy-dan əvvəl yoxlayın.
- Developer alətlərini və iş stansiyası təhlükəsizliyini təchizat zənciri əhatə dairəsinə daxil edin.

> Bu kateqoriya göstərir ki, veb təhlükəsizliyi artıq yalnız HTTP endpoint testidir. Tətbiqin harada qurulduğu, hansı kodun istehsala çatdığı və həmin kodun bütövlüyünün necə yoxlandığı da təhlükəsizlik qiymətləndirilməsinin bir hissəsidir.

---

## 6. A04:2025 — Kriptoqrafik Uğursuzluqlar (Cryptographic Failures)

**A04:2025 Cryptographic Failures** — həssas məlumatların çatışmayan, zəif və ya yanlış kriptoqrafiya ilə qorunması deməkdir.

Bu kateqoriya yalnız şifrələmənin istifadə edilib-edilmədiyini soruşmaqla məhdudlaşmır. Hansı məlumatın həssas olduğunu, harada saxlandığını, hansı kanalın onu daşıdığını, hansı açarın onu qoruduğunu, açarın necə rotasiya edildiyini, şifrələrin necə saxlandığını və həssas məlumatın loglar və ya keşlər kimi ikincil səthlərə düşüb-düşmədiyini əhatə edir.

> Yanlış kriptoqrafiya çox vaxt tətbiqin funksionallığını pozmur; məlumatlar sessizliklə az qorunmuş olduğu halda sistem normal görünə bilər.

---

### 6.1 Kök Səbəb

Kriptoqrafik uğursuzluq adətən alqoritmləri bilməməkdən deyil, kriptoqrafiyanı **yanlış yerdə, yanlış məqsəd üçün və ya natamam tətbiq etməkdən** qaynaqlanır:

- Həssas məlumatları açıq mətnlə saxlamaq
- Şifrələmə və ya sürətli həşlərlə şifrələri saxlamaq
- MD5 və ya SHA1 kimi zəif həşlərdən istifadə etmək
- TLS-i yanlış konfiqurasiya etmək və ya HTTP geriyə dönüşünü buraxmaq
- Mənbə kodunda gizli açarlar saxlamaq
- Eyni açarı mühitlər və ya tenantlar arasında yenidən istifadə etmək
- CSPRNG əvəzinə proqnozlaşdırıla bilən PRNG istifadə etmək
- Bütövlük yoxlaması olmadan şifrələmək
- Həssas məlumatları keşlərdə və ya loglarda buraxmaq

---

### 6.2 Şifrə Saxlama Səhvi

**Zəif nümunə** — sürətli həş, offline brute-force hücumlarına qarşı zəifdir:

```python
password_hash = hashlib.sha256(password.encode()).hexdigest()
db.save_user(username, password_hash)
```

**Müdafiə olunan yanaşma** — duz (salt) və iş faktoru olan adaptiv alqoritm:

```python
from argon2 import PasswordHasher

ph = PasswordHasher()
password_hash = ph.hash(password)
db.save_user(username, password_hash)
```

---

### 6.3 Həssas Məlumat Qərarı

Bütün məlumatlar eyni səviyyədə qorunma tələb etmir. Məlumat klassifikasiyası ilə başlayın:

| Məlumat Növü | Qorunma Səviyyəsi |
|-------------|------------------|
| Etimad məlumatları və sessiya tokenləri | Çox yüksək |
| Şifrələr və bərpa tokenləri | Çox yüksək |
| Ödəniş və kart məlumatları | Çox yüksək |
| Sağlamlıq məlumatları | Yüksək |
| Şəxsi məlumatlar | Yüksək |
| Biznes sirləri | Yüksək |
| API açarları və imzalama açarları | Çox yüksək |

---

### 6.4 TLS və Nəqliyyat Təhlükəsizliyi

Bütün həssas veb tətbiq trafiki TLS ilə qorunmalıdır. Lakin TLS-in mövcudluğu tək başına kifayət deyil:

- Köhnə protokolları və zəif şifrləri deaktiv edin
- HSTS tətbiq edin
- Sertifikat zəncirini yoxlayın
- Daxili xidmətdən-xidmətə trafiki qoruyun
- Həssas cavabları keşləməyin

Nümunə təhlükəsiz başlıqlar:

```http
Strict-Transport-Security: max-age=31536000; includeSubDomains
Cache-Control: no-store
Pragma: no-cache
```

---

### 6.5 Müdafiə Nəzarətləri

- Lazım olmadıqca həssas məlumat saxlamayın.
- Şifrələr üçün Argon2, scrypt, bcrypt və ya PBKDF2 kimi uyğun adaptiv həşləmədən istifadə edin.
- Sirləri sirr menecerində saxlayın.
- Açar rotasiyası və mühit ayrılığı tətbiq edin.
- Məlumat sinfinə görə istirahət (at-rest) və ötürmə (in-transit) şifrələmə tələblərini müəyyənləşdirin.
- Autentifikasiyalı şifrələmədən istifadə edin.
- Həssas cavablar üçün keşləməni deaktiv edin.

> Kriptoqrafiya uğursuzluqları çox vaxt səssizdir. Məlumat oğurlanana və ya tokenlər təxmin edilənə qədər tətbiq normal işləyə bilər.

---

## 7. A05:2025 — İnjeksiya (Injection)

**A05:2025 Injection** — etibar edilməyən girişin interpretator tərəfindən əmr, sorğu və ya aktiv məzmun kimi icra edilməsi zamanı baş verir.

İnjeksiyanın əsas təhlükəsi ondan ibarətdir ki, tətbiqin "məlumat" kimi aldığı məzmun aşağı axın sistemi tərəfindən göstəriş kimi şərh edilir. Bu aşağı axın sistemi verilənlər bazası, shell, brauzer, şablon mühəriki, LDAP serveri, XML parser və ya ifadə dili ola bilər.

> Hücumçular adətən yalnız bir xüsusi simvola güvənmirlər; girişin istifadə edildiyi konteksti öyrənirlər. Bu səbəbdən injeksiya müdafiəsi simvolları blok etməkdən deyil, məlumatı əmr strukturundan ayırmaqdan asılıdır.

---

### 7.1 Kök Səbəb

İnjeksiyanın kök səbəbi məlumatı əmrlərdən ayırmamaqdan qaynaqlanır. Tətbiq istifadəçi girişini sorğuya, əmrə, şablona və ya HTML cavabına birləşdirdikdə, interpretator girişin bir hissəsini struktur kimi qəbul edə bilər.

---

### 7.2 SQL Injection Nümunəsi

**Zəif sorğu:**

```python
query = "SELECT * FROM accounts WHERE customer_id = '" + request.args["id"] + "'"
rows = db.execute(query)
```

**Hücum sorğusu:**

```http
GET /accounts?id=' OR '1'='1 HTTP/1.1
Host: vulnerable-app.example
Cookie: session=user_session
```

> Bu payload sorğu məntiqini dəyişdirir və icazəsiz qeydlər qaytara bilər.

**Parametrləşdirilmiş təhlükəsiz yanaşma:**

```python
query = "SELECT * FROM accounts WHERE customer_id = ?"
rows = db.execute(query, [request.args["id"]])
```

---

### 7.3 Əmr İnjeksiyası (Command Injection) Nümunəsi

**Zəif kod:**

```python
domain = request.args["domain"]
os.system("nslookup " + domain)
```

**Hücum sorğusu:**

```http
GET /lookup?domain=example.com;id HTTP/1.1
Host: vulnerable-app.example
```

**Daha təhlükəsiz yanaşma** — icazə siyahısı (allowlist) və arqument massivlərindən istifadə edir:

```python
domain = validate_domain(request.args["domain"])
subprocess.run(["nslookup", domain], shell=False, check=True)
```

---

### 7.4 XSS Həm də İnjeksiya Növüdür

XSS brauzerdan HTML/JavaScript interpretatoru kimi istifadə edir. İstifadəçi girişi kontekstə uyğun kodlaşdırma olmadan HTML-ə yazılarsa, brauzer onu skript kimi icra edə bilər.

**Zəif çıxış:**

```html
<p>Search result for: <script>alert(1)</script></p>
```

**Müdafiə olunan çıxış:**

```html
<p>Search result for: &lt;script&gt;alert(1)&lt;/script&gt;</p>
```

---

### 7.5 Aşkarlama Yanaşması

İnjeksiyanı etibarlı şəkildə aşkarlamaq üçün bir payload kifayət deyil. Hansı interpretatoru girişi aldığını başa düşün:

| İnjeksiya Növü | Aşkarlama Əlaməti |
|---------------|------------------|
| SQL | SQL xətaları və ya cavab fərqləri |
| Vaxt Əsaslı | Vaxt gecikməsi |
| Boolean | Cavab fərqləri |
| Əmr | Əmr çıxışı və ya zamanlama |
| XSS | HTML kontekst dəyişiklikləri |
| Şablon | Şablon xətaları |
| LDAP | LDAP filtr davranışı |
| XML | JSON və ya XML parser xətaları |

---

### 7.6 Müdafiə Nəzarətləri

- Sorğular və əmrlər üçün parametrləşdirilmiş API-lərdən istifadə edin.
- Shell sətirlərini birləşdirməyin.
- Kontekstə uyğun çıxış kodlaşdırması tətbiq edin.
- Müsbət giriş doğrulaması istifadə edin.
- ORM istifadə edilsə belə dinamik sorğu birləşdirməsindən çəkinin.
- Dinamik SQL quran saxlanılan prosedurlarda parametrləşdirməni istifadə edin.
- CI/CD-yə SAST, DAST, IAST və fuzzing əlavə edin.

> Qara siyahı əsaslı simvol bloklama özlüyündə etibarlı injeksiya müdafiəsi deyil. Əsas məqsəd məlumatın interpretator tərəfindən struktur kimi şərh edilməsinin qarşısını almaqdır.

---

## 8. A06:2025 — Təhlükəsiz Olmayan Dizayn (Insecure Design)

**A06:2025 Insecure Design** — bir təhlükəsizlik nəzarətinin heç vaxt nəzərə alınmadığı və ya yanlış dizayn edildiyi deməkdir. OWASP A06:2025 səhifəsi bunu tətbiq səhvindən fərqləndirir: təhlükəsiz olmayan dizayn mükəmməl tətbiq edilsə belə, təhlükəsiz olmayan iş axını yarada bilər.

Bu kateqoriya xüsusilə iş məntiqi, maliyyə əməliyyatları, çox kirayəçili memarlıq, istifadəçi rolları, sürət məhdudlaşdırması, sui-istifadə qarşısının alınması və vəziyyət keçidləri üçün əhəmiyyətlidir.

---

### 8.1 Kök Səbəb

Insecure Design adətən bunlarda meydana gəlir:

- Təhdid modelləmə aparılmır
- Sui-istifadə halları yazılmır
- İş məntiği limitləri müəyyən edilmir
- Təhlükəsizlik tələbləri istifadəçi hekayələrinə daxil edilmir
- Kritik iş axınları açıq vəziyyət maşını olmadan dizayn edilir
- Çox kirayəçili, ödəniş, geri qaytarma, kupon axınları yalnız xoşbəxt yol üçün dizayn edilir

---

### 8.2 Tətbiq Səhvi vs. Dizayn Qüsuru

**Tətbiq Səhvi:**

```
Tələb: Hər istifadəçi yalnız öz fakturasını görə bilər.
Səhv: Endpoint owner_id yoxlamasını unutdu.
Kateqoriya: A01 Broken Access Control
```

**Dizayn Qüsuru:**

```
Tələb: Kampaniya kodu istifadəçi başına limitsiz istifadə oluna bilər.
Nəticə: İstifadəçi eyni kuponu minlərlə dəfə yenidən istifadə edib maliyyə itkisi yarada bilər.
Kateqoriya: A06 Insecure Design
```

> Birinci nümunədə düzgün təhlükəsizlik tələbi var, lakin yanlış tətbiq. İkincidə isə nəzarət heç vaxt dizayn edilməyib.

---

### 8.3 İş Məntiği Hücumu Nümunəsi

E-ticarət sistemi ödəmə prosesini bu sırayla həyata keçirir:

```
1. Müştəri səbət cəmini hesablayır
2. Backend müştəridən total_amount qəbul edir
3. Bu məbləğ ödəniş provayderinə göndərilir
4. Sifariş təsdiqlənir
```

Hücumçu sorğunu dəyişdirir:

```http
POST /checkout HTTP/1.1
Host: vulnerable-app.example
Content-Type: application/json

{
  "cart_id": "cart_8841",
  "total_amount": 1.00,
  "currency": "USD"
}
```

> Backend səbət cəmini yenidən hesablamırsa, bu dizayn problemidir. Kod dizayn edildiyi kimi işləyə bilər, lakin təhlükəsizlik nəzarəti yanlış yerdə yerləşdirilib.

---

### 8.4 Təhdid Modelləmə Mini Nümunəsi

```
Aktiv: Ödəniş əməliyyatı
Hücumçu: Standart istifadəçi
Məqsəd: Məhsulları real qiymətdən aşağıya almaq
Etibar Sərhədi: Brauzer -> Backend API
Təhdid: Müştəri tərəfi total_amount manipulyasiyası
Nəzarət: Backend məhsul kataloqunda səbət qiymətini yenidən hesablayır
Test: total_amount-ı dəyişdirin və backend-in rədd etdiyini yoxlayın
```

---

### 8.5 Müdafiə Nəzarətləri

- Dizayn zamanı təhlükəsizlik tələblərini yazın.
- Kritik iş axınları üçün təhdid modelləmə tələb edin.
- İstifadəçi hekayələrinə sui-istifadə halları əlavə edin.
- Müştəridən biznes kritik dəyərlərə etibar etməyin.
- Vəziyyət maşınlarını və icazə verilən keçidləri açıq şəkildə müəyyən edin.
- Sui-istifadə halları üçün vahid və inteqrasiya testləri yazın.
- Təhlükəsiz dizayn nümunələri və qurulmuş komponentlərdən istifadə edin.

> Insecure Design tapıntıları skanerl tərəfindən nadir hallarda asanlıqla aşkarlanır. Bu kateqoriya testerın iş məntiğini, rol modellərini və sistemin gözlənilən təhlükəsiz davranışını başa düşməsini tələb edir.

---

## 9. A07:2025 — Autentifikasiya Uğursuzluqları (Authentication Failures)

**A07:2025 Authentication Failures** — sistemin etibarsız və ya yanlış istifadəçini qanuni kimi tanımasına imkan verən zəifliklər deməkdir.

Autentifikasiya istifadəçinin kim olduğunu sübut etdiyi yerdir, ona görə uğursuzluqlar yalnız giriş ekranı ilə məhdudlaşmamalıdır. Qeydiyyat, şifrə sıfırlama, MFA qeydiyyatı, sessiya rotasiyası, məni xatırla tokenləri, API tokenləri, SSO callback-lər və çıxış axınları da autentifikasiya təhlükəsizliyinin bir hissəsidir.

---

### 9.1 Kök Səbəb

Autentifikasiya uğursuzluqları bu sahələrdə meydana gəlir:

- Standart və ya zəif etimad məlumatları
- Brute force və credential stuffing qoruması yox
- Kritik əməliyyatlar üçün MFA tələb edilmir
- Zəif şifrə sıfırlama iş axınları
- Girişdən sonra sessiya ID-si yenilənmir
- Sessiya tokenləri URL-lərdə və ya müştərinin əlçatımı olan yerlərdə yerləşdirilir
- Çıxışdan sonra tokenlər etibarlı qalır
- JWT `aud`, `iss`, müddət bitimi və ya əhatə doğrulaması çatışmır

---

### 9.2 Credential Stuffing Ssenarisi

Hücumçu əvvəllər sızdırılmış etimad cütlərini giriş endpoint-i ilə sınayır:

```http
POST /login HTTP/1.1
Host: vulnerable-app.example
Content-Type: application/json

{
  "username": "alex@example.com",
  "password": "Winter2026!"
}
```

> Tətbiqdə sürət məhdudlaşdırması, sızdırılmış şifrə yoxlaması, MFA və ya bot aşkarlaması yoxdursa, hücumçu etibarlı kombinasiyalar tapa bilər.

---

### 9.3 İstifadəçi Adı Sadalama (Username Enumeration)

**Zəif cavablar** — fərqli mesajlar etibarlı istifadəçi adları haqqında məlumat verir:

```http
POST /login
username=unknown@example.com&password=test

HTTP/1.1 401 Unauthorized
Message: User does not exist
```

```http
POST /login
username=valid@example.com&password=test

HTTP/1.1 401 Unauthorized
Message: Invalid password
```

**Daha təhlükəsiz cavab** — eyni mesaj istifadə edilir:

```http
HTTP/1.1 401 Unauthorized
Message: Invalid username or password
```

---

### 9.4 Sessiya Fiksasiyası (Session Fixation) Nümunəsi

```
1. Hücumçu qurbana məlum session_id ilə keçid göndərir
2. Qurban sistemə daxil olur
3. Tətbiq girişdən sonra session_id-ni yeniləmir
4. Hücumçu qurbanın hesabına daxil olmaq üçün eyni session_id-dən istifadə edir
```

> Uğurlu girişdən sonra sessiya ID-si mütləq yenilənməlidir.

---

### 9.5 Müdafiə Nəzarətləri

- Kritik hesablar və həssas əməliyyatlar üçün MFA-nı məcburi edin.
- Standart etimad məlumatları ilə deploy-u qadağan edin.
- Şifrələri sızdırılmış şifrə siyahılarına qarşı yoxlayın.
- Sürət məhdudlaşdırması, eksponensial geri çəkilmə və bot aşkarlaması tətbiq edin.
- Sadalamaya qarşı giriş, sıfırlama və qeydiyyat cavablarını normallaşdırın.
- Şifrə sıfırlama tokenlərini qısa müddətli, tək istifadəli və yüksək entropili edin.
- Girişdən sonra sessiya ID-sini yeniləyin.
- `Secure`, `HttpOnly` və `SameSite` cookie parametrlərindən istifadə edin.
- Çıxış və boşdurma müddəti bitdikdən sonra tokenləri etibarsız edin.
- JWT iddialarını mərkəzi olaraq doğrulayın.

---

## 10. A08:2025 — Proqram və ya Məlumat Bütövlüyü Uğursuzluqları (Software or Data Integrity Failures)

**A08:2025 Software or Data Integrity Failures** — kod, yeniləmələr, seriallaşdırılmış məlumatlar və ya kritik məlumatların bütövlük yoxlaması olmadan etibar edilməsi deməkdir.

Bu kateqoriya "mənbə etibar edilə biləndir?" sualından daha az, "bu məlumat və ya proqram komponenti gözlənilən mənbədən gəldi və dəyişdirilmədiyini yoxladıqmı?" sualına daha çox yönəlir.

---

### 10.1 Kök Səbəb

Bu kateqoriya aşağıdakı kimi fərziyyələrdən qaynaqlanır:

- "Bu yeniləmə etibarlı mənbədən gəlməlidir."
- "Bu seriallaşdırılmış obyekt istifadəçi tərəfindən dəyişdirilə bilməz."
- "Bu CDN skripti həmişə eyni məzmunu ehtiva edəcək."
- "Müştəri dəyişdirsə belə bu cookie vacib deyil."
- "Bu artifact düzgün build-dən gəlmiş olmalıdır."

> Təhlükəsizlikdə etibar yoxlama olmadan fərz edilməməlidir.

---

### 10.2 Təhlükəsiz Olmayan Deserializasiya

Tətbiq istifadəçidən seriallaşdırılmış vəziyyəti yoxlama olmadan emal edərsə, hücumçu obyekt qrafını dəyişdirə bilər:

```http
POST /cart/restore HTTP/1.1
Host: vulnerable-app.example
Content-Type: application/json

{
  "state": "rO0ABXNyABFjb20uZXhhbXBsZS5DYXJ0..."
}
```

> Backend bu məlumatı imza və ya bütövlük yoxlaması olmadan deserializasiya edərsə, icazəsiz vəziyyət dəyişikliyinə, imtiyaz artırmasına və ya bəzi platformalarda uzaqdan kod icrasına səbəb ola bilər.

---

### 10.3 Müştəri Tərəfi Vəziyyət Manipulyasiyası

**Zəif cookie:**

```
Cookie: user={"id":42,"role":"user","discount":10}
```

**Hücumçu cookie-ni dəyişdirir:**

```
Cookie: user={"id":42,"role":"admin","discount":90}
```

> Backend bu dəyəri imza, sessiya axtarışı və ya server tərəfi vəziyyət doğrulaması olmadan qəbul edərsə, bu məlumat bütövlüyü uğursuzluğu olur.

---

### 10.4 Daha Təhlükəsiz Yanaşma

Kritik vəziyyət mümkün olan hallarda server tərəfindən saxlanmalıdır. Müştəri tərəfindən saxlanılmalıdırsa, imzalanmalı və dar əhatə dairəsi olmalıdır:

```http
Set-Cookie: session=opaque_random_id; HttpOnly; Secure; SameSite=Lax
```

> Server öz verilənlər bazasından `opaque_random_id` istifadə edərək vəziyyəti oxuyur. Müştəri rol, endirim və ya icazə dəyərlərini müəyyən edə bilmir.

---

### 10.5 Üçüncü Tərəf Skript Riski

Xarici skriptin güvənilməsi, həmin skriptin kompromis edilməsi istifadəçi sessiyalarına təsir göstərə bilər. Kritik səhifələrdə üçüncü tərəf skriptləri məhdudlaşdırılmalı, **Subresource Integrity (SRI)** və **Content Security Policy (CSP)** kimi nəzarətlər nəzərə alınmalıdır:

```html
<script
  src="https://cdn.example/library.min.js"
  integrity="sha384-EXAMPLE_HASH"
  crossorigin="anonymous">
</script>
```

---

### 10.6 Müdafiə Nəzarətləri

- Proqram və məlumat artifact-larını rəqəmsal imzalar və ya bütövlük yoxlamaları ilə doğrulayın.
- Etibar sərhədi xaricindən imzalanmamış seriallaşdırılmış məlumat qəbul etməyin.
- Kritik vəziyyəti müştəridə saxlamayın.
- CI/CD pipeline-larını və artifact yüksəltməsini bütövlük nəzarəti ilə qoruyun.
- Üçüncü tərəf skript istifadəsini azaldın və CSP tətbiq edin.
- Avtomatik yeniləmə mexanizmlərindəki imzaları yoxlayın.
- Cookie-lər, JWT-lər və tokenlər üçün əhatə, müddət bitimi və imza doğrulamasını tələb edin.

> Bu kateqoriya "Bu məlumat haradan gəldi və dəyişdirilmədiyini necə bilirik?" sualını mərkəzə qoyur.

---

## 11. A09:2025 — Təhlükəsizlik Loglama və Xəbərdarlıq Uğursuzluqları (Security Logging and Alerting Failures)

**A09:2025 Security Logging and Alerting Failures** — təhlükəsizlik hadisələrinin kifayət qədər kontekstlə loglanmaması, izlənilməməsi və ya tədbirə çevrilməməsi deməkdir.

Bu kateqoriya preventiv nəzarət kimi görünməyə bilər, lakin real sistemlərdə hücumun nə qədər tez fərq edildiyini müəyyənləşdirir.

---

### 11.1 Kök Səbəb

Hücumlar çox vaxt bir sorğuyla bitmir. Brute force, IDOR sadalama, injeksiya fuzzing, SSRF sondaj və hesab ələ keçirilmə cəhdləri davranış izləri buraxır. Tətbiq bu izləri toplamır və ya şərh etmirsə, hücum yalnız məlumat itkisindən sonra fərq edilə bilər.

Ümumi səhvlər:
- Uğursuz giriş hadisələri loglanmır
- Giriş nəzarəti uğursuzluqları loglanmır
- Kritik əməliyyatların audit izləri yoxdur
- Loglar yalnız yerli olaraq saxlanılır
- Log bütövlüyü qorunmur
- Həssas məlumat loglara yazılır
- Xəbərdarlıq hədləri və eskalasiya yoxdur
- DAST və ya sızma testi trafiki xəbərdarlıq yaratmır

---

### 11.2 Yaxşı Log Necə Görünür?

**Zəif log:**

```
Error: forbidden
```

**Daha faydalı təhlükəsizlik logu:**

```json
{
  "event": "access_control_denied",
  "user_id": "user_1042",
  "source_ip": "203.0.113.10",
  "method": "GET",
  "path": "/api/invoices/9001",
  "resource_owner": "user_7781",
  "request_id": "req_6f81",
  "timestamp": "2026-07-07T10:15:30Z"
}
```

> Bu log triage, korrelyasiya və məhkəmə analizini dəstəkləyə bilər.

---

### 11.3 Log İnjeksiyası Riski

Loglar həm də injeksiya səthi ola bilər. İstifadəçi girişi kodlaşdırma olmadan loglanırsa, hücumçu log formatını poza bilər.

**Zəif log sətiri:**

```
login failed for user: admin
ALERT: login success for root
```

> Bu, hücumçunun yeni sətir simvollarından istifadə edərək saxta log sətirləri yaratmasına imkan verə bilər. Strukturlaşdırılmış loglama və çıxış kodlaşdırması bu riski azaldır.

---

### 11.4 Xəbərdarlıq Tetikləməli Davranışlar

- Qısa müddətdə çoxlu uğursuz giriş cəhdləri
- Eyni istifadəçi çoxlu IP ünvanından
- İstifadəçinin fərqli sahibliklə yüzlərlə resurs ID-sini sınayan
- Standart istifadəçilərin admin endpoint-lərini sınaması
- İnjeksiya payload nümunələri
- Xəta dərəcəsi artımları
- Honeytoken girişi
- İstehsal sirri və ya canary tokeni müşahidəsi

---

### 11.5 Müdafiə Nəzarətləri

- Giriş, çıxış, şifrə sıfırlama, MFA, giriş nəzarəti uğursuzluqları və kritik məlumat dəyişikliklərini loglayın.
- Sorğu ID-si, istifadəçi ID-si, mənbə IP-si, endpoint, qərar və resurs kontekstini daxil edin.
- Həssas məlumatları loglamayın; lazım olduqda maskalayın.
- Log bütövlüyünü qoruyun və mərkəzləşdirilmiş log idarəetməsindən istifadə edin.
- Xəbərdarlıq hədlərini iş kontekstinə əsasən müəyyən edin.
- Xəbərdarlıqları SOC-a və ya hadisəyə müdaxilə playbook-larına bağlayın.
- DAST və sızma testi fəaliyyətinin xəbərdarlıq yaradıb-yaratmadığını test edin.

> Loglama olmadan hücumlar görünməzdir. Xəbərdarlıq olmadan görünən hücumlar vaxtında tədbirə çevrilməyə bilər.

---

## 12. A10:2025 — İstisna Halların Yanlış İdarə Edilməsi (Mishandling of Exceptional Conditions)

**A10:2025 Mishandling of Exceptional Conditions** — OWASP Top 10:2025-dəki yeni bir kateqoriyadır. Rəsmi A10:2025 səhifəsi onu anormal şərtlər, yanlış xəta idarəetməsi, məntiq xətaları və fail open-in təhlükəsizlik zəifliyinə çevrilməsi kimi təsvir edir.

Bu risk bizə xatırladır ki, tətbiq yalnız normal yolda deyil, həm də xətalar və gözlənilməz şərtlər zamanı təhlükəsiz davranmalıdır.

---

### 12.1 Kök Səbəb

Tətbiq gözlənilməz bir vəziyyətlə qarşılaşdıqda, təhlükəsiz, ardıcıl və müşahidə oluna bilən şəkildə davranmalıdır. Yanlış idarəetmə bunlarda baş verir:

- İstisnalar tutulmur və tətbiq naməlum vəziyyətə keçir
- Xətalar istifadəçiyə stack trace-lər qaytarır
- Avtorizasiya xidməti uğursuz olduqda giriş icazəsi verilir
- Əməliyyat rollback olmadan qismən tamamlanır
- Resurslar təmizlənmir, xidmət rəddiyyəsinə səbəb olur
- Çatışmayan parametrlər təhlükəsiz olmayan dəyərlərə varsayılan olaraq keçir
- Xəta artımları loglanmır və ya xəbərdarlıq edilmir

---

### 12.2 Fail Open Nümunəsi

**Zəif avtorizasiya sarmalayıcısı** — siyasət xidməti uğursuz olduqda girişə icazə verir:

```python
def can_access(user, resource):
    try:
        return policy_service.check(user.id, resource.id)
    except Exception:
        return True  # FAIL OPEN — TƏHLÜKƏLİ!
```

**Fail closed — təhlükəsiz yanaşma:**

```python
def can_access(user, resource):
    try:
        return policy_service.check(user.id, resource.id)
    except Exception:
        log_security_event("policy_check_failed", user.id, resource.id)
        return False  # FAIL CLOSED — TƏHLÜKƏSİZ
```

---

### 12.3 Ətraflı Xəta İfşası

**Zəif cavab** — daxili IP, istifadəçi adı və bağlantı sətirini ifşa edir:

```http
HTTP/1.1 500 Internal Server Error
Content-Type: text/plain

DatabaseError: password authentication failed for user "billing_admin"
Connection string: postgresql://billing_admin:secret@10.0.3.20/billing
```

**Daha təhlükəsiz cavab** — generik mesaj, sorğu ID-si ilə:

```http
HTTP/1.1 500 Internal Server Error
Content-Type: application/json

{
  "error": "request_failed",
  "request_id": "req_91ab"
}
```

> Ətraflı xətalar server tərəfindən etibarlı şəkildə loglanmalı, istifadəçi isə sorğu ID-si ilə generik mesaj almalıdır.

---

### 12.4 Əməliyyat Uğursuzluğu Ssenarisi

Üç addımdan ibarət maliyyə əməliyyatı:

```
1. Mənbə hesabından debet et
2. Hədəf hesabına kredit et
3. Əməliyyat qeydini yarat
```

> İkinci addım uğursuz olarsa və birincisi rollback edilmirsə, sistem ardıcıl olmayan vəziyyətə keçir. Hücumçular şəbəkə kəsilmələri, vaxt aşımları və ya paralel sorğularla bu anormal vəziyyəti tetikləməyə cəhd edə bilərlər.

---

### 12.5 Müdafiə Nəzarətləri

- Kritik iş axınları üçün fail closed-i standart edin.
- Mərkəzləşdirilmiş istisna idarəetməsindən istifadə edin.
- İstifadəçilərə generik xəta mesajları və sorğu ID-ləri qaytarın.
- Ətraflı xətaları server tərəfindən etibarlı şəkildə loglayın.
- Əməliyyat sərhədlərini və rollback davranışını açıq şəkildə müəyyən edin.
- Resurs təmizlənməsi üçün finally/defer kimi mexanizmlərdən istifadə edin.
- Resurs tükənməsini sürət məhdudları, kvotalar və vaxt aşımları ilə azaldın.
- Xəta artımları və təkrarlanan istisnalar üçün xəbərdarlıq edin.

> Bu kateqoriya "xəta baş verdikdə nə olur?" sualını təhlükəsizlik sualına çevirir. Təhlükəsiz sistem yalnız normal yolda deyil, gözlənilməz şərtlər altında da düzgün davranır.

---

*© OWASP Top 10 (2025) — Azərbaycanca Tam Bələdçi | Kibertəhlükəsizlik Laboratoriyası üçün hazırlanmışdır*
