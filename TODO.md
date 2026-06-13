# PackAndWild — Master TODO

> Letzte Prüfung: 2026-06-13  
> Strategie: Landing Page first — Monetarisierung über Pinterest Affiliate, nicht direkt auf der Seite.

---

## 🔴 KRITISCH — Sofort erledigen (blockiert Live-Betrieb)

- [ ] **Impressum vervollständigen** — `imprint/index.html` öffnen und die rot markierten Platzhalter ersetzen:
  - Postanschrift (Straße, Hausnummer, PLZ, Ort) — Ladungsfähige Anschrift; Postfach reicht rechtlich nicht aus
  - Telefonnummer (DDG §5 Pflicht)
  - _Tipp: Bis zur Monetarisierung kann die Seite als private Hobby-Seite ohne Impressum laufen. Sobald Einnahmen fließen: Adress-Service für ~5 €/Monat holen (z.B. impressum-privatschutz.de)_
- [ ] **`git push`** ausführen — alle neuen Dateien committed, aber nicht live  
  `cd ~/Documents/Claude/Projects/PackAndWild && git add . && git commit -m "Add about page, Pinterest CTAs, privacy update" && git push`
- [ ] **HTTPS enforced** auf GitHub Pages aktivieren  
  GitHub → Settings → Pages → "Enforce HTTPS"

---

## 🟡 FEHLENDE / AUSSTEHENDE SEITEN

- [x] `/about/index.html` — About/Über uns mit Pinterest als Haupt-CTA ✅
- [ ] `/de/index.html` — Deutsche Startseite
- [ ] `/de/wandern/index.html` — Hiking DE
- [ ] `/de/vanlife/index.html` — Van Life DE
- [ ] `/de/camping/index.html` — Camping DE
- [ ] `/de/edc/index.html` — EDC DE
- [ ] `/de/reisen/index.html` — Travel DE
- [ ] `/de/zuhause/index.html` — Home DE

---

## 📣 PINTEREST-STRATEGIE (Priorität 1 nach Launch)

- [ ] **Pinterest Domain-Verifizierung** — packandwild.de mit Pinterest verbinden  
  _Pinterest → Settings → Claim website_
- [ ] **Rich Pins aktivieren** — ermöglicht Produkt-Metadaten direkt auf Pinterest-Pins  
  _Setzt Verifizierung voraus_
- [ ] **Boards aufbauen** — je Kategorie ein Board: Hiking, Van Life, Camping, EDC, Travel, Home
- [ ] **Affiliate-Programm für Pinterest** — Amazon PartnerNet oder AWIN-Links direkt in Pinterest Pins

---

## 💸 AFFILIATE-LINKS AUF DER WEBSITE (deferred — nach Pinterest-Launch)

Alle Produkt-CTAs zeigen aktuell auf `#` — absichtlich, bis Monetarisierung startet.

- [ ] `hiking/index.html` — 11 Links (6 Produkt-CTAs + 5 Merchant-Pills)
- [ ] `vanlife/index.html` — 10 Links (6 Produkt-CTAs + 4 Merchant-Pills)
- [ ] `camping/index.html` — 7 Links (6 Produkt-CTAs + Merchant-Pills)
- [ ] `edc/index.html` — 7 Links (6 Produkt-CTAs + Merchant-Pills)
- [ ] `travel/index.html` — 7 Links (6 Produkt-CTAs + 6 Merchant-Pills)
- [ ] `home/index.html` — 7 Links (6 Produkt-CTAs + Merchant-Pills)
- [ ] `index.html` — 3 Links (Featured Picks CTAs)

---

## 🖼️ CONTENT

- [ ] **Produktbilder** hochladen — alle Seiten nutzen aktuell Emoji-Platzhalter  
  _Bilder in `/img/products/` ablegen, `<img>` statt Emoji-Span einbauen_
- [ ] **OG-Bilder** erstellen (`/img/og-*.jpg`) — Open Graph Tags referenzieren diese, aber sie fehlen noch  
  _1200×630px, eines pro Kategorie_

---

## 📊 SEO & ANALYTICS

- [ ] **Google Search Console**: Domain verifizieren + sitemap.xml einreichen  
  _URL: https://search.google.com/search-console_
- [ ] **Analytics** einrichten — Empfehlung: **Plausible** (datenschutzfreundlich, kein Cookie-Banner nötig)

---

## ✅ ERLEDIGT

- [x] Homepage `index.html` mit Nav, Hero, 6 Category Cards, Featured Picks, Footer
- [x] `hiking/index.html` mit 6 Produktkarten, Merchant Strip, Why-Section
- [x] `vanlife/index.html` mit 6 Produktkarten
- [x] `camping/index.html` mit 6 Produktkarten
- [x] `edc/index.html` mit 6 Produktkarten
- [x] `travel/index.html` mit 6 Produktkarten
- [x] `home/index.html` mit 6 Produktkarten
- [x] **`/about/index.html`** — Brand Landing Page mit Pinterest als Haupt-CTA, Markengeschichte, Werte, Affiliate-Disclosure
- [x] **Pinterest CTA** auf Homepage — im About-Teaser + Footer-Nav + Disclosure-Bar
- [x] **Privacy Policy** aktualisiert — AWIN-Abschnitt durch "External Links & Pinterest" ersetzt (kein aktives Tracking)
- [x] **Disclosure-Bar** auf Homepage angepasst — kein aktives Affiliate-Claim mehr
- [x] Bilinguales EN/DE Toggle auf allen Seiten (localStorage-Persistenz)
- [x] Burger-Menü mit Click-outside-close auf allen Seiten
- [x] `rel="nofollow sponsored"` auf allen Affiliate-Platzhalter-Links
- [x] Canonical Tags auf allen Seiten
- [x] Meta Description auf allen Seiten
- [x] hreflang (en + de + x-default) auf allen Seiten
- [x] Open Graph Tags + Twitter Card Tags auf allen 7 Seiten
- [x] **Favicon** (favicon.svg, P&W Monogram)
- [x] **sitemap.xml** mit hreflang-Einträgen
- [x] **robots.txt** mit Sitemap-Verweis
- [x] **404.html** (bilingual)
- [x] **Google Fonts self-hosted** — Inter + Playfair Display lokal in `/fonts/` (DSGVO-konform)
- [x] **Copyright-Jahr** 2026 auf allen Seiten
- [x] **`.gitignore`** (node_modules ausgeschlossen)
- [x] **`imprint/index.html`** — Impressum nach DDG §5 ⚠ Adresse + Telefon noch einzutragen
- [x] **`privacy/index.html`** — DSGVO-Datenschutzerklärung, Stand: kein aktives Affiliate-Tracking
- [x] GitHub Repo erstellt und deployt
- [x] Ionos DNS konfiguriert (A-Records + CNAME)
- [x] Domain packandwild.de
- [x] CNAME File im Repo
- [x] SETUP.md Dokumentation

---

## 📊 FORTSCHRITT

**Kritisch:** 3 offen (Impressum-Adresse, git push, HTTPS)  
**Fehlende Seiten:** 7 offen (DE-Seiten)  
**Affiliate-Links:** 52 offen (bewusst deferred)  
**Gesamt:** ~30/~90 Aufgaben abgeschlossen ✅
