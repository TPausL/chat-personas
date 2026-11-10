# Complete Chat AI Capabilities Guide

## 🌟 Overview

GWDG Chat AI is a comprehensive AI platform offering multiple models, tools, and customization options for academic and research use.

**Access:** https://chat-ai.academiccloud.de/

---

## 🤖 Available Models

### Self-Hosted Models (Free, Privacy-Respecting)

| Model | Parameters | Best For | Speed |
|-------|------------|----------|-------|
| **DeepSeek V4.1 Flash** | Proprietary | Math, code, reasoning | Fast |
| **Qwen 3.6 35B A3B** | 35B | General tasks | Medium |
| **Qwen 3 30B A3B Instruct** | 30B | Instructions, following | Medium |
| **Meta Llama 3.1 8B** | 8B | Quick tasks | Very Fast |
| **Gemma 3 27B Instruct** | 27B | Explanations | Medium |
| **Llama 3.3 70B Instruct** | 70B | Complex reasoning | Slower |

### External Models (Paid, External Processing)

| Model | Provider | Notes |
|-------|----------|-------|
| ChatGPT | OpenAI | Latest GPT models |
| Claude | Anthropic | Strong reasoning |

**Note:** External models cost money and data leaves EU. Tools may not work.

---

## 🛠️ Tools & Capabilities

### 1. Web Search 🔍

**What it does:** Searches the web for current information

**Use cases:**
- Latest security vulnerabilities (CVEs)
- Recent ML research papers
- Current events for case studies
- Fact-checking information

**How to enable:**
Settings → Tools → Web Search ✓

**Example prompts:**
- "What are the latest critical CVEs this month?"
- "Find recent papers on transformer efficiency"
- "What's the current state of quantum computing?"

**Limitations:**
- Only works with GWDG-hosted models
- Search query is auto-generated from your conversation

---

### 2. Image Generation 🎨

**What it does:** Creates images from text descriptions

**Use cases:**
- Automata state diagrams
- Graph theory visualizations
- UML diagrams (basic)
- Flowcharts and process diagrams
- Concept illustrations

**How to enable:**
Settings → Tools → Image Generation ✓

**Example prompts:**
- "Generate a DFA that accepts strings with even number of 0s"
- "Create a graph with 5 nodes showing a Hamiltonian path"
- "Draw a class diagram for a library system"

**Limitations:**
- Text in images may be garbled
- Complex diagrams may need refinement
- Only works with GWDG-hosted models

---

### 3. Image Editing ✏️

**What it does:** Modifies existing images

**Use cases:**
- Annotate diagrams
- Mark up screenshots
- Add labels to visualizations
- Highlight important areas

**How to enable:**
Settings → Tools → Image Editing ✓

**Example prompts:**
- "Add arrows showing the state transitions"
- "Highlight the vulnerable components in red"
- "Label each layer of the neural network"

**Limitations:**
- Requires uploading an image first
- Only works with GWDG-hosted models

---

### 4. Text-to-Speech 🔊

**What it does:** Converts text responses to audio

**Use cases:**
- Listen to explanations while commuting
- Accessibility
- Multi-tasking during review
- Language learning

**How to enable:**
Settings → Tools → Text-to-Speech ✓

**Example prompts:**
- "Explain NP-completeness, then read it aloud"
- "Summarize this paper and convert to audio"

**Limitations:**
- Audio quality varies by language
- German accent may be noticeable
- Only works with GWDG-hosted models

---

## 🎭 Personas

### What are Personas?

Personas are pre-configured AI personalities with specific:
- System prompts (role/expertise)
- Model settings (temperature, top_p)
- Welcome messages
- Optional: Attached Arcanas

### Creating Personas

**JSON Structure:**
```json
{
  "title": "My Persona",
  "subtitle": "What it does",
  "model": "deepseek-v4.1-flash-1017",
  "model-name": "DeepSeek V4.1 Flash",
  "temperature": 0.5,
  "top_p": 0.8,
  "enable_tools": false,
  "messages": [
    {
      "role": "system",
      "content": "You are a helpful assistant..."
    },
    {
      "role": "info",
      "content": "Welcome message for users"
    }
  ]
}
```

### Loading Personas

