# Google-x-Kaggle-Agents-Intensive-Capstone-Project
AI Mental Wellness Companion – A multi-agent system that detects stress, suggests coping strategies, and generates personalized wellness routines. It tracks emotional patterns over time and provides alerts during high-stress situations to support mental well-being.


# 🧠 AI Mental Wellness Companion & Early Stress Detector

**Capstone Project – Google x Kaggle Agents Intensive**  
**Track:** Agents for Good  
**Author:** Adithya D  
**Date:** Nov 2025

---

## Project Description

Stress, anxiety, and emotional burnout are increasingly common among students and working professionals. Many people lack **instant, private emotional support** or a way to monitor their stress patterns over time. This project addresses that gap by implementing a **multi-agent mental wellness companion** that helps users detect stress early, get personalized support, and maintain long-term emotional health.

The system is built using a **modular multi-agent architecture** with the following key features:

1. **Emotion Detection** – Analyzes user text input to determine mood and stress levels (`neutral`, `stressed`, `high_stress`).  
2. **Coping Strategies** – Provides actionable advice based on stress intensity, such as breathing exercises, short walks, or grounding techniques.  
3. **Daily Routines** – Generates personalized wellness routines aligned with the detected mood, including meditation, journaling, hydration, or rest.  
4. **Escalation Alerts** – Notifies users when stress levels are very high and recommends seeking support from friends, family, or professionals.  
5. **Memory & Logging** – Tracks session-level state (`SessionMemory`) and stores long-term emotional history (`LongTermMemory`) with detailed logging for observability.

The workflow combines **sequential and parallel agent execution**, where emotions are analyzed first, then coping strategies, routines, and escalation checks are executed in parallel. This design ensures a responsive and realistic multi-agent system for mental wellness.

---

## Implementation Highlights

- **Agents:**  
  - `EmotionAnalyzerAgent` – detects mood and assigns stress scores  
  - `StrategyAgent` – generates coping strategies  
  - `RoutineAgent` – builds daily wellness routines  
  - `EscalationAgent` – triggers alerts for high-stress situations  

- **Memory & Logging:** Maintains both short-term session state and long-term mood logs with timestamps  
- **Output:** Returns a structured response including mood, stress score, recommended strategy, routine, and escalation message

---

## Example Usage

```python
user_input = "I feel like I'm going to cry, nothing is working, and I am depressed."
result = wellness_pipeline(user_input)
print(result)



{
  "mood": "high_stress",
  "stress_score": 90,
  "strategy": "Try grounding techniques: 5 things you see, 4 you can touch, 3 you can hear.",
  "routine": ["Breathing exercise", "Talk to a trusted friend", "Rest for 30 minutes"],
  "escalation": "⚠️ You seem highly distressed. You are not alone. Talk to someone you trust."
}

