1. Nombre del instituto.  
/ies/nombre/text()

2. Página web del instituto. 
/ies/web/text()

3. Nombre de los ciclos formativos. 
/ies/ciclos/ciclo/nombre/text()

4. Siglas por las que se conocen los ciclos formativos.
/ies/ciclos/ciclo/@id 

5. Años en los que se publicaron los decretos de título de los ciclos formativos.
/ies/ciclos/ciclo/decretoTitulo/@año

6. Ciclos formativos de Grado Medio (se trata de obtener el elemento completo).
/ies/ciclos/ciclo[grado = 'Medio']

7. Nombre de los ciclos formativos de Grado Superior.
/ies/ciclos/ciclo[grado/text()='Superior']/nombre

8. Nombre de los ciclos formativos anteriores a 2010.
//ciclos/ciclo[decretoTitulo[@año < 2010]]/nombre

9. Nombre de los ciclos formativos de 2008 o 2010.
//ciclos/ciclo[decretoTitulo[@año = 2008]or(decretoTitulo[@año = 2010])]/nombre