**Method 1: URL Import**
```
https://chat-ai.academiccloud.de/chat?import=<URL-to-JSON>
```

**Method 2: Data URI**
```
https://chat-ai.academiccloud.de/chat/?import=data:application/json,{...}
```

**Method 3: Web Interface**
- Click upload/import button
- Select JSON file

### Sharing Personas

1. Host JSON publicly (GitHub, personal website)
2. Share the URL
3. Others import with URL parameter

**Example:**
```
https://chat-ai.academiccloud.de/chat?import=https://raw.githubusercontent.com/user/repo/main/persona.json
```

---

## 📚 Arcanas (RAG - Retrieval Augmented Generation)

### What are Arcanas?

Arcanas are personal knowledge bases that Chat AI can query. They allow the AI to:
- Access your documents
- Answer questions based on your materials
- Provide context-specific responses

### Creating Arcanas

1. Go to Chat AI interface
2. Click "Arcana" or "Knowledge Base"
3. Upload documents (PDF, TXT, MD, etc.)
4. Wait for indexing

### Current Arcana Status

| Name | Size | Status | Use |
|------|------|--------|-----|
| buk | 6.79 GB | ✅ Indexed | Computability course materials |
| ds | 3.04 GB | ⏳ Not Indexed | Discrete Structures materials |
| elemlds | 1.24 GB | ⏳ Not Indexed | ML & Data Science materials |
| itsec | 2.02 GB | ⏳ Not Indexed | IT-Security materials |
| swt | 1.62 GB | ⏳ Not Indexed | Software Engineering materials |

### Using Arcanas

1. **Attach to conversation:**
   - Click "Attach" (+) button
   - Select your Arcana

2. **Ask questions:**
   - "Explain this concept from lecture 5"
   - "What did the professor say about NP-completeness?"
   - "Summarize the key points from the exercise sheet"

3. **Combine with personas:**
   - Load a persona
   - Attach relevant Arcana
   - Get specialized help with your materials

### Best Practices

✅ **Do:**
- Index all course materials
- Organize by course/semester
- Update regularly with new lectures
- Combine with relevant personas

❌ **Don't:**
- Upload copyrighted materials you don't own
- Include sensitive personal information
- Expect 100% accuracy (verify important info)

---

## 💾 Memory & Context

### Memory Modes

**1. None**
- Each conversation is independent
- No context from previous messages
- Best for: One-off questions

**2. Recall**
- Adds previous messages to context
- Maintains conversation flow
- Best for: Multi-turn discussions

**3. Learn** (Recommended)
- Extends Recall
- Updates memory with relevant parts
- Creates persistent knowledge
- Best for: Ongoing study sessions

### Managing Memory

**View Memory:**
- Settings → Memory Settings
- See what the AI has learned

**Clear Memory:**
- Settings → Clear button
- Removes all stored data

**Export Conversations:**
- Click download/export button
- Save as JSON or text
- Import later to continue

---

## ⚙️ Configuration Options

### Completion Settings

**Temperature** (0-2)
- Controls creativity vs. predictability
- Low (0.1-0.3): Precise, deterministic (math, code)
- Medium (0.4-0.6): Balanced (general use)
- High (0.7-2.0): Creative (brainstorming)

**Top_p** (0-1)
- Controls token selection pool
- Low (0.1-0.5): Focused, conservative
- Medium (0.6-0.8): Balanced
- High (0.9-1.0): Diverse, creative

**Recommended Combinations:**

| Task | Temperature | Top_p |
|------|-------------|-------|
| Math proofs | 0.2-0.3 | 0.5-0.6 |
| Programming | 0.2-0.3 | 0.5-0.6 |
| Explanations | 0.4-0.5 | 0.6-0.7 |
| Planning | 0.5-0.6 | 0.7-0.8 |
| Brainstorming | 0.7-0.9 | 0.8-0.9 |
| Creative writing | 0.9-1.2 | 0.9-1.0 |

### System Prompts

**What they do:** Define the AI's role and behavior

**Example:**
```
You are an expert mathematics tutor. You explain concepts clearly,
provide examples, and guide students to understanding without
simply giving answers. You use formal notation when appropriate
and explain in [language].
```

**Tips:**
- Be specific about expertise
- Define interaction style
- Specify language preference
- Include any constraints

