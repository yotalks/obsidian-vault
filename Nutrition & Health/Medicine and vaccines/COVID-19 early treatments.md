---
tags:
  - health
aliases:
  - Fluvoxamine
  - Proxalutamide
  - Hydroxychloroquine
  - c19early
  - Early treatment for COVID-19
up: "[[Nutrition & Health MOC]]"
---
> [!summary] Bottom line
> Pooled "early treatment" analyses from sites like c19early.com combine trials with observational studies and different outcomes, so their large effects can't be taken at face value. Fluvoxamine had the most promising evidence: a small trial was positive, the large TOGETHER trial found fewer emergency visits and hospitalizations, but the COVID-OUT trial found no benefit. The proxalutamide trials had serious problems with blinding, outcomes and unpublished data. Hydroxychloroquine didn't lower deaths in hospitalized patients in the large RECOVERY trial.

## Pooled early treatment analyses

In mid-2021, c19early.com listed random-effects meta-analyses of early COVID-19 treatments with very large benefits, like 89% improvement for fluvoxamine and 92% for proxalutamide. But they pooled different study designs and different outcomes together. The fluvoxamine estimate combined a randomized trial measuring clinical deterioration with a prospective cohort measuring death or ICU admission, and the proxalutamide estimate combined a death outcome with a viral clearance outcome. A risk ratio for one outcome can't be meaningfully averaged with a risk ratio for a different outcome.
![[c19early pooled early treatments.webp]]
→ [[Ivermectin for COVID-19]]

## Fluvoxamine

Fluvoxamine is an SSRI antidepressant that also stimulates the σ-1 receptor, which regulates cytokine production, so it was tested to prevent the immune overreaction in COVID-19.

![[c19early fluvoxamine pooled.webp]]

### Lenze trial

In a double-blind, fully remote trial of 152 outpatients with mild COVID-19, clinical deterioration within 15 days happened in 0 of 80 people on fluvoxamine and 6 of 72 on placebo (absolute difference 8.7%, 95% CI 1.8–16.4). Deterioration meant shortness of breath or hospitalization for shortness of breath or pneumonia, plus oxygen saturation under 92% on room air or needing oxygen to stay at 92% or more. Only 76% completed the trial, and the authors called the result preliminary because of the small sample and short follow-up.
![[Lenze 2020 fluvoxamine trial.webp]]
[Lenze 2020](https://pubmed.ncbi.nlm.nih.gov/33180097/)

The outcome turned a continuous measure, oxygen saturation, into a yes/no at a 92% cut-off. Median and interquartile range of baseline oxygen saturation were the same in both groups (97%, IQR 96–98), but the range wasn't: the lowest value was 93% with fluvoxamine and 92% with placebo. People starting right at the cut-off need only a tiny drop to count as deteriorating, so with only 6 events, a few such patients in one group could drive the result. That doesn't make the trial useless, but it means it needed confirming.
![[Lenze 2020 baseline oxygen saturation.png]]

### Seftel cohort

In a prospective cohort during a workplace outbreak, 65 people who chose fluvoxamine had no hospitalizations, versus 6 of 48 who declined it. People chose whether to take it, and the comparison wasn't adjusted for any confounders.
[Seftel 2021](https://pubmed.ncbi.nlm.nih.gov/33623808/)

### Larger trials

In the TOGETHER trial in Brazil (1,497 high-risk outpatients), fluvoxamine reduced emergency observation for more than 6 hours or transfer to hospital from 16% to 11% (RR 0.68, 95% credible interval 0.52–0.88). Deaths were 17 versus 25 (OR 0.68, 95% CI 0.36–1.27, not significant), and fewer in the per-protocol analysis of people who took nearly all their doses.
[Reis 2022](https://pubmed.ncbi.nlm.nih.gov/34717820/)

In the COVID-OUT trial (1,323 US outpatients), fluvoxamine didn't prevent hypoxemia, emergency visits, hospitalization or death (adjusted OR 0.94, 95% CI 0.66–1.36), and neither did ivermectin (1.05).
[Bramante 2022](https://pubmed.ncbi.nlm.nih.gov/36070710/)

## Proxalutamide

Proxalutamide is an androgen receptor blocker, tested because SARS-CoV-2 enters cells using TMPRSS2, a protease regulated by androgens.

![[c19early proxalutamide pooled.webp]]

**Outpatient men.** In a trial of 268 male outpatients in Brasília, proxalutamide reduced 30-day hospitalization (RR 0.09, 95% CI 0.03–0.27). The two deaths were both in the placebo group, so the death result rests on just 2 events. The trial was described as double-blind, but in the preprint group assignment was known to the study monitor, who works with the doctors managing patients. That matters most for outcomes doctors decide on, like hospitalization.
![[Proxalutamide trial blinding procedures.png]]
[McCoy 2021](https://pubmed.ncbi.nlm.nih.gov/34350193/)
[Research Square preprint](https://www.researchsquare.com/article/rs-135303/v2)

**Outpatient men and women.** In a trial of 236 outpatients, the primary outcomes were viral clearance by PCR on day 7 (82% vs 31%) and time to clinical remission, not deaths. Allocation was unequal (171 on proxalutamide vs 65 on placebo).
[Cadegiani 2021](https://pubmed.ncbi.nlm.nih.gov/33633920/)

**Hospitalized patients.** The trial behind the large death reduction (12 vs 141 deaths) was only a preprint at the time.
[Cadegiani 2021 preprint](https://www.medrxiv.org/content/10.1101/2021.06.22.21259318)

## Hydroxychloroquine

Early enthusiasm came from in vitro activity and small studies. In a single-arm French study, 20 treated patients cleared virus from nasopharyngeal swabs by day 6 more often than untreated controls from another centre and patients who refused the protocol. It measured viral load, not clinical outcomes. The paper was retracted in December 2024.
[Gautret 2020](https://pubmed.ncbi.nlm.nih.gov/32205204/) · [Retraction notice](https://pubmed.ncbi.nlm.nih.gov/39730229/)

In the RECOVERY trial, 1,561 hospitalized patients randomized to hydroxychloroquine and 3,155 to usual care:
- **Deaths.** 28-day mortality was 27.0% versus 25.0% (rate ratio 1.09, 95% CI 0.97–1.23), with consistent results in every prespecified subgroup.
- **Discharge.** Fewer patients on hydroxychloroquine were discharged alive within 28 days (59.6% vs 62.9%; rate ratio 0.90, 0.83–0.98).
- **Ventilation.** Among patients not ventilated at the start, more on hydroxychloroquine went on to mechanical ventilation or died (30.7% vs 26.9%; risk ratio 1.14, 1.03–1.27).

Enrollment in the hydroxychloroquine arm was stopped early for lack of efficacy.
[RECOVERY 2020](https://pubmed.ncbi.nlm.nih.gov/33031652/)

## Connections
**Builds on**
- [[Ivermectin for COVID-19]] — another repurposed drug that looked promising before the large trials
- [[COVID-19 lockdowns]] — the time lockdowns were buying while treatments were tested
