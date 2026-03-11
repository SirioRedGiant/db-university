Esercizio di oggi:
nome repo: db-university

Dopo aver creato un nuovo database nel vostro MySQL Workbench e aver importato lo schema allegato, eseguite le query del file allegato.

Cosa consegnare?
Dopo aver testato le vostre query con MySQL Workbench, riportatele in un file MD e caricatelo nella vostra repo.

Guida all’installazione
Installazione SQL e MySQL Workbench (Windows)
Scarichiamo il https://dev.mysql.com/downloads/installer/ e gestiamo tutto col Wizard.
Scegliamo la versione Full installando anche MySQL Workbench e MySQL Shell
Impostiamo l’avvio di MySQL all’avvio del PC
Impostiamo una password per l’utente root

# QUERY DA CERCARE

### 1. Selezionare tutti gli studenti nati nel 1990 (160)

```sql

    SELECT * FROM `db-university`.students
    WHERE students.date_of_birth >= "1990-01-01" and students.date_of_birth <= "1990-12-31";

```

### 2. Selezionare tutti i corsi che valgono più di 10 crediti (479)

```sql

```

### 3. Selezionare tutti gli studenti che hanno più di 30 anni

```sql

```

### 4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286)

```sql

```

### 5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21)

```sql

```

### 6. Selezionare tutti i corsi di laurea magistrale (38)

```sql

```

### 7. Da quanti dipartimenti è composta l'università? (12)

```sql

```

### 8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)
