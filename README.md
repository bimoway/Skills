# Moroccan Business and Commercial Law (Droit des Affaires et Commercial Marocain)

High-precision AI skill pack for Moroccan business, banking, financial-markets, and investment law — using official Moroccan legal French, exact law/article/Dahir citations, and progressive disclosure via reference files.

> **Disclaimer:** General information only, not legal or investment advice. Always verify consolidated texts in the *Bulletin Officiel* and consult an *avocat au Barreau du Maroc* / licensed advisor (*intermédiaire agréé*, *société de bourse*) before filing with BAM, AMMC, Office des Changes, CRI, or OMPIC.

## Skills in this repo

| # | Folder | Skill name | Version | What it covers |
|---|--------|------------|---------|----------------|
| 1 | [`moroccan-commercial-law-skill/`](moroccan-commercial-law-skill/) | `moroccan-commercial-law-skill` | 1.1.0 | DOC contracts, Code de Commerce 15-95, SARL/SA corporate law 5-96/17-95, commercial leases 49-16, commercial courts 53-95 |
| 2 | [`moroccan-banking-finance-skill/`](moroccan-banking-finance-skill/) | `moroccan-banking-finance-skill` | 1.0.0 | Bank Al-Maghrib Law 103-12, AMMC Law 43-12, OPCVM/OPCC/OPCI/FPCT funds, Office des Changes FX controls, Fintech/Crowdfunding Law 15-18 |
| 3 | [`moroccan-investment-guide-skill/`](moroccan-investment-guide-skill/) | `moroccan-investment-guide-skill` | 1.0.0 | Investment Charter 03-22 incentives, CRI/CRUI approval, industry/auto/aero, Generation Green agriculture, offshoring/CFC, tourism, Casablanca Stock Exchange (CSE/MASI), foreign-investor incorporation & FX repatriation |

All three skills support **English, French, and Arabic**, with a mandatory **Dual Terminology Rule** in English answers (English term + official Moroccan French term in parentheses on first use).

---

## 1. `moroccan-commercial-law-skill/` — Business & Commercial Law

**Path:** [`moroccan-commercial-law-skill/SKILL.md`](moroccan-commercial-law-skill/SKILL.md)

Advisor for DOC contracts, *statut de commerçant*, *Fonds de Commerce*, SARL/SA incorporation & governance, *baux commerciaux*, insolvency, and *Tribunal de Commerce* procedure.

**Use when:** drafting/analyzing contracts, incorporating a SARL/SA, advising on *Fonds de Commerce*, *baux commerciaux*, insolvency (*sauvegarde, redressement, liquidation judiciaire*), or commercial litigation.

**Reference routing:**

| User intent / triggers | Load |
|---|---|
| Contract validity, breach, damages (`consentement, inexécution, mise en demeure, dommages-intérêts, prescription`) | `references/doc-contracts.md` — DOC Arts 2, 230, 263, 264, 308, 387 |
| Commercial code, insolvency (`acte de commerce, commerçant, Fonds de Commerce, nantissement, Registre du Commerce, cessation des paiements`) | `references/code-de-commerce.md` — Loi 15-95, Fonds de Commerce Arts 79-83+, Livre V / Loi 73-17 |
| Incorporation (`SARL, SA, statuts, capital social, gérant, AG, commissaire aux comptes, OMPIC, ICE`) | `references/corporate-law-sarl-sa.md` — Lois 5-96 (SARL) & 17-95 (SA) |
| Commercial lease (`bail commercial, renouvellement, congé, éviction, loyer`) | `references/commercial-leases-49-16.md` — Loi 49-16 |
| Commercial courts (`Tribunal de Commerce, compétence, seuil, appel, cassation`) | `references/commercial-courts-53-95.md` — Loi 53-95 |

**Key formalities:** *Certificat négatif OMPIC, ICE, IF, Taxe Professionnelle (patente), CNSS, annonces légales + Bulletin Officiel.*

---

## 2. `moroccan-banking-finance-skill/` — Banking, Financial Services & Capital Markets

**Path:** [`moroccan-banking-finance-skill/SKILL.md`](moroccan-banking-finance-skill/SKILL.md)

Advisor for *Droit bancaire, financier et des marchés de capitaux*: licensing, prudential supervision, participatory banking, AMMC enforcement, APE/IPO, insider trading, asset management, FX controls, fintech/crowdfunding.

**Use when:** licensing banks/payment institutions/participatory banks, IPOs & public offerings, insider trading/market abuse, fund formation (OPCVM/OPCC/OPCI/FPCT), FDI convertibility & profit repatriation, or crowdfunding platforms.

**Reference routing:**

