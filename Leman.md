| Checklist | Actual result |
|---|---|
| 1. Yeni application yaratmaq<br>2. Qeydiyyatdan keçmiş user-lə dashboard hissəsinə keçid edirəm<br>3. New application buttonuna klik etmək<br>4. Phone number yazmaq<br>5. Choose buttonuna klik etmək<br>6. Browse a file buttonuna klik edərək file əlavə etmək<br>7. Submit passport to review buttonuna klik etmək<br>8. Passportu review etdikdən sonra approve buttonuna klik edərək yeni application yaratmaq | Network paneldə:<br>`https://smplifai-backend.vercel.app/api/applications/submit`<br>- submit request with status `201` |
| 1. Qeydiyyatdan keçmiş user-lə logout etmək mümkündür - Log out buttonuna klik edirəm | Network paneldə:<br>`https://tcrdbtaksnqezkbzgfys.supabase.co/auth/v1/logout?scope=global`<br>- logout sorğusu with status `204` |
| 1. Yaratdığım application-u delete etmək mümkündür - delete buttonuna klik etmək | Network paneldə:<br>`https://smplifai-backend.vercel.app/api/applications/{id}`<br>- delete sorğusu with status `204` |
