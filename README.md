## *Disclaimer*

*Este contenido es de caracter personal, de autoaprendizaje constante y recurrente, adicional quiero compartir con fines informativos y de aprendizaje para los demás profesionales de este sector. Es de aclarar que, los ejemplos y escenarios presentados son hipotéticos, así mismo, las plataformas utilizadas son públicas en donde pueden reflejar situaciones similares a las de las compñaías; estás plataformas cuentan con diferentes escenarios y en sus laboratorios. Las tecnologíasal igual que las herramientas utilizadas están sujetas a cambios constantes.*

# LetsDefend | Malicious AutoIT

    Rol: Security Analyst
    Dificultad: Beginner
    Escenario: Análisis de malware (identifcación)

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/Malicious-AutoIT.JPG "Lets Defend - Malicious AutoIT")


### 1. ¿Cuál es el hash MD5 del archivo de muestra? ###
	
- hash: Función matemática que transforma cualquier entrada (texto, archivo, etc.) en una cadena de caracteres de longitud fija llamada valor hash. Este valor es único e imposible de revertir.
	
- MD5: función hash criptográfica que se utiliza para generar un identificador único de un archivo en una cadena de caracteres de 128 bits (32 caracteres hexadecimales).
	
	    5e53b40cf972f4eb08990999ce17c5c8
	
	
### 2. Según la herramienta Detect It Easy (DIE), ¿Cuál es la entropía del archivo de muestra? ###
	
- Entropía de un archivo: Medida de la aleatoriedad o desorden de los datos que componen el archivo. Nos indica qué tan dispersos están los bytes que lo conforman.
	
- Importancia de la entropía:
  
	+ Detección de archivos sospechosos: Un archivo  vacío tendría una entropía muy baja, mientras que, un archivo cifrado o con datos aleatorios tendría una entropía muy alta.

	+ Análisis de malware: El análisis de la entropía puede ayudar a identificar archivos que contienen código malicioso, este a menudo puede presentar patrones de bits que se desvían de lo normal.

			6.58565

