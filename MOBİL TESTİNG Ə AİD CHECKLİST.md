# Test Hesabatı (Testing Report)

## EXPLORATORY TESTING

| ID | CHECKPOINT | EXPECTED RESULT | ACTUAL RESULT | STATUS |
| :--- | :--- | :--- | :--- | :--- |
| **CL-01** | Tətbiqin açılışı | Tətbiq loqo ilə aydın açılmalı, ana səhifəyə keçməlidir. | Tətbiq loqo ilə problemsiz açıldı və səhifə göründü. | ✅ PASS |
| **CL-02** | Əsas menyu və tablar arası keçid | Alt menyudakı bütün keçidlər kliklənən olmalı və düzgün səhifəni açmalıdır. | Alt menyudakı “home”, “courses”, “tasks”, “grades” və “profile” düymələri açır. | ✅ PASS |
| **CL-03** | Vizual elementlərin və yazıların nizamı | Şəkillər, mətnlər və düymələr səliqəli görünməli, bir-birinin üzərində görünməməlidir. | İnterfeys elementləri ekrana tam yerləşir və səliqəli görünür. | ✅ PASS |
| **CL-04** | Kurs kartlarına keçid funksiyası | Kursun üzərinə kliklədikdə materiallar açılmalıdır. | Həm “home”, həm də “courses” səhifəsində kurs kartlarına klik etdikdə heç nə açılmır. | ❌ FAIL |
| **CL-05** | “See all” düymələrini klik etmək | “See all” yazısına kliklədikdə müvafiq bölmənin tam siyahısı açılmalıdır. | Düyməyə basdıqda heç bir reaksiya baş vermir və səhifə açılmır. | ❌ FAIL |
| **CL-06** | Çıxış ssenarisi | Sistemdən çıxış etdikdən sonra istifadəçi məlumatları silinməli və giriş səhifəsinə yönləndirilməlidir. | Profil səhifəsindəki 3 nöqtəyə klik edib “sign out” düyməsinə klik etdikdə əsas səhifəyə yönləndirilir. | ✅ PASS |
| **CL-07** | Təkrar giriş etmək | Mövcud e-poçt yazıldıqda və “forgot password”a klik etdikdə gmaill-ə mesaj göndərilməli və şifrə sıfırlama bölməsindən parolu dəyişmək mümkün olmalı. | Gmail-ə mesaj göndərildi, “forgot reset” linkinə klik etdikdə **status code 422 xətası** verir. | ❌ FAIL |

---

## AD-HOC / MONKEY TESTING

| ID | CHECKPOINT | EXPECTED RESULT | ACTUAL RESULT | STATUS |
| :--- | :--- | :--- | :--- | :--- |
| **CL-08** | Düymələrə sürətli klikləmə | Alt menyudakı düymələrə çox sürətli kliklədikdə tətbiq donmamalıdır. | Düymələrə sürətli kliklədikdə tətbiq donmur, keçidlər icra olunur. | ✅ PASS |
| **CL-09** | Boş səhifələrin idarə edilməsi | Hələ məlumat daxil edilməyən səhifələrdə istifadəçiyə vizual bildiriş göstərilməlidir. | “Tasks” səhifəsində bildiriş mətni düzgün çıxır, lakin “grades” səhifəsi tamamilə boş ağ ekran olaraq qalır. | ❌ FAIL |
| **CL-10** | İnternet bağlantısının qəfil kəsilməsi | Tətbiqdə interneti söndürdükdə istifadəçiyə şəbəkə xətası (network error) çıxmalıdır. | Tətbiq tam çökmür, lakin ekranda kod xətası göstərir. | ❌ FAIL |
| **CL-11** | Tətbiqi arxa fona (background) atmaq | Tətbiqi qəfil bağlayıb yenidən açdıqda məlumatlar itməməlidir. | Tətbiqi arxa fona atıb yenidən açdıqda səhifə sıfırlanmır. | ✅ PASS |
| **CL-12** | Telefon zəngi kəsintisi | Aktiv olan zaman telefona zəng gəldikdə tətbiq çökməməlidir. | Zəng və bildiriş gəldikdə tətbiq arxa fonda stabil işləyir. | ✅ PASS |
| **CL-13** | Ekranı fırlatmaq | Telefonu yana çevirdikdə elementlər ekrana uyğunlaşmalı və sabit qalmalıdır. | Ekran fırladıldıqda elementlər ekrana düzgün uyğunlaşır. | ✅ PASS |
