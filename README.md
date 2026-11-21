# levavot-media — ספריית המדיה הציבורית של לבבות

ריפו **ציבורי, לווידאו ותמונות בלבד** (בלי קוד, בלי סודות). משמש כדי שכלי פרסום (vidIQ, Meta, TikTok וכו') יוכלו למשוך קובץ מכתובת HTTPS ציבורית.

## מבנה
- `reels/` — ריליס ו-Shorts מוכנים לפרסום (mp4, 9:16)
- `images/` — תמונות לפוסטים (לפי צורך)

## כתובת קבועה לקובץ
`https://raw.githubusercontent.com/InAiNak/levavot-media/main/reels/<שם-קובץ>.mp4`

## נהלים
1. **לא מעלים כאן** קוד, מפתחות, נתוני משפחות או צילומי מסך עם פרטים אישיים.
2. שמות קבצים: `levavot-<סוג>-<נושא>-vN.mp4` (למשל `levavot-short-3tips-v3.mp4`).
3. כל קובץ שמועלה כאן הוא ציבורי — מעלים רק תוכן שאושר לפרסום.
4. אחרי פרסום מעדכנים את `claude/SOCIAL-SCHEDULE.md` ו-`claude/PUBLICATION-LOG.md` בפרויקט.
5. גודל מירבי ל-vidIQ: 299MB. קבצי מקור/עריכה נשארים בריפו הפרטי (`InAiNak/Levavot`, ענף `media-inbox`).

## זרימת פרסום (vidIQ)
`vidiq_video_upload(url)` → `vidiq_social_post_draft_create` → אישור בעל המוצר → `vidiq_social_post_publish`.
לאינסטגרם: `vidiq_instagram_publish_reel` (עם תווית AI).
פירוט: `claude/VIDEO-UPLOAD-ROUTES.md` בפרויקט.

## קבצים
| קובץ | תיאור |
|---|---|
| reels/levavot-short-3tips-v3.mp4 | 3 טיפים (גרסה מתוקנת, פורסם ב-YouTube 21.11) |
| reels/levavot-v3-boker.mp4 | "בוקר בלי נדנודים" |