---

## 📎 File Attachments

### Supported Formats

- **Documents:** PDF, DOCX, TXT, MD, RTF
- **Code:** Any programming language files
- **Data:** CSV, JSON, XML, YAML
- **Images:** PNG, JPG, GIF, SVG

### Use Cases

**Study Materials:**
- Attach lecture notes
- Ask questions about specific content
- Get summaries and explanations

**Code Projects:**
- Attach source files
- Get debugging help
- Request code reviews

**Exercise Sheets:**
- Attach problem statements
- Get guided help (not solutions)
- Verify your approach

### How to Attach

1. Click "+" or "Attach" button
2. Select file(s)
3. Wait for upload
4. Reference in your prompt

**Example prompts:**
- "Explain the algorithm in the attached PDF"
- "What's wrong with the code in main.py?"
- "Summarize the key points from this lecture"

---

## 🌐 Web Interface Features

### Layout Overview

**Header:**
- Model selection dropdown
- Settings button
- New chat button

**Sidebar:**
- Conversation history
- Arcana management
- Persona imports

**Main Chat:**
- Message history
- Input box
- Attachment button
- Tool toggles

**Footer:**
- Terms of use
- FAQ link
- Language switcher (EN/DE)
- Version info

### Keyboard Shortcuts

- `Ctrl+Enter`: Send message
- `Ctrl+Shift+M`: Toggle memory mode
- `Ctrl+Shift+T`: Toggle tools
- `Esc`: Cancel generation

### Dark/Light Mode

- Click sun/moon icon
- Or: Settings → Appearance
- Auto-detects system preference

---

## 🔒 Privacy & Security

### Data Protection

**GWDG-Hosted Models:**
- ✅ Data stays in EU (Germany)
- ✅ No long-term storage
- ✅ Academic Cloud account required
- ✅ GDPR compliant

**External Models:**
- ⚠️ Data leaves EU
- ⚠️ Subject to provider's policies
- ⚠️ May be used for training
- ⚠️ Additional costs

### What's Stored

**Not Stored:**
- Conversation content (deleted after session)
- Personal information
- Attached files (deleted after processing)

**Stored Temporarily:**
- Session state (browser localStorage)
- Memory (if enabled, browser localStorage)

### Best Practices

✅ **Safe:**
- Course materials
- Code you wrote
- Public research papers
- Your own notes

❌ **Avoid:**
- Personal identifiable information
- Confidential research data
- Licensed/copyrighted content
- API keys or passwords

---

## 📊 Performance & Limits

### Rate Limits

- **Free tier:** Unlimited for GWDG models
- **External models:** Pay-per-use
- **Concurrent requests:** Limited during peak times

### Context Length

- **Maximum context:** Varies by model
- **DeepSeek V4.1:** ~128K tokens
- **Qwen 3.6:** ~32K tokens
- **Llama 3.1:** ~8K tokens

**Tips:**
- Long conversations may lose early context
- Summarize periodically for long sessions
- Export important conversations

### Response Time

| Model | Typical Response |
|-------|-----------------|
| Llama 3.1 8B | 1-3 seconds |
| DeepSeek V4.1 | 3-8 seconds |
| Qwen 3.6 35B | 5-15 seconds |
| Llama 3.3 70B | 10-30 seconds |

---

## 🎓 Academic Use Cases

### For Students

**Daily Study:**
- Explain difficult concepts
- Work through exercises (with guidance)
- Create study plans
- Generate practice questions

**Exam Preparation:**
- Mock oral exams
- Practice tests
- Summary sheets
- Weak area identification

**Projects:**
- Code debugging
- Design reviews
- Documentation help
- Research assistance

### For Researchers

**Literature Review:**
- Summarize papers
- Extract key findings
- Compare approaches
- Generate citations

**Writing:**
- Draft sections
- Improve clarity
- Check consistency
- Translate (EN↔DE)

**Analysis:**
- Data interpretation
- Method selection
- Statistical guidance
- Visualization ideas

### For Teachers

**Course Materials:**
- Generate exercises
- Create examples
- Design rubrics
- Prepare slides

**Student Support:**
- FAQ generation
- Automated feedback
- Personalized hints
- Office hour prep

