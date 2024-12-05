## TASK 1
SELECT *
FROM `students`
JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = 'Corso di Laurea in Economia';

## TASK 2
SELECT `degrees`.`name` as `laurea_magistrale`, `departments`.`name` as `nome_dipartimento`
FROM `degrees`
JOIN `departments` ON `degrees`.`department_id` = `departments`.`id`
WHERE `degrees`.`level` = 'magistrale'
AND `departments`.`name` = 'Dipartimento di Neuroscienze';

## TASK 3
SELECT `courses`.`name`
FROM `courses`
JOIN `course_teacher` ON `course_teacher`.`course_id` = `courses`.`id`
JOIN `teachers` ON `course_teacher`.`teacher_id` = `teachers`.`id`
WHERE `teachers`.`id` = 44;

## TASK 4
SELECT `students`.`surname` as `cognome`, 
`students`.`name` as `nome`,
`degrees`.`name` as `corso_laurea`,
`departments`.`name` as `dipartimento`
FROM `students`
JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id`
JOIN `departments` ON `degrees`.`department_id` = `departments`.`id`
ORDER BY `students`.`surname`, `students`.`name`;

## TASK 5
SELECT `degrees`.`name` as `nome_corso_laurea`,
`courses`.`name` as `nome_corso`,
CONCAT(`teachers`.`surname`, ' ', `teachers`.`name`) as `insegnante`
FROM `degrees`
JOIN `courses` ON `degrees`.`id`= `courses`.`degree_id`
JOIN `course_teacher` ON `courses`.`id`= `course_teacher`.`course_id`
JOIN `teachers` ON `course_teacher`.`teacher_id`= `teachers`.`id`;