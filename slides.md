---
theme: default
title: Lokální AI vol. 2 — Nekončící Odysea
info: |
  ## Lokální AI vol. 2: Nekončící Odysea
  ApiBeer meet-up (ApiTree) · Využití AI v praxi

  Autor: Vít Rozsíval
colorSchema: dark
transition: none
mdc: true
fonts:
  sans: 'Inter'
  mono: 'JetBrains Mono'
css: unocss
layout: cover
class: text-center
---

<div class="eyebrow">🍺 ApiBeer meet-up · Využití AI v praxi</div>

<h1 class="mt-4">Lokální AI vol. 2<br>Nekončící Odysea</h1>

<p class="text-2xl opacity-70 mt-4">...aneb jak mi vlastní AI řekla, že na to její logika nestačí</p>

<div class="mt-16 text-sm opacity-50 tracking-wide">Vít Rozsíval · ApiTree</div>

---
layout: default
---

# Přiznání barvy: clickbait reality check

<p class="text-lg opacity-70 -mt-2">Název zní jako clickbait z LinkedInu, ale je v něm 100 % reality — hledám názorový střed tam, kde ve veřejném prostoru chybí pragmatismus.</p>

<div class="grid grid-cols-3 gap-4 mt-8">
  <div class="card card-bad">
    <div class="tag tag-bad">Extrém A</div>
    <h3 class="mt-2">Hypefluencer</h3>
    <p class="text-sm opacity-70">Nekriticky sdílí nereprodukovatelné benchmarky, každý malý model je „zabijákem frontier modelů“ — aniž by ho reálně spustil.</p>
  </div>
  <div class="card card-neutral">
    <div class="tag tag-neutral">Inženýrská realita</div>
    <h3 class="mt-2">Můj postoj</h3>
    <p class="text-sm opacity-70">Praktické testování na vlastním železe, objektivní hodnocení bez emocí, hledání reálné přidané hodnoty pro denní praxi.</p>
  </div>
  <div class="card card-bad">
    <div class="tag tag-bad">Extrém B</div>
    <h3 class="mt-2">Zarytý hater</h3>
    <p class="text-sm opacity-70">Lokální AI je zbytečná hračka a neefektivní nesmysl; cokoliv z čínské produkce je en bloc špatné nebo propaganda.</p>
  </div>
</div>

<!--
- Přiznání barvy: Ten název zní trochu jako clickbait z LinkedInu, ale je v něm 100 % reality.
- Proč "Nekončící Odysea": Ani po 4 měsících to není stav "nastavil jsem a mám hotovo". Je to neustálý proces pokusů a omylů, porovnávání modelů, testování nových harnessů a objevování limitů.
- Hledání názorového středu (chybějící pragmatismus ve veřejném prostoru):
  - Extrém A (Hypefluenceři): Nekriticky sdílí nereprodukovatelné benchmarky a prohlašují každý 8B model za "zabijáka frontier modelů", aniž by ho reálně spustili.
  - Extrém B (Zarytí odpůrci / geopolitický bias): Tvrdí, že lokální AI je zbytečná hračka, neefektivní nesmysl a cokoliv z čínské produkce je en bloc špatné nebo propagandistické.
  - Inženýrská realita (Můj postoj): Praktické testování na vlastním železe, objektivní hodnocení bez emocí a hledání skutečné přidané hodnoty pro denní praxi.
-->

---
layout: default
---

# Recap vol. 1 — kde jsme skončili & co se změnilo

<div class="grid grid-cols-2 gap-6 mt-6">
<div>
  <div class="card card-neutral mb-4">
    <div class="tag tag-neutral">Vol. 1 v kostce</div>
    <ul class="mt-3 text-base leading-relaxed">
      <li><b>Setup:</b> vlastní rig stavěný na míru pro lokální LLMs — žádný cloud, 0 Kč za API tokeny</li>
      <li><b>Cíl:</b> odhalit, že spouštět modely lokálně je reálné, soukromé a extrémně rychlé</li>
    </ul>
  </div>
  <div class="card card-good">
    <div class="tag tag-good">Po 4 měsících</div>
    <ul class="mt-3 text-base leading-relaxed">
      <li>Rig stále v plném provozu — 4 měsíce kontinuálního vytížení</li>
      <li>Přechod od prvotního nadšení k dennímu testování v reálných workflow</li>
    </ul>
  </div>
