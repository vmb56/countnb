# countnb
import java.io.BufferedReader;

import java.io.FileReader;

import java.io.IOException;



public class WordCount {

    public static void main(String[] args) {

        String filePath = "path/to/your/largefile.txt"; // Remplacez par le chemin de votre fichier

        int totalWordCount = 0;



        try (BufferedReader reader = new BufferedReader(new FileReader(filePath))) {

            String line;

            while ((line = reader.readLine()) != null) {

                String[] words = line.split("\\s+"); // Séparer la ligne en mots en utilisant l'espace comme délimiteur

                totalWordCount += words.length; // Ajouter le nombre de mots dans cette ligne au total

            }

        } catch (IOException e) {

            e.printStackTrace();

        }



        System.out.println("Nombre total de mots : " + totalWordCount);

    }

}
