# Prompt Library

This repo contains a structured collection of prompts designed for multiple use cases.  
All prompts follow a consistent format with **Objective**, **Prompt**, and **Example Output** sections for clarity and reuse.

## How to Use

1. **Browse Categories**: Choose the category that matches your use case
2. **Select Prompt**: Pick the specific prompt that fits your needs
3. **Copy & Customize**: Copy the prompt text and modify it with your specific requirements
4. **Test & Iterate**: Use the prompt with your AI tool and refine based on results

### Example Usage

**Scenario**: You need to classify customer support tickets

1. Go to [Customer Support → Ticket Classification](./customer-support/ticket-classification)
2. Copy the prompt from `prompt-v1.md`
3. Replace the example ticket with your actual ticket text
4. Run it through ChatGPT/Claude/etc.

**Original prompt:**
```
Classify the following support ticket into a category and priority...
```

**Your customized version:**
```
Classify the following support ticket into a category and priority...

Ticket:
"Hi, my login isn't working and I have a presentation in 2 hours. Please help!"
```

## Structure

- **[Content Generation](./content-generation)** - Creative and informational text generation
- **[Data Analysis](./data-analysis)** - Data-focused prompts for classification, transformation, extraction, question answering, sentiment analysis, SQL generation, and summarization
- **[Coding](./coding)** - Programming and software development prompts for code generation, explanation, and debugging
- **[Customer Support](./customer-support)** - Ticket classification and empathetic response generation
- **[Education](./education)** - Lesson planning and quiz generation
- **[Professional Writing](./professional-writing)** - Emails and structured reports

## Prompt Format

Each prompt is written in this format:

### **Prompt: [Task Name]**

**Objective:** Short description of the task.  

**Prompt:**
```Prompt text goes here```

**Example Output:**\
```A typical output for the given prompt```