</div>
<div class="grid grid-cols-2 gap-3 h-full">
  <div class="relative h-full rounded-lg overflow-hidden border border-white/10">
    <img src="/assets/components.jpg" class="w-full h-full object-cover" alt="Komponenty rigu v krabicích">
    <div class="absolute bottom-0 inset-x-0 bg-black/60 text-xs text-center py-1">Komponenty v krabicích</div>
  </div>
  <div class="relative h-full rounded-lg overflow-hidden border border-white/10">
    <img src="/assets/workstation.jpg" class="w-full h-full object-cover" alt="Postavený rig">
    <div class="absolute bottom-0 inset-x-0 bg-black/60 text-xs text-center py-1">Postavený stroj</div>
  </div>
</div>
</div>

<div class="mt-10 text-center text-2xl opacity-80">
  Dnes neřešíme specifikace a HW. Dnes si povíme, kde stroj narazil na zeď — a čím naopak absolutně překvapil.
</div>

<!--
- "Pro ty, co tu minule nebyli: Před cca 4 měsíci jsem si pořídil vlastní HW rig, abych si vyzkoušel, kam až se dá jít s AI bez cloudu, kreditek a posílání dat na cizí servery."
- "Minule jsme si ukázali, že to jde a že malé modely nejsou jen na hraní."
- "Dneska už nebudeme řešit specifikace a HW parametry. Dneska si povíme, co se stalo, když ten stroj dostal 4 měsíce reálného provozu a testování, kde narazil na zeď a v čem mě naopak absolutně překvapil."
-->

---
layout: default
---

# Modelové sítko: obrovský hype, tvrdý dopad na zem

<div class="grid grid-cols-2 gap-6 mt-8">
  <div class="card card-bad">
    <div class="tag tag-bad">Zklamání</div>
    <h3 class="mt-2">Gemma-4-31B</h3>
    <ul class="text-base leading-relaxed opacity-90">
      <li>Skvělá na textové analýzy a prose text</li>
      <li>V kódu naprosto vyhořela — školácké chyby i u základu</li>
      <li><b>VRAM žrout:</b> neúměrně vysoké nároky na KV cache vzhledem k velikosti</li>
    </ul>
  </div>
  <div class="card card-bad">
    <div class="tag tag-bad">Zklamání</div>
    <h3 class="mt-2">Laguna-S-2.1</h3>
    <ul class="text-base leading-relaxed opacity-90">
      <li>Suverénně největší zklamání vůči marketingu</li>
      <li>Na papíře / benchmarku zabiják — v realitě cyklení při reasoningu</li>
      <li>Chybné tool calls, netransparentní spouštění reasoningu, zastaralé znalosti frameworků</li>
    </ul>
  </div>
</div>

<!--
- "Nejprve ty špatné zprávy. Gemma je prima na psaní dokumentace, ale jakmile po ní chcete kód, seká chyby jako junior první týden na stáži. A nároky na KV cache při delším kontextu vás vylejí z VRAM."
- "Laguna je perfektní příklad toho, proč nevěřit benchmarkům. Marketing sliboval zázraky, v praxi se model neustále zacykluje ve vlastním uvažování, sám od sebe neví, kdy použít reasoning, a generuje neplatné JSONy pro tool calls se zastaralými knihovnami."
-->

---
layout: default
---

# Malé superstars: kvalitní kód a rychlost na consumer HW

<div class="grid grid-cols-2 gap-6 mt-6">
  <div class="card card-good">
    <div class="tag tag-good">Nejlepší malý coding model</div>
    <h3 class="mt-2">Qwen3.6-27B</h3>
    <ul class="text-base leading-snug opacity-90">
      <li>Král codingu mezi malými modely, silný reasoning</li>
      <li>Agresivní kvantizace → vejde se na 1 consumer GPU</li>
      <li>Podpora MTP (Multi-Token Prediction) → brutální zrychlení spekulativním dekódováním</li>
      <li>Vynikající znalost češtiny</li>
    </ul>
    <p class="text-sm mt-3 opacity-60">Reality check: není to Claude Opus / frontier model — vyžaduje precizní prompty, smyčky a tvé code review.</p>
  </div>
  <div class="card card-good">
    <div class="tag tag-good">MoE rychlík na jednoduché tasky</div>
    <h3 class="mt-2">Qwen3.6-35B-A3B</h3>
    <ul class="text-base leading-snug opacity-90">
      <li>Nutná lossless kvantizace (UD-Q8_K_XL), jinak rapidně roste perplexity</li>
      <li>Vejde se na 1 GPU i s velkým kontextem</li>
      <li>MTP → prefill &gt; 2000 tok/s, output 90–100 tok/s</li>
    </ul>
    <p class="text-sm mt-3 opacity-60">Sweet spot: úpravy kódu s jasně daným patternem. S plným kontextem ztrácí nit u velkých celků.</p>
  </div>
