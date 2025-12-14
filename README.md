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
<img width="897" height="232" alt="Screenshot 2025-12-14 215014" src="https://github.com/user-attachments/assets/d0f259c5-f3a3-4cdf-8828-4cbd5fe963de" />

3. Exposer l’application avec ngrok
ngrok http 8282


URL publique générée : https://eura-broadish-endemically.ngrok-free.dev
-
Screenshot ngrok :
<img width="1099" height="552" alt="image" src="https://github.com/user-attachments/assets/9ef18d26-a97b-4b9a-bfa8-7d554f0c4199" />

CI/CD Jenkins

Pipeline configuré pour le build et le déploiement.

Exemple de tâche :

Build Maven

Exécution des tests
<img width="1057" height="323" alt="Screenshot 2025-12-14 214921" src="https://github.com/user-attachments/assets/fa57f7c7-15d7-4062-9967-ff7d77a6b776" />

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
