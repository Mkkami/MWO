### Szybki wybór rodzaju biletu
```mermaid
flowchart LR
uzytkownik --> id1([Szybki wybór rodzaju biletu])
id1([Szybki wybór rodzaju biletu]) --include--> id2([Sprawdzenie biletów])
id1([Szybki wybór rodzaju biletu]) --include--> id3([Anulowanie transakcji])
id4([Podpowiedź interfejsu]) --extends--> id1([Szybki wybór rodzaju biletu])
```

```mermaid
flowchart LR
uzytkownik --> id1([Wybór języka])
id1([Wybór języka]) --include--> id2([Domyślny język])
id1([Wybór języka]) --include--> id3([Anulowanie transakcji])
id4([Lista popularnych języków]) --extends--> id1([Wybór języka])
```