</div>

<!--
- "Qwen3.6-27B je pro mě absolutní špička. Když nad ním držíte precizní kontrolu a code review, dostanete výkon, který byste od lokálního modelu na jedné grafice ještě nedávno nečekali. Navíc podpora Multi-Token Prediction ho neskutečně zrychluje."
- "Qwen3.6-35B-A3B je zase čistá rychlost díky MoE. Když dodržíte dynamický 8bit kvant UD-Q8_K_XL, plní kontext rychlostí 2000 tokenů za vteřinu. Není to architekt na navrhování systémů od nuly, ale na úpravy kódu podle jasných vzorů je to neuvěřitelný dělník."
-->

---
layout: default
---

# Švýcarák na stole: RAG, Vision, Utility & DeepSeek

<div class="grid grid-cols-2 gap-6 mt-6">
  <div class="card card-neutral">
    <h3>Qwen3.5-2B <span class="tag tag-neutral ml-1">Ultra-light</span></h3>
    <ul class="text-sm leading-snug opacity-90">
      <li>Bleskové commit messages, labely, sumarizace</li>
      <li>Překvapivě přesná detekce objektů z obrázků jen s 2B parametry</li>
    </ul>
  </div>
  <div class="card card-neutral">
    <h3>Qwen3-Embedding-0.6B</h3>
    <p class="text-sm opacity-90">RAG sweet spot pro web search a prohledávání dokumentace.</p>
  </div>
  <div class="card card-neutral">
    <h3>DeepSeek-V4-Flash <span class="tag tag-neutral ml-1">CPU offload</span></h3>
    <ul class="text-sm leading-snug opacity-90">
      <li>Větší MoE model, CPU offloading expertů</li>
      <li>10–15 tok/s → nevhodné na live coding, výborné na background agentické tasky s obřím kontextem</li>
    </ul>
  </div>
  <div class="card card-neutral">
    <h3>Text-to-Image</h3>
    <ul class="text-sm leading-snug opacity-90">
      <li><b>Ideogram-4:</b> plakáty a grafika, JSON prompty (řešeno malým LLM skillem)</li>
      <li><b>Qwen-Image-2512:</b> fotorealismus z vlastního stolu — ukázky na dalším slidu</li>
    </ul>
  </div>
</div>

<!--
- "Malé modely vás často šokují tam, kde byste to nečekali. Qwen3.5-2B zabere minimum paměti, ale okamžitě vám píše commit messages a s 2B parametry přesně pozná objekty na fotce."
- "DeepSeek-V4-Flash je ukázka toho, že i když se vám MoE model už nevejde do VRAM, dá se použít. Přelijete část expertů na CPU, dostanete 10–15 tokenů za vteřinu a máte neuvěřitelně přesný kódovací engine na pozadí pro agentické úlohy, kde vás latence nebolí."
- "A generování obrázků? Tady na slajdu vidíte 3 fotorealistické výstupy z Qwen-Image-2512. Všechno vygenerováno lokálně na mém rigu bez posílání dat na Midjourney."
-->

---
layout: center
---

# Fotorealismus přímo ze stolu: Qwen-Image-2512

<p class="text-center opacity-60 mt-1 mb-6">Vygenerováno lokálně na vlastním rigu, bez posílání dat do cloudu</p>

<div class="grid grid-cols-3 gap-6 px-4">
  <img class="showcase-img" src="/assets/qwen-image-1.webp" alt="Qwen-Image-2512 ukázka 1">
  <img class="showcase-img" src="/assets/qwen-image-2.webp" alt="Qwen-Image-2512 ukázka 2">
  <img class="showcase-img" src="/assets/qwen-image-3.webp" alt="Qwen-Image-2512 ukázka 3">
</div>

---
layout: center
class: text-center
---

<div class="eyebrow mt-6">Live ukázka</div>

# Malý model v akci

<p class="text-lg opacity-70 mb-8">Stavba React aplikace (Top-to-Bottom) na lokálním křemíku</p>

