# Simplifai Checklist Verification Report

| Test Case | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|
| 1. “New Application” buttonu vasitəsilə yeni tətbiq yaratmaq | Simplifai-də “New Application” buttonuna klik edərək yeni tətbiq yaratdım | Network paneldə: <br> `https://smplifai-backend.vercel.app/api/applications/submit` <br> Status Code: `201 Created` <br> Request Method: `GET` | Pass |
| 2. “Logout” buttonu vasitəsilə hesabdan çıxış etmək | Simplifai-də “Logout” buttonuna klik edərək hesabdan çıxış etdim | Network paneldə: <br> `https://tcrdbtaksnqezkbzgfys.supabase.co/auth/v1/logout?scope=global` <br> Status Code: `204 No Content` <br> Request Method: `POST` | Pass |
| 3. “Delete” buttonu vasitəsilə tətbiqi silmək | Simplifai-də “Delete” buttonuna klik edərək yaratmış olduğum tətbiqi sildim | Network paneldə: <br> `https://smplifai-backend.vercel.app/api/applications/{id}` <br> Status Code: `204 No Content` <br> Request Method: `DELETE` | Pass |
