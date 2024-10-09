## *Disclaimer*

*Este contenido es de caracter personal, de autoaprendizaje constante y recurrente. Por consiguiente, quiero compartir con fines informativos y de ayuda  para los demás profesionales del sector. Cabe aclarar que los ejemplos y escenarios presentados son hipotéticos, las plataformas utilizadas son públicas y pueden reflejar situaciones similares a las de algunas compñaías, estás plataformas cuentan con diferentes escenarios y laboratorios. Así mismo, Las tecnologías al igual que las herramientas utilizadas están sujetas a cambios constantes.*

# LetsDefend | Malicious AutoIT

    Rol: Security Analyst
    Dificultad: Beginner
    Escenario: Análisis de malware (identifcación)

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/Malicious-AutoIT.JPG "Lets Defend - Malicious AutoIT")

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/openChallenge.jpg "Open Challenge")

### 1. ¿Cuál es el hash MD5 del archivo de muestra? ###
	
- hash: Función matemática que transforma cualquier entrada (texto, archivo, etc.) en una cadena de caracteres de longitud fija llamada valor hash. Este valor es único e imposible de revertir.
	
- MD5: función hash criptográfica que se utiliza para generar un identificador único de un archivo en una cadena de caracteres de 128 bits (32 caracteres hexadecimales).

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/1-hashMD5.jpg "Hash: MD5")

	5e53b40cf972f4eb08990999ce17c5c8
	
	
### 2. Según la herramienta Detect It Easy (DIE), ¿Cuál es la entropía del archivo de muestra? ###
	
- Entropía de un archivo: Medida de la aleatoriedad o desorden de los datos que componen el archivo. Nos indica qué tan dispersos están los bytes que lo conforman.
	
- Importancia de la entropía:
  
	+ Detección de archivos sospechosos: Un archivo  vacío tendría una entropía muy baja, mientras que, un archivo cifrado o con datos aleatorios tendría una entropía muy alta.

	+ Análisis de malware: El análisis de la entropía puede ayudar a identificar archivos que contienen código malicioso, este a menudo puede presentar patrones de bits que se desvían de lo normal.

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/2-entropy.jpg "Entropy")

	6.58565


### 3. Según la herramienta Detect It Easy(DIE), ¿Cuál es la dirección virtual de la sección «.text»? ###

Formato de respuesta: 0x0000
	
- Dirección virtual: Es un número que un programa utiliza para referirse a una ubicación dentro de la memoria, pero no su ubicación física.

- Sección «.text»: Este es el cerebro del programa, aquí reside el código que le indica al ordenador qué hacer.

- ¿Qué es este formato 0x0000?: Notación hexadecimal. Es la forma de representar números en base 16.

	+ 0x: Indica que el número siguiente está en formato hexadecimal (HEX).
 
 	+ 0000: Cuatro dígitos hexadecimales que puede tomar valores del 0 al 9 y de la A a la F.

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/3-virtualAddress.jpg "Virtual Address")

	0x1000


### 4. Según la herramienta Detect Easy, ¿Cuál es el "time date stamp"? ###
	
- Time Date Stamp(sello de fecha y hora): Es la marca de tiempo que indica la última vez que se creó, modificó o se accedió al archivo.

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/4-timeDateStamp.jpg "Time Date Stamp")

	2020-02-26 21:41:13


### 5. Según la herramienta Detect It Easy (DIE), ¿Cuál es la dirección del punto de entrada del ejecutable? ###
Formato de respuesta: 0x000000
	
- Entry Point (dirección del punto de entrada): Es el lugar exacto en el código donde comienza la ejecución del programa cuando se inicia. Es representado en hexadecimal (HEX) debido a que indica la ubicación exacta de la primera instrucción del programa en memoria.

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/5-entryPoint.jpg "Entry Point")
	
	0x42800a


### 6. ¿Cuál es el dominio utilizado por el código malicioso incrustado? ###

Para el ejercicio se puede traer de varias formas, mostraremos 2 de ellas.

- VirusTotal: Buscando el HASH MD5 del archivo.

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/6-1-domain.jpg "VirusTotal")

- AutoIT Ripper: Es un Script en python

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/6-2-domain.jpg "AutoIT Ripper")
	
	office-cleaner-commander.com

	
7. ¿Cuál es la ruta del archivo codificada en hexadecimal en el código malicioso?

Utilizando el mismo SCRIPT del punto anterior, logramos ver en la fila XX la cadena "XXXXXXX" con el valor "0x3A5C57696E646F77735C53797374656D33325C". Aquí podemos utilizar cualquier sitio web que convierta hexadecimal (HEX) a texto (TEXT).

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/7-nameHEX.jpg "Name HEX")

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/7-nameTEXT.jpg "Name TEXT")

	:\Windows\System32\
	

8. ¿Cuál es el nombre de la DLL invocada por el código malicioso?

Que es una DLL: Es un tipo especial de archivo que contiene código y datos que pueden ser utilizados por múltiples programas al mismo tiempo.

![image](https://github.com/jccerquera/LetsDef-Beg_MaliciousAutoIT/blob/main/img/8-dllCall.jpg "DLL Name")

	user32.dll


# Herramientas Utilizadas

- Detect IT Easy (DIE) (https://github.com/horsicq/Detect-It-Easy)

- VirusTotal (https://www.virustotal.com/)

- AutoIT Easy (https://github.com/nazywam/AutoIt-Ripper)

- CyberChef (https://gchq.github.io/CyberChef/) [Se puede buscar cualquier herramienta que convierta desde HEX a TEXT]