---

## 🔧 Advanced Features

### Model Context Protocol (MCP)

**What is MCP:**
- Standard for connecting AI to external tools
- Extend Chat AI with custom servers
- Access databases, APIs, file systems

**Setup:**
1. Settings → MCP Servers
2. Add server URL
3. Configure authentication
4. Use in conversations

**Use Cases:**
- Database queries
- API integrations
- Custom tools
- Workflow automation

### API Access

**For developers:**
- REST API available
- Same models as web interface
- Programmatic access
- Batch processing

**Documentation:**
https://docs.hpc.gwdg.de/services/ai-services/saia/index.html

### VS Code Integration

**CoCo AI:**
- Use Chat AI models in VS Code
- Code completion
- Inline explanations
- File-aware assistance

**Setup:**
https://docs.hpc.gwdg.de/services/coco

---

## 📱 Mobile & Accessibility

### Mobile Access

- Responsive web design
- Works on tablets and phones
- Touch-optimized interface
- Same features as desktop

### Accessibility Features

- **Screen reader support:** Semantic HTML
- **Keyboard navigation:** Full keyboard access
- **High contrast:** Dark mode available
- **Text-to-speech:** Built-in TTS tool
- **Language support:** German and English

---

## 🆘 Troubleshooting

### Common Issues

**"Model not available"**
- Try a different model
- Check service status
- Wait and retry (may be temporary)

**"Tool not working"**
- Ensure tool is enabled in settings
- Only works with GWDG-hosted models
- Check browser console for errors

**"Slow responses"**
- High server load
- Try less busy times
- Use smaller models for quick tasks

**"Memory not persisting"**
- Check browser settings (localStorage)
- Not using "Learn" mode
- Browser privacy settings blocking storage

**"Can't import persona"**
- Check JSON syntax
- Ensure URL is publicly accessible
- Verify model name is valid

### Getting Help

1. **FAQ:** https://docs.hpc.gwdg.de/services/ai-services/chat-ai/faq/
2. **Documentation:** https://docs.hpc.gwdg.de/services/ai-services/chat-ai/
3. **Email:** kisski-support@gwdg.de
4. **Status Page:** Check for service outages

---

## 🚀 Future Developments

### Planned Features

- More open-source models
- Improved image generation
- Voice input (speech-to-text)
- Enhanced MCP support
- Better mobile experience
- Collaborative features
- Advanced RAG capabilities

### Community Contributions

- Submit personas to: https://github.com/gwdg/chat-ai-personas
- Report issues and suggestions
- Share best practices
- Contribute documentation

---

## 📚 Resources

### Official Documentation

- [Chat AI Main Docs](https://docs.hpc.gwdg.de/services/ai-services/chat-ai/index.html)
- [Features Guide](https://docs.hpc.gwdg.de/services/ai-services/chat-ai/features/index.html)
- [Models List](https://docs.hpc.gwdg.de/services/ai-services/chat-ai/models/index.html)
- [Personas Repo](https://github.com/gwdg/chat-ai-personas)
- [Arcana/RAG Docs](https://docs.hpc.gwdg.de/services/ai-services/arcana/index.html)
- [SAIA Backend](https://docs.hpc.gwdg.de/services/ai-services/saia/index.html)
- [CoCo AI (VS Code)](https://docs.hpc.gwdg.de/services/coco)

### Community Resources

- [Persona Catalog](https://github.com/gwdg/chat-ai-personas/blob/main/PERSONAS.md)
- [Example Personas](https://docs.hpc.gwdg.de/services/ai-services/chat-ai/features/personas/index.html#example-personas)
- [Research Paper](https://www.researchsquare.com/article/rs-6648693/v1)

---

## 🎯 Quick Start Checklist

- [ ] Create Academic Cloud account
- [ ] Access https://chat-ai.academiccloud.de/
- [ ] Select appropriate model for your task
- [ ] Enable relevant tools (Web Search, Image Gen, etc.)
- [ ] Set memory mode to "Learn" for ongoing sessions
- [ ] Upload course materials to Arcanas
- [ ] Import study personas from this repository
- [ ] Bookmark frequently used personas
- [ ] Configure optimal settings for your workflow
- [ ] Start using AI assistance in your studies!
