# נכסי מותג · OZ Global B2B

אתר גיידליין פנימי של OZ Global B2B — לוגו, צבעים, פונטים וחומרים להורדה,
עם פאנל ניהול לעדכון תוכן והחלפת קבצים.

## מבנה
- `index.html` — הפורטל (דו‑לשוני עברית/אנגלית).
- `admin.html` — פאנל הניהול (עריכת תוכן + העלאת/החלפת קבצים).
- `data/content.json` — כל התוכן שנמצא באתר. זהו "מקור האמת" — הפאנל עורך אותו.
- `assets/logo/` — קובצי הלוגו (SVG / PNG / JPG / AI, ב‑RGB ו‑CMYK).
- `assets/fonts/` — הפונט פלוני: WOFF2 לאתר + OTF להורדה.
- `assets/resources/` — חומרים להורדה (תבניות, פונטים, PDF וכו').

## העלאה ל‑GitHub Pages
1. צרו מאגר חדש ב‑GitHub (לדוגמה `brand`).
2. העלו את **כל התוכן של התיקייה הזו לשורש המאגר** (כך ש‑`index.html` יושב בשורש).
   דרך הדפדפן: בעמוד המאגר → **Add file → Upload files** → גררו את כל הקבצים → **Commit**.
   או דרך טרמינל:
   ```bash
   git init && git add -A && git commit -m "OZ brand portal"
   git branch -M main
   git remote add origin https://github.com/<owner>/<repo>.git
   git push -u origin main
   ```
3. במאגר: **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   בחרו ענף `main` ותיקייה `/ (root)`, ושמרו.
4. אחרי כדקה האתר יעלה בכתובת `https://<owner>.github.io/<repo>/`.

## פאנל הניהול — עדכון תוכן והחלפת קבצים
נכנסים ל‑`…/admin.html`.

**חיבור חד‑פעמי ל‑GitHub** (לשונית "חיבור GitHub"):
- ממלאים owner, repo, branch.
- יוצרים Fine‑grained Personal Access Token עם הרשאת **Contents: Read and write** על המאגר,
  ומדביקים. הטוקן נשמר רק בדפדפן שלכם.

**אחרי החיבור** אפשר:
- לערוך טקסטים, צבעים, טון דיבור, אימג'רי.
- להוסיף/להחליף חומרים להורדה: בלשונית "חומרים להורדה" → "בחירת קובץ" (למשל טמפלייט פאוורפוינט) → **שמירה ל‑GitHub**.
- הקובץ נשמר במאגר תחת `assets/resources/`, ה‑`content.json` מתעדכן, וה‑GitHub Pages נבנה מחדש אוטומטית (בערך דקה).

**בלי טוקן?** בלשונית "מתקדם" יש **"הורדת content.json"** — מורידים, מעלים למאגר ידנית,
ואת הקבצים הנלווים מעלים לתיקיית `assets/resources/`.

## עדכון קובץ קיים במהירות (בלי הפאנל)
פשוט מעלים קובץ באותו שם ל‑`assets/resources/` במאגר (Upload files → Commit). זהו.
