Selezionare tutti gli studenti nati nel 1990 (160)
```SQL
SELECT *
FROM `students`
WHERE year(date_of_birth) = 1990
```
Selezionare tutti i corsi che valgono più di 10 crediti (479)
```SQL
SELECT *
 FROM `courses`
WHERE cfu > 10
```
Selezionare tutti gli studenti che hanno più di 30 anni
```SQL
SELECT * 
FROM `students`
WHERE TIMESTAMPDIFF(YEAR,date_of_birth, CURDATE()) > 30
```
Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
laurea (286)
```SQL
SELECT * 
FROM `courses`
WHERE period= 'I semestre'  AND year = '1'
```
Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21)
```SQL
SELECT * 
FROM `exams`
WHERE HOUR(hour) >= 14 AND date = '2020-06-20'
```
Selezionare tutti i corsi di laurea magistrale (38)
```SQL
SELECT * FROM `degrees`
WHERE level = 'magistrale'
```

 Da quanti dipartimenti è composta l'università? (12)
 ```SQL
 SELECT COUNT(*) AS 'number' 
 FROM `departments`
 ```

 Quanti sono gli insegnanti che non hanno un numero di telefono? (50)

 ```SQL
 SELECT COUNT(id) AS total 
 FROM `teachers` 
 WHERE `phone` IS NULL
 ```
 Inserire nella tabella degli studenti un nuovo record con i propri dati (per il campo
degree_id, inserire un valore casuale)
```SQL
INSERT INTO `students` (
`degree_id`,
`name`,
`surname`,
`date_of_birth`,
`fiscal_code`, 
`enrolment_date`,
`registation_number`
`email`) VALUES (
    '2323'
'Leonardo','Corazzini','2001-10-19','crzlrd01r19b832x','2019-01-01','564684','leocora10@gmail.com')
 ```

 Cambiare il numero dell’ufficio del professor Pietro Rizzo in 126
 ```SQL
 UPDATE `teachers` SET `office_number` = '126'
WHERE `id` = '58' AND `name` = 'Pietro' AND `surname` = 'Rizzo' 
 ```

 Eliminare dalla tabella studenti il record creato precedentemente al punto 9
 ```SQL
 DELETE FROM `students` 
WHERE `id` = '5001' AND `name` = 'Leonardo' AND `surname` = 'Corazzini'
 ```

