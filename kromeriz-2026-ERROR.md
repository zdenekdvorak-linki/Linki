# Kroměříž 2026 – stažení kandidátů selhalo

- **Zdroj:** https://programydovoleb.cz/volby/komunalni-volby/176/obec/588296
- **Čas pokusu:** 2026-09-24 18:50:06 UTC
- **Příkaz:** `curl -sS https://programydovoleb.cz/volby/komunalni-volby/176/obec/588296`

## Chyba

```
curl: (56) CONNECT tunnel failed, response 403
```

Egress proxy prostředí (agent proxy) odmítla spojení na `programydovoleb.cz:443`
(`connect_rejected` – „gateway answered 403 to CONNECT (policy denial or upstream failure)“).
Stránka se tedy nestáhla a žádná data o kandidátech nebyla získána.
Soubory `kromeriz-2026-kandidati.csv` a `kromeriz-2026-vekove-prumery.md` proto nevznikly –
data nebyla odhadována ani doplňována.

## Jak to vyřešit

Povolit doménu `programydovoleb.cz` v síťové politice prostředí Claude Code
(Environment → Network access, např. „Full“ nebo vlastní allowlist) a úlohu spustit znovu.
