# CSAI 422: Laboratory Assignment 5

## **Building LLM Workflows: From Basic to Advanced**

### **Overview**

This project implements various LLM workflows to repurpose a blog post into multiple formats. The workflows include:

- Basic Pipeline Workflow
- Directed Acyclic Graph (DAG) Workflow
- Self-Correction with Reflexion
- Agent-Driven Workflow
- Chain-of-Thought (CoT) Reasoning
- Comparative Evaluation System (Bonus)

### **Project Structure**

```
|-- llm_workflows.py  # Main Python script implementing workflows
|-- README.md         # Documentation
|-- sample_blog_post.json  # Example input file
|-- .env              # API keys (not included in repo)
```

---

### **Setup Instructions**

#### **1. Install Dependencies**

Ensure Python 3.10+ is installed. Install required libraries using:

```sh
pip install -r requirements.txt
```

#### **2. Configure API Keys**

Create a `.env` file in the project root and add the necessary API keys:

```sh
MODEL_SERVER=NGU  
NGU_API_KEY=your_api_key_here  
NGU_BASE_URL=https://ngullama.femtoid.com/v1  
NGU_MODEL=qwen2.5-coder:7b  
```

#### **3. Execute the Workflow**

Run the script to process the sample blog post:

```sh
python llm_workflows.py
```

---

### **Implemented Workflows**

#### **1. Basic Pipeline Workflow**

A sequential workflow that:

1. Extracts key points from the blog post
2. Generates a summary
3. Creates social media posts
4. Generates an email newsletter

Run:

```python
run_pipeline_workflow(blog_post)
```

#### **2. DAG Workflow**

A more flexible workflow where multiple tasks can run in parallel.
Run:

```python
run_dag_workflow(blog_post)
```

#### **3. Reflexion-Based Self-Correction**

This workflow applies self-correction to refine outputs based on quality evaluation.
Run:

```python
run_workflow_with_reflexion(blog_post)
```

#### **4. Agent-Driven Workflow**

An AI agent dynamically determines the workflow execution sequence.
Run:

```python
run_agent_driven_workflow(blog_post)
```

#### **5. Chain-of-Thought (CoT) Reasoning**

Enhances reasoning capabilities for improved task execution.
Run:

```python
run_cot_workflow(blog_post)
```

#### **6. Comparative Evaluation (Bonus)**

Evaluates and compares different workflow approaches.
Run:

```python
compare_workflows(blog_post)
```

---

### **Example Output**

```json
{
    "key_points": ["AI improves diagnosis", "Enhances treatment plans"],
    "summary": "AI is revolutionizing healthcare by improving diagnosis and treatment.",
    "social_posts": {
        "twitter": "AI is transforming healthcare!",
        "linkedin": "AI is improving diagnostics and treatment. How will it shape the future?",
        "facebook": "Discover how AI is enhancing healthcare outcomes."
    },
    "email": {
        "subject": "The Future of AI in Healthcare",
        "body": "AI is changing the way doctors diagnose and treat diseases..."
    }
}
```

---

### **Challenges and Solutions**

| **Challenge**                                    | **Solution**                                             |
| ------------------------------------------------ | -------------------------------------------------------- |
| LLM responses were inconsistent                  | Implemented structured tool-calling and explicit prompts |
| Content lacked coherence                         | Applied Reflexion for self-correction                    |
| Formatting inconsistencies in social media posts | Standardized output parsing                              |

---

### **Submission Information**

- **GitHub Repository:** [https://github.com/AlyaMohamedd/Lab5](https://github.com/AlyaMohamedd/Lab5)
- **Submission Deadline:** March 30, 2025 (March 24 for an early submission bonus)

**Project Completed by:** *Alya Mohamed*