<video class="mx-auto rounded-xl border border-white/10 shadow-lg" style="width: 700px;" src="/assets/qwen36-27b-showcase.mp4" controls preload="auto"></video>

<!--
- "Ale dost bylo teorie a výčtu parametrů. Pojďme se podívat, co takový malý vyprofilovaný model dokáže přímo v praxi."
- "Tady vidíte zrychlený záznam z dnešního večera. Zadal jsem modelu jednoduše scoping na React aplikaci. Sledujte tu latenci, přesnost a to, že na to nepotřebujeme ani jeden API request do cloudu."
- "Když dáte malému modelu jasně vymezené mantinely a čistou strukturu, dodá vám kompletní kód za pár vteřin."
-->

---
layout: default
---

# Nekončící Odysea: rig na max, neposlušní agenti a 2 000 stran matiky

<div class="grid grid-cols-3 gap-5 mt-6">
  <div class="card card-neutral compact">
    <div class="tag tag-neutral">Utilizace na krev</div>
    <h3 class="mt-2">Boje s infrastrukturou</h3>
    <ul class="text-sm leading-snug opacity-90">
      <li>Neustálá změna prostředí — stabilizovat stack v AI divočině je alchymie</li>
      <li>Kompletní přepisování konfigurace llama.cpp serveru</li>
      <li>Matematické výpočty VRAM/RAM footprintu, výběr kvantizací pro 100% utilizaci rigu</li>
    </ul>
  </div>
  <div class="card card-neutral compact">
    <div class="tag tag-neutral">Stálý projekt v procesu</div>
    <h3 class="mt-2">Autonomní agentický stack</h3>
    <ul class="text-sm leading-snug opacity-90">
      <li>Vyzkoušena hromada frameworků, orchestrací a workflow přístupů</li>
      <li>Zatím nedokončeno, stále v procesu — „na to moje logika nestačí“</li>
      <li>I přes nezdary viditelný pokrok a obrovská zábava</li>
    </ul>
  </div>
  <div class="card card-neutral compact">
    <div class="tag tag-neutral">Návrat k fundamentům</div>
    <h3 class="mt-2">AI Bible</h3>
    <ul class="text-sm leading-snug opacity-90">
      <li>Rozhodnutí jít do hloubky, zahodit povrchní tutoriály</li>
      <li>Bishop (Deep Learning), Goodfellow (Deep Learning), Russell &amp; Norvig (AI: A Modern Approach)</li>
      <li>Minulý týden zahájeno studium — hardcore, ale odkrývá reálnou podstatu fungování modelů</li>
    </ul>
  </div>
</div>

<!--
- "Tady narážíme na to, proč se přednáška jmenuje Nekončící Odysea. Vygenerovat React appku z jednoho promptu je sranda, ale dostat z hardware maximum vyžaduje matematiku. Kolikrát jsem předělával konfiguraci llama.cpp serveru, počítal bajty VRAM pro různé quants a ladil parametry, už ani nespočítám."
- "A pak je tu můj 'pet project' – vlastní autonomní agentický stack. Upřímně? Ještě ho nemám hotového a je to moje osobní Odysea. Prošel jsem nespočet frameworků, smyček a orchestrací. Občas to funguje skvěle, občas mi model po hodině zacyklení napíše, že na to jeho logika nestačí. Ale ten posun je neskutečný a neuvěřitelně mě to baví."
- "Abych se v tom neplácal jen pokusem a omylem, rozhodl jsem se jít ke kořenům. Zahodil jsem rychlé návody z YouTube a nakoupil AI bible – Bishop, Goodfellow, Russell & Norvig. Proberete se prvním matematickým aparátem a najednou přesně vidíte, proč ti agenti selhávají tam, kde selhávají."
-->

---
layout: center
---

# Návrat k fundamentům: AI Bible

<p class="text-center opacity-60 mt-1 mb-4">Bishop, Goodfellow & Norvig — právě rozečtené</p>

<div class="flex justify-center">
  <img src="/assets/ai-bibles.jpg" class="rounded-xl border border-white/10 shadow-lg" style="max-height: 380px; max-width: 90%; object-fit: contain;" alt="Bishop, Goodfellow, Russell & Norvig — AI bible knihy">
</div>
---
layout: default
---

# Stop kanónům na vrabce: kdy použít malé modely a jak ušetřit

