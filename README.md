# E-Waste PCB Analyzer & Sorter: AI-Powered E-Waste Classifier

**Developed for the CREONIX '25 National Level Hackathon.**

E-Waste PCB Analyzer & Sorter is a vision-based AI system designed to intelligently sort and classify scrap Printed Circuit Boards (PCBs) to make e-waste recycling more efficient, profitable, and sustainable. [cite_start]The system analyzes an image of a PCB and provides a detailed breakdown of its components, reusability potential, and a final segregation recommendation. [cite: 2]

![Demo Screenshot](link_to_your_demo_screenshot.png)  
*(You should replace this line with a real screenshot of your Gradio app working)*

---

## 🚀 Key Features

* [cite_start]**Real-Time Component Detection:** Utilizes a custom-trained YOLOv8 model to detect and locate multiple electronic components (ICs, capacitors, etc.) on any given PCB image. [cite: 26]
* **Detailed Reusability Analysis:** Calculates a "Reusability Score" based on the quality, quantity, and density of valuable components, and provides a transparent list of the factors considered in its decision.
* **Intelligent Segregation Recommendation:** Provides an instant, actionable recommendation to classify a board for its most efficient waste stream:
    * ♻️ **Reusable:** High potential for component harvesting.
    * ☣️ **Hazardous:** Requires special handling and disposal.
    * [cite_start]⚙️ **General Recycling:** Suitable for standard shredding and material recovery. [cite: 15]

---

## 🛠️ Tech Stack

* **AI/ML Framework:** Python, Ultralytics YOLOv8, OpenCV, NumPy
* **UI/Application Framework:** Gradio
* [cite_start]**Dataset Management:** Roboflow [cite: 24]
* **Development Environment:** Google Colab

---

## ⚙️ How to Run

This project is designed to run in a cloud environment like Google Colab or a local environment with the proper dependencies installed.

### Prerequisites

* Python 3.8+
* A trained model file (`best.pt`)

### Installation

1.  Clone the repository:
    ```bash
    git clone [https://github.com/MS-SHREYA/E-Waste-Sorter-CREONIX-25.git](https://github.com/MS-SHREYA/E-Waste-Sorter-CREONIX-25.git)
    cd E-Waste-Sorter-CREONIX-25
    ```
2.  Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```

### Running the Demo

The project can be run using the provided Jupyter/Colab notebook (`SRMHack.ipynb`) or the standalone Python scripts. The Gradio script will launch a web interface for easy, interactive demos.

---

## Future Scope

While this prototype is fully functional, the system is designed for scalability. Future improvements could include:

* [cite_start]**Integration with Robotics:** The final recommendation output can be used as a command signal for a physical robotic arm or conveyor system to automate the physical sorting process. [cite: 16]
* [cite_start]**Expanded Dataset:** Training the model on a larger, more diverse dataset of PCBs will improve accuracy and the ability to recognize a wider variety of components, especially on damaged or corroded boards. [cite: 43, 44]
* **Advanced Component Analysis:** Integrating OCR to read part numbers from ICs to enable precise value estimation and datasheet lookups.
