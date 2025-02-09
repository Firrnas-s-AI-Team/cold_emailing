# Automated Cold Emailing System

## 🚀 Overview
This project is an **AI-Powered Cold Email Automation System** designed to optimize business outreach processes. It automates personalized email generation, sending, response classification, and follow-up handling using advanced NLP models and Retrieval-Augmented Generation (RAG) techniques.

## 📂 Project Structure
```
├── cold_email_automation.ipynb  # Main Jupyter Notebook for automation
├── VR_and_Software_Companies_2.csv  # List of target companies
├── detailed_product_catalog.pdf     # Product catalog for personalized content
├── temp_emails.json                 # Temporary storage for email tracking
└── README.md                        # Project documentation
```

## 🔑 Features
1. **Personalized Cold Email Generation**  
   - Utilizes **Meta LLaMA-3.2-3B-Instruct** for crafting customized emails.
   - Leverages **RAG** to enhance content relevance from the product catalog.

2. **Automated Email Sending**  
   - Sends emails using **SMTP (Gmail)** with dynamic content and attachments.
   - Tracks sent emails in an **SQLite database** for easy management.

3. **Response Monitoring & Classification**  
   - Checks for incoming responses every 60 seconds using **IMAP**.
   - Classifies replies using **Qwen 2.5 model (4-bit quantization)** into:
     - **Not Interested:** Ignored.
     - **Need More Details:** Auto-replies with relevant product information.
     - **Meeting Request:** Automatically forwarded to HR.

4. **Product Recommendation System**  
   - Employs **FAISS** and **Sentence Transformers** for semantic search.
   - Retrieves the most relevant product details based on queries.

## ⚙️ Technologies Used
- **Python Libraries:** `pandas`, `transformers`, `smtplib`, `PyPDF2`, `faiss`, `sqlite3`, `sentence-transformers`
- **AI Models:** Meta LLaMA-3.2-3B-Instruct, Qwen 2.5 (4-bit quantization)
- **Email Protocols:** SMTP for sending, IMAP for receiving
- **Database:** SQLite for email tracking

## 🗃️ Dataset & Files
- **`VR_and_Software_Companies_2.csv`**: Contains details of target companies for cold emailing.
- **`detailed_product_catalog.pdf`**: Source of product information for personalized email content.
- **`temp_emails.json`**: Temporary storage for tracking email threads and responses.

## 🚀 How to Run
1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/cold-email-automation.git
   cd cold-email-automation
   ```

2. **Configure Email Credentials:**  
   Update your SMTP credentials in the notebook/script.

3. **Run the Automation Notebook:**
   ```bash
   jupyter notebook cold_email_automation.ipynb
   ```

## ✅ Future Improvements
- Integration with CRM tools for seamless lead management.
- Enhanced sentiment analysis for more precise response classification.
- Dashboard for real-time email analytics and reporting.
