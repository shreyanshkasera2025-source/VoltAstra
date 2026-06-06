# ⚡ VoltAstra: Physics-Informed Solar Telemetry & Anomaly Auditor

VoltAstra is an open-source, cyber-physical software platform designed to audit residential solar array efficiency. Instead of relying solely on baseline weather predictions, VoltAstra combines empirical atmospheric data with real-world laws of physics (thermodynamics and geometric optics) to identify physical system faults—such as localized panel shading or surface dust accumulation (soiling).

---

## 🚀 Key Features

- **Vectorized Physics Pipeline:** Utilizes **NumPy** to evaluate daily time-series solar irradiance sequences ($W/m^2$) instantaneously without loop structures.
- **Thermodynamic Cell Modeling:** Dynamically estimates photovoltaic cell internal heating and applies linear power degradation coefficients ($\alpha = 0.004$) when internal cell temperatures exceed 25°C.
- **Statistical Anomaly Engine:** Evaluates user-uploaded inverter logs or live telemetry entry against physics-informed models to flag efficiency variances greater than 15%.
- **Zero-Cost Infrastructure:** Runs entirely on open-source frameworks via a dark-themed interactive **Streamlit** dashboard using the completely free **Open-Meteo API**.

---

## 🛠️ Software Architecture & Tech Stack

- **Language:** Python 3.x
- **Data Arrays & Core Math:** NumPy
- **Sequence Handling & Dataframes:** Pandas
- **Live Environmental Ingestion:** Requests + Open-Meteo API
- **User Interface Framework:** Streamlit

---

## 💻 Local Installation & Setup

To run VoltAstra Core locally on your machine, clone this repository and install the minimal required modules:

```bash
# Clone the repository
git clone [https://github.com/YOUR_GITHUB_USERNAME/VoltAstra.git](https://github.com/YOUR_GITHUB_USERNAME/VoltAstra.git)

# Navigate into the project directory
cd VoltAstra

# Install the required dependencies
pip install streamlit numpy pandas requests

# Launch the interactive engineering dashboard
streamlit run app.py
