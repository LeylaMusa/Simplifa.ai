# Bug Report: #004 — Cars bölməsində POST sorğusunda icazəsiz 201 Created status kodunun qaytarılması

## Başlıq
Cars bölməsində POST sorğusu göndərərkən avtorizasiya xətasına baxmayaraq hər dəfə `201 Created` status kodunun gəlməsi (401 Unauthorized əvəzinə).

## Təsvir
İstifadəçi Swagger sənədləşməsində lazımi qaydada avtorizasiya olmadan (və ya yanlış məlumatlarla) `cars` bölməsində yeni post sorğusu yaratmaq üçün Body məlumatlarını daxil edib sorğu göndərdikdə, sistem təhlükəsizlik xətası vermək əvəzinə sorğunu uğurla icra edir.

---

## Addımlar (Steps to Reproduce)
1. Swagger saytına keçid edin.
2. Avtorizasiya (Authorization) bölməsinə Bearer Token-i əlavə edin.
3. **Cars** bölməsinə keçid edin.
4. POST sorğusunu aktivləşdirmək üçün **Try it out** düyməsinə klik edin.
5. Request Body hissəsindəki məlumatları doldurun (məsələn, `na il` bölməsinə `77777` yazın).
6. **Execute** düyməsinə klik edərək sorğunu göndərin.

---

## Gözlənilən Nəticə (Expected Result)
Sistem tərəfindən avtorizasiya və ya məlumat validation xətası olaraq **`401 Unauthorized`** (və ya müvafiq xəta kodu) göstərilməlidir. İcazəsiz post yaradılmasına icazə verilməməlidir.

## Real Nəticə (Actual Result)
Sorğu uğurla icra olunur və response olaraq **`201 Created`** status kodu qaytarılır.

---

## Meta Məlumatlar
* **Prioritet (Priority):** Medium
* **Ciddilik (Severity):** Medium
* **Status:** Açıq (Open)
* **Tapılan Tarix:** 19.05.2026
* **Tapan (Reporter):** Təbriz Cəbrayılov
