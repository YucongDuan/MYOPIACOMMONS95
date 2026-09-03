# DIKWP-MYOPIACOMMONS95

## Global Myopia Recovery, Progression Management, High-Myopia Safety, Access Equity and Evidence Accountability OS

DIKWP-MYOPIACOMMONS95 is an English-only, local-first, open-source reference system for people with myopia, families, clinicians, researchers, public-health programmes, and other AI or Agent systems.

It does not claim that clearer unaided vision, a lower spectacle prescription, corneal reshaping, or refractive surgery equals biological reversal of axial myopia. It separates five outcomes that are often commercially collapsed:

1. optical correction;
2. recoverable visual function;
3. slowing of myopia progression and axial elongation;
4. detection and treatment of myopia-related disease;
5. experimental structural restoration.

The platform also treats access as a clinical variable. A missing axial-length measurement, unavailable cycloplegic refraction, absent retinal specialist, or inability to buy spectacles is recorded as an unresolved gap rather than as a normal result.

## Core capabilities

- symptom-based urgent safety triage;
- per-eye refraction and axial-length timelines;
- life-stage pathways from childhood to older adulthood;
- high-myopia, macular, retinal, glaucoma, lens, ocular-surface, and functional-vision lanes;
- WHO SPECS 2030-aligned access and equity planning;
- a patient-owned portable Myopia Passport;
- product- and jurisdiction-specific regulatory verification gates;
- an evidence registry with dated source boundaries;
- a measurement truth contract;
- a 20-rule commercial and scientific claim auditor;
- append-only outcome, adverse-event, and consent ledgers;
- an offline dashboard;
- read-only MCP and OpenAPI reference interfaces;
- no automatic diagnosis, prescription, dose selection, device control, surgical selection, payment, or external action.

## Quick start

```bash
python -m venv .venv
. .venv/bin/activate
pip install -e .

myopiacommons95 doctor
myopiacommons95 demo --out outputs/demo
myopiacommons95 verify --out outputs/demo/pediatric_progression
```

Compile a local profile:

```bash
cp examples/patient_intake_template.json my_profile.json
# Edit the file, use a local identifier, and set explicit consent to true.
myopiacommons95 compile --profile my_profile.json --out outputs/my_record
```

Audit a marketing claim:

```bash
myopiacommons95 audit-claim \
  "Clear unaided vision proves that the eyeball has permanently shortened"
```

Start the loopback-only read-only API:

```bash
myopiacommons95 serve --out outputs/my_record --host 127.0.0.1 --port 8799
```

## Emergency boundary

A sudden increase in floaters, new flashes, a curtain or shadow, a new visual-field defect, or sudden vision loss can accompany retinal detachment. Seek immediate qualified eye care or an emergency department. Do not delay for this software, exercises, massage, red-light exposure, contact-lens wear, or a routine appointment.

## Evidence and regulatory boundary

The evidence snapshot is dated 2026-09-03. Product indications and regulatory status must be verified for the exact product, formulation, concentration, device, age range, and jurisdiction. This repository is not a complete or continuously synchronized global regulatory database.

## License

The reference implementation is licensed under Apache-2.0. The license does not transfer rights in patient data, third-party publications, product names, clinical materials, trademarks, personal identity, or regulatory claims.
