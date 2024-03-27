# Etape 1: Utiliser une image de base légère
FROM openjdk:8-jdk-alpine

# Installer les dépendances nécessaires, minimisant le nombre de couches et la taille
RUN apk --no-cache add maven

# Copier les fichiers locaux nécessaires dans l'image
COPY . /usr/src/app
WORKDIR /usr/src/app

# Installer OpenCV jar dans le repo Maven local
RUN mvn install:install-file -Dfile=./lib/opencv-3410.jar \
    -DgroupId=org.opencv -DartifactId=opencv -Dversion=3.4.10 -Dpackaging=jar

# Compiler l'application
RUN mvn package

# Définir la variable d'environnement pour la bibliothèque OpenCV
ENV JAVA_OPTS="-Djava.library.path=./lib/"

# Exposer le port sur lequel l'application s'exécute
EXPOSE 8080

# Lancer l'application
CMD ["java", "-Djava.library.path=lib/", "-jar", "target/fatjar-0.0.1-SNAPSHOT.jar"]
