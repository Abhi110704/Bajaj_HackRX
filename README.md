
# 🛡️ Policy Aware Assistant – HackRx 6.0

An intelligent FastAPI-based backend system that parses insurance documents (PDFs), understands user queries, and responds with accurate, policy-specific answers using rule-based NLP and optional Perplexity API fallback.

---

## 👥 Team Details

**Team Name:** HackerXHacker  
**Team Members:**
- Abhiyanshu Anand  
- Sanskar Singh  
- Abhishek Singh  
- Siddharth Tripathi  
- Harsh Katiyar

---

## 🚀 Features

✅ PDF Policy Parsing  
✅ Multiple Question Answering  
✅ Intelligent Semantic Matching  
✅ Optional Perplexity LLM Integration  
✅ Docker-Ready Deployment  
✅ Works With Any Policy Document (Health, General, etc.)

---

## 🏗️ Folder Structure

```
HackRx_Complete_Submission/
├── hackrx_policy_aware_final.py        # Main FastAPI backend
├── requirements.txt                    # Python dependencies
├── .env.example                        # Example env with token and keys
├── Dockerfile                          # For container build
├── docker-compose.yml                  # For local & scalable deployment
├── HackRx_Local_Testing_Guide.txt      # Manual testing instructions
```

---

## 🧪 How to Run Locally

1. **Clone Repo & Setup Virtual Env**
```bash
python -m venv venv
venv\Scripts\activate      # On Windows
pip install -r requirements.txt
```

2. **Create `.env` File**
```env
BEARER_TOKEN=your_custom_token_here
PERPLEXITY_API_KEY=pplx-xxxxxxxxxxxxxxxxxxxxxx   # Optional
```

3. **Run the API**
```bash
uvicorn hackrx_final_robust_api_cleaned:app
```

4. **Test at Swagger UI**
Visit 👉 http://127.0.0.1:8000/docs  
Use `POST /hackrx/run` endpoint to ask queries on any insurance PDF via URL.

---

## 🔁 Sample Request (JSON)

```json
{
  "documents": "https://example.com/sample-policy.pdf",
  "questions": [
    "What is the waiting period for cataract surgery?",
    "Does this policy cover AYUSH treatment?",
    "Is ICU stay covered?"
  ]
}
```

⚠️ Add the Bearer Token in `Authorize`:
```
Bearer your_token_here
```

---

## 🧠 How It Works

- Extracts text from insurance PDFs (remote URLs)
- Uses keyword rules & pattern matching for policy-specific answers
- Falls back to Perplexity API for generic or fuzzy queries (optional)
- Detects mismatched or unrelated policy references and avoids hallucination

---

## 📦 Docker Deployment (Optional)

```bash
docker-compose up --build
```

Then visit: [http://localhost:8000/docs](http://localhost:8000/docs)

---

## ✅ HackRx Testing Checklist

| Feature                            | Status |
|-----------------------------------|--------|
| Upload Insurance Doc (via URL)    | ✅     |
| Ask Multiple Questions            | ✅     |
| Rule-based Answer Extraction      | ✅     |
| Token-based API Auth              | ✅     |
| Perplexity LLM Fallback (optional)| ✅     |
| Docker + Compose Support          | ✅     |

---

## 📚 Example PDFs to Try

- Arogya Sanjeevani Policy (Govt Health Policy)
- National Health Insurance (Private)
- Any PDF with standard terms like coverage, exclusions, waiting period

---

## 📬 Contact

Built with 💡 for **HackRx 6.0** – Policy Aware AI Challenge  
Team: HackerXHacker  
