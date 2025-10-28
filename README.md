# Elevate-Labs-CyberSecurity-Internship-Task-6

<br>

### Task 6 : Create a Strong Password and Evaluate Its Strength<br>

<br>

### 🎯 Objective:

<p align="left">The primary objective of this project is to empirically demonstrate the relationship between password complexity (incorporating length, case, numbers, and symbols) and its resulting cryptographic strength. This involves testing various password configurations using industry-standard tools, analyzing the scores and feedback, and documenting best practices to mitigate common password attacks.</p><br>
<br>

### 🛠️ Lab Setup: <br><br>

<p align="left">To accurately check password strength, the most reliable online checkers are those that run an open-source, client-side algorithm called <strong>zxcvbn.</strong> These tools process your password locally in your browser, so your password is never sent to a server, which makes them much safer than other online options. The following are highly-rated, privacy-focused password strength checkers that use the <strong>zxcvbn algorithm.</strong></p>

#### 1. Bitwarden Password Strength Tester:
<p align="left">Bitwarden is a respected password manager known for its security and privacy standards. This tool uses <strong>zxcvbn</strong> to calculate password strength locally in your browser.<br>
  
  Official Website - https://bitwarden.com/how-secure-is-my-password/</p><br>
#### 2. How Secure Is My Password? (Security.org):
<p align="left">This tool is created by a well-known security researcher, and is one of the most widely cited and respected checkers. It runs locally and evaluates your password against common patterns and dictionary words.<br>
  
Official Website - https://www.security.org/how-secure-is-my-password/</p><br>
#### 3. RoboForm Password Checker:
<p align="left">This tool advertises its use of the robust <strong>zxcvbn</strong> estimator and checks against lists of compromised passwords from services like <strong>Have I Been Pwned (HIBP).</strong><br>
  
  Official Website - https://www.roboform.com/how-secure-is-my-password</p><br>
  <br>
### Step-1: Creating multiple passwords with varying complexity<br>
<br>
<p align="left">Use uppercase, lowercase, numbers, symbols, and length variations to create passwords of variuos complexities for testing their strength. As this is just for the testing purpose, i have selected "password" as a keyword and demonstrated how to use various combinations with just one word.</p><br>
<p align="left">Complexity Level 1: <strong>password</strong> (Lowercase, Short Length)</p>
<p align="left">Complexity Level 2: <strong>password129</strong> (Lowercase + Numbers, Medium Length)</p>
<p align="left">Complexity Level 3: <strong>p@$$vvord123</strong> (Lowercase + Numbers + Special Characters, Medium Length)</p>
<p align="left">Complexity Level 4: <strong>P@$5w0rd@129</strong> (Uppercase + Lowercase + Numbers + Special Characters, Medium Length)</p>
<p align="left">Complexity Level 5: <strong>F0rg0tmyp@5$w0rdinp@ris</strong> (Uppercase + Lowercase + Numbers + Special Characters, Long Length)</p><br>
<br>

### Step-2: Test each password on password strength checker<br>
<br>

<strong>1. Complexity Level 1: password (Lowercase, Short Length)</strong><br>

<br>  <img width="1890" height="1071" alt="Screenshot 2025-10-28 162823" src="https://github.com/user-attachments/assets/cee92616-e1e4-49a9-8fa7-051674bcd0bd" />  <br>
<br>
<br>
<br>

<strong>2. Complexity Level 2: password129 (Lowercase + Numbers, Medium Length)</strong><br>

<br>  <img width="1892" height="1081" alt="Screenshot 2025-10-28 162846" src="https://github.com/user-attachments/assets/eebf1887-4ab7-4837-9200-615220de2791" />  <br>
<br>
<br>
<br>

<strong>3. Complexity Level 3: p@$$vvord123 (Lowercase + Numbers + Special Characters, Medium Length)</strong>

