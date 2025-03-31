# 📊 Function Intersection Finder  
Finding the intersection of **y = exp(-x)** and **y = sin(x)** using Python  

## 📝 Description  
Mathematical equations often have points where two functions intersect. Finding these intersection points is crucial in various fields like **physics, engineering, and data science**.  

This project numerically finds and visualizes the intersection of two functions:  

✅ **Exponential decay function**:  y = e^{-x}   
✅ **Sine function**:  y = sin(x)  

Using the **SciPy optimization library**, we determine the point where these functions are equal e^{-x} = sin(x).  
We also generate a **visual representation** of both functions and highlight their intersection.  

---

## 📂 Table of Contents  
- [Project Overview](#Project-Overview)
- [Mathematical Explanation](#mathematical-explanation)
- [Requirements & Installation](#requirements-installation)
- [How to Run](#how-to-run)
- [Code Breakdown](#code-breakdown)
- [Results & Findings](#results--findings)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)
- [Connect with Me](#connect-with-me)  

---

## 📌 Project Overview  
This project aims to:  
✔ **Find the intersection point** of y = e^{-x}  and y = sin(x) using numerical methods.  
✔ **Use SciPy’s root-finding algorithm** to compute the x-value where both functions are equal.  
✔ **Visualize the functions** and highlight the intersection using Matplotlib.  

---

## 🧮 Mathematical Explanation  
The problem reduces to solving the equation:  


e^{-x} = sin(x)


Since this equation is difficult to solve **analytically**, we use a **numerical root-finding method** from SciPy to approximate the **x value** where both sides are equal.  

📌 The function we solve is:  


f(x) = e^{-x} - sin(x) = 0


We provide an **initial guess** to the solver and let it compute an **approximate intersection point**.  

---

## ⚙️ Requirements & Installation  

### 1️⃣ Prerequisites  
Ensure you have **Python 3.x** installed. Check your version:  
```bash
python --version
```

### 2️⃣ Install Required Libraries  
Run the following command to install dependencies:  
```bash
pip install numpy scipy matplotlib
```

---

## 🚀 How to Run  

### 1️⃣ Clone the Repository  
```bash
git clone https://github.com/onyeiwu/Function_Intersection_Analysis.git
cd Function_Intersection_Analysis
```

### 2️⃣ Run the Python Script  
```bash
python intersection_finder.py
```

Alternatively, you can open and run the **Jupyter Notebook** version of the project:  
📄 **File Path**: `"C:\Users\hp\Function_intersection_Analysis.ipynb"`

---

## 📜 Code Breakdown  

### 1️⃣ Import Necessary Libraries  
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.optimize import root
```
✔ `numpy`: For mathematical operations  
✔ `matplotlib.pyplot`: For plotting  
✔ `scipy.optimize.root`: To find the intersection  

### 2️⃣ Define the Functions  
```python
def y1(x):
    return np.exp(-x)

def y2(x):
    return np.sin(x)
```
✔ `y1(x)` represents **exponential decay**  
✔ `y2(x)` represents **sine wave oscillation**  

### 3️⃣ Define the Equation to Solve  
```python
def equation(x):
    return y1(x) - y2(x)
```
✔ Finds where the two functions are equal (**exp(-x) = sin(x)**)  

### 4️⃣ Compute the Root  
```python
result = root(equation, 0.5)
root_x = result.x[0]
print(f"Intersection at x ≈ {root_x:.4f}")
```
✔ The `root` function **numerically** finds x where `equation(x) = 0`.  

### 5️⃣ Plot the Functions and Intersection  
```python
x_vals = np.linspace(-1, 2, 500)

plt.figure(figsize=(10, 6))
plt.plot(x_vals, y1(x_vals), label="y1 = exp(-x)", color="blue", linewidth=2)
plt.plot(x_vals, y2(x_vals), label="y2 = sin(x)", color="orange", linewidth=2)
plt.axvline(root_x, color="red", linestyle="--", label=f"Root (x ≈ {root_x:.4f})")
plt.scatter(root_x, y1(root_x), color="red", s=100, zorder=5)

plt.title("Intersection of exp(-x) and sin(x)")
plt.xlabel("x")
plt.ylabel("y")
plt.legend()
plt.grid(True, alpha=0.3)
plt.show()
```
✔ This **plots the two functions** and marks the **intersection point**.  
![Gitpicture](https://github.com/user-attachments/assets/468d7eb5-8d85-44b7-9205-f8d2cd4ba2c8)


---

## 📈 Results & Findings  

### 1️⃣ Output in Terminal  
```bash
Intersection at x ≈ 0.5885
```
✔ This means that **exp(-x) = sin(x)** at approximately **x = 0.5885**.  

### 2️⃣ Graphical Output  
✔ **Blue Curve** → y = e^{-x}   
✔ **Orange Curve** → y = sin(x)   
✔ **Dashed Red Line** → Intersection at **x ≈ 0.5885**  
✔ **Red Dot** → Intersection point  

📌 **Insights:**  
- The **two functions intersect only once** in the given range.  
- **exp(-x) decreases** while **sin(x) oscillates**, creating a single crossing point.  

---

## 🚀 Future Enhancements  
🔹 Extend the script to find **multiple intersections**.  
🔹 Use **symbolic computation (sympy)** for exact solutions.  
🔹 Develop a **GUI using Tkinter or Dash**.  
🔹 Allow users to **input custom functions** for intersection analysis.  

---

## 🤝 Contributing  
We welcome contributions! 🚀  
✔ **Report issues** via [GitHub Issues](https://github.com/onyeiwu/Function_Intersection_Analysis/issues)  
✔ **Submit Pull Requests (PRs)** for new features or bug fixes.  

---

## 📜 License  
This project is licensed under the **MIT License** – you are free to **use and modify** the code!  

---

## Connect with Me  
👤 **Onyeiwu Gabriel**  

💻 **GitHub**: [Onyeiwu Gabriel](https://github.com/Onyeiwu)  
🔗 **LinkedIn**: [Gabriel Onyeiwu](https://www.linkedin.com/in/gabriel-onyeiwu-2b3956171)  
🎵 **TikTok**: [@onyeiwu_gabriel.7](https://www.tiktok.com/@onyeiwu_gabriel.7)  
📧 **Email**: [onyeiwugabriel913@gmail.com](mailto:onyeiwugabriel913@gmail.com)  

📢 **If you found this project helpful, give it a ⭐ on GitHub!** 🚀  

---

