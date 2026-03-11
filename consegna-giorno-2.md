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
    ------------------------------------
    SELECT *, YEAR(students.date_of_birth)
    FROM students
    WHERE YEAR(students.date_of_birth) = 1990

```

### 2. Selezionare tutti i corsi che valgono più di 10 crediti (479)

```sql

    SELECT *
    FROM courses
    WHERE courses.cfu > 10;

```

### 3. Selezionare tutti gli studenti che hanno più di 30 anni

```sql

    SELECT *, YEAR(students.date_of_birth)
    FROM students
    where year(students.date_of_birth) <= 1996
    ----------------------------------------------
    SELECT *, TIMESTAMPDIFF(YEAR,students.date_of_birth, CURDATE())
    FROM students
    WHERE TIMESTAMPDIFF(YEAR, students.date_of_birth, CURDATE()) > 30

```

### 4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286)

```sql

    SELECT *
    FROM courses
    WHERE courses.period = "I semestre" AND  courses.year = 1

```

### 5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21)

```sql

    SELECT *
    FROM exams
    WHERE exams.hour >= "14:00:00" AND exams.date = "2020-06-20"
    ----
    SELECT *, HOUR(exams.hour)
    FROM exams
    WHERE HOUR(exams.hour) >= 14 AND exams.date = "2020-06-20";


```

### 6. Selezionare tutti i corsi di laurea magistrale (38)

```sqlD

    SELECT *
    FROM  degrees
    WHERE degrees.name LIKE "Corso di Laurea Magistrale%"


```

### 7. Da quanti dipartimenti è composta l'università? (12)

```sql

    SELECT COUNT(*)
    FROM departments

```

### 8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)

```sqlD

    SELECT *
    FROM teachers
    WHERE teachers.phone is null

```
