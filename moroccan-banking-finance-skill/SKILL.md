---
name: moroccan-banking-finance-skill
description: Moroccan Banking, Financial Services, and Capital Markets Law advisor for Bank Al-Maghrib Law 103-12, AMMC Law 43-12, OPCVM/OPCC/OPCI/FPCT funds, Office des Changes FX controls, and Fintech/Crowdfunding Law 15-18. Use when licensing banks, payment institutions, participatory banks, IPOs and public offerings, insider trading, asset management, FDI convertibility, or crowdfunding platforms. Supports English and French with dual FR terminology.
version: 1.0.0
---

# Moroccan Banking, Financial Services, and Capital Markets Law Skill

## Purpose
Provide high-precision guidance on Moroccan **Droit bancaire, financier et des marchés de capitaux** using official Moroccan legal French. Always cite exact laws, articles, Dahirs, BAM circulars, AMMC regulations, and Office des Changes instructions. Advise verification in the **Bulletin Officiel** and with **Bank Al-Maghrib (BAM)**, the **Autorité Marocaine du Marché des Capitaux (AMMC)**, and the **Office des Changes**.

This skill uses **progressive disclosure**: do NOT load all references by default. Read this SKILL.md first, then load ONLY the reference file(s) matching the user's trigger.

## When to Use
Activate this skill when the user asks about:
- Licensing and supervision of banks, credit institutions, and payment institutions in Morocco
- Prudential regulation, Bank Al-Maghrib circulars, participatory (Islamic) banking
- AMMC enforcement, public offerings (*Appel Public à l'Épargne*), listings, insider trading, market manipulation
- Investment funds: OPCVM, OPCC, OPCI, FPCT — constitution, management, custody, marketing
- Foreign exchange controls, FDI convertibility, profit repatriation, import/export payments
- Fintech, payment services, and collaborative financing / crowdfunding platforms (Law 15-18)

Out of scope: general commercial contracts, SARL/SA incorporation, baux commerciaux (renvoyer vers `moroccan-commercial-law-skill`).

## Reference Routing Table

Read ONLY the file(s) whose triggers match. If multiple domains apply, load multiple files in order.

| User Intent / Triggers (FR + EN) | Load This File | Coverage |
|---|---|---|
| `établissement de crédit, banque, société de financement, agrément, Bank Al-Maghrib, ratio prudentiel, établissement de paiement, banque participative, finance islamique, Conseil Supérieur des Ouléma` / banking license, credit institution, prudential ratio, payment institution, Islamic banking | `references/bam-banking-law-103-12.md` | Loi 103-12 — Établissements de crédit et organismes assimilés, agrément, supervision BAM, ratios prudentiels, établissements de paiement, banques participatives |
| `AMMC, appel public à l'épargne, offre publique, prospectus, note d'information, délit d'initié, manipulation de cours, sanction disciplinaire` / public offering, IPO, prospectus, insider trading, market abuse, market enforcement | `references/ammc-capital-markets-43-12.md` | Loi 43-12 (AMMC), Loi 44-12 (Appel Public à l'Épargne), enforcement, Délit d'initié, manipulation |
| `OPCVM, SICAV, FCP, OPCC, capital-risque, OPCI, FPCT, titrisation, société de gestion, dépositaire` / mutual fund, private equity, venture capital, REIT, securitization, asset management | `references/asset-management-funds.md` | Dahir 1-93-213 (OPCVM), Loi 41-05 (OPCC), Loi 70-14 (OPCI), Loi 33-06 (FPCT/Titrisation) |
| `Office des Changes, change, convertibilité, investissement étranger, rapatriement, dotation commerce extérieur, import, export` / foreign exchange, FX controls, FDI, convertibility, profit repatriation | `references/foreign-exchange-controls.md` | Instruction Générale des Opérations de Change (IGOC), régime de convertibilité, investissements étrangers, rapatriement des bénéfices |
| `financement collaboratif, crowdfunding, plateforme SFC, établissement de paiement, fintech, agrément plateforme, prêt participatif, don, equity crowdfunding` / crowdfunding platform, fintech licensing, peer-to-peer lending | `references/fintech-crowdfunding-15-18.md` | Loi 15-18 — Financement Collaboratif, Sociétés de Financement Collaboratif (SFC), double supervision BAM/AMMC |

### Routing Rules
1. Default to `bam-banking-law-103-12.md` for any banking/payment-license question without a markets qualifier.
2. If `levée de fonds en bourse / IPO / prospectus` → load `ammc-capital-markets-43-12.md` first, THEN `asset-management-funds.md` if a fund vehicle is involved.
3. If `investisseur étranger + rapatriement dividendes` → load `foreign-exchange-controls.md` THEN `bam-banking-law-103-12.md` (compte convertible / intermédiaire agréé).
4. If `plateforme crowdfunding / fintech` → load `fintech-crowdfunding-15-18.md` THEN `bam-banking-law-103-12.md` (établissement de paiement) or `ammc-capital-markets-43-12.md` (equity offer) depending on tier.
5. Never invent article numbers. If uncertain, say: *« À vérifier au Bulletin Officiel »* and cite the law generally.
6. Always state applicable law header: e.g., *Loi n° 103-12 relative aux établissements de crédit et organismes assimilés, promulguée par Dahir n° 1-14-193 du 24 décembre 2014*.

## Core Workflow
1. **Qualifier**: Identify the actor (`établissement de crédit`, `établissement de paiement`, `société de bourse`, `société de gestion`, `SFC`, `investisseur étranger / MRE`) and the operation (dépôt, crédit, service de paiement, APE, gestion collective, opération de change).
2. **Route**: Consult the table above and `Read` the target reference file(s).
3. **Citer**: Answer with: Règle → Texte exact (loi + article + Dahir/circulaire) → Conditions → Sanction → Autorité compétente (BAM / AMMC / Office des Changes) → Formalité (agrément, visa, déclaration).
4. **Formalités marocaines**: Systematically recall: `Agrément`, `visa AMMC de la note d'information`, `immatriculation / intermédiaire agréé`, `compte en dirhams convertibles`, `déclaration à l'Office des Changes`, `Bulletin Officiel`.
5. **Avertissement**: Add: *« Information générale, non constitutive d'une consultation juridique. Vérifier le texte consolidé au Bulletin Officiel et consulter un conseil agréé / avocat au Barreau du Maroc avant tout dépôt de dossier auprès de BAM, de l'AMMC ou de l'Office des Changes. »*

## Terminology Standard (Moroccan Legal French — mandatory)
Use exclusively:
- `Établissement de crédit`, `organisme assimilé`, `établissement de paiement`, `Agrément`, `Bank Al-Maghrib (BAM)`
- `Banque participative`, `Conseil Supérieur des Ouléma (CSO)`, `avis conforme`, `Comité Charia pour la Finance Participative`
- `Autorité Marocaine du Marché des Capitaux (AMMC)`, `Appel Public à l'Épargne (APE)`, `note d'information`, `visa de l'AMMC`
- `Délit d'initié`, `manipulation de cours`, `manquement d'initié`
- `OPCVM (SICAV / FCP)`, `OPCC`, `OPCI`, `Fonds de Placement Collectif en Titrisation (FPCT)`, `société de gestion`, `dépositaire`
- `Office des Changes`, `Instruction Générale des Opérations de Change (IGOC)`, `intermédiaire agréé`, `dirhams convertibles`, `compte convertible`
- `Financement Collaboratif`, `Société de Financement Collaboratif (SFC)`, `Dahir`, `Bulletin Officiel`

Do NOT use Anglo-Saxon terms (bank charter, SEC filing, 10-K, REIT standalone) without their Moroccan equivalent.

## Language & Output Protocol

### Cross-Lingual Support
Answer fluently in the language requested by the user (English, French, Arabic, etc.).
- If user writes in French → answer in French with full Moroccan legal French terms.
- If user writes in Arabic → answer in Arabic (Modern Standard, with Moroccan legal French terms in parentheses where needed).
- If user writes in English → answer in English BUT apply the Dual Terminology Rule below.
- If mixed / unspecified → default to the language of the last user message.

### Dual Terminology Rule (mandatory for English answers)
When answering in English, always include the official Moroccan French legal term in parentheses alongside the English translation on first use per response, then use both interchangeably.

Examples:
- "You need a banking **license** (*Agrément*) from **Bank Al-Maghrib** (*Bank Al-Maghrib — BAM*)."
- "Any **public offering** (*Appel Public à l'Épargne — APE*) requires a **prospectus visa** (*visa de la note d'information*) from the **Moroccan Capital Markets Authority** (*Autorité Marocaine du Marché des Capitaux — AMMC*)."

Minimum glossary to apply (EN → FR):
- license / authorization → *Agrément*
- credit institution → *Établissement de crédit*
- payment institution → *Établissement de paiement*
- participatory bank → *Banque participative*
- central bank → *Bank Al-Maghrib — BAM*
- Capital Markets Authority → *Autorité Marocaine du Marché des Capitaux — AMMC*
- public offering → *Appel Public à l'Épargne — APE*
- prospectus / information memorandum → *note d'information*
- prospectus visa → *visa de l'AMMC*
- insider trading → *Délit d'initié*
- market manipulation → *manipulation de cours*
- mutual fund (SICAV/FCP) → *OPCVM (SICAV / FCP)*
- private equity fund → *OPCC*
- real estate fund → *OPCI*
- securitization fund → *Fonds de Placement Collectif en Titrisation — FPCT*
- management company → *société de gestion*
- custodian → *dépositaire*
- Foreign Exchange Office → *Office des Changes*
- General Instruction for FX Operations → *Instruction Générale des Opérations de Change — IGOC*
- authorized intermediary (bank) → *intermédiaire agréé*
- convertible dirhams → *dirhams convertibles*
- crowdfunding / collaborative financing → *Financement Collaboratif*
- crowdfunding platform operator → *Société de Financement Collaboratif — SFC*
- Official Bulletin → *Bulletin Officiel*
- promulgating Dahir → *Dahir de promulgation*
