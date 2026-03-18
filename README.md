# Autovrakoviště Sviadnov

DEMO: https://stuchla.info5249.workers.dev/

Moderní webová prezentace pro autovrakoviště, výkup a ekologickou likvidaci autovraků, prodej náhradních dílů a autoservis. Projekt je postaven na rychlém a moderním statickém generátoru [Astro](https://astro.build/) s čistým HTML a custom CSS pro maximální rychlost a uživatelský zážitek.

## 🚀 Technologie & Vlastnosti

*   **Astro Framework:** Komponentově orientovaný statický generátor zaměřený na výkon.
*   **Custom CSS:** Vlastní rozsáhlý stylopis `public/style.css` založený na sadě CSS proměnných (barvy, weby) pro jednoduchou údržbu vizuální identity a layoutů.
*   **Responzivní design:** Veškeré sekce jsou plně přizpůsobeny pro mobilní a desktopová zařízení s využitím moderních grid/flexbox přístupů.
*   **Interaktivní funkce:** Obsahuje překryvné vyhledávání (`search overlay`), poptávkové modální okno (`PoptavkaModal.astro`) a responzivní ovládání navigace v hlavičce (`Header.astro`).
*   **Splide.js:** Plynulé frontend slidery s dynamickým ovládáním (např. sekce zákaznických hodnocení).
*   **FsLightbox:** Integrace elegantních překryvných fotogalerií a zvětšení obrázků (`ContactSection`, `ContactSectionLight`, galerie vozů aj.).

## 📂 Struktura Projektu

Projekt logicky rozděluje šablony (layouts), specifické komponenty (components) a samotné cesty podstránek (pages):

```text
/
├── public/                 # Statické soubory, které nepodléhají buildu (obrázky, ikony SVG, `style.css`)
├── src/
│   ├── components/         # Astro komponenty rozdělené do funkčních bloků (Header, Footer, Grid, Banner, Form...)
│   ├── layouts/            # Základní layout obalující aplikace (připojení stylů, meta hlavičky, sloty pro obsah)
│   └── pages/              # Definice podstránek generovaných Astro routováním:
│       ├── index.astro            # Úvodní domovská stránka (Home)
│       ├── autovrakoviste.astro   # Přehled autovrakoviště, značek a skladů (katalog)
│       ├── autoservis.astro       # Informace a ceník k autoservisu
│       ├── likvidace.astro        # Stránka zaměřená detailům ekologické likvidace vozidel
│       ├── kontakty.astro         # Otevírací hodiny a kontaktní údaje 
│       ├── blog.astro             # Výpis tematických článků a aktualit webu
│       └── blog-detail.astro      # Strana ukázkového článku/detialu novinky
│
├── package.json            # Závislosti Node.js (Astro cli plugin ad.) a spouštěcí npm příkazy 
└── astro.config.mjs        # Konfigurace základního běhu platformy Astro
```

## 💻 Spuštění pro vývoj (Development)

Poté co si projekt zkopírujete na lokální disk, využijte standardní CLI NPM příkazy:

1. Zkompilovat/Nainstalovat potřebné balíčky aplikací:
```bash
npm install
```

2. Spuštění lokálního testovacího serveru na adrese s živým aktualizováním (typically `http://localhost:4321/`):
```bash
npm run dev
```

## 🏗️ Build do produkce (Production Build)

Pro finální nahrání stránek na libovolný webový hosting projekt plně vygeneruje statické připravené soubory (výstupy HTML, zabalenou JS strukturu).

```bash
npm run build
```

Zkompilované soubory se automaticky uloží do cílové podsložky `dist/`. Celá složka `dist` tak tvoří hotový čistý statický web bez nutnosti složité databáze. Poté vygenerovaný obsah už stačí jen nahrát na server pomocí protokolu FTP či deployment systémů (Vercel, Netlify, Github Pages aj.).
