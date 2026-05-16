# Simplifai Checklist Verification Report

---

# 1. Logout vasitəsilə hesabdan çıxış etmək

### Checklist Verification

Simplifai-da logout vasitəsilə hesabımdan çıxış etdim.

### Expected Result

Network paneldə aşağıdakı sorğu göründü:

```http
https://tcrdbtaksnqezkbzgfys.supabase.co/auth/v1/logout?scope=global
```

Status Code: `200 OK`

Sorğu növü: `CONNECT`

### Actual Result

İstifadəçi hesabdan uğurla çıxış etdi və logout request-i uğurla göndərildi.

---

# 2. “Sign in with Google” vasitəsilə hesaba daxil olmaq

### Checklist Verification

Simplifai saytında “Sign in with Google” vasitəsilə hesabıma daxil olmağa çalışdım.

### Expected Result

Network paneldə aşağıdakı request göründü:

```http
https://ui-avatars.com/api/?name=User&background=random
```

Status Code: `200 OK`

Sorğu növü: `GET`

### Actual Result

Google vasitəsilə giriş prosesi uğurla başladı və request düzgün şəkildə göndərildi.

---

# 3. “New application” vasitəsilə yeni tətbiq yaratmaq

### Checklist Verification

Simplifai saytında “New application” buttonu vasitəsilə yeni tətbiq yaratdım.

### Expected Result

Network paneldə aşağıdakı request göründü:

```http
https://tcrdbtaksnqezkbzgfys.supabase.co/rest/v1/profiles?select=phone%2Cphone_verified&{id}
```

Status Code: `200 OK`

Sorğu növü: `GET`

### Actual Result

Yeni tətbiq yaradılarkən profil məlumatları uğurla əldə edildi.

---

# 4. “Delete” buttonu vasitəsilə tətbiqi silmək

### Checklist Verification

Simplifai saytında yaratdığım tətbiqi “Delete” buttonu vasitəsilə sildim.

### Expected Result

Network paneldə aşağıdakı request göründü:

```http
https://smplifai-backend.vercel.app/api/applications/98e598aa-dac7-4e05-905e-07599283016b
```

Status Code: `204 No Content`

Sorğu növü: `DELETE`

### Actual Result

Tətbiq uğurla silindi və server tərəfindən uğurlu cavab qaytarıldı.
