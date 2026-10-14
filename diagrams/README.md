# Sistemos projektas

Pradinė projektavimo užklausa: [design_prompt.txt](../prompts/design_prompt.txt). Pirmiau pateikta PlantUML versija, po jos – tos pačios sistemos Mermaid versija. Tai šiam darbui parengti projektavimo rezultatai.

## 1. PlantUML komponentų diagrama

```plantuml
@startuml
title DI pagrįsta programavimo klaidų analizės sistema
actor "Vartotojas" as User
package "Google Colab prototipas" {
  component "Įvestis ir validavimas" as Input
  component "Užklausos sudarymas" as Prompt
  component "Atsakymo validavimas\nir sintaksės patikra" as Check
  component "Rezultatų pateikimas" as View
  database "JSON rezultatai" as Store
}
cloud "Gemini API" as Gemini
User --> Input : Python kodas ir kontekstas
Input --> Prompt : validuotas X
Prompt --> Gemini : instrukcija ir X
Gemini --> Check : sugeneruota analizė
Check --> View : analizė ir patikros rezultatas
Check --> Store : JSON
View --> User : paaiškinimas ir taisymas
@enduml
```

## 2. PlantUML veiklos diagrama

```plantuml
@startuml
start
:Priimti Python kodą ir kontekstą;
if (Įvestis tinkama?) then (taip)
  :Sudaryti instrukciją ir X;
  :Kreiptis į Gemini API;
  if (Gautas validus atsakymas?) then (taip)
    :Patikrinti pataisyto kodo sintaksę;
    :Palyginti su y, jei tai demonstracinis pavyzdys;
    :Parodyti analizę ir išsaugoti JSON;
  else (ne)
    :Parodyti API arba formato klaidą;
  endif
else (ne)
  :Parodyti įvesties klaidą;
endif
stop
@enduml
```

## 3. Mermaid komponentų diagrama

```mermaid
flowchart TD
  U["Vartotojas"] -->|"Python kodas ir kontekstas"| I["Įvestis ir validavimas"]
  subgraph C["Google Colab prototipas"]
    I -->|"validuotas X"| P["Užklausos sudarymas"]
    A["Atsakymo validavimas ir sintaksės patikra"] --> V["Rezultatų pateikimas"]
    A --> S[("JSON rezultatai")]
  end
  P -->|"instrukcija ir X"| G["Gemini API"]
  G -->|"sugeneruota analizė"| A
  V --> U
```

## 4. Mermaid veiklos diagrama

```mermaid
flowchart TD
  S(["Pradžia"]) --> I["Priimti Python kodą ir kontekstą"]
  I --> Q{"Įvestis tinkama?"}
  Q -->|"ne"| E["Parodyti įvesties klaidą"]
  Q -->|"taip"| P["Sudaryti instrukciją ir X"]
  P --> G["Kreiptis į Gemini API"]
  G --> R{"Gautas validus atsakymas?"}
  R -->|"ne"| F["Parodyti API arba formato klaidą"]
  R -->|"taip"| A["Patikrinti pataisyto kodo sintaksę"]
  A --> T["Palyginti su y, jei demonstracinis pavyzdys"]
  T --> O["Parodyti analizę ir išsaugoti JSON"]
  E --> Z(["Pabaiga"])
  F --> Z
  O --> Z
```
