### **Prompt: Support Ticket Classifier**

**Objective:** Classify a support ticket by category and priority.

**Prompt:**
```
Classify the following support ticket into a category and priority. Categories: Billing, Technical Issue, Account Access, Feature Request, Other. Priority levels: Low, Medium, High, Urgent. Return JSON.

Ticket:
"Hi, I upgraded yesterday but I was charged twice. Please refund the extra charge."
```

**Example Output:**
```json
{
  "category": "Billing",
  "priority": "High",
  "rationale": "Duplicate charge involves money and needs timely resolution"
}
```
