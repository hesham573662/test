# PoC – Vulnerable JavaScript Library: moment.js (v2.17.1)

## 📌 Summary
A vulnerable version of `moment.js` (v2.17.1) was identified in the production environment, used to handle date/time formatting. This version allows invalid inputs to be accepted, which may lead to flawed logic or abuse in time-sensitive applications.

---

## 🧪 Proof of Concept

### 1. Invalid Date Accepted

```javascript
moment("2025-13-99", "YYYY-MM-DD").isValid(); 
// ➜ returns true (should be false)
