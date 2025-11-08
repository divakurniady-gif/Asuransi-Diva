### 🧮 Asuransi Diva

A modern web application designed to make **life insurance calculations** faster, smarter, and more interactive.  

With **Asuransi Diva**, you can perform **premium and reserve calculations** for:  
- **Last Survivor (Clayton Copula)**  
- **Single Life**  

Built with precision and simplicity in mind, the platform combines **Flask (Python)** for backend logic, **SQL** for data management, and **HTML** powered by **Tailwind CSS** for a clean, responsive experience.  

Every feature is crafted to make actuarial computations feel seamless — from input to visualization, from theory to result.  


🌐 **Live demo:** [https://divakurniady.pythonanywhere.com/](https://divakurniady.pythonanywhere.com/)

---

## 🧩 Features

- 🔐 **User Authentication** – Register, login, logout  
- 📊 **Premium & Reserve Calculation**  
  - Life Insurance Premium & Reserve (Last Survivor – Clayton Copula)  
  - Life Insurance Premium & Reserve (Single Life)  
- 🧮 **Dashboard** – View, search, filter, edit, and delete calculation results  
- 📁 **Export to CSV** – Download filtered or complete datasets  
- 👤 **Guest Mode** – Try the app without logging in  
- 💡 **Responsive Interface** – Built with Tailwind CSS  

---
---

## 🧮 Calculation Theory 


**Single Life**  
<p align="center">
  <img src="Assets/Single Life.jpg" alt="Single Life" width="250"  height="300">
</p>


**Last Survivor**  
<p align="center">
  <img src="Assets/Last Survivor.jpg" alt="Last Survivor" width="250"  height="300">
</p>


> Data source: Indonesian Mortality Table 2023.

## ⚙️ Tech Stack

| Layer | Technology |
|:------|:------------|
| **Frontend** | HTML, Tailwind CSS |
| **Backend** | Flask (Python) |
| **Database** | MySQL |
| **Deployment** | PythonAnywhere |

---

## 🧠 Libraries

| Library | Description |
|----------|-------------|
| **Flask** | Web framework for building the app interface and backend logic. |
| **mysql-connector-python** | Connects Flask with MySQL database. |
| **Werkzeug** | Handles secure password hashing. |
| **pandas** | Data processing for mortality table and dashboard. |
| **NumPy** | Numerical and actuarial calculations. |
| **SciPy** | Provides statistical tools for Clayton models. |

---

## 🏗️ System Architecture

The **Asuransi Diva** system follows a clean, modular architecture that connects users, computation logic, and data storage into one seamless process.

### 🔄 Flow Overview

1. **User Interaction (Frontend Layer)**  
   - Users access the app via a browser interface built with **HTML** and **Tailwind CSS**.  
   - They can register, log in, or use the app as a guest.  
   - Through input forms, users provide data such as name, age, location, benefit, duration, and interest rate.

2. **Flask Routing & Logic (Application Layer)**  
   - Flask handles all routes (e.g., `/login`, `/dashboard`, `/hitung`) and user sessions.  
   - Once a user submits data, Flask receives the inputs via POST requests and processes them using Python logic.  
   - The actuarial engine (built with **NumPy**, **Pandas**, and **SciPy**) performs computations for:
     - **Last Survivor (Clayton Copula)**  
     - **Single Life**  
   - The results include **premiums** and **reserves table** that are dynamically rendered in HTML templates.

3. **Database Management (Data Layer)**  
   - **MySQL** stores user credentials and calculation history.  
   - Data is managed through `mysql-connector-python`, allowing Flask to perform:
     - Insert (save new records)  
     - Read (display on dashboard)  
     - Update (edit existing data)  
     - Delete (remove entries)

4. **Visualization & Export**  
   - Results are displayed in the web interface with tables generated via Jinja templates.  
   - Users can **filter, search, and export** selected data to `.csv` files for further analysis.

### 🧭 End-to-End Flow Summary

**User → Flask (Python) → Actuarial Computation (NumPy, SciPy, Pandas) → MySQL Database → Dashboard / Export Output**

This structure ensures that every calculation—from input to visualization—remains transparent, accurate, and reproducible.

---

## 🖼️ Preview


<table>
  <tr>
    <td><img src="https://github.com/divakurniady-gif/Asuransi-Diva/blob/main/Assets/web.jpg" width="640" height="221"></td>
    <td><img src="https://github.com/divakurniady-gif/Asuransi-Diva/blob/main/Assets/web1.jpg" width="640" height="221"></td>
  </tr>
  <tr>
    <td><img src="https://github.com/divakurniady-gif/Asuransi-Diva/blob/main/Assets/web2.jpg" width="640" height="221"></td>
    <td><img src="https://github.com/divakurniady-gif/Asuransi-Diva/blob/main/Assets/web3.jpg" width="640" height="221"></td>
  </tr>
  <tr>
    <td><img src="https://github.com/divakurniady-gif/Asuransi-Diva/blob/main/Assets/web4.jpg" width="640" height="221"></td>
    <td><img src="https://github.com/divakurniady-gif/Asuransi-Diva/blob/main/Assets/web5.jpg" width="640" height="221"></td>
  </tr>
  <tr>
    <td><img src="https://github.com/divakurniady-gif/Asuransi-Diva/blob/main/Assets/web6.jpg" width="640" height="221"></td>
    <td><img src="https://github.com/divakurniady-gif/Asuransi-Diva/blob/main/Assets/web7.jpg" width="640" height="221"></td>
  </tr>
</table>


## 📝 Notes and Limitations

- This is a **personal learning project**, not a production-ready app.
- Copula model parameters are estimated based on 1,000 simulated random pairs using the Gompertz distribution approach, derived from the 2023 Indonesian Mortality Table. 
- Interest rate is assumed constant throughout the contract period.
- Results may vary slightly depending on the mortality table and actuarial assumptions used.

---

## 📬 Contact

If you have any suggestions, feedback, or ideas for improvement, feel free to reach me at:  
📧 **divakurniady@gmail.com**

Thank you. Step by step, I want to keep learning, building, and growing.
