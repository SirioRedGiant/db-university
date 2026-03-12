# EXERCISES

### 1. Contare quanti iscritti ci sono stati ogni anno

```sql
    SELECT YEAR(`enrolment_date`), COUNT(*) AS `students_count`
    FROM `students`
    GROUP BY YEAR(`enrolment_date`)
    ORDER BY YEAR(`enrolment_date`) DESC;
    -----------------------------------------
    SELECT YEAR(`enrolment_date`) AS `enrolment_year`, COUNT(*) AS `students_count`
    FROM `students`
    GROUP BY `enrolment_year`
    ORDER BY `enrolment_year` DESC;

```

### 2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

```sql
    SELECT COUNT(*)
    FROM teachers
    GROUP BY teachers.office_address
    ORDER BY teachers.office_address DESC

```

### 3. Calcolare la media dei voti di ogni appello d'esame

```sql


```

### 4. Contare quanti corsi di laurea ci sono per ogni dipartimento
