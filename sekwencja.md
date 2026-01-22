# Diagram sekwencji - Szybki wybór rodzaju biletu
```mermaid
sequenceDiagram
autonumber
    actor U as Użytkownik
    participant B as Biletomat

    U ->> B: Rozpoczęcie interakcji
    B -->> U: Wyświetlenie listę biletów
    
    U->>B: Wybór kategorii biletu
    B-->>U: Wyświetlenie listy biletów
    
    U->>B: Wybór biletu
    B-->>U: Wyświetlenie podsumowania

    alt Potwierdzenie
        U->>B: Potwierdzenie wyboru
        B-->>U: Wyświetlenie komunikatu o potwierdzeniu
    else Anulowanie
        U->>B: Anuluje proces
        U-->>B: Powrót do ekranu startowego
    end

```

```mermaid
sequenceDiagram
autonumber
    actor U as Użytkownik
    participant B as Biletomat

    U ->> B: Rozpoczęcie interakcji
    B -->>U: Wyświetlenie opcji języka

    U ->> B: Wybór języka
    B ->>B: Dostosowanie interfejsu
    B -->>U: Wyświetlenie interfejsu

    opt Anulowanie
        U ->> B: Anulowanie procesu
        B -->> U: Powrót
    end    
```