<div class="grid grid-cols-2 gap-5 mt-3">
  <div class="card card-good compact">
    <div class="tag tag-good">Kde malé modely excelují</div>
    <ul class="text-sm leading-snug opacity-90 mt-2">
      <li>Repetitivní a strukturované úlohy — extrakce dat, generování e-mailů, interních dokumentů, směrnic, refaktoring a vývoj podle již nastavených patternů</li>
      <li>Úlohy s jasně vymezeným kontextem a scopingem</li>
    </ul>
  </div>
  <div class="card card-bad compact">
    <div class="tag tag-bad">Kde stále ztrácejí</div>
    <ul class="text-sm leading-snug opacity-90 mt-2">
      <li>Komplexní architektura od nuly</li>
      <li>Abstraktní reasoning bez vodítek, obří neurčité celky</li>
      <li>Long-running agentic tasky</li>
    </ul>
  </div>
</div>

<div class="card card-neutral compact mt-3">
  <div class="tag tag-neutral">Ekonomika v praxi</div>
  <p class="mt-1 text-sm opacity-90">Cloud ≠ pouze frontier modely — malé modely spouští i cloudoví provideři (Requesty, Ollama Cloud). API call na malý vyprofilovaný Qwen stojí doslova <i>peanuts</i> v porovnání s frontier monstry jako Claude Opus nebo GPT-5.6.</p>
</div>

<div class="mt-3 text-center text-lg opacity-80">
  Zralá firma nepoužívá na všechno ten nejdražší model — staví tierovanou architekturu podle náročnosti tasku.
</div>

<!--
- „Pojďme si říct tu nejdůležitější věc pro inženýrskou i ekonomickou praxi: Používat na každý běžný task frontier model typu Claude Opus je jako jezdit do samoobsluhy pro rohlíky kamionem. Je to drahé, pomalé a nedává to smysl.“
- „V každé firmě máme mraky repetitivních činností — psaní e-mailů, návrhy interních dokumentů, směrnic, parsing dat nebo refaktoring podle vzoru. Na to malé modely nejenže stačí, ale jsou často rychlejší a determinističtější.“
- „A to hlavní – nemusíte hned zítra kupovat rig a stavět ho pod stůl. I v cloudu u providerů stojí provoz a API volání malého Qwenu absolutní drobné. Správná architektura spočívá v delegování 80 % běžné práce na menší modely a frontier modely si nechat jen jako drahé konzultanty na ty nejtvrdší oříšky.“
-->

---
layout: center
class: text-center
---

# Takeaways z 4 měsíců v zákopech

<div class="grid grid-cols-3 gap-5 mt-8 text-left">
  <div class="card card-neutral">
    <h3>Pragmatismus nad Hype</h3>
    <p class="text-sm opacity-80">Nevěřit marketingovým benchmarkům ani LinkedIn „expertům“. Měřit realitu na vlastním kódu a workflows.</p>
  </div>
  <div class="card card-neutral">
    <h3>Tierovaná architektura</h3>
    <p class="text-sm opacity-80">Frontier modely na architekturu a komplexní zadání, každodenní tasky na malé vyprofilované modely.</p>
  </div>
  <div class="card card-neutral">
    <h3>Inženýrská poctivost</h3>
    <p class="text-sm opacity-80">Návrat k matematickým základům (Bishop, Goodfellow, Russell) odkrývá limity modelů dřív, než na ně proinvestujete čas nebo peníze.</p>
  </div>
</div>

<p class="mt-10 text-xl italic opacity-80">„Pojďme u nás stavět štíhlá, účelová řešení místo pálení kreditů na generické dotazy.“</p>

<div class="mt-12 text-3xl font-700">Otázky &amp; diskuse</div>
<p class="opacity-60 mt-2">Díky za pozornost!</p>


<!--
- „Kdybych měl celé ty 4 měsíce experimentů, tavení rigu a čtení AI biblí shrnout do tří věcí, jsou to tyto:“
- „Za prvé: Nenechme se opít rohlíkem. Hype je obrovský, ale inženýrská realita se měří na reálných kódovacích smyčkách, latenci a přesnosti.“
- „Za druhé: Stavějme chytré tierované architektury. Malé modely v cloudu i u nás na stole zvládají většinu denní práce za zlomek ceny.“
- „A za třetí: Chceme-li AI fakt rozumět a stavět spolehlivé věci, musíme jít pod povrch a chápat matematické limity architektury, na které to celé stojí.“
- „Díky moc a pojďme na otázky!“
-->
