# ⚡ Lightning Vaccinal Book

## 👥 G3N3S1S Team

- **AGBALE Bellevie** – UI/UX Designer 
- **AGBOTON Ariane** – Backend Developper – https://github.com/Dona-ima
- **AHOGNISSE Ariel** –  Backend et mobile developper – https://github.com/arielcarmen
- **EDAYE DOKOUI Béni-Christ** – Frontend develpper –
- **HOUEDANOU Gildas** – Computer scientist –

---

## 📄 Executive Summary

**Lightning Vaccinal Book** It is a digital vaccination record application that allows patients to store their vaccination proofs on a secure platform. It helps health centers certify vaccinations and enables inspectors to verify them quickly using QR codes.

Our solution combats fake vaccination booklets, facilitates vaccination tracking, and strengthens health security — especially in sensitive contexts such as travel or health inspections.

---

## ❗ Identified Problem

### 🔍 Le problème

In many countries, vaccination booklets are still **physical, fragile, and easily falsifiable**. This undermines data reliability, complicates verification processes, and poses a barrier to health security (e.g., COVID-19, yellow fever).

>In West Africa, 1 in 3 people is unable to present a complete or legible vaccination record.

### 👥 Target Audience

Our solution is designed for three types of users :
- **Patients** : to store their certificates without the risk of loss or damage.
- **Health centers** :to issue **authentic and tamper-proof** vaccination proofs.
- **Controllers** (hospitals, borders, schools): to quickly verify certificate.

Patients need a reliable way to keep their vaccination records without risk of loss or damage. Health centers, on their part, must be able to issue authentic and tamper-proof proof of administered vaccinations. Finally, inspectors (at borders, schools, or hospitals) require a simple and fast tool to verify the authenticity of vaccination records.
Today, the loss or deterioration of vaccination records is common, especially in West Africa, where approximately one in three people cannot present a complete or well-preserved booklet. This lack of traceability leads to difficulties accessing certain health, education, or mobility services. Additionally, the proliferation of fake certificates poses a serious threat to health security, particularly during epidemics such as COVID-19 or yellow fever.

It is therefore essential to provide a digital, portable, and secure solution that allows every individual to have a reliable and easily verifiable vaccination record. It is in this context that our application offers a concrete response, adapted to local realities, by strengthening trust between patients, health centers, and authorities.


---

## ✅ Solution Proposée

Le projet **Carnet Vaccinal Lightning** a pour objectif de développer un système numérique sécurisé permettant d’enregistrer, conserver et vérifier les preuves de vaccination. En s’appuyant sur le réseau Lightning et la cryptographie, ce système assure l’authenticité des certificats vaccinaux sans recourir à une infrastructure centralisée ni à la gestion classique de comptes utilisateur.
Chaque individu dispose d’une identité sécurisée basée sur une clé publique Lightning, garantissant la confidentialité et la sécurité des données personnelles. Le projet vise à fournir une solution légère, rapide et adaptée aux contextes où la connectivité internet est limitée, notamment dans des régions comme le Bénin.


---

## 🧩 Fonctionnalités clés

### 🔐 Preuve de vaccination sécurisée et portable
Après validation de sa vaccination, le patient reçoit une certification qui est ajoutée à son carnet vaccinal numérique. Il peut ensuite générer un QR code à partir de son carnet pour présenter une preuve de vaccination infalsifiable et facilement vérifiable.


### 📶 Vérification rapide et hors ligne
Les contrôleurs peuvent vérifier l’authenticité d’un certificat sans connexion internet, simplement en scannant le QR code. La validité est confirmée localement à partir de la signature cryptographique.


### 📅 Prise de rendez-vous simple et sécurisée
Le patient crée un compte et soumet une demande de rendez-vous en précisant :
- son **numéro d’identification national**
- le **type de vaccin souhaité**
- une **date préférée**

Le jour du rendez-vous, il confirme son identité avec son numéro d’identification national présent sur sa **carte nationale**.

---

## 🛠️ Mise en œuvre technique

### 🏗️ Architecture générale

#### 🧑‍💻 Côté Patient
- Application Mobile 
- Création de compte sur la plateforme
- Fonctions :
  - Prise de rendez-vous
  - Consultation du carnet
  - Génération de QR code du carnet
- Stockage **local** (navigateur) ou image QR

#### 🏥 Côté Centre de santé
- Interface web sécurisée
- Fonctions :
  - Réception des demandes de rendez-vous
  - Validation / Rejet / Modification
  - Enregistrement de vaccinations
  - Signature des preuves avec **clé privée**

#### 🕵️ Côté Contrôleur
- Application mobile ou web
- Scan QR code patient
- Vérification :
  - Signature cryptographique
  - Clé publique présente dans la liste blanche
- **Fonctionne hors ligne**

#### 🔗 Échange de données
- Messages sécurisés (JSON) contenant :
  ```json
  {
    "type": "vaccine_request",
    "N° d'identification": "1245505",
    "vaccine": "COVID-19",
    "preferred_date": "2025-07-12T09:00:00",
    "timestamp": 1721000000
  }
- Signature ECDSA (secp256k1)

---

## 🧪 Technologies utilisées

| Composant         | Technologie              |
|-------------------|--------------------------|
| **Frontend**      | HTML, CSS, JavaScript    |
| **Backend**       | FastAPI                  |
| **Base de données** | Firestore             |
| **Design UI/UX**  | Figma                    |
| **APIs/Services** | Lightning_pb2_grpc       |

---

## ⚙️ Ressoures

- Serveur backend : https://github.com/arielcarmen/python-lnd-connect
- Serveur frontend : 
- Application mobile : https://github.com/arielcarmen/vaccination_book_app
- Maquettes : https://www.figma.com/design/dGGxc8iEpWnEztIxOaZSHq/Book-Vaccinal-Lightning?node-id=85-3&p=f&t=GL4wf0vt7T49OIJp-0
- Application (generated) : https://drive.google.com/drive/folders/15nFxgE5UjH8U1zUEkUnznjrC2Ngqa1aq (Essayez v1 ou v2 en fonction de l'architecture de votre téléphone)


---

## 📌 Licence

MIT

---

## 🤝 Contribuer

Les contributions sont les bienvenues ! Si vous avez des suggestions, ouvrez une _issue_ ou soumettez une _pull request_.

---

## 📬 Contact

Pour toute question, contactez un membre de l’équipe **G3N3S1S**.

