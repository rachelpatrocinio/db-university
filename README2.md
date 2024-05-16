### SELEZIONARE TUTTI GLI STUDENTI ISCRITTI AL CORSO DI LAUREA IN ECONOMIA
- SELECT * FROM `students` INNER JOIN `degrees` ON `degrees`.`id` = `students`.`degree_id` WHERE `degrees`.`name` = 'Corso di Laurea in Economia';

### SELEZIONARE TUTTI I CORSI DI LAUREA MAGISTRALE DEL DEPARTIMENTO DI NEUROSCIENZE
- SELECT `degrees`.*, `departments`.`name` FROM `degrees` INNER JOIN `departments` ON `departments`.`id`= `degrees`.`department_id` WHERE `degrees`.`level` = 'magistrale' AND `departments`.`name` = 'dipartimento di neuroscienze';

### SELEZIONARE TUTTI I CORSI IN CUI INSEGNA FULVIO AMATO (ID=44)
- SELECT `teachers`.`id`, `teachers`.`name`, `teachers`.`surname`, `course_teacher`.`teacher_id`, `degrees`.`name` FROM `teachers` INNER JOIN `course_teacher` ON `teachers`.`id` = `course_teacher`.`teacher_id` INNER JOIN `courses` ON `courses`.`id` = `course_teacher`.`course_id` INNER JOIN `degrees` ON `degrees`.`id` = `courses`.`degree_id` WHERE `teachers`.`id` = 44;

### SELEZIONARE TUTTI GLI STUDENTI CON I DATI RELATIVI AL CORSO DI LAUREA A CUI SONO SCRITTI E IL RELATIVO DIPARTIMENTO, IN ORDINE ALFABETICO PER COGNOME E NOME
- SELECT `students`.`id`, `students`.`name`,`students`.`surname`, `degrees`.`name`, `departments`.`name` FROM `students` INNER JOIN `degrees` ON `degrees`.`id` = `students`.`degree_id` INNER JOIN `departments` ON `departments`.`id` = `degrees`.`department_id` ORDER BY `students`.`surname` ASC, `students`.`name` ASC;
