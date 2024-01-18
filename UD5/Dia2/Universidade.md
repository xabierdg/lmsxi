1. Nombre de la universidad.

/universidad/nombre

2. Pais de la universidad.

/universidad/pais

3. Nombres de las carreras.

/universidad/carreras/carrera/nombre

4. Años de plan de estudio de las carreras.

/universidad/carreras/carrera/plan/text()

5. Nombres de todos los alumnos.

/universidad/alumnos/alumno/nombre

6. Identificadores de todas las carreras.

/universidad/carreras/carrera/@id

7. Datos de la carrera cuyo id es c01.

/universidad/carreras/carrera[@id='c01']

8. Centro en que se estudia de la carrera cuyo id es c02.

/universidad/carreras/carrera[@id='c02']/centro

9. Nombre de las carreras que tengan subdirector.

/universidad/carreras/carrera[subdirector]/nombre

10. Nombre de los alumnos que estén haciendo proyecto.

//alumnos/alumno[estudios/proyecto]/nombre

11. Códigos de las carreras en las que hay algún alumno matriculado.

//alumnos/alumno/estudios/carrera/@codigo

12. Apellidos y nombre de los alumnos con beca.

//alumnos/alumno[@beca='si']/apellido1 | //alumnos/alumno[@beca='si']/apellido2 | //alumnos/alumno[@beca='si']/nombre

13. Nombre de las asignaturas de la titulación c04.

/universidad/asignaturas/asignatura[@titulacion='c04']/nombre

14. Nombre de las asignaturas de segundo trimestre.

//asignaturas/asignatura[trimestre/text()=2]/nombre

15. Nombre de las asignaturas que no tienen 4 créditos teóricos.

//asignaturas/asignatura[creditos_teoricos/text()!=4]/nombre

16. Código de la carrera que estudia el último alumno.

//alumno[last()]/estudios/carrera/@codigo

17. Código de las asignaturas que estudian mujeres.

//alumno[sexo='Mujer']/estudios/carrera/@codigo

18. Nombre de los alumnos que están matriculados en la asignatura a02.

//alumno[estudios/asignaturas/asignatura[@codigo='a02']]/nombre

19. Códigos de las carreras que estudian los alumnos matriculados en alguna asignatura.

//alumno/estudios[asignaturas/asignatura]/carrera/@codigo

20. Apellidos de todos los hombres.

//alumno[sexo='Hombre']/apellido1/text() | //alumno[sexo='Hombre']/apellido2/text()


