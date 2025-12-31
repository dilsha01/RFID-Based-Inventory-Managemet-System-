# RFID-Based Inventory Management System

A comprehensive inventory management system utilizing RFID technology for real-time tracking and monitoring. This full-stack application features a Spring Boot backend with MySQL database and a modern React frontend.

## 🚀 Features

- **Real-time RFID Integration**: MQTT-based communication for RFID tag detection
- **Product Management**: Add, view, edit, and track products
- **Stock Management**: Real-time stock level monitoring and updates
- **Release Tracking**: Track product releases and movements
- **Dashboard Analytics**: Visual representation of inventory data with Chart.js
- **WebSocket Support**: Real-time updates across connected clients
- **RESTful API**: Well-structured backend API endpoints

## 🏗️ Architecture

### Backend
- **Framework**: Spring Boot 3.4.1
- **Language**: Java 21
- **Database**: MySQL
- **Key Technologies**:
  - Spring Data JPA
  - Spring WebSocket
  - MQTT Integration
  - RESTful APIs

### Frontend
- **Framework**: React 18.3.1
- **Build Tool**: Vite 6.0.5
- **State Management**: Redux Toolkit
- **UI Library**: Material-UI (MUI)
- **Charts**: Chart.js with react-chartjs-2
- **Real-time**: STOMP over WebSocket

## 📋 Prerequisites

- Java Development Kit (JDK) 21 or higher
- Node.js (v16 or higher)
- MySQL Server
- Maven (included via wrapper)
- MQTT Broker (for RFID integration)

## 🛠️ Installation & Setup

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Configure the database in `src/main/resources/application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/InventRFID
   spring.datasource.username=root
   spring.datasource.password=your_password
   ```

3. Build and run the application:
   ```bash
   # Windows
   mvnw.cmd spring-boot:run
   
   # Linux/Mac
   ./mvnw spring-boot:run
   ```

   The backend will start on `http://localhost:8080`

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

   The frontend will start on `http://localhost:5173`

## 📁 Project Structure

```
├── backend/                    # Spring Boot backend
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/org/inventrfid/backend/
│   │   │   │   ├── config/           # Configuration classes
│   │   │   │   ├── controller/       # REST controllers
│   │   │   │   ├── dto/             # Data transfer objects
│   │   │   │   ├── entity/          # JPA entities
│   │   │   │   ├── exception/       # Exception handlers
│   │   │   │   ├── repository/      # Data repositories
│   │   │   │   ├── service/         # Business logic
│   │   │   │   └── util/            # MQTT utilities
│   │   │   └── resources/
│   │   │       └── application.properties
│   │   └── test/                    # Test classes
│   └── pom.xml                      # Maven dependencies
│
└── frontend/                   # React frontend
    ├── src/
    │   ├── components/              # Reusable components
    │   ├── pages/                   # Page components
    │   ├── State/                   # Redux store & actions
    │   └── assets/                  # Static assets
    ├── package.json
    └── vite.config.js

```

## 🔌 API Endpoints

### Products
- `GET /api/products` - Get all products
- `POST /api/products` - Create a new product
- `GET /api/products/{id}` - Get product by ID
- `PUT /api/products/{id}` - Update product
- `DELETE /api/products/{id}` - Delete product

### Stock
- `GET /api/stock` - Get all stock items
- `POST /api/stock` - Add stock
- `GET /api/stock/{id}` - Get stock by ID
- `PUT /api/stock/{id}` - Update stock
- `DELETE /api/stock/{id}` - Delete stock

### Release
- `GET /api/release` - Get all releases
- `POST /api/release` - Create release
- `GET /api/release/{id}` - Get release by ID

### Dashboard
- `GET /api/dashboard/summary` - Get dashboard summary statistics

## 🔧 Technologies Used

### Backend
- Spring Boot 3.4.1
- Spring Data JPA
- Spring WebSocket
- MySQL Connector
- MQTT for RFID integration
- Lombok
- Maven

### Frontend
- React 18.3.1
- Redux Toolkit for state management
- Material-UI (MUI) for UI components
- Axios for HTTP requests
- Chart.js for data visualization
- React Router for navigation
- STOMP/SockJS for WebSocket
- Vite for fast development

## 💡 Usage

1. **Start the backend server** - Ensure MySQL is running and the backend is started
2. **Start the frontend development server**
3. **Access the application** at `http://localhost:5173`
4. **Configure MQTT broker** for RFID tag detection
5. **Begin managing inventory** through the web interface

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👥 Authors

- [dilsha01](https://github.com/dilsha01)

## 🐛 Known Issues

- MQTT broker configuration needs to be set up separately
- Database credentials should be configured before running

## 📞 Support

For issues and questions, please open an issue in the GitHub repository.