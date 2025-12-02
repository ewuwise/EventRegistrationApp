# **Event Registration App**

A React Native application for event registration with form validation and confirmation screen.

![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Expo](https://img.shields.io/badge/Expo-1B1F23?style=for-the-badge&logo=expo&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## 📱 Preview

<div align="center">
  <img src="https://via.placeholder.com/300x600/4A90E2/FFFFFF?text=Registration+Form" width="200" alt="Registration Form">
  <img src="https://via.placeholder.com/300x600/4CAF50/FFFFFF?text=Confirmation+Screen" width="200" alt="Confirmation Screen">
</div>

## ✨ Features

- **📝 User Registration Form**
  - Name input field with validation
  - Email input with format validation
  - Phone number input with digit validation
  - Event selection dropdown (Conference, Workshop, Webinar, etc.)

- **✅ Smart Validation**
  - Real-time form validation
  - Error messages for invalid inputs
  - Required field checking
  - Email format validation using regex
  - Phone number validation (minimum 10 digits)

- **🎯 Confirmation Screen**
  - Dynamic display of user registration details
  - Success message upon registration
  - Option to return to registration form

- **🎨 Modern UI/UX**
  - Beautiful background images with blur effects
  - Card-based design with shadows
  - Responsive layout for all screen sizes
  - Smooth transitions between screens

- **⚡ Performance & Quality**
  - State management with React Hooks
  - Conditional rendering for optimal performance
  - Test IDs for automated testing
  - Clean, maintainable code structure

## 🚀 Quick Start

### Prerequisites
- Node.js (v14 or later)
- npm or yarn
- Expo CLI (optional)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/ewuwise/EventRegistrationApp.git
cd EventRegistrationApp
```

2. **Install dependencies**
```bash
npm install
# or
yarn install
```

3. **Run the application**

For web:
```bash
npm run web
```

For Android:
```bash
npm run android
```

For iOS:
```bash
npm run ios
```

## 📁 Project Structure

```
EventRegistrationApp/
├── App.js                 # Main application component
├── RegistrationForm.js    # Registration form component
├── Confirmation.js       # Confirmation screen component
├── package.json          # Dependencies and scripts
├── README.md             # Project documentation
└── .gitignore           # Git ignore file
```

## 🧩 Components

### App.js
The main component that manages the application state and handles toggling between the registration form and confirmation screen.

### RegistrationForm.js
Contains the form with:
- TextInput fields for name, email, and phone
- Picker dropdown for event selection
- Form validation logic
- Submit button with validation

### Confirmation.js
Displays the confirmation screen with:
- User registration details
- Success message
- Back button to return to registration

## 🔧 Technical Details

### State Management
```javascript
// Example state management
const [registrationDetails, setRegistrationDetails] = useState(null);
const [name, setName] = useState('');
const [email, setEmail] = useState('');
const [phone, setPhone] = useState('');
const [event, setEvent] = useState('Select an event');
```

### Form Validation
```javascript
// Email validation
const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

// Phone validation
const phoneRegex = /^[0-9]{10,}$/;

// Required fields check
if (!name || !email || !phone || event === 'Select an event') {
  Alert.alert('Error', 'Please fill in all fields.');
}
```

### Conditional Rendering
```javascript
{registrationDetails ? (
  <Confirmation details={registrationDetails} onBack={handleBack} />
) : (
  <RegistrationForm onConfirm={handleConfirm} />
)}
```

## 🧪 Testing IDs

The application includes test IDs for automated testing:

| Test ID | Component | Purpose |
|---------|-----------|---------|
| `formName` | Name field container | Testing name input |
| `formEmail` | Email field container | Testing email input |
| `formPhone` | Phone field container | Testing phone input |
| `formPicker` | Event picker container | Testing dropdown selection |
| `registrationFormDetails` | Form container | Testing form layout |
| `confirmationDetails` | Confirmation container | Testing confirmation screen |
| `confirmText` | Confirmation text | Testing confirmation message |
| `registerButton` | Register button | Testing form submission |
| `backButton` | Back button | Testing navigation back |

## 📋 Dependencies

```json
{
  "react": "18.2.0",
  "react-native": "0.72.6",
  "expo": "~49.0.0",
  "@react-native-picker/picker": "2.4.8",
  "react-native-web": "~0.19.6"
}
```

## 🎯 Learning Objectives

This project demonstrates:
1. **Form handling** in React Native with TextInput and Picker
2. **State management** using React useState hooks
3. **Form validation** with error handling
4. **Conditional rendering** between components
5. **Event handling** for form submission
6. **Dynamic data display** in confirmation screens
7. **UI/UX best practices** with responsive design

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Ewu Wise**
- GitHub: [@ewuwise](https://github.com/ewuwise)
- Project Link: [https://github.com/ewuwise/EventRegistrationApp](https://github.com/ewuwise/EventRegistrationApp)

## 🙏 Acknowledgments

- React Native community for excellent documentation
- Expo team for making React Native development easier
- Unsplash for beautiful background images

---

<div align="center">
  
### ⭐️ Support the Project
  
If you found this project helpful, please give it a star!
  
[![Star History Chart](https://api.star-history.com/svg?repos=ewuwise/EventRegistrationApp&type=Date)](https://star-history.com/#ewuwise/EventRegistrationApp&Date)

</div>

---

**Happy Coding! 🚀**
