# ⚡ Lightning Vaccinal Book

## 👥 Équipe G3N3S1S

- **AGBALE Bellevie** – UI/UX Designer –
- **AGBOTON Ariane** – Web Developer – https://github.com/Dona-ima
- **AHOGNISSE Ariel** – Web & Mobile Developer – https://github.com/arielcarmen
- **EDAYE DOKOUI Béni-Christ** – Front-end Developer –
- **HOUEDANOU Gildas** – Computer scientist –

---

## 📄 Executive Summary

**Lightning Vaccinal Book** It is a digital vaccination record application that allows patients to store their vaccination proofs on a secure platform. It helps health centers certify vaccinations and enables inspectors to verify them quickly using QR codes.

Our solution combats fake vaccination booklets, facilitates vaccination tracking, and strengthens health security — especially in sensitive contexts such as travel or health inspections.

---

## ❗ Identified Problem

### 🔍 The Problem

In many countries, vaccination booklets are still physical, fragile, and easily falsifiable. This undermines data reliability, complicates verification processes, and poses a barrier to health security (e.g., COVID-19, yellow fever).

> In West Africa, **1 in 3 people** is unable to present a complete or legible vaccination record.

### 👥 Target Audience

Our solution is designed for three types of users :
- **Patients** : to store their certificates without the risk of loss or damage.
- **Health centers**: to issue **authentic and tamper-proof** vaccination proofs.
- **Inspectors** (hospitals, borders, schools): to quickly verify certificates.
  
Patients need a reliable way to keep their vaccination records without risk of loss or damage. Health centers, on their part, must be able to issue authentic and tamper-proof proof of administered vaccinations. Finally, inspectors (at borders, schools, or hospitals) require a simple and fast tool to verify the authenticity of vaccination records.

Today, the loss or deterioration of vaccination records is common, especially in West Africa, where approximately one in three people cannot present a complete or well-preserved booklet. This lack of traceability leads to difficulties accessing certain health, education, or mobility services. Additionally, the proliferation of fake certificates poses a serious threat to health security, particularly during epidemics such as COVID-19 or yellow fever.

It is therefore essential to provide a digital, portable, and secure solution that allows every individual to have a reliable and easily verifiable vaccination record. It is in this context that our application offers a concrete response, adapted to local realities, by strengthening trust between patients, health centers, and authorities.

---

## ✅ Our Solution

The Lightning Vaccination Record project aims to develop a secure digital system for recording, storing, and verifying vaccination proofs. By leveraging the Lightning Network and cryptography, this system ensures the authenticity of vaccination certificates without relying on centralized infrastructure or traditional user account management.

Each individual has a secure identity based on a Lightning public key, guaranteeing confidentiality and the security of personal data. The project seeks to provide a lightweight, fast solution adapted to contexts with limited internet connectivity, especially in regions like Benin.

---

## 🧩 Key Features

### 🔐 Secure and Portable Vaccination Proof
After validation of their vaccination, the patient receives a certification that is added to their digital vaccination record. They can then generate a QR code from their record to present a tamper-proof and easily verifiable proof of vaccination.


### 📶 Vérification rapide et hors ligne
Les contrôleurs peuvent vérifier l’authenticité d’un certificat sans connexion internet, simplement en scannant le QR code. La validité est confirmée localement à partir de la signature cryptographique.


### 📅 Simple and Secure Appointment Booking
The patient creates an account and submits an appointment request by specifying :
- their national identification number
- the desired type of vaccine
- a appointment

On the day of the appointment, they confirm their identity using their national identification number shown on their **national ID card**.

---

## 🛠️ Mise en œuvre technique

### 🏗️ General Architecture

#### 🧑‍💻 Patient Side
- Mobile Application 
- Account creation on the platform
- **Fonctions** :
  - Appointment booking
  - Vaccination record consultation
  - QR Code Generation for the Record
- **Local storage** (browser) or QR code image

#### 🏥 Health Center Side
- Secure Web Interface
- **Fonctions** :
  - Reception of appointment requests
  - Approval / Rejection / Modification
  - Vaccination Recording
  - Signing proofs with a **private key**
    
#### 🕵️ Controller Side
- Mobile or Web Application
- Scan Patient QR Code
- Vérification :
  - Cryptographic Signature
  - Public key present in the whitelist
    
- **Works offline**

#### 🔗 Data exchange
- Secure messages (JSON) containing :
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

## 🧪 Technologies Used

|     Composant       |        Technology        |
|---------------------|--------------------------|
| **Frontend**        | HTML, CSS, JavaScript    |
| **Backend**         | FastAPI                  |
| **Database**        | Firestore                |
| **UI/UX Design**    | Figma                    |
| **APIs/Services**   | Lightning_pb2_grpc       |

---

## ⚙️ Ressoures

- Backend Server : https://github.com/arielcarmen/python-lnd-connect
- Frontend Server : 
- Mobile Application : https://github.com/arielcarmen/vaccination_book_app
- Mockups  : https://www.figma.com/design/dGGxc8iEpWnEztIxOaZSHq/Book-Vaccinal-Lightning?node-id=85-3&p=f&t=GL4wf0vt7T49OIJp-0
- Application (generated) : https://drive.google.com/drive/folders/15nFxgE5UjH8U1zUEkUnznjrC2Ngqa1aq (Essayez v1 ou v2 en fonction de l'architecture de votre téléphone)


---

## 📌 Licence

MIT

---

## 🤝 Contribute

Contributions are welcome! If you have suggestions, please open an **issue** or **submit a pull request**.

---

## 📬 Contact

For any questions, please contact a team member **G3N3S1S**.

