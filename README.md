
📘 Budget Manager - README
===========================

ברוכים הבאים לפרויקט ניהול התקציב האישי!  
לפניכם הוראות התקנה ראשוניות להפעלת המערכת בצורה תקינה.

📦 שלב ראשון: התקנת ספריות ה־Node
----------------------------------
בטרמינל, יש להריץ את הפקודה הבאה מתוך תיקיית הפרונטאנד:

```
npm install
```

🛠️ שלב שני: עדכון קובץ החיבור למסד הנתונים
------------------------------------------
בפרויקט של צד השרת (ASP.NET Core), יש להיכנס לקובץ `Program.cs`  
ולוודא ששורת החיבור (`connectionString`) מצביעה אל ה־**Database** הנכון שלך. לדוגמה:

```csharp
 string connectionString = "Server=YOUR_DB; Database=AccountManagementDb; Trusted_Connection=True;TrustServerCertificate=True;";
```
🗄️ שלב שלישי: הרצת מיגרציה ליצירת הטבלאות במסד הנתונים

------------------------------------------
לאחר עדכון ה-Connection String, יש להריץ את הפקודה הבאה בפרויקט צד השרת כדי ליצור את הטבלאות במסד הנתונים:


dotnet ef database update


🔴 **החלף את שם מסד הנתונים (`YOUR_DB`) לשם שבחרת אצלך ב־SQL Server.**

🧾 שלב רביעי: הרצת סקריפטים של קטגוריות
 SQL בשרת - גש לתיקיית ה
---------------------------------------
יש להריץ **את שני הסקריפטים** המצורפים (`IncomeCategoriesScripr.sql` ו־`ExpenseCategoriesScript.sql`) על מסד הנתונים,  
כדי לוודא שהאפליקציה תעבוד עם הקטגוריות הבסיסיות.

🤖 שלב חמישי: שימוש ב־GPT
---------------------------
המערכת כוללת יכולת של ניתוח AI מבוסס GPT.

> על מנת להפעיל את ה־API של GPT, יש לפנות אליי לקבלת המפתח האישי (`API Key`).

📱 ניתן לפנות אליי גם דרך **WhatsApp** לקבלת המפתח. 

לאחר קבלת המפתח:

1. פתח את קובץ `appsettings.json` בפרויקט של השרת.
2. הוסף את השורה הבאה:

```json
"GptSettings": {
  "ApiKey": "הכנס כאן את המפתח שלך"
}
```

3. שמור והפעל את השרת כרגיל.


🚀 הפעלת המערכת
----------------
- ודא שהשרת פעיל (`dotnet run` או דרך Visual Studio).
- ודא שהפרונט פועל (`npm start`).
- פתח את הדפדפן בכתובת `http://localhost:3000`.

בהצלחה 🎉  
אם יש לך שאלות או תקלות – אני כאן!


## אודות הפרויקט

מערכת ניהול תקציב אישי המאפשרת למשתמשים לעקוב אחר הכנסות והוצאות חודשיות בצורה מסודרת וידידותית למשתמש.

### תכונות עיקריות:
- רישום הכנסות והוצאות לפי קטגוריות (כגון: שכר, שכירות, קניות, בילויים וכו').
- צפייה במידע החודשי באמצעות גרף פאי מפורט.
- עריכת נתונים חודשיים גם על חודשים קודמים.
- ממשק משתמש אינטואיטיבי הבנוי ב־React.
- הרשמה כלקוח Basic (גישה מלאה לניהול תקציב) או כלקוח PRO (גישה ל־GPT לקבלת המלצות ניהול חכמות).
- ניתוח נתוני התקציב עם בינה מלאכותית (ללקוחות PRO בלבד).

### התממשקות עם GitHub:
הקוד כולו מנוהל ב־GitHub. ניתן לשכפל את הריפוזיטורי באמצעות הפקודה:
```bash
SERVER: clone https://github.com/KarenMiz/AccountManagementServer
CLIENT: clone https://github.com/KarenMiz/BudgetManagement
```

---
