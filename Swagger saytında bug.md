# Bug Report

| Field | Details |
|---|---|
| **Bug ID** | 1 |
| **Başlıq** | Swagger interfeysində e-mail sahəsinə düzgün formatdan fərqli olaraq yalnız mətn daxil edildi və validasiya yoxlanıldı |
| **Təsvir** | Swagger saytında e-mail sahəsinə yalnız mətn formatında məlumat daxil edildi. Daxil edilən məlumatda “@” işarəsi və domen hissəsi (məsələn, gmail.com) mövcud deyildi. Bu səbəbdən sistem tərəfindən e-mail formatının validasiya olunması gözlənildi. |
| **Addımlar** | 1. POST `/students` endpoint-də “Try it out” düyməsinə klik etdim. <br> 2. Body hissəsini doldurdum, lakin e-mail sahəsinə “@gmail.com” yazmadan yalnız string formatında məlumat daxil etdim. <br> 3. “Execute” düyməsinə klik etdim. |
| **Gözlənilən nəticə** | `400 Bad Request` qaytarılmalıdır, çünki e-mail formatı yanlışdır. |
| **Real nəticə** | `201 OK` status kodu qaytarıldı. |
| **Prioritet** | Orta |
| **Severity** | Orta |
| **Status** | Açıq |
| **Tapılan tarix** | 19.05.2024 |
| **Aşkar edən şəxs** | Abuşova Selcan |
| **Əlavələr** | ![Bug Screenshot](https://github.com/user-attachments/assets/4e7e0b4c-52a3-4f28-beb9-ae945057d253) |
