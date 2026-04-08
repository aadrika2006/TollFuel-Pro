# 🚗 TollFuel Pro

A smart mobile application that calculates **toll charges, fuel expenses, and total trip cost** in real-time, helping users plan road trips efficiently and manage travel expenses.

## 📌 Overview

**TollFuel Pro** is a full-stack mobile application built using **Flutter (frontend)** and **Kotlin Spring Boot (backend)**. It enables users to estimate travel costs by combining toll data and fuel consumption, making it ideal for daily commuters, travelers, and fleet managers.


## ✨ Features

* 🚧 **Toll Cost Estimation** – Calculates toll charges based on distance and route
* ⛽ **Fuel Cost Calculator** – Estimates fuel expenses using mileage and fuel price
* 💰 **Total Trip Cost Breakdown** – Displays combined toll + fuel cost
* 📊 **Trip History** – Stores and retrieves previous trips
* 📱 **Cross-Platform UI** – Built with Flutter for smooth mobile experience
* ⚙️ **REST API Backend** – Kotlin Spring Boot handles business logic
* 🗄 **Database Integration** – MySQL for persistent storage

---

## 🏗 Tech Stack

### Frontend (Mobile App)

* Flutter
* Dart
* Dio (API communication)
* Material UI

### Backend (Server)

* Kotlin
* Spring Boot
* Spring Data JPA
* REST APIs

### Database

* MySQL

---

## 📂 Project Structure

```
TollFuelPro/
│
├── frontend/                # Flutter mobile application
│   └── lib/
│       ├── screens/         # UI screens (Trip screen, etc.)
│       ├── services/        # API service layer
│       ├── models/          # Data models
│       └── main.dart        # App entry point
│
├── backend/                 # Kotlin Spring Boot backend
│   └── src/main/kotlin/com/tollfuelpro/
│       ├── controller/      # REST controllers
│       ├── service/         # Business logic
│       ├── model/           # Entity classes
│       ├── repository/      # Database access layer
│       └── TollFuelProApplication.kt
│
└── database/                # Database configuration
```

---

## ⚙️ Installation & Setup

### 🔹 Prerequisites

* Flutter SDK
* Android Studio / VS Code
* Java 17+
* MySQL installed
* Gradle

---

### 🔹 Backend Setup (Kotlin Spring Boot)

1. Navigate to backend folder:

```
cd backend
```

2. Configure database in `application.properties`:

```
spring.datasource.url=jdbc:mysql://localhost:3306/tollfuel
spring.datasource.username=root
spring.datasource.password=yourpassword
```

3. Create database:

```sql
CREATE DATABASE tollfuel;
```

4. Run backend server:

```
./gradlew bootRun
```

Server runs on:

```
http://localhost:8080
```

---

### 🔹 Frontend Setup (Flutter)

1. Navigate to frontend folder:

```
cd frontend
```

2. Install dependencies:

```
flutter pub get
```

3. Run the app:

```
flutter run
```

---

## 🔌 API Endpoints

### Calculate Trip Cost

```
POST /trip/calculate
```

**Request Body:**

```json
{
  "distance": 100,
  "mileage": 20,
  "fuelPrice": 100
}
```

**Response:**

```json
{
  "fuelCost": 500,
  "tollCost": 150,
  "totalCost": 650
}
```

---

### Save Trip

```
POST /trip/save
```

---

### Get All Trips

```
GET /trip/all
```

---

## 📱 Emulator Configuration

⚠️ For Android Emulator use:

```
http://10.0.2.2:8080
```

Instead of:

```
localhost
```

---

## 🚀 Future Enhancements

* 🗺 Google Maps route integration
* 📍 Live toll detection
* 🔔 Toll alerts & notifications
* 🚗 Fleet management system
* 💳 Payment & subscription system
* 📊 Advanced analytics dashboard

---

## 🧠 How It Works

1. User enters trip details (distance, mileage, fuel price)
2. Flutter app sends request to backend API
3. Backend calculates:

   * Fuel cost = Distance / Mileage × Fuel Price
   * Toll cost = Estimated based on route
4. Response is returned and displayed in UI

---

## 📊 Use Cases

* Daily commuters
* Road trip planners
* Cab drivers
* Logistics & transport companies

---

## 🤝 Contribution

Contributions are welcome!

1. Fork the repository
2. Create a new branch
3. Make changes
4. Submit a pull request

---

## 📄 License

This project is open-source and available under the MIT License.

---

## 👩‍💻 Author

**Rika**

* Passionate about building innovative tech solutions 🚀
* Exploring Flutter, AI, and full-stack development

---

## ⭐ Support

If you like this project, give it a ⭐ on GitHub!
