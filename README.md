# Fakultet

Да се имплементира апликација за евидентирање на оценките на студентите на еден факултет. Студентите на факултетот може да 
бидат запишани на тригодишни или четиригодишни студии. Во текот на студиите, студентите имаат два семестри во секоја година
и во секој од семестрите имаат по најмногу 3 предмети. За таа цел, дефинирајте класа Faculty во која што ќе чувате информации
за студентите и нивните оценки во сите семестри. За класата да се имплементираат:

* Default конструктор Faculty()
* метод void addStudent(String id, int yearsOfStudies)- за додавање на студент на факултетот со индекс ID и години на студии yearsOfStudies.
* метод void addGradeToStudent(String studentId, int term, String courseName, int grade) - за додавање на оценка grade по предметот courseName
на студентот со индекс studentId во семестар term.
  * Со помош на исклучок од тип OperationNotAllowedException да се спречи додавање на повеќе од 3 оценки по семестар. Во таков случај да се испечати
  порака од формат Student [studentID] already has 3 grades in term [term]. Со истиот тип на исклучок да се спречи додавање на оценка во семестар поголем
  од 6 за тригодишни студии односно во семестар поголем од 8 за четиригодишни студии. Во овој случај да се испечати порака 
  Term [term] is not possible for student with ID [studentId].
  * Да се детектира дипломирање на студентот. Студентот дипломира тогаш кога ќе положи 18 или 24 предмети во зависност од тоа колку години студира. 
  Во моментот на дипломирање на студентот истиот треба да се избрише од евиденцијата и да се зачува лог за него во формат 
  Student with ID [studentID] graduated with average grade [averageGrade] in [yearsOfStudies] years.
  
* Метод String getFacultyLogs () - што ќе ги врати логовите за дипломираните студенти.
* Метод String getDetailedReportForStudent (String id) - метод што ќе врати детален извештај студентот со индекс id. 
Пристапот до студентот со индекс ИД да има комплексност О(1)! Деталниот извештај е во формат:
