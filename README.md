# NIYAMR AI - Universal Credit Act 2025 Agent

## 📌 Objective
Build a mini AI agent capable of reading, summarizing, and analyzing the **Universal Credit Act 2025**. This solution extracts structured data from PDF format and performs legislative compliance checks using a local LLM pipeline.

## 🛠 Architecture & Tools Used

### 1. Data Extraction: **Docling**
* **Why?** Unlike standard OCR, Docling preserves complex document structures like tables and headers, which are critical for reading legal Acts.

### 2. Vector Database: **ChromaDB**
* **Model:** `nomic-embed-text-v1.5`
* **Why?** Nomic has a long context window (8192 tokens), making it ideal for retrieving large chunks of legal text without losing context.

### 3. LLM Reasoning: **Qwen 2.5-7B (Instruct)**
* **Why?** One of the best open-source 7B models with strong instruction-following capabilities.
* **Optimization:** Loaded with **BitsAndBytes (4-bit quantization)** to run efficiently on consumer hardware (Free Colab T4/L4 GPUs).

## 📂 Project Structure

```bash
├── data/                                           # Input PDF storage
├── NIYAMR AI - Universal Credit Act 2025 Agent     # Original development notebook
├── output/                                         # Final JSON reports        
├── requirements.txt                                # Dependencies
└── README.md                                       # Documentation
```
## 🚀 How to Run

### **1. Install Dependencies:**
```
pip install -r requirements.txt
```
### **2. Run the Agent:**
```
python src/main.py
```
### **3. Upload PDF when ask**

### **4. Wait Till get the final file named "Final_Submission_Output.json"**
