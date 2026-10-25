# 콤프턴 산란 파장변화 계산기

정지한 자유 표적에 의한 광자 산란의 파장 증가량을 계산한다.

- ID: E115
- App: https://nanalab.kr/eng-compton-shift/
- Repository: https://github.com/NaNaCompany/eng-compton-shift
- Formula: Δλ = (h/(mc))(1−cos θ) = (2h/(mc))sin²(θ/2)

## Model and data

m>0이며 0≤θ≤π다. θ는 입사 광자 방향과 산란 광자 방향 사이 각도다. 표적은 처음 정지한 자유 입자로 취급하며 결합에너지·집단 산란·매질 효과는 제외한다. 출력은 산란 후 파장 자체가 아니라 증가량이다. 작은 각도에서는 동치인 sin² 식으로 뺄셈 손실을 줄인다.

Inputs normalize to SI. Repeated-input models support adding/removing actual input rows. Calculations, finite-number checks and physical-domain checks run locally; no external property database or solver API is used.

## Validation

Run node --test tests/*.test.mjs and python scripts/build-locales.py --check. tests/reference.json contains independently computed high-precision default and boundary references. The source notices distinguish original MIT work from citation-only external references.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
