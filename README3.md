### CONTARE QUANTI ISCRITTI CI SONO STATI OGNI ANNO
- SELECT COUNT(*) AS `numero_iscritti`, YEAR(`enrolment_date`) AS `enrolment_year` FROM `students` GROUP BY YEAR(`enrolment_date`);