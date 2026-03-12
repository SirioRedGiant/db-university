# EXERCISES

### 1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia --> 68

```sql

    SELECT *
    FROM `db-university`.`students`
    INNER JOIN `db-university`.`degrees`
    ON  degrees.id = `students`.`degree_id`
    WHERE degrees.name = "Corso di Laurea in Economia"

```

### 2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze --> 1

```sql

    SELECT *
    FROM `db-university`.departments
    INNER JOIN `db-university`.degrees
    ON departments.ID = degrees.department_id
    WHERE departments.name = "Dipartimento di Neuroscienze" AND degrees.LEVEL = "magistrale"

```

### 3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44) --> 11

```sql
#Controllo in teachers table
select *
from teachers
where teachers.name = "Fulvio" and teachers.surname = "Amato"

#soluzione
SELECT
	teachers.*,
    courses.*
FROM teachers

INNER JOIN course_teacher
ON teachers.id = course_teacher.teacher_id

INNER JOIN courses
ON course_teacher.course_id = courses.id
where teachers.name = "Fulvio" and teachers.surname = "Amato"

```

### 4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome --> 5000

```sql

    SELECT *
    FROM students
    INNER JOIN degrees
    ON students.degree_id = degrees.id

    INNER JOIN departments
    ON  departments.id = degrees.department_id
    ORDER BY students.surname ASC, students.name ASC

```

### 5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti --> 1317

```sql


```

### 6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54) --> 54!

```sql


```

### 7. BONUS: Selezionare per ogni studente il numero di tentativi sostenuti per ogni esame, stampando anche il voto massimo. Successivamente, filtrare i tentativi con voto minimo 18. --> 21880
