## STRUTTURA
- dipartimenti
- corsi laurea
- corsi specifici
- insegnanti
- studenti
- appelli


## DIPARTIMENTI
- ID --> BIGINT, AI
- name
- sito weeb
- numero di telefono
- email

## CORSI LAUREA (collegato ai dipartimenti)
- ID --> BIGINT, AI
- id_dipartimento
- nome
- descrizione
- duraata

## CORSI SPECIFICI (collegato ai corsi di laurea)
- ID --> BIGINT, AI
- id_corso_laurea
- nome
- descrizione

## PIVOT
- id_corso_specifico
- id_insegnante

## INSEGNANTI
- ID --> BIGINT, AI
- id_corso_specifico
- nome
- cognome
- email

## STUDENTI
- ID --> BIGINT, AI
- id_corso_laurea
- nome
- cognome
- data di nascita
- email
- numero di telefono

# ESAMI STUDENTI
- id_studente
- id_appello
- voto

## APPELLI
- ID --> BIGINT, AI
- id_corso_specifico
- data
- ora 
- tipo