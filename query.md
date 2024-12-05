## TASK 1
select *
from students
where year(date_of_birth) = 1990;

## TASK 2
select *
from courses
where cfu > 10

## TASK 3
select *
from students
where TIMESTAMPDIFF(YEAR, 'date_of_birth', CURDATE()) > 30

## TASK 4
select *
from courses
where period = 'I semestre'
and year = 1

## TASK 5
select *
from exams
where hour(hour) >= 14
and date = '2020-06-20'

## TASK 6
select *
from degrees	
where level = 'magistrale'

## TASK 7
select count('id') as totale dipartimenti
from departments

## TASK 8
select *
from teachers
where phone is null

## TASK 9
insert into students (degree_id, name, surname, date_of_birth, fiscal_code, enrolment_date, registration_number, email)
values (56, 'Pietro', 'Ponte', '2003-01-15', 'PNTPTR03A15D969Q', '2024-12-04', 345457657, 'pietro.ponte.03@gmail.com');

## TASK 10
UPDATE teachers
SET office_number = 126
WHERE name = 'Pietro'
AND surname = 'Rizzo'

## TASK 11
delete from students
where name = 'Pietro'
and surname = 'Ponte'