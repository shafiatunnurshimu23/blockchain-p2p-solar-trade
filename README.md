My analysis summary: [analysis_summary.docx](https://github.com/user-attachments/files/20902983/analysis_summary.docx)

Overall Work Description:[summary of my work.docx](https://github.com/user-attachments/files/20903019/summary.of.my.work.docx)

# ☀️🔗💡 Blockchain-Inspired P2P Solar Energy Trading Simulation

*A lightweight, data-driven simulation of a peer-to-peer (P2P) solar energy trading market for rural microgrids. This project uses a greedy matching algorithm and a hashed ledger to demonstrate a practical, low-cost approach to decentralized energy management.*

---

## 1. Problem Statement

In many rural communities, centralized grid infrastructure is economically and logistically unfeasible, leading to a lack of access to affordable and reliable electricity. While local solar microgrids present a solution, they require an efficient, transparent, and trustworthy mechanism for residents to trade surplus energy.

This project tackles this challenge by designing and simulating a **decentralized P2P energy trading platform**. The core objective is to create a system that is economically viable and technically feasible for resource-constrained environments, leveraging the principles of blockchain without the high computational cost of a full deployment.

## 2. The Solution: A Lightweight Blockchain-Inspired Simulation

Instead of implementing a resource-intensive blockchain, this project simulates its most important features in a lightweight Python environment. This approach maintains the core benefits of decentralization and trust while ensuring the system is practical for rural microgrids.

The simulation's key architectural features are:
- **Data-Driven Logic:** Uses a real-world time-series dataset of household solar generation and consumption to drive the simulation.
- **Automated Matching:** A greedy algorithm identifies households with surplus energy (sellers) and those with a deficit (buyers), then automatically executes trades.
- **Tamper-Evident Ledger:** Every transaction is recorded in a sequential, cryptographically-linked ledger. Each new "block" (trade record) contains the SHA-256 hash of the previous block, creating an immutable chain of records that ensures transparency and auditability.

![image](https://github.com/user-attachments/assets/c572f982-66b5-4260-8295-503d07ac1663)
 <!-- ### TODO: UPDATE THIS LINK (from your PDF's Figure 3.1) ### -->

## 3. Tech Stack

| Category | Technologies |
|---|---|
| **Data Analysis & Simulation** | Python, Pandas, NumPy, Hashlib (for SHA-256 Hashing) |
| **Data Visualization** | Matplotlib, Seaborn, NetworkX (for Trade Network Graphs) |
| **Environment** | Jupyter Notebook, VS Code |

## 4. Analytical Workflow & Key Findings

### 4.1. The Trading Algorithm

The simulation operates on hourly aggregated data to maximize matching opportunities. The process for each hour is as follows:
1.  **Surplus/Deficit Classification:** Households are classified as buyers or sellers based on their `net_kWh` (solar generation - consumption).
2.  **Greedy Matching:** The algorithm iteratively matches sellers with the largest surplus to buyers with the greatest need, ensuring efficiency.
3.  **Dynamic Pricing:** The trade price is set as the average of the buyer's and seller's price, creating a fair, decentralized pricing mechanism.
4.  **Transaction Logging:** Every successful trade is recorded as a new block in the blockchain-inspired ledger.

### 4.2. Behavioral Insights: Who Trades and When?

Analysis of the trading data revealed clear behavioral patterns and the emergence of specialized roles within the microgrid.

- **Role Specialization:** Certain households consistently acted as "sellers" (net producers), while others were consistent "buyers." Hybrid roles also emerged, with households like H4 acting as a central hub, both buying and selling to balance the local energy flow.

![image](https://github.com/user-attachments/assets/35bd80df-bf5f-4d61-8d19-0d7254231fcb)

- **Temporal Patterns:** A heatmap analysis showed that trading activity peaked during mid-morning and early afternoon, aligning with peak solar generation. Weekends, particularly Saturdays, saw heightened activity, likely due to increased daytime energy usage at home.

![image](https://github.com/user-attachments/assets/1b2f395d-457a-4910-8b08-cee8c0571e9f)
 <!-- ### TODO: UPDATE THIS LINK (from your PDF's Figure 3.3) ### -->
 <!-- ### TODO: UPDATE THIS LINK (from your PDF's Figure 4.2) ### -->

### 4.3. Visualizing the Decentralized Network

A network graph was created using NetworkX to visualize the flow of energy. Nodes represent households (color-coded by their dominant role) and the thickness of the edges represents the volume of energy traded. This clearly illustrates the decentralized, peer-to-peer nature of the market.

![image](https://github.com/user-attachments/assets/95f64175-049f-473b-a35d-bcdb25c15cb2)

 <!-- ### TODO: UPDATE THIS LINK (from your PDF's Figure 4.1) ### -->

## 5. Quantifiable Economic Impact

The simulation proved the economic feasibility of the P2P trading model. By allowing direct trade between peers, the system bypassed traditional, higher-priced grid electricity.

| Metric | Result | Insight |
|---|---|---|
| **Total Energy Traded** | 3.26 kWh | Facilitated significant local energy redistribution. |
| **Average P2P Price** | 0.127 currency units/kWh | The decentralized market price was determined by peer negotiation. |
| **Assumed Grid Price** | 0.200 currency units/kWh | Represents the higher cost of centralized electricity. |
| **Relative Cost Reduction** | **~36.5%** | **Participants saved over 36% on energy costs** compared to buying from the grid. |

This significant cost saving demonstrates the powerful economic incentive for adopting such a system in rural communities, directly improving energy affordability and sustainability.

## 6. How to Run This Project

### Prerequisites
- Python 3.8+
- `pip` for package management

### Instructions
1.  **Clone the repository:**
    ```bash
    git clone https://github.com/shafiatunnurshimu23/blockchain-p2p-solar-trade.git
    cd blockchain-p2p-solar-trade
    ```

2.  **Set up a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On macOS/Linux
    .\venv\Scripts\activate   # On Windows
    ```

3.  **Install dependencies:**
    *(Ensure you have a `requirements.txt` file in your repository.)*
    ```bash
    pip install -r requirements.txt
    ```

4.  **Explore the analysis:**
    - The complete simulation logic, data analysis, and visualizations are contained within the Jupyter Notebook(s) in the `/notebooks/` directory.
    - Open and run the cells in the notebook to reproduce the entire workflow, from data loading to the final analysis and ledger creation.
