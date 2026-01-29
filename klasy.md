```mermaid
classDiagram

  class Użytkownik {}

  class SystemBiletomatu {
    -List krokiWyboruBiletu
    -string pomoc
    +List rozpoczęcieInterakcji()
    +void anuluj()
    +void wyświetleniePomocy()
  }

  Użytkownik --> SystemBiletomatu
```

```mermaid
classDiagram
  class Użytkownik {
  }

  class SystemBiletomatu {
    +void anuluj()
    +void wybórPowoduAnulowania()
  }

  class Logger {
      +void zapiszLogAnulowania(powod)
  }

  class Interfejs {
    +void resetInterfejsu()
  }

    Użytkownik --> SystemBiletomatu : anulowanie
    SystemBiletomatu --> Logger : zapis danych
    SystemBiletomatu --> Interfejs : wyswietla

```