<br>  <img width="1885" height="1070" alt="Screenshot 2025-10-28 175204" src="https://github.com/user-attachments/assets/2af626a3-ee3f-4ba4-a62a-871989fcd0b0" />  <br>
<br>
<br>
<br>

<strong>4. Complexity Level 4: P@$5w0rd@129 (Uppercase + Lowercase + Numbers + Special Characters, Medium Length)</strong>

<br>  <img width="1889" height="1082" alt="Screenshot 2025-10-28 163005" src="https://github.com/user-attachments/assets/b47416f8-a4ad-4af2-b067-0ac71bc28b92" />  <br>
<br>
<br>
<br>

<strong>5. Complexity Level 5: F0rg0tmyp@5$w0rdinp@ris (Uppercase + Lowercase + Numbers + Special Characters, Long Length)</strong>

<br>  <img width="1890" height="1075" alt="Screenshot 2025-10-28 162720" src="https://github.com/user-attachments/assets/b5841ad3-5287-4294-b755-ee3b77063f16" />  <br>
<br>
<br>
<br>

### Step-3: Password Strength Evaluation (Zxcvbn / Bitwarden Analysis)<br><br>

<p align="left">The following passwords were evaluated using the Zxcvbn algorithm (as implemented in tools like Bitwarden), which calculates entropy to estimate the time required for a dedicated attacker to successfully crack the password.</p>

| Complexity Level | Complexity Type |Password | Length | Character Set | Zxcvbn Score (0-4) | Estimated Crack Time (Offline Attack) | Feedback/Weakness Identified |
| :---: | :--- | :--- | :---: | :---: | :---: | :---: | :--- |
| **1** | **Very Weak** | `password` | 8 | Lowercase | 0 | **< 1 Second** | Very common dictionary word. Highly vulnerable to dictionary attacks. |
| **2** | **Weak** | `password129` | 11 | Lowercase + Numbers | 1 | **Few Seconds** | Still contains a common word ("password") followed by an easy-to-guess numeric sequence. |
| **3** | **Medium** | `p@$$vvord123` | 12 | All Types | 2 | **Few Hours/Days** | Uses common substitutions (`@` for 'a', `$$` for 's'), and contains a predictable numeric sequence (`123`). Pattern is still recognizable. |
| **4** | **Strong** | `P@$5w0rd@129` | 12 | All Types | 3 | **Months to Years** | Better mixing and more complex substitutions. Length remains moderate, which keeps the crack time below the highest level. |
| **5** | **Very Strong** | `F0rg0tmyp@5$w0rdinp@ris` | 23 | All Types (Passphrase) | 4 | **Centuries to Millennia** | The **massive increase in length (23 characters)** creates extremely high entropy, making the password statistically infeasible to crack through brute force. |
<br>
<br>
<br>



### Step-4: Identify Best Practices For Creating Strong Passwords<br>

<br>  <img width="1726" height="923" alt="Screenshot 2025-10-28 175821" src="https://github.com/user-attachments/assets/a8742543-ca3e-4f7f-99e9-404ab97bf0ee" />  <br>
<br>

The evaluation highlights the single most important factor in password security: <strong>Length (Entropy).</strong>

<p align="left">• Moving from 8 to 12 characters (Levels 1-4) yields a gain of hours to years.</p>
<p align="left">• Moving from 12 to 23 characters (Level 5) yields a gain from years to <strong>centuries/millennia</strong></p>
<br>

### <strong>Noting Down The Best Practices Learned From The Evaluation:</strong><br>

