# Test Hesabatı (Bug Report & Verifikasiya)

## Xülasə (Summary)
Aşağıda tətbiqin funksionallıqları üzrə gözlənilən və faktiki nəticələrin müqayisəsi qeyd olunmuşdur.

---

## Test Nəticələrinin Cədvəli

| # | Addım / Ssenari | Gözlənilən Nəticə (Expected) | Faktiki Nəticə (Actual) | Status |
|:-:|:---|:---|:---|:---:|
| **1** | Yeni tətbiq (application) yaratmaq | "Yeni application yarat" düyməsinə kliklədikdə yeni tətbiq uğurla yaradılmalıdır. | **Sorğu uğursuz oldu.** <br> `POST` URL: `https://smplifai-backend.vercel.app/api/application/` <br> **Status Code:** `500 Internal Server Error` | ❌ **Failed** |
| **2** | Profil məlumatlarının yenilənməsi | Profil tabına kliklədikdə məlumatlar uğurla yenilənməli/görünməlidir. | **Sorğu uğurla tamamlandı.** <br> `GET/PUT` URL: `https://smplifai-backend.vercel.app/api/profiles/` <br> **Status Code:** `200 OK` |  **Passed** |
| **3** | Saytdan çıxış (Logout) etmək | "Logout" düyməsinə kliklədikdə istifadəçi sessiyası sonlandırılmalıdır. | **Sorğu uğurla tamamlandı (Məzmun yoxdur).** <br> `POST` URL: `https://smplifai-backend.vercel.app/api/profiles/` <br> **Status Code:** `204 No Content` |  **Passed** |

---

## Ətraflı Log və Şərhlər

### 1. Yeni Application Yaratmaq
> **Xəta Təsviri:** İstifadəçi yeni tətbiq yaratmaq istədikdə backend tərəfində daxili server xətası baş verir. Network panelində `500` xətası alınır. Bu funksionallıq bloklanıb və təcili düzəldilməlidir.

### 2. Profil Məlumatlarının Yenilənməsi
> **Qeyd:** Profil tabına keçid zamanı API düzgün cavab verir (`200 OK`). Məlumatların çəkilməsində və ya yenilənməsində hər hansı bir problem aşkarlanmadı.

### 3. Saytdan Çıxış (Logout)
> **Qeyd:** Çıxış sorğusu API tərəfindən uğurla qəbul edilir. `204 No Content` status kodu sessiyanın problemsiz şəkildə sonlandırıldığını göstərir.
