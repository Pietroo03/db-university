## TASK 1
select year(enrolment_date) as anno, count(id) as numero_iscritti
from students
group by year(enrolment_date)

## TASK 2
select office_address, count(id) as numero_professori
from teachers
group by office_address

## TASK 3
select exam_id, avg(vote) as media_voto
from exam_student
group by exam_id

## TASK 4
select department_id as id_dipartimento, count(id) as corsi_di_laurea
from degrees
group by department_id