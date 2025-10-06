# Reflected XSS Attack Walkthrough 🚨

This repository demonstrates a **Reflected Cross-Site Scripting (XSS)** attack using DVWA in a controlled lab environment.  
The walkthrough includes **step-by-step screenshots**, payloads, and results under different DVWA security levels (Low, Medium, High).  

---

## 📸 Screenshots & Steps

### 1. DVWA Welcome Page

![DVWA Welcome Page](screenshots/Welcome%20page%20.png)

### 2. Setting Security to Low

![Set Security Low](screenshots/Security%20Low.png)

### 3. Click upon the Reflected XSS

![click on reflected xss](screenshots/Click%20Reflected%20XSS.png)

### 4. Normal Input (Your Name)

![Type your name](screenshots/type%20your%20name%20and%20hit%20enter.png)

### 5. HTML Injection Payload
Payload: html
<h1>Srichandan</h1>

![Html code](screenshots/html%20heading%20tag.png)

### 6.Inject Pop-up JavaScript Alert
Payload:<script>alert("hello")</script>

![Java Script code](screenshots/enter%20pop%20up%20java%20script%20code.png)

### 7.Popup Result (Low Security)

![popup result](screenshots/pop%20up%20result.png)

### 8.Stealing Cookies(Low Security)
Payload:<script>alert(document.cookie)</script>

![cookie](screenshots/stealing%20cookie%20.png)

### 9.Cookie / Session ID Disclosure(Low Security)

![session id](screenshots/Look%20at%20the%20Session%20.png)

### 10.Switching Security to Medium

![medium security](screenshots/security%20Medium.png)

### 11.Basic Pop-up Payload Test
Payload:<script>alert("hello")</script>

![basic payload test](screenshots/pop%20up%20js%20code%20while%20security%20medium.png)

### 12.Bypassing Script Filters
Payload:<scr<script>ipt>alert("hello")</script>

![bypasstest](screenshots/to%20by%20pass%20this%20add%20extra%20script%20tag.png)

### 13.Popup Result (Medium Security)

![popup result](screenshots/pop%20up%20result.png)

### 14.Stealing Cookies(Medium Security)
Payload:<script>alert(document.cookie)</script>

![popup result](screenshots/Screenshot%202025-10-06%20103659.png)

### 15.Stealing Cookies Method(Medium Security)
Payload:<scr<script>ipt>alert(document.cookie)</script>

![popup result](screenshots/Look%20at%20the%20Session%20.png)

### 16.Switching Security to High

![high security](screenshots/security%20High.png)

### 17.Testing Payload
Payload:<script>alert("hello")</script>

![high security](screenshots/Formal%20hello%20with%20high%20security.png)

### 18.Reviewing Source Code

![Source Code](screenshots/Source%20code%20review%20of%20high%20security.png)

### 19.Using HTML Event Handler
Payload:<img src=x OnMouseOver=alert("hello")>

![image clicking](screenshots/click%20on%20the%20image%20beside%20hello%20then%20see%20the%20result.png)

### 20.Hover Result

![hovering result](screenshots/result%20of%20hovering%20.png)


🎯 Key Learnings

Low Security: Direct payload execution without filters.

Medium Security: Script tags partially blocked → bypass possible using obfuscation.

High Security: Stronger sanitization, but still exploitable via event handlers.

🛡️ Mitigation

Use proper output encoding (HTML, JavaScript, attributes).

Employ input validation and allowlists.

Implement Content Security Policy (CSP).

Disable inline JavaScript (on* events, <script>).


⚠️ Disclaimer

This project is for educational and research purposes only.
Do not attempt these attacks outside a controlled lab environment.


## Author
👤 **Aditya Srichandan**  
- 💼 Aspiring SOC Analyst | Cybersecurity Enthusiast  
- 🌐 [LinkedIn](https://www.linkedin.com/in/aditya-srichandan/)  
- 📂 [GitHub](https://github.com/Adi-CUTM/Adi-CUTM)  