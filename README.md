# **DHS Dispatch & Delivery Analysis Project**

## **🚀 Project Overview**
This project analyzes **courier dispatching, order assignments, and delivery efficiency** using data from the **TSL-Meituan Dispatch System**. The goal is to uncover patterns, inefficiencies, and opportunities for optimizing the food delivery process. 

### **📌 Key Objectives**
- **Understand dispatch trends**: How and when couriers are assigned to orders.
- **Analyze delivery efficiency**: Measure time gaps between order creation, dispatch, pickup, and delivery.
- **Investigate dispatch bottlenecks**: Identify delays in order-to-courier assignment.
- **Compare prebooked vs. non-prebooked orders**: Evaluate differences in dispatch and delivery performance.

---

## **📂 Dataset Description**
The project utilizes **four key datasets**:

1. **`all_waybill_info_meituan.csv`** 📦  
   - Contains detailed information about each order, including timestamps, locations, and courier interactions.  
   - Key columns: `order_id`, `courier_id`, `dispatch_time`, `grab_time`, `fetch_time`, `arrive_time`.

2. **`courier_wave_info_meituan.csv`** 🛵  
   - Captures **wave-based courier assignments**, showing how couriers batch deliveries.
   - Key columns: `wave_id`, `wave_start_time`, `wave_end_time`, `order_ids`.

3. **`dispatch_rider_meituan.csv`** 🚴  
   - Logs **couriers available for dispatch** at different times.
   - Key columns: `courier_id`, `dispatch_time`, `rider_lat`, `rider_lng`, `courier_waybills`.

4. **`dispatch_waybill_meituan.csv`** 📝  
   - Contains **order-level dispatch assignments**.
   - Key columns: `order_id`, `dispatch_time`.

---

## **🔍 Exploratory Data Analysis (EDA)**
### **1️⃣ Data Cleaning & Preprocessing**
✅ Convert timestamps to readable `datetime` format.  
✅ Handle missing or incorrect values (`0` timestamps converted to NaT).  
✅ Parse list-based fields (e.g., `order_ids` in `courier_wave_info_meituan.csv`).  

### **2️⃣ Dispatch System Efficiency**
- 📊 **Order assignment delays**: Time between order creation and dispatch.
- ⏳ **Wave dispatch timing**: Trends in how couriers are assigned in batches.

<!-- ### **3️⃣ Courier Workload & Performance**
- 📦 **Orders per courier per wave**: Measure how many deliveries couriers handle at once.
- 🚀 **Courier reassignment trends**: Track how often orders switch couriers.
- ⏱️ **Time between consecutive dispatches per courier**. -->


---

## **📜 Project Structure**
```
📂 dsh-data-exploration
│── courier_dispatch_analysis.ipynb       # Primary analysis notebook
│── DHS Dispatch Data Analysis.pdf        # Presentation
│── README.md                             # Project documentation
│── requirements.txt                      # Dependencies and libraries
```

---

## **📌 How to Run the Analysis**
### **1️⃣ Install Dependencies**
```bash
pip install -r requirements.txt
```
### **2️⃣ Run Jupyter Notebook**
```bash
jupyter notebook
```
- Open `main.ipynb` and execute cells step-by-step.

