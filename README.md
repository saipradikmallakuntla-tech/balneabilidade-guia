# Balneabilidade Guia / Bathing-water Guide

[Aplicativo / Live app](https://saipradikmallakuntla-tech.github.io/balneabilidade-guia/)

PT: guia educativo PT/EN para consultar fontes e comparar datas de boletins. Quatro cenários fictícios filtráveis por município e presença de data, comparador de dias e checklist. Não fornece classificação de água, boletins reais, validade sanitária ou liberação para banho.

EN: PT/EN educational source-reading guide with four fictional filterable scenarios, a date-difference calculator and a checklist. It supplies no actual water classification, reports, sanitary validity rule or bathing clearance.

## Run / Executar

No build, dependencies, API, analytics, geolocation or persistent form-data storage. Serve with `python3 -m http.server 8080`. Pages: `main` root, `.nojekyll`, enforced HTTPS, no custom domain. `?lang=en` selects English; navigation works without JavaScript.

## Model and limits / Modelo e limites

`core.js` exports pure `day`, `compare`, `filter` and `scenarios` for Node tests. Dates must be real ISO calendar dates in 2000–2100; UTC day arithmetic avoids daylight-saving differences. A visit before the report is rejected. Equal dates = zero days; 2024-02-28 to 2024-03-01 = two days. The default November dates are fixed examples, not fetched bulletins. No freshness threshold or safety score is calculated.

Reference selected 2026-11-15: https://cetesb.sp.gov.br/praias/ . The selection date is not a sampling date or proof of current conditions. Consult official reports, the precise sampling location, current signage and health guidance. City labels organize fictional exercises; they are not monitored beach records or field observations.

See [NETWORK.md](NETWORK.md) and the hub's release report for the actual test scope. PT/EN covers static text, dynamic results, errors, filters and navigation. No claim is made that source websites offer English.
