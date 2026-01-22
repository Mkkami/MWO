### Otrzymanie instrukcji na ekranie

```mermaid
sequenceDiagram
    autonumber
    actor Uzytkownik as Użytkownik
    participant System as System Biletomatu

    Uzytkownik->>System: Rozpoczęcie interakcji
    
    activate System
    System-->>Uzytkownik: Wyświetlenie kroków wyboru biletu
    
    Uzytkownik->>System: Wykonywanie kroków (wybór biletu/zatwierdzenie)
    
    opt Potrzeba wsparcia [Extend]
        System-->>Uzytkownik: Wyświetlenie szczegółowej pomocy
    end

    alt Kontynuacja
        System-->>Uzytkownik: Prośba o płatność
    else Anulowanie transakcji
        rect rgb(240, 240, 240)
            critical Referencja: Anulowanie transakcji
                Uzytkownik->>System: Wybranie opcji "Anuluj"
            end
        end
    end
    deactivate System
```
### Anulowanie transakcji

```mermaid
sequenceDiagram
    autonumber
    actor Uzytkownik as Użytkownik
    participant System as System Biletomatu

    Uzytkownik->>System: Wybranie opcji "Anuluj"
    
    activate System
    System-->>Uzytkownik: Wyświetlenie potwierdzenia anulowania
    
    opt Zapis powodu anulowania
        Uzytkownik->>System: Wybranie powodu
        System->>System: Zapisanie powodu w logach
    end

    System->>System: Reset interfejsu
    deactivate System
```
