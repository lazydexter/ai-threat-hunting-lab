
# 🚀 AI-Assisted Threat Hunting Lab (Beginner Project)

This project explores how **AI (LLMs)** can assist in threat hunting by analyzing Windows logs and process trees.  
I set up a local lab using **Ollama + Mistral** on my Windows workstation, integrated **Sysmon & Security logs**, and generated AI-powered SOC-style summaries.

---

## 🔎 Phase 1 – Proof of Concept (Completed)
- Installed Sysmon with SwiftOnSecurity config  
- Exported **Sysmon + Security logs** into text/JSON  
- Fed process trees into **Mistral (via Ollama)**  
- AI generated:  
  - Executive summary of suspicious activity  
  - MITRE ATT&CK mapping  
  - Extracted IOCs  
  - Severity rating  



---

## 💡 Key Learning
Even as a beginner, I saw how LLMs can:
- Save time in **initial triage**  
- Provide structured **incident summaries**  
- Highlight MITRE ATT&CK techniques automatically  

AI doesn’t replace defenders — it **augments SOC analysts**.

---

## 📌 Roadmap
**Phase 2 (Next):**
- Automate pipeline: Sysmon → JSON → Ollama → Summary  
- Correlate across multiple log sources (DNS, Proxy, EDR)  
- Compare models (Mistral vs Gemma vs LLaMA)  

**Phase 3 (Future):**
- Integrate with **SIEM (Splunk/ELK)**  
- Enrich findings with **Threat Intel feeds**  
- Export **ATT&CK heatmaps**  
- Auto-populate incident tickets  

---

