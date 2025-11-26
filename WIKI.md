
# Welcome to the MidnightAviator196.github.io Wiki

## 📖 Table of Contents
- [Home](#home)
- [Features](#features)
- [Pages Overview](#pages-overview)
- [Getting Started](#getting-started)
- [Security Features](#security-features)
- [Technical Details](#technical-details)

---

## 🏠 Home

This is a simple static website project featuring multiple interactive pages built with HTML, CSS, and JavaScript. The website includes a home page, a real-time California clock, and a password-protected secret page.

---

## ✨ Features

- **Responsive Design** - Works on desktop and mobile devices
- **Real-time Clock** - Displays current California (PST/PDT) time
- **Password Protection** - Secure page with authentication
- **Rate Limiting** - Protection against brute-force attacks
- **Modern UI** - Clean and professional styling with Tailwind CSS

---

## 📄 Pages Overview

### 1. Home Page (`index.html`)
The main landing page of the website.

**Features:**
- Welcome message
- Navigation links to all pages
- External links to Google and Python.org
- Clickable Python logo that reloads the page

**Styling:**
- Red heading for the welcome message
- Blue heading for "Hello World"

---

### 2. California Time (`california_time.html`)
A real-time clock displaying the current time in California (America/Los_Angeles timezone).

**Features:**
- Live updating time (updates every second)
- Displays both time and full date
- 12-hour format with AM/PM
- Day of the week included
- Return button to navigate back to home

**Technology Used:**
- Tailwind CSS for modern styling
- JavaScript `Intl.DateTimeFormat` API for timezone handling
- Responsive design with mobile support

**Time Format:**
- Time: `HH:MM:SS AM/PM`
- Date: `Weekday, Month Day, Year`

---

### 3. Secret Page (`secreat.html`)
A password-protected page with advanced security features.

**Default Password:** `hello_world`

**Security Features:**
1. **Password Protection** - Required to view content
2. **Rate Limiting** - Maximum 5 login attempts
3. **Account Lockout** - 30-second lockout after 5 failed attempts
4. **Constant-time Comparison** - Protection against timing attacks
5. **Session Management** - Stay logged in during browser session
6. **Visual Password Toggle** - Eye icon to show/hide password

**Features After Login:**
- Welcome message
- Company logos (Google, Apple)
- Return button to home page
- Logout button to clear session

**Session Storage:**
- Authentication state persists during browser session
- Login attempts tracked to prevent brute force
- Automatic lockout timer management

---

## 🚀 Getting Started

### Running Locally on Replit

1. **Clone or Fork the Repository**
   ```
   Fork this Repl to your account
   ```

2. **Click the Run Button**
   - The Run button will start a Python HTTP server on port 5000

3. **View Your Website**
   - The webview will automatically open
   - Navigate to different pages using the links

### File Structure
```
.
├── index.html              # Home page
├── california_time.html    # California time clock
├── secreat.html           # Password-protected page
├── README.md              # Project readme
└── .replit                # Replit configuration
```

---

## 🔒 Security Features

### Password Protection System

The secret page implements multiple security layers:

#### 1. Rate Limiting
- Tracks login attempts using `sessionStorage`
- Maximum 5 attempts allowed
- Counter resets on successful login

#### 2. Account Lockout
- Triggered after 5 failed attempts
- 30-second lockout period
- Input field disabled during lockout
- Countdown timer displayed

#### 3. Constant-Time Comparison
```javascript
function constantTimeCompare(a, b) {
    if (a.length !== b.length) return false;
    let result = 0;
    for (let i = 0; i < a.length; i++) {
        result |= a.charCodeAt(i) ^ b.charCodeAt(i);
    }
    return result === 0;
}
```
This prevents timing attacks by ensuring password comparison takes the same time regardless of where the mismatch occurs.

#### 4. Session Management
- Authentication state stored in `sessionStorage`
- Persists across page navigation
- Cleared on logout or browser close

---

## 🛠️ Technical Details

### Technologies Used
- **HTML5** - Page structure and semantics
- **CSS3** - Styling and layout (including Tailwind CSS)
- **JavaScript (ES6+)** - Interactivity and logic
- **Python HTTP Server** - Development server

### Browser Compatibility
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile responsive design
- JavaScript required for interactive features

### Time Zone Handling
The California time page uses the JavaScript Internationalization API:
```javascript
const timeOptions = {
    hour: '2-digit', 
    minute: '2-digit', 
    second: '2-digit', 
    hour12: true, 
    timeZone: 'America/Los_Angeles'
};
```

### Server Configuration
The application runs on a Python HTTP server:
```bash
python3 -m http.server 5000 --bind 0.0.0.0
```

**Port Configuration:**
- Development: Port 5000
- Production: Forwarded to ports 80/443

---

## 📝 Credits

- **California Time Page** - Created with assistance from Gemini
- **Design** - Custom CSS and Tailwind CSS
- **Icons & Logos** - Google, Apple, Python logos from official sources

---

## 🤝 Contributing

This is a personal project, but feel free to fork and customize for your own use!

---

## 📜 License

This project is open source and available for educational purposes.

---

## 📞 Support

For questions or issues, please use the GitHub Issues page or contact the repository owner.

---

*Last Updated: November 2025*
