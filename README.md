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

## חובה בכל סרטון (הוראת בעל המוצר, 21.11)
כל סרטון מסתיים בחתימה הקולית: צליל שני התווים (chime), ואחריו דיבוב הסלוגן בקול Danit (ElevenLabs voice_id `s0T0DT6EAPeX57MQpn3I`): "לבבות, הקניית הרגלים לילדים. פחות תזכורות, יותר לבבות." סרטון בלי חתימה קולית לא עולה לכאן.
קובץ הקול: ריפו Levavot, ענף media-inbox, `media/inbox/eleven/slogan-danit.mp3`; מיקס: `media/reels/src/audio.py` → `build()`.

## זרימת פרסום (vidIQ)
`vidiq_video_upload(url)` → `vidiq_social_post_draft_create` → אישור בעל המוצר → `vidiq_social_post_publish`.
לאינסטגרם: `vidiq_instagram_publish_reel` (עם תווית AI).
פירוט: `claude/VIDEO-UPLOAD-ROUTES.md` בפרויקט.

## קבצים
| קובץ | תיאור |
|---|---|
| reels/levavot-short-3tips-v3.mp4 | 3 טיפים (גרסה מתוקנת, פורסם ב-YouTube 21.11) |
| reels/levavot-v3-boker.mp4 | "בוקר בלי נדנודים" |
| reels/levavot-reel-games-v1.mp4 | משחקי הלימוד בלבבות (לוח הכפל, שברים, אנגלית, חשיבה) – הורים שחשוב להם לימוד. נוצר 21.11, ממתין לאישור |
| reels/levavot-reel-ru-v1.mp4 | גרסה ברוסית – הורים דוברי רוסית. נוצר 21.11, עודכן עם חתימה קולית; ממתין לאישור ובדיקת דובר שפת אם |
| reels/levavot-game-english-v1.mp4 | סדרת "משחק השבוע": אנגלית (apple) | 
| reels/levavot-game-shapes-v1.mp4 | משחק השבוע: צורות (משושה) |
| reels/levavot-game-fractions-v1.mp4 | משחק השבוע: שברים (פיצה) |
| reels/levavot-game-thinking-v1.mp4 | משחק השבוע: חשיבה לכיתה ב׳ (סדרות) |
| reels/levavot-game-israel-v1.mp4 | משחק השבוע: ידיעת הארץ |
| reels/levavot-game-flags-v1.mp4 | משחק השבוע: דגלי העולם |
| reels/levavot-v1-kvar-asiti.mp4 | "כבר עשיתי!" (מאושר 17.11) |
| reels/levavot-v2-bochrim-osim-tzovrim.mp4 | "הם בוחרים. הם עושים. הם צוברים." (מאושר 17.11) |
| reels/levavot-reel-store-v1.mp4 | חנות הלבבות: הילד בוחר פרס, ההורה מאשר |
| reels/levavot-reel-siblings-v1.mp4 | בלי תחרות בין אחים: כל ילד מול עצמו |
