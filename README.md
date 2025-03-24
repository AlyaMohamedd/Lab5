# CSAI 422: Laboratory Assignment 5

## **Building LLM Workflows: From Basic to Advanced**

### **📌 Overview**

This project implements **various LLM workflows** to repurpose a blog post into multiple formats. The workflows include:

- **Basic Pipeline Workflow**
- **DAG Workflow**
- **Self-Correction with Reflexion**
- **Agent-Driven Workflow**
- **Chain-of-Thought (CoT) Reasoning**
- **Comparative Evaluation System** (Bonus)

### **📂 Project Structure**

```
|-- LLM_Workflows.py  # Main Python script implementing workflows
|-- README.md         # Documentation
|-- sample_blog_post.json  # Example input file
|-- .env              # API keys (not included in repo)
```

---

### **⚙️ Setup Instructions**

#### **1️⃣ Install Dependencies**

Make sure you have Python 3.10+ installed. Install required libraries using:

```sh
pip install -r requirements.txt
```

#### **2️⃣ Set Up API Keys**

Create a `.env` file in the project root and add your API keys:

```sh
MODEL_SERVER=NGU  
NGU_API_KEY=your_api_key_here  
NGU_BASE_URL=https://ngullama.femtoid.com/v1  
NGU_MODEL=qwen2.5-coder:7b  
```

#### **3️⃣ Run the Workflow**

Execute the script to process the sample blog post:

```sh
python llm_workflows.py
```

---

### **🛠 Implemented Workflows**

#### **1️⃣ Basic Pipeline Workflow**

A sequential workflow that:

1. Extracts key points from the blog post
2. Generates a summary
3. Creates social media posts
4. Generates an email newsletter

Run:

```python
run_pipeline_workflow(blog_post)
```

#### **2️⃣ DAG Workflow**

A more flexible workflow where multiple tasks can run in parallel.
Run:

```python
run_dag_workflow(blog_post)
```

#### **3️⃣ Reflexion-Based Self-Correction**

This workflow uses **self-correction** to refine outputs based on quality evaluation.
Run:

```python
run_workflow_with_reflexion(blog_post)
```

#### **4️⃣ Agent-Driven Workflow**

An AI agent decides the best workflow dynamically.
Run:

```python
run_agent_driven_workflow(blog_post)
```

#### **5️⃣ Chain-of-Thought (CoT) Reasoning**

Enhances reasoning for better task execution.
Run:

```python
run_cot_workflow(blog_post)
```

#### **6️⃣ Comparative Evaluation (Bonus)**

Evaluates and compares different workflow approaches.
Run:

```python
compare_workflows(blog_post)
```

---

### **📊 Example Output**

```json
{
    "key_points": ["AI improves diagnosis", "Enhances treatment plans"],
    "summary": "AI is revolutionizing healthcare by improving diagnosis and treatment.",
    "social_posts": {
        "twitter": "AI is transforming healthcare! 🏥💡 #AI #HealthTech",
        "linkedin": "AI is improving diagnostics and treatment. How will it shape the future?",
        "facebook": "Discover how AI is enhancing healthcare outcomes!"
    },
    "email": {
        "subject": "The Future of AI in Healthcare",
        "body": "AI is changing the way doctors diagnose and treat diseases..."
    }
}
```

---

### **📌 Challenges & Solutions**

| **Challenge**                           | **Solution**                                      |
| --------------------------------------- | ------------------------------------------------- |
| LLM responses were inconsistent         | Used structured tool-calling and explicit prompts |
| Content sometimes lacked coherence      | Implemented Reflexion for self-correction         |
| Formatting issues in social media posts | Standardized output parsing                       |

---

### **📌 Submission Information**

- **GitHub Repository:** [https://github.com/AlyaMohamedd/Lab5](https://github.com/AlyaMohamedd/Lab5)
- **Submission Deadline:** March 30, 2025 (March 24 for a 20% bonus)

🚀 **Project Completed by:** *Alya Mohamed*

