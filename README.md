# Seguridad_Social2
Segunda parte del programa de simulación de pensiones,añadiendo complementos por bajas rentas e invalidez y subiendo datos a una base mysql
Añadí un nuevos campo booleano llamado invalidez, para el número de identificación utilizé un código hash para que fuese único y poder simular el DNI correctamente.También creé otra tabla con los mismos números de identificación y las rentas del año anterior.Para todos los pensionistas que tengan la invalidez a true se le añaden 300 euros a su pensión
## Power Bi
Cargamos los csvs datos_jubilacion_calculados y rentas_jubilados en Power Bi.Una vez ahí limpiamos los datos,hacemos el modelado y creamos la columna Pensión final con completos con código DAX, los pensionistas con menos de 1000 euros y rentas menores de 5000 euros el año anterior pasan a cobrar 1000 euros y una vez procesado si les corresponde o no se pasa a procesar si tienen o no invalidez y se añaden 300 euros a todos los pensionistas que la tengan.Por ejemplo si tu pensión es de 600 y tienes 3000 euros de renta automásticamente pasas a 1000 y si tienes invalidez a 1300
## Carga de datos
Una vez tengamos todo el proceso de tratamiento de datos hecho en el power bi, copiamos la tabla y la pegamos a un excel vacío llamado TablaPensionistasParaMsql y lo cargamos en una tabla llamada datos en una base de datos llamada pensionisstas
