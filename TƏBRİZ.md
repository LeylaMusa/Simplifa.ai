# Bug Hesabatı (Bug Report)

| Sahə | Məlumat |
| :--- | :--- |
| **Bug ID** | #4 |
| **Başlıq** | POST `/cars` sorğusunda mənfi il qəbul edilir və 201 Created qaytarılır. |
| **Prioritet (Priority)** | HIGH |
| **Ciddilik (Severity)** | HIGH |
| **Status** | Açıq (Open) |
| **Tapılan Tarix** | 19.05.2026 |
| **Tapan (Reporter)** | Təbriz Cəbrayılov |

## Təsvir (Description)
POST `/cars` sorğusunda il (year) hissəsinə mənfi qiymət yazıldıqda və sorğu execute edildikdə sistem bunu uğurla qəbul edir və `201 Created` cavabı qaytarır.

## Addımlar (Steps to Reproduce)
1. Swagger saytına keçid edin.
2. Autorizasiya (Authorization) bölməsinə Bearer tokeni əlavə edin.
3. **Cars** bölməsinə keçid edin.
4. **POST** sorğusunu *Try it out* edin.
5. Body bölməsində il sahəsinə mənfi qiymət daxil edin (məsələn: `-2024`).
6. Digər bölmələri düzgün şəkildə daxil edin.
7. *Execute* düyməsinə klik edin.

## Gözlənilən Nəticə (Expected Result)
Sistem mənfi ili qəbul etməməli, response olaraq `400 Bad Request` xətası göstərilməli və sorğu işləməməlidir.

## Real Nəticə (Actual Result)
Sorğu uğurla icra olundu və `201 Created` cavabı qaytarıldı (Mənfi il bazaya yazıldı).
