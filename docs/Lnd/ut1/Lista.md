
* **Párrafos**


      Este es un párrafo.


      Este es otro párrafo.




* **Encabezados (de distintos niveles).**
   


# Encabezado de nivel 1
## Encabezado de nivel 2
### Encabezado de nivel 3
#### Encabezado de nivel 4
##### Encabezado de nivel 5
###### Encabezado de nivel 6






* **Enlaces externos.**




[Musica](https://youtu.be/kRt2sRyup6A?feature=shared)








 * **Imágenes.**


![enlace de imagen](https://i.kym-cdn.com/entries/icons/facebook/000/035/976/mucho-texto.jpg)




   * **Texto en negrita.**


Este es un **Tuve fe**.




   * **Bloques o líneas de código.**


Aquí va una `línea de código`.


```
import java.util.Scanner;
import java.util.Random;
import java.io.File;
import javax.sound.sampled.AudioSystem;
import javax.sound.sampled.Clip;
import javax.sound.sampled.AudioInputStream;


public class BromaNumeroConMusica {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();
        int numeroSecreto = random.nextInt(100) + 1;
        int adivinanza = 0;


        System.out.println("¡Bienvenido al juego de adivinar el número!");
        System.out.println("Debes adivinar un número entre 1 y 100");


        while (adivinanza != numeroSecreto) {
            System.out.print("Introduce tu adivinanza: ");
            adivinanza = scanner.nextInt();


            if (adivinanza > numeroSecreto) {
                System.out.println("El número es menor... ñomp ñomp.");
                reproducirMusica("rickroll.wav");
            } else if (adivinanza < numeroSecreto) {
                System.out.println("El número es mayor... ñomp ñomp.");
                reproducirMusica("rickroll.wav");
            } else {
                System.out.println("¡Felicidades! Adivinaste el número.");
            }
        }


        scanner.close();
    }


    // Método para reproducir un archivo WAV
    public static void reproducirMusica(String rutaArchivo) {
        try {
            File archivo = new File(rutaArchivo);
            AudioInputStream audioStream = AudioSystem.getAudioInputStream(archivo);
            Clip clip = AudioSystem.getClip();
            clip.open(audioStream);
            clip.start();


            // Espera a que termine de sonar la música
            Thread.sleep(5000); // Pausa durante 5 segundos


            clip.close();
        } catch (Exception e) {
            System.out.println("Error al reproducir la música: " + e.getMessage());
        }
    }
}


```


*  **Listas.**
 


  Lista de Supermercado
1. Agua
2. Bolsa de basura
3. Carne
4. Arroz
5. Shampoo
6. Jabón




*  Una tabla.
 


| Peliculas Favoritas | Peliculas no favoritas |
|--------------|--------------|
| A Toda Gas | Cerdita |
| Cars | Aquaman |
|Resacón en las vegas|Bitelchus|




* **Enlace que permita acceder a otro documento.**


[volver al inicio](ut1_a2.md)





