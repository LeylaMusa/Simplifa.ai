# Bug Report

| Sahə | Məzmun |
|------|---------|
| **Bug İD** | BUG_98 |
| **Title** | POST /clients sorğusunda mənfi age qəbul edilir və 201 qaytarılır |
| **Description** | POST /clients sorğusunda age hissəsinə mənfi qiymət yazıldıqda və execute edildikdə 201 status kodu qaytarılır |
| **Addımlar** | 1. Bearer token ilə authorize olun. <br> 2. POST /clients sorğusuna keçid edib “Try it out” düyməsinə klik edin. <br> 3. Age bölməsinə mənfi yaş yazın. <br> 4. Qalan bölmələrə və id hissəsinə valid data daxil edin. <br> 5. Execute düyməsinə klik edin. |
| **Expected Result** | 400 Bad Request çıxmalı və sorğu işlənməməli idi |
| **Actual Result** | 201 OK status kodu çıxdı |
| **Prioritet** | Yüksək |
| **Severity** | Yüksək |
| **Status** | Açıq / Təsdiqlənmiş |
| **Tapılan tarix** | 19.05.2026 |
| **Aşkar edən şəxs** | Ləman Qurbanova |
| **Əlavələr** | <img width="974" height="475" alt="image" src="https://github.com/user-attachments/assets/db0bafa9-2e42-4f05-a827-0da6b49f5d20" />
 |