| User intent / triggers | Load |
|---|---|
| Banking license, prudential, Islamic banking (`établissement de crédit, agrément, ratio prudentiel, établissement de paiement, banque participative, CSO`) | `references/bam-banking-law-103-12.md` — Loi 103-12, Dahir 1-14-193 |
| Public offering, enforcement (`AMMC, appel public à l'épargne, prospectus, note d'information, délit d'initié, manipulation de cours`) | `references/ammc-capital-markets-43-12.md` — Loi 43-12 (AMMC), Loi 44-12 (APE) |
| Funds (`OPCVM, SICAV, FCP, OPCC, OPCI, FPCT, titrisation, société de gestion, dépositaire`) | `references/asset-management-funds.md` — Dahir 1-93-213, Lois 41-05, 70-14, 33-06 |
| FX controls (`Office des Changes, convertibilité, investissement étranger, rapatriement, import/export`) | `references/foreign-exchange-controls.md` — IGOC |
| Crowdfunding/fintech (`financement collaboratif, SFC, fintech, prêt participatif`) | `references/fintech-crowdfunding-15-18.md` — Loi 15-18 (dual BAM/AMMC supervision) |

**Authorities:** *Bank Al-Maghrib (BAM), Autorité Marocaine du Marché des Capitaux (AMMC), Office des Changes.*

---

## 3. `moroccan-investment-guide-skill/` — Investment Guide, Sectors & Casablanca Stock Exchange

**Path:** [`moroccan-investment-guide-skill/SKILL.md`](moroccan-investment-guide-skill/SKILL.md)

Investor-ready guide to the *Charte de l'Investissement*, sector ecosystems (industry, agri-tech, services), *Casablanca Finance City (CFC)* status, and *Bourse de Casablanca (CSE)* market access.

**Use when:** advising on investing in Morocco — sector selection, subsidies/CRI approval, industrial zones, CFC status, CSE listing/trading, 100% foreign ownership, or profit repatriation.

**Reference routing:**

| User intent / triggers | Load |
|---|---|
| Investment incentives (`Charte de l'Investissement, Loi-cadre 03-22, prime, subvention, CRI, CRUI, convention`) | `references/investment-charter-incentives.md` — Loi-cadre 03-22, Dahir 1-22-76 |
| Industry (`ZAI, automobile, Renault/Stellantis, aéronautique, Midparc, décarbonation`) | `references/sector-industry-automotive-aero.md` |
| Agriculture (`Génération Green, foncier agricole, SOGETA/SODEA, bail emphytéotique, dessalement, hydrogène vert`) | `references/sector-agriculture-agritech.md` |
| Services (`offshoring, Technopolis, tourisme Cap 2026, CFC, statut CFC`) | `references/sector-services-offshoring-cfc.md` |
| Stock market (`Bourse de Casablanca, CSE, MASI/MASI20, action cotée, dividende, T+2, principal vs alternatif`) | `references/casablanca-stock-exchange-cse.md` |
| Foreign setup (`100% étranger, compte en dirhams convertibles, rapatriement, IS, TVA, ANAPEC`) | `references/investor-faqs-incorporation.md` |

**Key formalities:** *CRI + CRUI, Convention d'investissement, Certificat négatif OMPIC + ICE + IF + patente, Compte en Dirhams Convertibles via intermédiaire agréé, Déclaration Office des Changes, Visa AMMC.*

---

## How to use (progressive disclosure)

1. Read the relevant `SKILL.md` first — do **not** load all references by default.
2. Match the user question against that skill's **Reference Routing Table** and `Read` only the matching `references/*.md` file(s).
3. Answer with: Rule → exact text (law + article + Dahir/circular) → conditions → sanction/rate → competent authority → formality.
4. Cross-skill handoffs:
   - Commercial contracts, SARL/SA, *baux commerciaux*, *Tribunal de Commerce* → `moroccan-commercial-law-skill/`
   - Banking license, APE/IPO, OPCVM, FX licensing, crowdfunding licensing → `moroccan-banking-finance-skill/`
   - Investment incentives, sector choice, CFC, CSE investing, foreign setup → `moroccan-investment-guide-skill/`
5. Never invent article numbers, rates, or thresholds. If uncertain: *« À vérifier au Bulletin Officiel »* and cite the law generally.

## Repo structure

```text
.
├── README.md
├── moroccan-banking-finance-skill/
│   ├── SKILL.md
│   └── references/
├── moroccan-commercial-law-skill/
│   ├── SKILL.md
│   └── references/
└── moroccan-investment-guide-skill/
    ├── SKILL.md
    └── references/
```

## Terminology (Moroccan legal French — mandatory)

- *Fonds de Commerce, Registre du Commerce, Tribunal de Commerce, Dahir des Obligations et Contrats (DOC), Bulletin Officiel, OMPIC, ICE, statuts, gérant, commissaire aux comptes, bail commercial, indemnité d'éviction, cessation des paiements*
- *Établissement de crédit, Agrément, Bank Al-Maghrib (BAM), Banque participative, AMMC, Appel Public à l'Épargne (APE), note d'information, visa de l'AMMC, Délit d'initié, OPCVM/OPCC/OPCI/FPCT, Office des Changes, IGOC, intermédiaire agréé, Financement Collaboratif (SFC)*
- *Charte de l'Investissement (Loi-cadre 03-22), Prime à l'investissement, CRI/CRUI, ZAI, Génération Green, bail emphytéotique, CFC/statut CFC, Bourse de Casablanca (CSE), MASI/MASI20, règlement-livraison T+2, IS/TVA, Compte en Dirhams Convertibles*
