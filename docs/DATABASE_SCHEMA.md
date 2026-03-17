# DATABASE_SCHEMA.md

## Tabela: users
- id (uuid, PK)
- email (text, unique)
- created_at (timestamptz)
- role (text)

## Tabela: profiles
- id (uuid, PK)
- user_id (uuid, FK -> users.id)
- full_name (text)
- timezone (text)
- locale (text)
- bio (text)

## Tabela: lessons
- id (uuid, PK)
- title (text)
- description (text)
- course_id (uuid, FK -> courses.id)
- duration_minutes (int)
- content_url (text)
- created_at (timestamptz)

## Tabela: progress
- id (uuid, PK)
- user_id (uuid, FK -> users.id)
- lesson_id (uuid, FK -> lessons.id)
- status (text: planned/in-progress/completed)
- completion_date (timestamptz)
- time_spent_minutes (int)

## Relacje
- users 1:n profiles
- users 1:n progress
- courses 1:n lessons
- lessons 1:n progress

## Wzorzec RLS
- każdym zapytaniu do progress ofertuje verificační user_id = auth.uid()
- ograniczenie odczytu i zapisu w funkcjach do właściciela i roli admin
