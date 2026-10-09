# SparkLoop: AI that notices when you drift, and pulls you back in.
**A Vibathon 2026 Submission**

## 🚨 The Problem
Students quietly disengage, and nobody notices in time. A student who drifts rarely asks for help. First-year students with low connectivity suffer from boredom with zero feedback, get stuck silently, and are learning alone. 

## 💡 Our Solution: SparkLoop
SparkLoop is an offline-first educational AI that detects *why* students disengage, not just if they get answers wrong. 

**How it works (From Drift to Re-engagement):**
1. **Signal Detection:** Student stalls, skips lessons, or hits an error streak.
2. **AI Classification:** The LLM analyzes the metadata to classify why they drifted (Bored, Stuck, Alone).
3. **Tailored Output:** Generates a highly personalized, constraint-driven 25-word nudge.
4. **Offline Action:** Delivers a 5-minute challenge that doesn't require an active internet connection.

## ⚙️ Technical Design
Built with an offline-first architecture to cache lessons and sync when connectivity returns. 
*   **Frontend:** React PWA / Mobile Web (Offline capabilities)
*   **Backend:** FastAPI / Server
*   **AI Layer:** Claude API (Utilizing Few-Shot, Structured JSON, Constraints, and Role Prompting)
*   **Data / Cache:** SQLite (Local Cache)

## 🚀 Impact & Future Scope
We don't track students. We re-spark them. Rural first-years get a personal coach that works offline. Our validation testing yielded an 8/10 correct classification rate on simulated disengagement signals. 
**Next Steps:** Developing a teacher dashboard and peer-matching capabilities for the "Alone" classification.

## 💻 Running Locally
1. Clone the repository: `git clone https://github.com/your-username/sparkloop.git`
2. Install Python dependencies: `pip install -r requirements.txt`
3. Set your Claude API key in a `.env` file: `CLAUDE_API_KEY=your_key_here`
4. Run the FastAPI backend: `uvicorn main:app --reload`
5. Navigate to the `client` folder and start the React PWA: `npm install && npm start`
