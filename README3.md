### CONTARE QUANTI ISCRITTI CI SONO STATI OGNI ANNO
- SELECT COUNT(*) AS `numero_iscritti`, YEAR(`enrolment_date`) AS `enrolment_year` FROM `students` GROUP BY YEAR(`enrolment_date`);

### CONTARE GLI INSEGNANTI CHE HANNO L'UFFICIO NELLO STESSO EDIFICIO
- SELECT COUNT(*) AS `teachers_with_same_office`, `office_address` FROM `teachers` GROUP BY `office_address`;

### CALCOLARE LA MEDIA DEI VOTI DI OGNI APPELLO D'ESAME
- SELECT COUNT(*) AS `exams_per_date`, `exams`.`date`, AVG(`exam_student`.`vote`) AS `average_vote` FROM `exam_student` INNER JOIN `exams` ON `exams`.`id` = `exam_student`.`exam_id` GROUP BY `exams`.`date`;