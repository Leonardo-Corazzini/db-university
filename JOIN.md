Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
```SQL
SELECT `students`.name, `students`.surname AS surname, `degrees`.name as degree_name
FROM `students`
JOIN `degrees`
ON `students`.degree_id = `degrees`.id
WHERE `degrees`.name = 'Corso di laurea in economia'
ORDER BY surname ASC;
```
Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze
```SQL
SELECT `degrees`.name as degree_name, `degrees`.level, `departments`.name as department_name
FROM `degrees`
JOIN `departments`
ON `degrees`.department_id = `departments`.id
WHERE `departments`.name = 'dipartimento di neuroscienze' AND `degrees`.level LIKE 'magistrale';
```