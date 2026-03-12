# EXERCISES

### 1. Contare quanti iscritti ci sono stati ogni anno

```sql
    SELECT YEAR(`enrolment_date`), COUNT(*) AS `students_count`
    FROM `students`
    GROUP BY YEAR(`enrolment_date`)
    ORDER BY YEAR(`enrolment_date`) DESC;

```

### 2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

```sql


```

### 3. Calcolare la media dei voti di ogni appello d'esame

```sql


```

### 4. Contare quanti corsi di laurea ci sono per ogni dipartimento
