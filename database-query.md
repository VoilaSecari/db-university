Selezionare tutti gli studenti nati nel 1990
(160)

```sql
SELECT COUNT(`id`)
FROM `students`
WHERE
	YEAR(`date_of_birth`) = 1990;
```

Selezionare tutti i corsi che valgono più di 10 crediti
(479)

```sql
SELECT COUNT(`id`)
FROM `courses`
WHERE `cfu` > 10;
```

Selezionare tutti gli studenti che hanno più di 30 anni

```sql
SELECT *
FROM `students`
WHERE
	YEAR(`date_of_birth`) < 1995;
```

Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
laurea (286)

```sql
SELECT COUNT(*)
FROM `courses`
WHERE
	`year` = 1 AND
	`period` = "I semestre";
```

Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21)

```sql
SELECT COUNT(*)
FROM `exams`
WHERE
	DATE(`date`) = "2020-06-20"
    AND TIME(`hour`) > "14:00:00";
```

Selezionare tutti i corsi di laurea magistrale (38)

```sql
SELECT COUNT(*)
FROM `degrees`
WHERE
	`name` LIKE "%Magistrale%";
```

Da quanti dipartimenti è composta l'università? (12)

```sql
SELECT COUNT(`id`)
FROM `departments`;
```

Quanti sono gli insegnanti che non hanno un numero di telefono? (50)

```sql
SELECT COUNT(`id`)
FROM `teachers`
WHERE
	`phone` IS NULL;
```
