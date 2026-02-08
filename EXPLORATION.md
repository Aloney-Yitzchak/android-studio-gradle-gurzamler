# חקר Android Studio - תשובות התלמיד

**שם התלמיד:** גור
**תאריך:** 06.02.2026

---

## חלק א' - סיור ב-Android Studio (30 נקודות)

### שאלה 1: תיקיות ראשיות (10 נקודות)
צלם screenshot של חלון הProject (תצוגת Android) והדבק כאן:

**[הדבק תמונה]**
<img width="959" height="597" alt="image" src="https://github.com/user-attachments/assets/bbbee777-a533-4145-a92b-9c057716fa85" />
<img width="958" height="597" alt="image" src="https://github.com/user-attachments/assets/441fe8ba-e49d-4517-8553-f4e64b13e679" />
<img width="960" height="595" alt="image" src="https://github.com/user-attachments/assets/fc8a6e26-6375-40dd-9872-277e855e59d3" />
<img width="958" height="598" alt="image" src="https://github.com/user-attachments/assets/7d2b18b7-1c56-4ed5-9585-7b5b695eac3a" />





רשום את שמות 3 התיקיות הראשיות שאתה רואה:

1. JAVA
2.  RES
3. MANIFESTS

---

### שאלה 2: AndroidManifest.xml (10 נקודות)
צלם screenshot של קובץ AndroidManifest.xml והדבק כאן:

**[הדבק תמונה]**
<img width="959" height="597" alt="image" src="https://github.com/user-attachments/assets/eb297727-fdc0-443f-867f-b87d5512554f" />

**מה התפקיד של קובץ זה? (2-3 משפטים)**


הוא הקובץ המרכזי שמגדיר את מבנה האפליקציה באנדרואיד.
הוא מציין את כל ה-Activities, Services, Permissions ושאר רכיבי האפליקציה, ומאפשר למערכת האנדרואיד לדעת איך להפעיל את האפליקציה ומה היא צריכה כדי לעבוד.

---

### שאלה 3: תיקיית res (10 נקודות)
צלם screenshot של תוכן תיקיית res והדבק כאן:

**[הדבק תמונה]**
<img width="146" height="133" alt="image" src="https://github.com/user-attachments/assets/28aa41e7-ee2a-4063-b8cf-eeabde9c322c" />

**רשום 3 תיקיות משנה שנמצאות בתוך res:**

1. XML
2. LAYOUT
3. VALUES

**מה נמצא בכל אחת מהתיקיות האלה?**
1.  xml
מכילה קבצי הגדרות XML שונים של האפליקציה, כמו הגדרות תפריטים, הגדרות Preference או קובצי Navigation.

2. layout
מכילה את קבצי ה-XML שמגדירים את מבנה הממשק (UI) של האפליקציה – מסכים, כפתורים, טקסטים ומסגרות.

3. values
מכילה קבצי משאבים כמו מחרוזות (strings.xml), צבעים (colors.xml), גדלים (dimens.xml) וסגנונות (styles.xml).



---

## חלק ב' - עבודה עם Gradle (40 נקודות)

### שאלה 4: build.gradle (Module) (15 נקודות)
צלם screenshot של build.gradle (Module: app) אחרי שהוספת את Gson:

**[הדבק תמונה]**
<img width="412" height="240" alt="image" src="https://github.com/user-attachments/assets/b9154f6d-23ad-48dc-a363-b8e237c7376b" />


**איזו שורה הוספת בדיוק?**

```gradle
 implementation 'com.google.code.gson:gson:2.10.1'  
```

---

### שאלה 5: מה זה Gson? (15 נקודות)

**הסבר במילים שלך: מה Gson עושה ולמה זה שימושי?**
Gson היא ספרייה של גוגל שממירה בין JSON לאובייקטים של Java ולהפך.
כלומר, היא מאפשרת לקחת מידע שמגיע מהשרת בפורמט JSON ולהפוך אותו לאובייקטים של מחלקות בקוד שלך, ולהיפך — להפוך אובייקטים לקובץ JSON שניתן לשלוח לשרת.

זה שימושי כי רוב האפליקציות מתקשרות עם שרתים שמחזירים מידע ב־JSON, ו-Gson חוסכת הרבה קוד ידני ומונעת שגיאות, במיוחד כשיש מבנה נתונים מורכב עם רשימות ומחלקות מקוננות.



**תן דוגמה: מתי תשתמש ב-Gson באפליקציה אמיתית? (למשל באפליקציות כמו WhatsApp או Instagram)**


ב־WhatsApp או Instagram, אם האפליקציה מקבלת רשימת הודעות, פוסטים או פרטי משתמש מהשרת, Gson יכולה להפוך את המידע הזה ישירות לאובייקטים בקוד ואז להציג אותם במסך בלי לכתוב קוד נפרד לפירוק JSON

---

### שאלה 6: Gradle Sync (10 נקודות)

**מה קורה כשלוחצים על "Sync Now"?**
כשלוחצים על Sync Now, Android Studio מבצע את הפעולות הבאות:

Gradle קורא את הקובץ build.gradle המעודכן.

מוריד את כל הספריות (dependencies) החדשות שהוספת, כמו Gson.

מחבר את הספריות החדשות לפרויקט, כך שהקוד יכול להשתמש בהן.

מעדכן את ההגדרות של הפרויקט ומוודא שהבנייה (Build) תעבוד.

בקיצור – זה "מסנכרן" את הקובץ Gradle עם הפרויקט בפועל.



**מה יקרה אם לא נלחץ על Sync Now אחרי שהוספנו dependency?**

הספרייה החדשה לא תיטען למחשב.

הקוד לא יזהה את המחלקות של הספרייה (למשל Gson).

יופיעו שגיאות Unresolved reference או Cannot resolve symbol.

האפליקציה לא תתקמפל עד שתבצע Sync.


---

## חלק ג' - ארגון קבצים (30 נקודות)

### שאלה 7: strings.xml (10 נקודות)

**צלם screenshot של קובץ strings.xml שלך (עם לפחות 3 strings):**

**[הדבק תמונה]**

<img width="959" height="600" alt="image" src="https://github.com/user-attachments/assets/e94e7faf-4efe-4e74-ba65-72fa757f0fea" />

**רשום את 3 ה-strings שהוספת:**

1.<string name="app_name">MyApp</string>

2.<string name="title_main">Main Screen</string>

3.<string name="btn_save">Save</string>
---

### שאלה 8: Layout File חדש (10 נקודות)

**איך יצרת layout file חדש? תאר את התהליך צעד אחר צעד:**

1. _________________
2. _________________
3. _________________
4. _________________

**צלם screenshot של ה-layout החדש:**

**[הדבק תמונה]**

---

### שאלה 9: הבנה כללית (10 נקודות)

**מה ההבדל בין build.gradle (Project) ל-build.gradle (Module)?**




**למה חשוב להפריד בין קוד (java/) לבין משאבים (res/)?**




---

## שאלות בונוס (10 נקודות נוספים)

### בונוס 1: (5 נקודות)
**מצא ותעד dependency נוסף שלא דיברנו עליו בשיעור. מה הוא עושה?**

**Dependency:**
```gradle

```

**מה הוא עושה:**



---

### בונוס 2: (5 נקודות)
**מה ההבדל בין minSdk ל-targetSdk ב-build.gradle?**




---

## סיכום אישי

**מה למדת היום שהכי עזר לך להבין את Android Studio?**




**מה היה הכי מאתגר?**




---

**סיימתי את המשימה! ✅**

**זמן שלקח לי:** ______ דקות
