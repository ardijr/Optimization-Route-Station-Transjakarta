# TransJakarta Route & Stop Optimization  
### Using Exploratory Data Analysis (EDA) and Diagnostic Analysis

This project focuses on optimizing **TransJakarta route and stop operations** by leveraging **Exploratory Data Analysis (EDA)** and **Diagnostic Analysis**. The objective is to identify **underutilized stops, overcrowded corridors, directional imbalance, premium OD pairs, and time-based demand fluctuations**, then translate those findings into **actionable fleet and service recommendations**.

---

## 1. Project Summary

TransJakarta operates a large and dynamic BRT ecosystem where passenger demand changes significantly across:

- Hour of day
- Corridor
- Travel direction
- Stop utilization
- Weekday vs weekend
- Origin–Destination flow

Without adaptive operational planning, these patterns may create:

- Overcrowded buses during peak periods
- Low occupancy during off-peak hours
- Idle fleet on weak-demand routes
- Inefficient headway settings
- Longer waiting times
- Higher operating cost

This project provides **data-driven operational insights** to improve:

- Fleet utilization
- Stop-level efficiency
- Directional balance
- Corridor performance
- Headway optimization
- Passenger waiting experience
- Operating cost efficiency

**Dataset Source:** Internal TransJakarta capstone dataset provided by Purwadhika Data Science Bootcamp.

---

## 2. Repository Structure

```bash
transjakarta-route-stop-optimization/
├── capstone2.ipynb      # full EDA + diagnostic analysis
├── Transjakarta.csv     # dataset
└── README.md            # project documentation
```

---

## 3. Tools & Technologies

| Category | Tools |
|---|---|
| Programming | Python (Pandas, NumPy) |
| Notebook | Jupyter Notebook / VS Code |
| Visualization | Matplotlib, Seaborn, Folium |
| Data Format | CSV |
| Version Control | Git & GitHub |

---

## 4. Analysis Components

### **4.1 Hourly Demand Analysis**
- Peak demand occurs at **06:00** and **17:00**
- Mid-day demand (**10:00–15:00**) falls below **10% of peak volume**
- Indicates strong **time-sensitive demand pattern**
- Supports **dynamic frequency adjustment by hour**

### **4.2 Weekday vs Weekend Demand**
- Weekday demand significantly exceeds weekend demand
- Weekend usage remains stable but much lower
- Suggests need for **reduced weekend frequency** to minimize idle trips

### **4.3 Stop Occupancy Analysis**
- Major imbalance across stops
- High-demand stops include:
  - Penjaringan
  - Garuda Taman Mini
  - BKN
- Some stops record only **1 tap-in**
- Highlights **over-utilized vs under-utilized stops**

### **4.4 Corridor Performance Analysis**
- Several corridors generate **20×+ higher trips** than weaker corridors
- Indicates possible **fleet misallocation across corridors**
- High-performing corridors need reinforcement

### **4.5 Directional Gap Analysis**
- Some routes show **13–16 trip gap** between inbound and outbound flow
- Confirms **non-symmetrical passenger movement pattern**
- Equal fleet split per direction may reduce efficiency

### **4.6 OD Matrix / Premium Route Analysis**
- A small number of OD pairs contribute most trips
- Majority of OD combinations have low usage
- Reveals **premium routes with high operational leverage**

### **4.7 Spatial Hotspot Analysis**
- Heatmap analysis identifies tap-in concentration in key Jakarta areas
- Useful for:
  - stop reinforcement
  - corridor redesign
  - express route opportunity
  - hotspot-based dispatching

---

## 5. Key Insights

- Passenger demand is **uneven across time, direction, corridor, and stop**
- Peak congestion is concentrated in specific hours and routes
- Many stops contribute minimal demand
- Directional imbalance creates excess empty returns
- Premium OD pairs dominate overall mobility
- Weekend and mid-day operations have significant optimization opportunities
- Spatial hotspot analysis reveals concentrated boarding zones

---

## 6. Recommendations

### **1. Dynamic Headway Optimization**
- Tighten headway at **06:00 and 17:00**
- Extend headway during **10:00–15:00**
- Reduce unnecessary empty trips

### **2. Reinforce High-Demand Stops and Corridors**
- Add buses on overloaded stops/corridors
- Reduce queue buildup and overcrowding

### **3. Reallocate Low-Utilization Fleet**
- Move buses from weak-demand stops and corridors
- Maintain minimum service threshold only

### **4. Direction-Based Fleet Allocation**
- Allocate buses dynamically by **dominant travel direction**
- Reduce idle capacity on weak return flow

### **5. Optimize Weekend Service**
- Lower service frequency during weekend low-demand periods
- Improve occupancy and reduce operating waste

### **6. Prioritize Premium OD Routes**
- Focus reliability and express service on top OD pairs
- Improve travel speed and bus turnover

### **7. Spatial Dispatch Optimization**
- Use hotspot zones as dispatch priority areas
- Improve responsiveness during localized demand surges

---

## 7. Business Impact

Expected impact from this optimization framework:

- Higher fleet occupancy
- Lower idle bus ratio
- Better corridor-level service reliability
- Reduced operating cost
- Faster passenger throughput
- Better peak-hour experience
- Improved route profitability

---

## 8. Author

**Ardi Ansyah**  
Purwadhika Data Science Bootcamp  
Capstone Module 2  

---

## 9. How to Run This Project

1. Clone this repository
2. Open `capstone2.ipynb`
3. Run all cells sequentially
4. Review visualizations and recommendations
5. Open generated Folium HTML maps in browser if notebook preview is blocked

---

## 10. Closing

Thank you for reviewing this project.

This capstone demonstrates how **EDA + diagnostic analytics** can directly support **public transportation route optimization, fleet efficiency, and service quality improvement** for TransJakarta.

