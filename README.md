# Devops-Final-Project
# 🚀 Maven Build Optimization using Jenkins CI/CD

This project demonstrates how to optimize Maven build times using parallel execution and modular builds, both locally and in a Jenkins CI/CD pipeline.

## 📌 Project Objective

To reduce Maven build times using:
- Parallel builds using `-T` flag
- Building specific modules with `-pl` and `-am` flags
- Automating the process via a Jenkins CI/CD pipeline

---

## 🛠️ Technologies Used

- **Maven**
- **Jenkins**
- **Git & GitHub**
- **Java**
- **Linux Shell Commands**

---

## 🔄 Optimization Techniques Applied

| Technique                          | Description                                                                 |
|-----------------------------------|-----------------------------------------------------------------------------|
| `-T 4`                             | Enables parallel build threads (4 threads used here)                        |
| `-pl <module>` + `-am`            | Builds only required modules and dependencies                               |
| Jenkins Pipeline (Parallel stages) | Builds and runs two modules (`module-a` and `module-b`) simultaneously     |

---

## 📁 Project Structure

Maven_Build_Optimization/
├── module-a/
│ └── src/...
├── module-b/
│ └── src/...
├── Jenkinsfile
└── README.md

---

## 🧪 Build Time Comparison

| Environment     | Total Build Time |
|----------------|------------------|
| **Local (Terminal)** | ~5.2 seconds     |
| **Local (Terminal) - testskip ** | ~2.887 seconds     |
| **CI (Jenkins)**     | ~24.9 seconds    |

🔍 *Note: Jenkins build takes longer due to no caching, network latency, and fresh environment setup.*

---

## 🚧 Jenkins Setup

1. Open Jenkins → **New Item** → Choose **Pipeline**
2. Set **Repository URL** to:
3. Set branch to `main`
4. Script Path: `Jenkinsfile`
5. Click **Build Now**

---

## ✅ Outcome

This project successfully demonstrates:
- Real-world Maven build optimization
- Modular project structure
- Measurable performance gains
- Automation with Jenkins Pipeline

---

## 📚 Author

**Nithesh M P**  
GitHub: [NITHESH-MP](https://github.com/NITHESH-MP)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
