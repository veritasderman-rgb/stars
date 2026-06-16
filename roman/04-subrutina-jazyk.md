# Jazyková subrutina pro military SF v češtině

Cíl: hlídat, **aby nevznikaly jazykové průšvihy** — a aby text zněl jako
Fabian (3. os., přítomný čas, dvouvrstvá čeština), ne jako AI slop.

Stavíme na **existujícím redakčním systému** (`CLAUDE.md`, `SKILL.md`,
strážci v kořeni repa), který je ale laděný na urban fantasy + erotiku (LOFT).
Tento dokument říká, **co převzít beze změny, co přenastavit a co přidat**.

---

## A) Co z existujícího systému zůstává (žánrově neutrální)

Spustit beze změny, jen krmit biblí tohoto projektu (`roman/01-svet-bible.md`,
`roman/02-postavy.md`):

- **`CLAUDE.md`** — orchestrace, 7 vrstev, smyčka max. 3 cykly, konvergence,
  nedestruktivní git workflow. Platí, ale **pořadí vrstev a cesty je nutné
  zapojit** — viz D (pořadí) a F (zapojení do orchestrátoru). Bez toho jede
  starý cyklus LOFTu.
- **`konzistence`** — bible + kontrola soudržnosti. Klíčové pro glosář termínů
  (kýlový klín, hladiny, proudy, Přerod…) — nejednotnost terminologie je
  v SF častější průšvih než v erotice.
- **`rytmus`** — kadence vět. Funguje, jen v instrukci nahradit „erotická
  gradace" za „bojová gradace" (krátké údery v akci, dech v popisu/politice).
- **`hlas-strazce`** — pojistka proti uhlazení, právo veta. Zůstává; jen
  „erotika má být odvážná" → „akce má být syrová, humor drsný, vulgarita
  vojáků se nemá učesávat".

## B) Co se PŘEPISUJE (erotika → military SF)

Tyhle strážce nelze pustit beze změny — jsou plné erotických instrukcí:

