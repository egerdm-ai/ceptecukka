# Yazılım planı (yeni repo — Leonida’ya ekleme)

Amaç: arkadaşın prompt’unu **dosya üreten masa** yapmak. İlk dilim video encoder, GTA cutter, Rio Hale **değil**.

## Dilim 1 — kâğıt gibi, ama kayıtlı

- Next.js masa (Türkçe UI).
- MOD 1: editör kaynak URL / not yapıştırır veya ajan aday üretir; skor formu; 70 altı gizli.
- MOD 2: iddia satırları + etiket dropdown.
- MOD 3: caption taslağı (karakter sayacı 1100–1700) + görsel slot 6–10 + onay kutusu.
- SQLite. Git’e caption gizli kalmak zorunda değil; **hak dosyası URL + lisans** evet. Secrets ayrı.

İnsan onayı olmadan Instagram API çağrısı yok.

## Dilim 2 — keşif yardımcı

- Kaynak listesinden başlık çekme (RSS / açık sayfalar). Caption çalma yok.
- IG keşif hesapları: **elle** “bu post’a bak” — scraping savaşı yok (ToS, ban, telif).

## Dilim 3 — görsel hak

- Wikimedia / Met / Rijksmuseum açık API veya elle accession.
- `hak_kontrolu_gerekli` olanlar onayda kilitli.

## Dilim 4 — yayın (isteğe bağlı, geç)

- Upload-Post veya Meta content publishing: **ayrı** app, ayrı token, Ceptecukka Business hesabı. Leonida `@gtanewwss` key’ini kopyalama.
- Carousel yükleme, caption yapıştırma. Otomatik schedule ancak `approved` sonrası ve editör tıkı.

## Dilim 5 — planlama

- Haftalık: 1 moda kotası, damar dengesi, “bu hafta 4 onaylı / 2 araştırma”.
- Takvim UI. Analytics sonra.

## Leonida’dan alınacak kod yok; alınacak desen

Onay tablosu, dry-run publish, `.env.local`, analyze≠publish. Şemalar bu klasörde `schemas/`.

## Teknik varsayılan (Ege)

TypeScript, Next, Tailwind, shadcn — Leonida ile aynı zevk, **ayrı package**. ffmpeg şart değil (carousel statik). Whisper yok. LLM: aday ve caption taslağı; editör her cümleyi keser. Model yasak kalıp listesini system prompt’ta tutar ([04-dil-ve-yasaklar.md](04-dil-ve-yasaklar.md)).
