# Quick Reference Card - Study Personas

## 🎯 Persona Selection Guide

### Need Help With... | Use This Persona
---|---
Exercise problems | `[course]/tutor.json`
Understanding concepts | `[course]/tutor.json`
Weekly planning | `[course]/planner.json`
Exam preparation | `[course]/exam-prep.json`
Study organization | `[course]/planner.json`
Practice tests | `[course]/exam-prep.json`

## 📱 Quick Load URLs

**Template:**
```
https://chat-ai.academiccloud.de/chat?import=https://raw.githubusercontent.com/YOUR_USERNAME/chat-personas/main/COURSE/TYPE.json
```

**Course Codes:**
- `buk` - Computability & Complexity
- `ds` - Diskrete Strukturen
- `elemlds` - ML & Data Science
- `itsec` - IT-Security
- `swt` - Software Engineering

**Types:**
- `tutor.json` - Exercise help
- `planner.json` - Study planning
- `exam-prep.json` - Exam prep

## 💬 Best Prompt Starters

### Tutor Persona
```
"I'm working on this problem: [paste]. My approach is [explain]. Am I on the right track?"
"Can you explain [concept] with a concrete example?"
"Here's my proof attempt. What's wrong with the reasoning?"
```

### Planner Persona
```
"Create a study plan for this week. I have lectures on [days], deadlines on [dates]."
"I'm struggling with [topic]. How should I allocate my time?"
"Plan my exam preparation for [course] in [weeks] weeks."
```

### Exam Prep Persona
```
"My exam is in [weeks] weeks. Create a practice test on [topics]."
"Conduct a mock oral exam on [subject]."
"I keep making mistakes in [area]. Give me targeted practice."
```

## ⚙️ Optimal Settings

| Task | Temperature | Top_p | Tools |
|------|-------------|-------|-------|
| Math/Proofs | 0.3 | 0.6 | None |
| Coding | 0.2 | 0.5 | None |
| Planning | 0.5 | 0.7 | None |
| Brainstorming | 0.7 | 0.8 | Web Search |
| Research | 0.4 | 0.6 | Web Search |
| Diagrams | 0.3 | 0.6 | Image Gen |

## 🛠️ Tool Activation

**Enable in Settings → Tools:**

- 🔍 **Web Search**: Current info, security news, ML papers
- 🎨 **Image Generation**: Diagrams, automata, UML, graphs
- ✏️ **Image Editing**: Annotate diagrams
- 🔊 **TTS**: Listen to explanations

## 📚 Arcana Integration

**Indexed:**
- ✅ `buk` - Computability (6.79 GB)

**To Index:**
- ⏳ `ds` - Diskrete Strukturen (3.04 GB)
- ⏳ `elemlds` - ML & Data Science (1.24 GB)
- ⏳ `itsec` - IT-Security (2.02 GB)
- ⏳ `swt` - Software Engineering (1.62 GB)

**Usage:** Load persona → Attach Arcana → Ask course-specific questions

## 🎓 Course-Specific Tips

### buk (Computability)
- Focus: Proofs, reductions, automata
- Use tutor for: Proof guidance
- Enable: None (math-heavy)

### ds (Discrete Structures)
- Focus: Logic, combinatorics, graphs
- Use tutor for: Induction proofs
- Enable: None (formula-heavy)

### elemlds (ML)
- Focus: Algorithms + implementation
- Use tutor for: Code + theory
- Enable: Web Search (latest research)

### itsec (Security)
- Focus: Attacks, defenses, crypto
- Use tutor for: Security analysis
- Enable: Web Search (current vulns)

### swt (Software Eng)
- Focus: Design patterns, UML, processes
- Use tutor for: Design decisions
- Enable: Image Generation (diagrams)

## ⏰ Study Workflow

**Daily:**
1. Morning: Review previous notes (10 min)
2. After lecture: Same-day review (30 min)
3. Evening: Exercise work with Tutor (1-2 hours)

**Weekly:**
1. Monday: Plan week with Planner
2. Tue-Thu: Study blocks + Tutor help
3. Friday: Weekly review
4. Weekend: Practice tests with Exam Prep

**Pre-Exam:**
- 8 weeks: Start Exam Prep persona
- 4 weeks: Daily practice tests
- 2 weeks: Focus on weak areas
- 1 week: Light review only

## 🔖 Bookmark These

Create browser bookmarks for quick access:

1. **Main Chat AI**: https://chat-ai.academiccloud.de/
2. **Documentation**: https://docs.hpc.gwdg.de/services/ai-services/chat-ai/
3. **Your Personas**: Replace YOUR_USERNAME and bookmark each course

## 📊 Model Selection

**Default in personas:** DeepSeek V4.1 Flash (best for reasoning)

**Alternatives:**
- Fast tasks: Meta Llama 3.1 8B
- Balanced: Qwen 3.6 35B
- Explanations: Gemma 3 27B

## ⚡ Power User Tips

1. **Combine personas with Arcanas** for course-specific help
2. **Use Web Search** for security/ML current events
3. **Enable Memory: Learn** for ongoing conversations
4. **Export conversations** to save study sessions
5. **Create custom personas** for your learning style
6. **Use Image Generation** for automata/UML diagrams
7. **Start with hints** before asking for full solutions

## 🚨 Common Mistakes to Avoid

❌ "Do my homework" → ✅ "Help me understand this problem"
❌ "Give me the answer" → ✅ "What's the approach for this type?"
❌ Vague questions → ✅ Specific, contextual questions
❌ No Arcana attachment → ✅ Attach relevant course materials
❌ Wrong tool settings → ✅ Match settings to task type

## 📞 Support

- Platform issues: kisski-support@gwdg.de
- Documentation: https://docs.hpc.gwdg.de/services/ai-services/chat-ai/faq/
