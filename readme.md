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

## CORSI LAUREA (collegato ai dipartimenti)
- ID --> BIGINT, AI
- id_dipartimento
- nome

## CORSI SPECIFICI (collegato ai corsi di laurea)
- ID --> BIGINT, AI
- nome
- id_corso_laurea
- id_insegnante

## INSEGNANTI
- ID --> BIGINT, AI
- id_dipartimento
- id_corso_specifico
- nome
- cognome
- email

## STUDENTI
- ID --> BIGINT, AI
- id_dipaartimento
- id_corso_specifico
- nome
- cognome
- data di nascita
- email
- numero di telefono

## APPELLI
- ID --> BIGINT, AI
- id_corso_specifico