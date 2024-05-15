### SELEZIONARE TUTTI GLI STUDENTI NATI NEL 1990 (160)
- SELECT * FROM `students` WHERE YEAR(date_of_birth) = 1990;

### SELEZIONARE TUTTI I CORSI CHE VALGONO PIU' DI 10 CREDITI (479)
- SELECT * FROM `courses` WHERE `cfu` > 10;

### SELEZIONARE TUTTI GLI STUDENTI CHE HANNO PIU' DI 30 ANNI
- SELECT * , TIMESTAMPDIFF(YEAR, `date_of_birth`,CURDATE()) AS `age` FROM `students`;

### SELEZIONARE TUTTI I CORSI DEL PRIMO SEMESTRE DEL PRIMO ANNO DI UN QUALSIASI CORSO DI LAUREA (286)
- SELECT * FROM `courses` WHERE `period` = 'I semestre' AND `year`=1;

### SELEZIONARE TUTTI GLI APPELLI D'ESAME CHE AVVENGONO NEL POMERIGGIO (DOPO LE 14) DEL 20/06/2020 (21)
- SELECT * FROM `exams` WHERE `date` = '2020-06-20' AND `hour` BETWEEN '14:00:00' AND '23:59:59';

### SELEZIONARE TUTTI I CORSI DI LAUREA MAGISTRALE (38)
- SELECT * FROM `degrees` WHERE `level` = 'magistrale';

### DA QUANTI DIPARTIMENTI E' COMPOSTA L'UNIVERSITA'?
- SELECT COUNT(*) AS `university_departments` FROM `departments`;

### QUANTI SONO GLI INSEGNANTI CHE NON HANNO UN NUMERO DI TELEFONO? (50)
- SELECT * FROM `teachers` WHERE `phone` IS NULL;