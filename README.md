Pipeline CI/CD avec Jenkins, GitHub, Docker et ngrok
-
Description

Ce projet est une application Point of Sale (POS) développée avec Spring Boot, exécutée en local, et exposée sur Internet grâce à ngrok pour le test à distance.
Il inclut également un pipeline CI/CD Jenkins pour automatiser les builds et le déploiement.

Prérequis
-
Java 17

Maven

Docker Desktop (optionnel si conteneurisation)

ngrok

Jenkins (pour CI/CD)

Installation et exécution
-
1. Cloner le projet
git clone https://github.com/RACHIDOV10/first_test_jenkis.git
cd POV-JAVA

2. Lancer l’application Spring Boot localement
mvn clean package
java -jar target/PointOfSaleApplication.jar


L’application est accessible sur http://localhost:8282.
-
Screenshot CMD :
<img width="1245" height="456" alt="image" src="https://github.com/user-attachments/assets/4f43b040-ae85-4f27-8fdb-30196bfa7cb1" />
_
<img width="965" height="255" alt="Screenshot 2025-12-13 140436" src="https://github.com/user-attachments/assets/4345df83-032c-4e6c-910e-4bf4ae54c818" />

3. Exposer l’application avec ngrok
ngrok http 8282


URL publique générée : https://eura-broadish-endemically.ngrok-free.dev
-
Screenshot ngrok :
<img width="1105" height="426" alt="Screenshot 2025-12-13 135953" src="https://github.com/user-attachments/assets/1b62f365-b280-49f1-9bdd-d5ef418f3667" />
CI/CD Jenkins

Pipeline configuré pour le build et le déploiement.

Exemple de tâche :

Build Maven

Exécution des tests

Déploiement dans Docker ou test local
Architecture
Spring Boot -> Tomcat intégré -> Docker (optionnel) -> ngrok -> Accès externe
Jenkins CI/CD -> Build -> Test -> Déploiement

Auteur
-
Rachid Chaibi 

Encadré par 
-
Pr LACHGAR MOHAMED
