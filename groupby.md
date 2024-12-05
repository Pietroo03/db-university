## TASK 1
SELECT YEAR(`enrolment_date`) AS `anno`, COUNT(`id`) AS `numero_iscritti`
FROM `students`
GROUP BY YEAR(`enrolment_date`);

## TASK 2
SELECT `office_address`, COUNT(`id`) AS `numero_professori`
FROM `teachers`
GROUP BY `office_address`;

## TASK 3
SELECT `exam_id`, AVG(`vote`) AS `media_voto`
FROM `exam_student`
GROUP BY `exam_id`;

## TASK 4
SELECT `department_id` AS `id_dipartimento`, COUNT(`id`) AS `corsi_di_laurea`
FROM `degrees`
GROUP BY `department_id`;