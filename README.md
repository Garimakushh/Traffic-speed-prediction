# 🚦 Traffic Speed Prediction

Predicting traffic speeds using advanced spatiotemporal deep learning techniques with real-world datasets and weather integration.

 The proposed model combines Graph Convolutional Networks (GCNs) and Long Short-Term Memory (LSTM) networks to effectively predict traffic speeds by capturing both spatial and temporal dependencies.
This hybrid architecture allows the model to learn complex, real-time traffic dynamics, making it suitable for intelligent transportation systems and smart city applications.

## 📊 Datasets Used

- **PEMS-BAY**: Traffic sensor data from the Bay Area (California)
- **METR-LA**: Loop detector traffic data from Los Angeles County
- **Weather Data**: Integrated temperature,wind speed, humidity, etc., to enhance prediction accuracy

> *Traffic data is augmented with real-time weather features to improve forecasting under varying environmental conditions.*



## 🔍 Problem Statement

Predict traffic speed at various sensors across a city using historical speed and weather data. This helps in:

- 🚗 Reducing congestion
- 📈 Optimizing route planning
- ⏱️ Improving travel time predictions

## 🧠 Model Architecture
### 🔗 Hybrid LSTM-GCN
The core of this project is a hybrid deep learning model that leverages the strengths of both LSTM (Long Short-Term Memory) networks and GCN (Graph Convolutional Networks) to effectively capture the complex patterns in traffic speed data.

### 📌 Why LSTM + GCN?
Traffic data is inherently spatiotemporal:
* 🧭 Spatial dependencies exist between different road sensors (e.g., congestion at one location can impact others nearby).

* ⏱️ Temporal dependencies capture how traffic evolves over time at each location.

To address this, we combine:

* Graph Convolutional Networks (GCNs) to model the spatial relationships between traffic sensors using the road network as a graph.

* LSTM layers to learn temporal patterns over sequences of traffic speed data for each sensor.

### 🧩 How the Hybrid Model Works
1. **Input Layer**
   - Traffic speed time series data for each sensor  
   - Weather features (e.g., temperature, rainfall, humidity)

2. **Graph Construction**
   - Sensors are represented as **nodes** in a graph  
   - Edges reflect:
     - Physical proximity  
     - Road network connectivity  
   - Represented using an **adjacency matrix**

3. **GCN Layers (Graph Convolutional Networks)**
   - Each sensor’s features are updated using information from its neighboring sensors  
   - Captures **spatial dependencies** and correlations in traffic flow across the network

4. **LSTM Layers (Long Short-Term Memory)**
   - Processes the **GCN-enhanced time series** for each sensor  
   - Learns **temporal patterns** in traffic speed variations over time

5. **Fully Connected Layers**
   - Final dense layers to map LSTM outputs to prediction space  
   - Predicts future traffic speeds for multiple time horizons:
     - **5 minutes ahead**
     - **10 minutes ahead**
     - **15 minutes ahead**

### 🎯 Advantages
  * 🌐 Captures both local and global spatial dependencies

* ⏳ Learns complex temporal behaviors

* 🌦️ Adapts to changing conditions via weather feature integration

* 📈 Outperforms traditional LSTM or GCN-only models in accuracy and robustness
## 📥 Dataset Access
These datasets are private due to size or license. You can request access via the links below:

* 🔒 [Request Access to METR-LA Dataset](https://drive.google.com/file/d/1LhNB_JxH9c9O8ye3ENSJEWPflttRqoZl/view?usp=drivesdk)
* 🔒 [Request Access to PEMS-BAY Dataset](https://drive.google.com/file/d/1LWVY-mEB2wC6ymnTxHmpQMrOl4f38i9J/view?usp=drivesdk)
* 🌦️ Weather Data Source

## 📊 Visual Results
![images](https://github.com/Garimakushh/Traffic-speed-prediction/blob/13c3683c41855487e7f584fecfac633737021b13/Results/Screenshot%20(101).png)

# 🤝 Contributions
Have suggestions or want to improve the model? Contributions are welcome!

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/Garimakushh">Garima Kushwaha</a>
</p>


