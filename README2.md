### SELEZIONARE TUTTI GLI STUDENTI ISCRITTI AL CORSO DI LAUREA IN ECONOMIA
- SELECT * FROM `students` INNER JOIN `degrees` ON `degrees`.`id` = `students`.`degree_id` WHERE `degrees`.`name` = 'Corso di Laurea in Economia';

### SELEZIONARE TUTTI I CORSI DI LAUREA MAGISTRALE DEL DEPARTIMENTO DI NEUROSCIENZE
- SELECT `degrees`.*, `departments`.`name` FROM `degrees` INNER JOIN `departments` ON `departments`.`id`= `degrees`.`department_id` WHERE `degrees`.`level` = 'magistrale' AND `departments`.`name` = 'dipartimento di neuroscienze';