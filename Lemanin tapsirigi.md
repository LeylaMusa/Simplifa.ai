# Bug Report

| Sahə | Məzmun |
|------|---------|
| **Bug İD** | BUG_98 |
| **Title** | POST /clients sorğusunda mənfi `age` qəbul edilir və `201` qaytarılır |
| **Description** | `POST /clients` sorğusunda `age` hissəsinə mənfi qiymət yazıldıqda və sorğu execute edildikdə `201 Created` cavabı qaytarılır. |
| **Addımlar** | 1. Bearer token ilə authorize olun.<br>2. `POST /clients` sorğusuna keçid edib **Try it out** düyməsinə klik edin.<br>3. `age` bölməsinə mənfi qiymət yazın.<br>4. Qalan bölmələrə və `id` hissəsinə valid data daxil edin.<br>5. **Execute** düyməsinə klik edin. |
| **Expected Result** | `400 Bad Request` çıxmalı və sorğu işləməməli idi. |
| **Actual Result** | `201 Created` cavabı qaytarıldı. |
| **Prioritet** | Yüksək |
| **Status** | Açıq / Təsdiqlənmiş |
| **Tapılan tarix** | 19.05.2026 |
| **Aşkar edən şəxs** | Leman Qurbanova |
| **Əlavələr** | - |
