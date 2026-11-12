# Lifting Calculator

Free lifting calculator based on the Revised NIOSH Lifting Equation. Enter load, reach, pick-up and set-down heights, twist, grip, frequency and shift length to get the recommended weight limit, Lifting Index and maximum lifts — US, EU, UK and Brazil. For information only; not a substitute for a professional ergonomic assessment.

**Live version:** https://resdavo.github.io/lifting-calculator/

The calculator is a single HTML file (`index.html`). It runs entirely in your browser — there is nothing to install, and no data you enter is sent anywhere.

## How to use it

1. Open the live version above, or open `index.html` in a browser.
2. Choose a region at the top: United States, European Union, United Kingdom, or Brazil.
3. Enter the values for the lift (see below). Use the − and + buttons or type the values directly.
4. Press **Recalculate**. If you change a value afterwards, the result is marked as out of date until you press Recalculate again.
5. Read the recommended maximum, the Lifting Index, and the maximum lifts. The calculator checks both ends of the lift and reports which one governs.

## What you enter

- Load weight
- Horizontal distance — from the mid-point between the ankles to the hands
- Pick-up height — floor to hands where the load is picked up
- Set-down height — floor to hands where the load is put down, with a “Set-down = pick-up” shortcut if both heights are the same
- Twist / asymmetry angle
- Frequency — lifts per minute
- Total lifting minutes — count any minute in which at least one lift happens as one minute of lifting
- Length of shift — 8, 10, or 12 hours
- Grip / coupling — good, fair, or poor
- Who is lifting — general adult workforce, women, or a young / older / returning worker

Vertical travel and lift direction are worked out automatically from the pick-up and set-down heights.

## What it calculates

- Recommended weight limit at pick-up and at set-down, with the lower of the two governing
- Lifting Index — load ÷ recommended limit. An index of 1.0 or less is the design goal
- Maximum lifts in the lifting period you entered
- Maximum lifts per shift, worked out separately — the two maximums are never mixed
- Lifts you have scheduled in the lifting period, from your frequency and lifting minutes
- The individual multipliers behind the result, so you can see which factor is reducing the limit most
- A comparison of all four regions for the same lift

## How the calculation works

The Recommended Weight Limit (RWL) is:

```text
RWL = 23 kg × HM × VM × DM × AM × FM × CM
```

where HM is the horizontal multiplier, VM the vertical multiplier, DM the travel-distance multiplier, AM the twist (asymmetry) multiplier, FM the frequency multiplier, and CM the grip (coupling) multiplier. Each multiplier starts at 1.00 under ideal conditions and only goes down.

Points that matter when checking a result:

- The limit is worked out at both the pick-up (origin) and the set-down (destination), as the NIOSH method requires. The lower limit governs.
- Frequency multipliers are the published NIOSH table values for the duration band and vertical zone that apply. If the frequency you enter is not itself a listed table value, the next higher listed frequency is used — the conservative direction. Values are never rounded down and never interpolated.
- The maximum lifts in your lifting period and the maximum lifts per shift are calculated separately, in different duration bands. They are not the same number scaled up.
- The NIOSH equation is validated for work periods up to 8 hours. Results for 10- and 12-hour shifts should be treated with extra caution.

## Regional notes

- **United States — OSHA / NIOSH:** OSHA has no weight-limit standard. The result is the Revised NIOSH Lifting Equation, the recognised assessment method behind General Duty Clause enforcement.
- **European Union:** Directive 90/269/EEC requires avoiding or reducing manual handling risk and sets no single weight limit. The number shown applies the ISO 11228-1 method, with a 25 kg reference mass under ideal conditions.
- **United Kingdom:** The result compares your load with the HSE guideline filter weight for that zone of the body. Exceeding a filter weight is not an automatic breach of the Manual Handling Operations Regulations 1992 — it means a detailed assessment is required. The UK filter weight is a separate guideline and stands even when the NIOSH frequency multiplier is 0.
- **Brazil:** The recommended limit follows the same ergonomic method used under NR-17 assessments and is checked separately against the CLT legal ceilings (60 kg; 20 kg continuous / 25 kg occasional for women). Passing a CLT ceiling does not make a lift ergonomically safe.

## Reporting an error

If you find an error, please open an Issue in this repository. Include the values you entered — region, load, distances, heights, twist, frequency, lifting minutes and shift length — and the result you expected, so the calculation can be checked against the same inputs.

## Sources

- Revised NIOSH Lifting Equation and Applications Manual; CDC/NIOSH: https://www.cdc.gov/niosh/topics/ergonomics/nlecalc.html
- OSHA ergonomics and the General Duty Clause: https://www.osha.gov/ergonomics
- Council Directive 90/269/EEC on manual handling of loads: https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=celex%3A31990L0269
- ISO 11228-1:2021, Ergonomics — Manual handling — Part 1: https://www.iso.org/standard/76820.html
- Manual Handling Operations Regulations 1992: https://www.legislation.gov.uk/uksi/1992/2793/made
- HSE manual handling guidance and guideline filter weights: https://www.hse.gov.uk/msd/manual-handling/index.htm
- Brazil — CLT (Decreto-Lei 5.452/1943), Art. 198 and Art. 390: https://www.planalto.gov.br/ccivil_03/decreto-lei/del5452.htm
- Brazil — NR-17 Ergonomics: Ministério do Trabalho e Emprego, https://www.gov.br/trabalho-e-emprego/pt-br

These standards are summarised in the calculator. Read the full text before making compliance decisions.

## Disclaimer — please read before using this calculator

This calculator was created by David O Restrepo to the best of his knowledge and abilities, with assistance from Muse AI. It is provided free of charge, “as is,” without any warranty of any kind, express or implied, including any warranty of accuracy, completeness, or fitness for a particular purpose.

Despite careful checking, this calculator may contain errors — in its formulas, tables, conversions, or interpretation of the underlying standards. Its results are estimates based on the published methods cited above. They are not a substitute for a professional ergonomic assessment, the advice of a qualified safety professional, or the full text of the applicable standard or regulation. Always verify important results independently and consult the official sources listed above before making workplace, health, safety, or compliance decisions.

By using this calculator, you agree that you do so entirely at your own risk and that you assume full responsibility for any decision or action taken based on its results. To the fullest extent permitted by law, by using it you waive and release David O Restrepo from any and all claims, demands, damages, losses, and liabilities of any kind arising out of or in connection with your use of this calculator or reliance on its results. If you do not agree to these terms, do not use this calculator.

## Author

Created by David O Restrepo, using Muse AI.
