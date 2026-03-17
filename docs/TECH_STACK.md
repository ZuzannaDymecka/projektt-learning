# TECH_STACK.md

## Frontend: React JS
React zapewnia modularność, wydajność i łatwość tworzenia komponentów interfejsu. Zastosowanie hooków upraszcza logikę stanu i integrację z API Supabase.

## Styl: Tailwind CSS
Tailwind daje aplikacji wysoki stopień elastyczności i spójną stylistykę z minimalnym CSS. Klasa utility-first przyspiesza iteracje UI.

## Komponenty: Shadcn UI
Shadcn UI oferuje gotowe, dostępne komponenty React, zoptymalizowane pod Tailwind i zgodne ze standardami UX. Wykorzystanie przyspiesza MVP i spójność UI.

## Backend / Baza: Supabase
Supabase stanowi backend jako usługę (BaaS) z natywną obsługą PostgreSQL, Auth i Storage. Pozwala szybko wprowadzić uwierzytelnianie, chronione dane i pliki bez własnej infrastruktury.

## Integracja
- React <-> Supabase Client: uwierzytelnianie, zapytania CRUD, subskrypcje real-time.
- Tailwind + Shadcn: ujednolicone style, komponenty formularzy, układ responsywny.
- Supabase RLS: kontrola dostępu na poziomie wiersza.
