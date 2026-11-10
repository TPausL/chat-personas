# Chat AI Study Personas - Complete Guide

## 📚 Overview

This directory contains **5 comprehensive study personas** (one per course) designed to work with the [GWDG Chat AI](https://chat-ai.academiccloud.de/) platform. Each persona integrates with your course Arcana and can handle all study tasks.

### Course Structure

```
chat-personas/
├── buk.json      Computability and Complexity
├── ds.json       Diskrete Strukturen
├── elemlds.json  Elements of ML and Data Science
├── itsec.json    IT-Security
└── swt.json      Software Engineering
```

### Key Features

Each persona includes:
- ✅ **Arcana integration** - Direct access to your course materials
- ✅ **Tools enabled** - Web search, image generation when helpful
- ✅ **Large context** - Qwen 3.5 397B A17B (400K+ tokens)
- ✅ **All-in-one** - Exercises, planning, and exam prep in one

---

## 🚀 Quick Start

### Loading a Persona

1. **Via URL Import** (recommended):
   ```
   https://chat-ai.academiccloud.de/chat?import=https://raw.githubusercontent.com/tpausl/chat-personas/main/buk.json
   ```

2. **Via Data URI** (for local files):
   - Copy the JSON content
   - URL-encode it
   - Use: `https://chat-ai.academiccloud.de/chat/?import=data:application/json,<encoded-json>`

3. **Via Web Interface**:
   - Go to https://chat-ai.academiccloud.de/
   - Click the upload/import button
   - Select the JSON file

### Example Usage Links

Replace `YOUR_USERNAME` with your GitHub username after pushing:

| Course | Persona Link |
|--------|--------------|
| **Computability & Complexity** | [Load buk.json](https://chat-ai.academiccloud.de/chat?import=https://raw.githubusercontent.com/tpausl/chat-personas/main/buk.json) |
| **Diskrete Strukturen** | [Load ds.json](https://chat-ai.academiccloud.de/chat?import=https://raw.githubusercontent.com/tpausl/chat-personas/main/ds.json) |
| **ML & Data Science** | [Load elemlds.json](https://chat-ai.academiccloud.de/chat?import=https://raw.githubusercontent.com/tpausl/chat-personas/main/elemlds.json) |
| **IT-Security** | [Load itsec.json](https://chat-ai.academiccloud.de/chat?import=https://raw.githubusercontent.com/tpausl/chat-personas/main/itsec.json) |
| **Software Engineering** | [Load swt.json](https://chat-ai.academiccloud.de/chat?import=https://raw.githubusercontent.com/tpausl/chat-personas/main/swt.json) |

---

## 🎯 How to Use Your Persona

Each persona handles **all study tasks** - just tell it what you need:

### Exercise Help
```
"I'm working on this problem: [paste]. My approach is [explain]. Am I on the right track?"
"Can you explain [concept] using the lecture notes?"
"Here's my proof attempt. What's wrong with the reasoning?"
```

### Study Planning
```
"I have exams in 8 weeks. Create a study plan for [course]."
"This week I have lectures on [topics]. How should I structure my study time?"
"Help me plan my week considering these deadlines: [list]"
```

### Exam Preparation
```
"My exam is in 4 weeks. Create practice questions on [topics]."
"Conduct a mock oral exam on [subject]."
"I keep making mistakes in [area]. Give me targeted practice."
"Create a summary sheet of important concepts."
```

### The persona will automatically:
- ✅ Use your course Arcana materials
- ✅ Enable web search when relevant (especially for IT-Security, ML)
- ✅ Generate diagrams when helpful (for DS graphs, SWT UML)
- ✅ Adapt to your needs (tutor/planner/exam coach)

---

## 🛠️ Chat AI Features

### Model Selection

All personas use **Qwen 3.5 397B A17B** because:
- ✅ **Huge context window** (400K+ tokens) - perfect for Arcana RAG
- ✅ **Excellent reasoning** - handles math, proofs, code
- ✅ **Multi-modal** - can process images when needed
- ✅ **Self-hosted** - privacy-respecting, free

### Tools (Already Enabled)

All personas have tools enabled and will use them automatically:

| Tool | When It's Used |
|------|----------------|
| 🔍 **Web Search** | Current security vulns (itsec), latest ML research (elemlds) |
| 🎨 **Image Generation** | Graph diagrams (ds), UML diagrams (swt), automata (buk) |
| 🔊 **Text-to-Speech** | When you want to listen instead of read |

### Memory Modes

- **None** - Each conversation is independent
- **Recall** - Adds previous messages for context
- **Learn** - Updates memory with relevant parts (recommended for ongoing study)

---

## 📖 Arcana Integration

**Arcanas are already embedded in each persona!** No need to attach manually.

### Current Arcana Status

| Course | Arcana ID | Status | Size |
|--------|-----------|--------|------|
| Computability | `buk-46d227bd...` | ✅ Indexed | 6.79 GB |
| Diskrete Strukturen | `ds-f63a8c86...` | ⏳ Not Indexed | 3.04 GB |
| ML & Data Science | `elemlds-6c70025a...` | ⏳ Not Indexed | 1.24 GB |
| IT-Security | `itsec-264b0168...` | ⏳ Not Indexed | 2.02 GB |
| Software Engineering | `swt-2bb96f17...` | ⏳ Not Indexed | 1.62 GB |

### Next Steps

1. **Index remaining Arcanas** in Chat AI for full functionality
2. Load any persona - Arcana is already attached
3. Ask questions - persona will use your course materials automatically

**Example:**
```
Load buk.json → Ask: "Explain this exercise using lecture 5" 
→ Persona automatically uses your buk Arcana materials
```

---

## 💡 Best Practices

### For Effective Learning

1. **Start with the Tutor** for understanding concepts
2. **Use the Planner** to organize your study time
3. **Practice with Exam Prep** before tests
4. **Combine with Arcanas** for course-specific context
5. **Enable Web Search** for current topics (security, ML)

### Prompt Engineering Tips

**Good prompts:**
- "I'm trying to prove that this language is not regular. Here's my attempt: [paste]. What's wrong with my approach?"
- "Create a 4-week study plan for my IT-Security exam. Topics: cryptography, network security, web security. I can study 2 hours daily."
- "Explain the difference between NP-hard and NP-complete with concrete examples."

**Avoid:**
- "Do my homework" (violates academic integrity)
- "Give me the answer" (you won't learn)
- Vague questions like "I don't get it" (be specific)

### Study Workflow Example

**Monday (after lecture):**
1. Load **Planner** persona → "Plan my week for Computability"
2. Follow the plan → study blocks scheduled

**Tuesday (exercise work):**
1. Load **Tutor** persona + attach Arcana
2. Work through exercises with guidance
3. Ask for hints, not solutions

**Wednesday (review):**
1. Use **Tutor** to clarify difficult concepts
2. Create summary notes

**Weekend (exam prep, 4 weeks before):**
1. Load **Exam Prep** persona
2. Take practice test on week's topics
3. Review incorrect answers with **Tutor**

---

## 🔧 Advanced Features

### Creating Custom Personas

You can modify existing personas or create new ones:

```json
{
  "title": "My Custom Tutor",
  "subtitle": "Specialized for my learning style",
  "model": "deepseek-v4.1-flash-1017",
  "model-name": "DeepSeek V4.1 Flash",
  "temperature": 0.3,
  "top_p": 0.6,
  "enable_tools": false,
  "messages": [
    {
      "role": "system",
      "content": "Your custom system prompt here..."
    },
    {
      "role": "info",
      "content": "Your welcome message here..."
    }
  ]
}
```

### Sharing Personas

1. Push to GitHub
2. Share the raw URL
3. Others can import with: `https://chat-ai.academiccloud.de/chat?import=<raw-url>`

### Bookmarking Personas

Create browser bookmarks with data URIs for quick access:
```
https://chat-ai.academiccloud.de/chat/?import=data:application/json,{...}
```

---

## 📊 Chat AI Platform Capabilities

### What Chat AI Offers

✅ **Privacy-focused**: No data stored on external servers (except external models)
✅ **Multiple models**: Access to various open-source and commercial models
✅ **Tools integration**: Web search, image generation, TTS
✅ **Personas**: Customizable AI personalities
✅ **Arcanas/RAG**: Connect your own documents
✅ **Memory**: Conversational context across sessions
✅ **File attachments**: Upload PDFs, code, images for context
✅ **Export/Import**: Save and share conversations
✅ **Multi-language**: German and English support

### Model Comparison

| Model | Best For | Speed | Quality |
|-------|----------|-------|---------|
| DeepSeek V4.1 Flash | Math, code, reasoning | Fast | ⭐⭐⭐⭐⭐ |
| Qwen 3.6 35B | General tasks | Medium | ⭐⭐⭐⭐ |
| Meta Llama 3.1 8B | Quick questions | Very Fast | ⭐⭐⭐ |
| Gemma 3 27B | Explanations | Medium | ⭐⭐⭐⭐ |

### External vs. Internal Models

**Internal (GWDG-hosted):**
- ✅ Free to use
- ✅ Privacy-respecting
- ✅ No data leaves GWDG
- ✅ All tools work
- ❌ Limited to available models

**External (OpenAI, Anthropic):**
- ✅ Latest models
- ❌ Costs money
- ❌ Data leaves EU
- ❌ Some tools don't work

---

## 🎓 Course-Specific Tips

### Computability & Complexity (buk)
- **Tutor**: Best for proof guidance and reduction explanations
- **Planner**: Schedule regular proof practice
- **Exam Prep**: Focus on constructing rigorous proofs
- **Arcana**: ✅ Already indexed - attach for lecture-specific help

### Diskrete Strukturen (ds)
- **Tutor**: Great for induction proofs and combinatorics
- **Planner**: Emphasize formula memorization schedules
- **Exam Prep**: Practice both calculations and proofs
- **Arcana**: ⏳ Index first for best results

### ML & Data Science (elemlds)
- **Tutor**: Excellent for algorithm explanations + code
- **Planner**: Balance theory study with coding practice
- **Exam Prep**: Prepare for both theory and implementation questions
- **Tools**: Enable Web Search for latest ML research
- **Arcana**: ⏳ Index first

### IT-Security (itsec)
- **Tutor**: Strong on attack/defense analysis
- **Planner**: Include time for security news and CTF practice
- **Exam Prep**: Practice both crypto calculations and security analysis
- **Tools**: Enable Web Search for current vulnerabilities
- **Arcana**: ⏳ Index first

### Software Engineering (swt)
- **Tutor**: Great for design pattern explanations
- **Planner**: Coordinate with team project schedules
- **Exam Prep**: Focus on scenario-based design decisions
- **Tools**: Enable Image Generation for UML diagrams
- **Arcana**: ⏳ Index first

---

## 📝 Next Steps

1. **Push to GitHub** to enable URL imports:
   ```bash
   git init
   git add .
   git commit -m "Initial study personas setup"
   git remote add origin https://github.com/tpausl/chat-personas.git
   git push -u origin main
   ```

2. **Index remaining Arcanas** in Chat AI for RAG support

3. **Bookmark your favorite personas** for quick access

4. **Start using** the personas in your daily study routine!

5. **Customize** personas to match your learning style

---

## 📚 Additional Resources

- [Chat AI Documentation](https://docs.hpc.gwdg.de/services/ai-services/chat-ai/index.html)
- [Chat AI Features](https://docs.hpc.gwdg.de/services/ai-services/chat-ai/features/index.html)
- [Available Models](https://docs.hpc.gwdg.de/services/ai-services/chat-ai/models/index.html)
- [Personas Repository](https://github.com/gwdg/chat-ai-personas)
- [Arcana/RAG Documentation](https://docs.hpc.gwdg.de/services/ai-services/arcana/index.html)

---

## 🆘 Support

For issues with Chat AI platform:
- Email: kisski-support@gwdg.de
- FAQ: https://docs.hpc.gwdg.de/services/ai-services/chat-ai/faq/index.html

For these personas:
- Check the [STUDY-SETUP.md](./STUDY-SETUP.md) for general study strategies
- Customize personas to fit your needs
