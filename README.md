# 🔥 Firebase JWT Token Generator

A simple, secure web-based tool to generate and manage Firebase JWT tokens for development and testing purposes. This tool provides an easy-to-use interface for Firebase authentication and JWT token generation with multiple sign-in methods.

## ✨ Features

- **🔧 Easy Firebase Configuration**: Simply paste your Firebase config JSON
- **🔐 Multiple Authentication Methods**:
  - Email/Password authentication
  - Google Sign-in
  - GitHub Sign-in
- **🎯 Automatic JWT Token Generation**: Tokens are automatically retrieved after sign-in
- **🔄 Token Refresh**: Easy token refresh functionality
- **📋 Token Decoding**: View decoded JWT claims
- **📱 Responsive Design**: Works on desktop and mobile devices
- **🔗 Direct Firebase Console Links**: Get project-specific links to Firebase settings
- **🛡️ Domain Authorization Helper**: Automatic domain detection and setup instructions

## 🚀 Quick Start

### Prerequisites

1. A Firebase project with Authentication enabled
2. Web hosting or local server to serve the HTML file

### Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/muthuishere/firebase-jwt-generator.git
   cd firebase-jwt-generator
   ```

2. **Serve the Application**
   
   **Option A: Using Python**
   ```bash
   cd public
   python3 -m http.server 8000
   ```
   
   **Option B: Using Node.js (http-server)**
   ```bash
   npx http-server public -p 8000
   ```
   
   **Option C: Using Task (if you have Taskfile.yml)**
   ```bash
   task serve
   ```

3. **Access the Application**
   Open your browser and navigate to `http://localhost:8000`

## 🔧 Firebase Configuration

### Step 1: Get Firebase Config

1. Go to [Firebase Console](https://console.firebase.google.com)
2. Select your project or create a new one
3. Navigate to Project Settings ⚙️ → General tab
4. Scroll to "Your apps" section and select your web app
5. Copy the config object from "Firebase SDK snippet"

### Step 2: Enable Authentication

1. In Firebase Console, go to Authentication → Sign-in method
2. Enable the authentication providers you want to use:
   - **Email/Password**: Enable and optionally allow email link sign-in
   - **Google**: Enable and configure OAuth consent screen
   - **GitHub**: Enable and configure GitHub OAuth app

### Step 3: Configure Authorized Domains

1. Go to Authentication → Settings
2. Scroll to "Authorized domains"
3. Add your domain (e.g., `localhost:8000` for local development)

## 📖 Usage Guide

### 1. Initialize Firebase
- Paste your Firebase configuration JSON in the text area
- Click "Initialize Firebase"
- The tool will show you direct links to configure your Firebase project

### 2. Authenticate User
- Choose your preferred authentication method:
  - **Email/Password**: Enter credentials and click "Sign In with Email"
  - **Google**: Click "Sign In with Google" for OAuth flow
  - **GitHub**: Click "Sign In with GitHub" for OAuth flow

### 3. JWT Token Management
- After successful authentication, JWT token is automatically retrieved
- View the token and its decoded claims
- Use "Refresh Token" to get a new token
- Copy token to clipboard for use in your applications

## 🛠️ Project Structure

```
firebase-jwt-creator-html/
├── public/
│   ├── index.html          # Main application file
│   └── up                  # Simple deployment script
├── config/
│   └── deploy.yml          # Deployment configuration
├── Dockerfile              # Docker configuration
├── Taskfile.yml           # Task runner configuration
├── fireweb.json           # Project metadata
├── secrets.go             # Go secrets handler
└── README.md              # This file
```

## 🔒 Security Considerations

- **Domain Authorization**: Always configure authorized domains in Firebase Console
- **Development Only**: This tool is intended for development and testing purposes
- **Token Security**: JWT tokens contain sensitive information - handle with care
- **HTTPS Recommended**: Use HTTPS in production environments
- **OAuth Configuration**: Properly configure OAuth apps for Google/GitHub sign-in

## 🚢 Deployment Options

### Docker Deployment
```bash
docker build -t firebase-jwt-generator .
docker run -p 8080:80 firebase-jwt-generator
```

### Static Hosting
The application can be deployed to any static hosting service:
- GitHub Pages
- Netlify
- Vercel
- Firebase Hosting
- AWS S3 + CloudFront

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Development Setup
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

**Muthu Kumar**
- LinkedIn: [@muthuishere](https://www.linkedin.com/in/muthuishere/)
- GitHub: [@muthuishere](https://github.com/muthuishere)

## 🆘 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/muthuishere/firebase-jwt-generator/issues) page
2. Create a new issue with detailed information
3. Connect with me on [LinkedIn](https://www.linkedin.com/in/muthuishere/)

## 🙏 Acknowledgments

- Firebase team for the excellent authentication service
- Font Awesome for the beautiful icons
- The open source community for inspiration and support

---

⭐ If you find this project helpful, please consider giving it a star on GitHub!