- **`klise-lovec`** → nahrazen `klise-scifi` (viz `.claude/agents/`).
  Nové pasti: gear-porn klišé, technobabble, katalog akce („pak vystřelil,
  pak se kryl, pak…"), heroická klišé.
- **`vnitrni-hlas`** → přenastavit: místo „sebepoznání skrz tělesnou scénu"
  hlídat **psychologii pod tlakem** (strach, vina, velitelské rozhodnutí,
  cena rozkazu). Reyeverovo mlčení, Vosino podezření, Sarnova logika.
- **`dialog`** → ponechat jádro, ale doplnit **vojenský rejstřík**: rozlišit
  radiovou/velitelskou komunikaci (formální, vykání, „rozumím, konec") od
  drsné obecné češtiny mezi vojáky. Hlídat autentičnost volacích znaků.
- **`smysly`** — v repu **chybí** (README ho zmiňuje, ale není zacommitovaný).
  Pro SF doporučuji ho doplnit se zaměřením na **smyslový naturalismus**
  (prach, mráz, pach kovu/spáleniny, tlak přetížení) — Fabianova devíza.

## C) Co se PŘIDÁVÁ (nové, čeština je v tomhle komplikovaná)

- **`cestina-strazce`** (viz `.claude/agents/cestina-strazce.md`) — mechanická
  kontrola českých chyb, které jsou v žánru časté a které ani Fabian neuhlídal.
  Tohle je nová, ryze jazyková vrstva navíc.

---

## D) Doporučené pořadí vrstev (upravený cyklus)

1. `konzistence` (mapování → bible + **glosář termínů**)
2. `klise-scifi` (klišé, gear-porn, technobabble, AI vzorce)
3. `smysly` (smyslový naturalismus — pokud doplněn)
4. `vnitrni-hlas` (psychologie pod tlakem)
5. `dialog` (dvouvrstvá čeština, vojenský rejstřík)
6. `rytmus` (bojová vs. klidová kadence)
7. **`cestina-strazce`** (mechanická čeština — NOVÉ, předposlední)
8. `hlas-strazce` (pojistka proti uhlazení, právo veta — poslední)
9. `konzistence` (režim kontroly)

---

## E) ČEŠTINSKÝ KONTROLNÍ SEZNAM (jádro subrutiny)

Konkrétní průšvihy, na které je čeština v military SF náchylná. Tohle je
„co hlídat" — detailní instrukce pro `cestina-strazce`.

### E1. Přítomný čas (Fabianův režim)
- Narativ **důsledně v přítomném čase** 3. osoby. Minulý čas **jen** ve
  vsuvkách s minulostí/expozicí (historie, vzpomínka).
- Hlídat **nechtěné prokluzy** do minulého času uvnitř akční scény — častá
  chyba při psaní. (Opačně: vzpomínka napsaná omylem v přítomném čase.)

### E2. Interpunkce přímé řeči
- Pouze **české uvozovky „…"**, ne anglické "…" ani »…«.
- Uvozovací věta za řečí: malé písmeno + správná interpunkce
  (*„Teď," zašeptá.* / *„Pohyb!" křikne Vos.*).
- Čárka/tečka **uvnitř** uvozovek dle pravidla. Hlídat chybějící interpunkci
  před uvozovací větou (reálná chyba v předloze).
- **Zavírací uvozovka = U+201C** („…“), ne ASCII (U+0022) ani U+201D.
  Hlídat HYBRID „text+ASCII (správná otevírací, špatná zavírací) — strážce ho
  snadno přehlédne. Test: počet „ == počet “ a ASCII uvozovek = 0.

### E3. Koncovky sloves 3. os. mn. č. (-í, ne -i)
- „inkasují", „účinkují", „míří", „postupují" — ne „inkasuji" atd.
  (reálná chyba v předloze). Cílená kontrola tvarů na `-i`/`-í`.

### E4. Anglikalky a kalky
- „rozhodl se" ne „udělal rozhodnutí"; „nemá to smysl / je to nesmysl" ne
  „to nedává smysl"; přirozený slovosled bez anglické postpozice přívlastku.
- Vojenský žargon **počeštit** (přepadová četa, operátor těžkých zbraní,
  naváděcí paprsek) — anglicismus jen tam, kde český termín nezní (sci-fi
  reálie). Jednou zvolený tvar držet (glosář).

### E5. Redundantní „svůj" a přivlastňování
- „vzal pušku" ne „vzal svou pušku do své ruky". Mazat zbytné „svůj/jeho/její".

### E6. Přechodníky — ZÁKAZ
- V akčním žánru znějí knižně a směšně („vystřeliv, padl"). **Nepoužívat
  vůbec.** Řešit souřadně nebo vedlejší větou.

### E7. Berličky časové návaznosti
- „pak / potom / náhle / najednou / vtom" — povolit střídmě, hlídat jako tik.
  V akci raší nejvíc. Nahrazovat akcí/reakcí, ne lepidlem.

### E8. Dvouvrstvost rejstříku (klíčová devíza)
- **Vypravěč spisovný a plastický.** **Přímá řeč vojáků obecná/vulgární**
  (seš, vožralej, nemoh, do prdele). Rejstříky **nemíchat nahodile** —
  vypravěč nesmí sklouznout do hovorovosti, voják nesmí mluvit knižně
  (pokud to není záměr — civilista/diplomat Renn mluví spisovně schválně).

### E9. Terminologická jednotnost (glosář)
- Jeden tvar pro jeden pojem (ne „hladiny" vs. „vrstvy" náhodně). Skloňování
  zavedených termínů držet (kýlový klín → do kýlového klínu; proud → po
  proudu; clona → clony). Velká písmena: **Soulad, Přerod, Smíření, Legie,
  Kondominium** velká; *kýlový klín, clony, hladiny, proudy, mělčina* malá.

### E10. AI slop (viz `SKILL.md`, sekce I) — žánrová specifika
- Symetrické triády („chytrý, odvážný a nezlomný") → rozbít.
- Emocionální eskalace bez ukotvení („srdce bušilo, dech se zatajil…") →
  konkrétní vjem místo kumulace.
- „jeho mysl / její srdce" + abstraktum → napsat, co si sakra myslí.
- Falešná hloubka / fortune-cookie moudra → škrtnout.
- Houpavý rovnoměrný rytmus → variovat (řeší `rytmus`).

---

## F) Než to půjde spustit — zapojení do orchestrátoru (TODO)

> **Pozor — nic z (D) zatím NENÍ zapojené.** Existující `CLAUDE.md`
> a `sefredaktor.md` (systém LOFTu) pořád plánují **starý 7vrstvý cyklus**
> s `klise-lovec` a **bez** `cestina-strazce`, a jsou hard-coded na cestu
> `rukopis/` (ne `roman/rukopis/`). Kdo dnes spustí `sefredaktor`, dostane
> erotikou laděný cyklus na špatné cestě. Tyhle soubory **záměrně neměníme**,
> dokud běží redakce LOFTu — přepis by ji rozbil.

Před prvním během redakce tohoto románu je tedy nutné jedno z:

- **A) Oddělený orchestrátor.** Zkopii `CLAUDE.md` + `sefredaktor.md` upravit
  pro tento projekt: pořadí vrstev dle (D), `klise-lovec` → `klise-scifi`,
  doplnit `cestina-strazce`, vstup/výstup nasměrovat na složku rukopisu
  tohoto románu. (LOFT systém zůstane netknutý.)
- **B) Explicitní spuštění.** Orchestrátor nepoužít a vrstvy dle (D) zavolat
  ručně přes `Task` na jmenované agenty.

## G) Jak to spustit (po zapojení dle F)

1. Rukopis (nebo kapitoly) do **`rukopis/`** (konvence existujícího
   `CLAUDE.md`; pokud zvolíš jinou cestu, srovnej ji v orchestrátoru).
2. `git checkout -b redakce/cyklus-1`.
3. Orchestrátor projede vrstvy dle pořadí v (D) — **až po zapojení dle F**.
4. Konvergence < 0,5 % vět → konec; jinak max. 3 cykly.
5. Finál + `REDAKCE-LOG.md`.

> Tato fáze projektu = **jen analýza a plán**. Strážci se spustí, až bude
> text a až bude orchestrátor zapojený dle (F). Teď jsou připraveni „na sucho".
