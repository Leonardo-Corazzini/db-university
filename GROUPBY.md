1. Contare quanti iscritti ci sono stati ogni anno
```SQL
  SELECT COUNT(id) as total_students, YEAR(enrolment_date) as year
FROM `students`
GROUP BY YEAR(enrolment_date);
 ```
2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
```SQL
  
 ```
3. Calcolare la media dei voti di ogni appello d'esame
```SQL
  
 ```
4. Contare quanti corsi di laurea ci sono per ogni dipartimento
```SQL
  
 ```