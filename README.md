![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Laboratorio | Expresiones LOD y paneles

En esta práctica de laboratorio, continuará trabajando con el mismo libro de trabajo de Tableau de la última práctica de laboratorio (práctica de laboratorio para 6.2). Como recordatorio rápido, estaba utilizando archivos `abTesting.csv` así como archivos `case_study_ab_test.md`. Si necesita darle un vistazo más al archivo del estudio de caso, puede encontrarlo en `files_for_lab/case_study_ab_test.md`.

### Instrucciones

- En el siguiente gráfico, queremos analizar los clientes del `grupo 1` (de los grupos de edad que hicimos a partir de la columna `clnt_age`). El objetivo es encontrar y filtrar aquellos participantes cuyo saldo de cuenta sea inferior al promedio del grupo. Sigue estos pasos:

  - Cree un campo calculado con una expresión LOD como `{ FIXED [clnt_age (group)] : AVG([Bal]) }`.
  - Cree otro campo calculado para almacenar la diferencia entre el saldo promedio del grupo y el saldo del individuo como `{ FIXED [Client Age]: AVG([Bal]) } - { FIXED [Client Id]: AVG([Bal] ) }`.
  - Agregue `Client_IDs` a las filas. Filtre todos los clientes que no sean "grupo_1".
  - Agregar saldo promedio para cada cliente.
  - Ordenar los datos en orden ascendente de equilibrio.
  - Agregue el campo calculado con la expresión LOD.
  - Agregar el campo calculado con la diferencia.
  - Agregue un filtro para los valores de diferencia para seleccionar solo valores positivos (es decir, casos en los que el saldo individual es menor que el saldo promedio del grupo).

- Tienes parcelas del laboratorio anterior. Utilice esos gráficos para crear un panel interactivo para los usuarios.