1.  <p align="left"><strong>Prioritize Length:</strong> The most critical factor is a minimum length of 12-16 characters or more. This exponentially increases the time required for a brute-force attack, shifting the crack time from seconds to millennia.</p>
2.  <p align="left"><strong>Embrace Passphrases:</strong> Instead of complex, short passwords (like P@ssword@129), use long, memorable passphrases that consist of multiple unrelated words, like a short, silly sentence (e.g., purple-stapler-rides-a-unicorn). This provides high length while being easy to recall.</p>
3.  <p align="left"><strong>Mix Character Sets:</strong> Incorporate uppercase letters, lowercase letters, numbers, and symbols to maximize the pool of available characters. While length is most important, adding these characters makes a brute-force attack computationally much more expensive.</p>
4.  <p align="left"><strong>Avoid Common Patterns:</strong> Do not use dictionary words, sequential numbers (123), keyboard patterns (qwerty), or common substitutions that are easy for hackers' tools to guess (like $ for S or 0 for O).</p>
5.  <p align="left"><strong>Unique for Every Site:</strong> Never reuse the same password. A breach on one site must not compromise another.
6.  <p align="left"><strong>Avoid Personal Context:</strong> Do not use names, birthdays, pet names, or any information easily found via social media or public records.
7.  <p align="left"><strong>Use a Password Manager:</strong> Utilize tools like Bitwarden to generate long, random, and unique passwords for all accounts, and to safely store them.
<br>
<br>
<br>

 ### Step-5: Research Common Password Attacks<br><br>

Understanding the attacker's methods highlights why defense must go beyond simple complexity rules. Modern attacks target both computational weak points and human behavior.

| Attack Type | Mechanism | Target of Attack | Primary Defense |
| :--- | :--- | :--- | :--- |
| **Brute Force** | Automated programs try every possible combination of characters until the correct one is found. | Short passwords or those with limited character sets. | **Password Length** (15+ characters). |
| **Dictionary Attack** | Programs use lists of common words, names, leaked passwords, and simple substitutions (l33t-speak) to guess rapidly. | Passwords based on common words, names, or predictable sequences. | **Unpredictability** (Passphrases of unrelated words). |
| **Credential Stuffing** | Attackers use lists of stolen username/password pairs (from previous data breaches) and automatically attempt to log in to **other sites** (exploits reuse). | Users who reuse the same password across multiple services. | **Password Uniqueness** (A different password for every account). |
| **Phishing / Social Engineering** | Attackers trick the user (via fake login pages, malicious emails, etc.) into **voluntarily submitting** their credentials. | Human trust, fear, or urgency. | **User Education** and **Multi-Factor Authentication (MFA)**. |
<br>
<br>
<br>

### Summary:

The evaluation demonstrated that complexity is less about rules (like requiring a symbol) and more about generating **entropy** to defeat automated attacks.

| Complexity Component | Impact on Password Entropy | Defense Against Guessing (Brute Force/Dictionary) | Defense Against Reuse (Credential Stuffing) |
| :--- | :--- | :--- | :--- |
| **Length (15+ Characters)** | **Exponentially Increases Entropy.** Moves crack time from days to centuries. | **CRITICAL:** Defeats Brute Force entirely. | Indirect, but provides a stronger master key. |
| **Mixed Character Types** | Adds complexity and expands the total character pool (keyspace). | **Strong:** Slows down the guessing rate. | Low. |
| **Avoiding Dictionary Words** | Ensures the password is not in any pre-computed list. | **CRITICAL:** Defeats Dictionary Attacks. | Low. |
| **Password Uniqueness** | Ensures the password is not known, even if stolen elsewhere. | N/A (Does not affect guessing time). | **CRITICAL:** Defeats Credential Stuffing. |
<br>
<br>
<br>

### Conclusion:<br><br>

<p align="left">The practical evaluation confirms a crucial shift in modern security: <strong>length and uniqueness are most important</strong>. The passphrase <strong>"F0rg0tmyp@5$w0rdinp@ris"</strong> proved vastly more secure than shorter, complex variations because its <strong>high entropy</strong> defeats modern brute-force techniques. Furthermore, in the face of widespread data breaches, using a <strong>unique password for every account</strong> is the only defense against <strong>Credential Stuffing</strong>. Ultimately, the best practice is to rely on a trusted password manager to <strong>generate and store unique, high-entropy passphrases</strong> for all services, minimizing both the human element of error and the computational vulnerability to attack.</p><br>
<br>
