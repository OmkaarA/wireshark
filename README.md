# 🕵️‍♂️ Wireshark Packet Analysis Project

This project is a hands-on exploration of network packet analysis using **Wireshark**. The objective is to develop practical skills in capturing and interpreting network traffic, identifying common protocols, and understanding how data moves across networks.

## 🧠 Objective

To build foundational skills in:
- Capturing and filtering network packets.
- Analyzing traffic patterns and common protocols.
- Gaining awareness of protocol-level data (e.g., HTTP, TCP, DNS).

## 🛠️ Steps with Screenshots

### 1. Install Wireshark  
Downloaded and installed Wireshark from the [official website](https://www.wireshark.org/).  

📷 **Screenshot:**  
<img width="1440" alt="Screenshot 2025-06-02 at 12 14 37" src="https://github.com/user-attachments/assets/8e42ea09-8235-4913-97c1-13f5c64a99d6" />

---

### 2. Start Capture  
Started capturing packets on the active network interface (e.g., Wi-Fi or Ethernet).  

📷 **Screenshot:**  
<img width="1552" alt="Screenshot 2025-06-02 at 12 16 57" src="https://github.com/user-attachments/assets/bdf46964-af2b-48bd-8ae8-20320874499e" />

---

### 3. Generate Network Traffic  
Visited [vulnweb.com](http://www.vulnweb.com) and attempted to log in to simulate HTTP traffic.  

📷 **Screenshot:**  
<img width="955" alt="Screenshot 2025-06-02 at 12 18 13" src="https://github.com/user-attachments/assets/4c7d1e50-7321-4108-9d8a-e976133fa8f9" />

---

### 4. Stop Capture  
Stopped capturing after approximately one minute to analyze the traffic.  

📷 **Screenshot:**  
<img width="862" alt="Screenshot 2025-06-02 at 11 14 55" src="https://github.com/user-attachments/assets/85cdaf37-f510-4b55-aed8-da0b39f537d5" />

---

### 5. Apply Protocol Filters  
Filtered traffic using Wireshark display filters like:
- `http`
- `tcp`
- `dns`

📷 **Screenshot:**  
<img width="1440" alt="Screenshot 2025-06-02 at 11 16 50" src="https://github.com/user-attachments/assets/a4872e7a-2c1c-4e13-b810-905e23539cd3" />
<img width="1440" alt="Screenshot 2025-06-02 at 11 52 57" src="https://github.com/user-attachments/assets/e8e0185e-26ac-448e-802f-fb2fba3441f8" />
<img width="1440" alt="Screenshot 2025-06-02 at 11 53 20" src="https://github.com/user-attachments/assets/ff12fd39-b8aa-432b-b6bc-53fbd920333a" />
<img width="1552" alt="Screenshot 2025-06-02 at 12 21 32" src="https://github.com/user-attachments/assets/95acb82a-a252-4738-a1ba-5078f0cd43f8" />

---

### 6. Identify Protocols  
During analysis, I identified multiple network protocols present in the packet capture:

- **HTTP** – used during web browsing and login attempts to vulnweb.com
- **TCP** – transport protocol supporting HTTP traffic

📝 *Note:*  
DNS traffic was not captured during this session. This may be due to:
- DNS caching on the local system
- The use of encrypted DNS (e.g., DoH or DoT)
- Capture beginning after DNS resolution had already occurred

📷 **Screenshot:**  
<img width="1552" alt="Screenshot 2025-06-02 at 12 24 39" src="https://github.com/user-attachments/assets/1d3f93d7-2e0a-4bcc-a6c5-6181358a7adf" />

---

### 7. Export as .pcap  
Exported the capture using `File > Export Specified Packets`.  

---

### 8. Analyze and Summarize Findings  
Used the filter `http.request.method == "POST"` to locate login attempts.  
Inspected packet details like source/destination IPs, headers, and data.  

📷 **Screenshot:**  
<img width="1552" alt="Screenshot 2025-06-02 at 12 39 08" src="https://github.com/user-attachments/assets/86975f54-a4fd-4e92-9730-504289fff900" />


---

## 🧩 Key Learnings

- Importance of encryption in web communications.
- How to navigate and filter packets in Wireshark.
- Common protocol behaviors and their roles in networking.

## ✅ Requirements

- Wireshark (any recent version)
- Internet connection
- A browser (used for generating traffic)

## 📬 Feedback

Feel free to open issues or pull requests if you want to contribute or discuss further!

## 🪪 License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute it with proper attribution.
