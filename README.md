# Diffy - AI Calculus Tutor

Free real-time derivative solver with AI step-by-step explanations, 3D visualizations, and C++ export for embedded systems.

## Tagline

Calculus made simple - AI that teaches, not just solves

## Why Diffy

Unlike Wolfram/Symbolab that give static answers, Diffy acts like a personal tutor:

| Feature             | Wolfram/Symbolab    | Diffy (MVP)                  |
|---------------------|---------------------|------------------------------|
| Step Explanations   | One-size-fits-all   | AI-tailored to your level    |
| Visualizations      | Basic 2D graphs     | Interactive 3D + animations  |
| Error Diagnosis     | "Invalid input"     | Pinpoints why you're wrong   |
| Code Export         | None                | C++ (GiNaC) for IoT/embedded |
| Real-Time Collab    | None                | Multiplayer workspace        |
| Price               | $30+/month          | FREE (no credit card)        |

## Tech Stack (All Free)

| Component       | Tool                      | Reason                           |
|-----------------|---------------------------|----------------------------------|
| AI Engine       | SymPy + Llama 3 8B        | Open-source math + free GPU      |
| Backend         | Flask (Python)            | Lightweight, pairs with SymPy    |
| Frontend        | Next.js + TypeScript      | Full-stack expertise             |
| Visuals         | Plotly.js                 | Free 3D plots                    |
| Hosting         | GitHub Pages + HF Spaces  | Free, no credit card             |
| Real-Time       | Socket.io                 | Open-source WebSockets           |

## Developer

**Kier Christian F. Reyes** — Full-Stack + AI/ML

- University of Cabuyao, BSCS 4th Year, Dean's List
- Expertise: C++ (pointers, optimization), Next.js, TypeScript, Cloud Load Balancing, IoT
- Past Projects: AI resume app, Cloud load-balancing visualizer, Full-stack e-commerce
- Built solo in 52 hours for Hackathon 2026

## Project Structure
    diffy-ai/
├── backend/
│ ├── app.py
│ ├── derivative_engine.py
│ ├── cpp_export.py
│ └── requirements.txt
├── frontend/
│ ├── pages/
│ │ ├── index.tsx
│ │ └── result.tsx
│ ├── components/
│ │ ├── Calculator.tsx
│ │ ├── Graph3D.tsx
│ │ └── Steps.tsx
│ └── package.json
├── cpp-export/
│ └── template.cpp
├── ai-explanations/
│ └── prompts.md
└── README.md
## Timeline (52 Hours)

| Phase | Time     | Focus                    | Status   |
|-------|----------|--------------------------|----------|
| 1     | 0-4 hrs  | Setup & Planning         | Done     |
| 2     | 4-10 hrs | Core Derivative Engine   | Next     |
| 3     | 10-18 hrs| AI Step Explanations     | Pending  |
| 4     | 18-28 hrs| Frontend UI              | Pending  |
| 5     | 28-38 hrs| Real-Time Collaboration  | Pending  |
| 6     | 38-46 hrs| Testing & Optimization   | Pending  |
| 7     | 46-52 hrs| Deployment & Pitch       | Pending  |

## Setup

### Clone Repo

```bash
git clone https://github.com/kierreyes/diffy-ai.git
cd diffy-ai
```

### Backend

```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install sympy flask flask-socketio
```

Test SymPy:

```python
from sympy import symbols, diff, sin
x = symbols('x')
f = x**2 * sin(x)
print(diff(f, x))  # 2*x*sin(x) + x**2*cos(x)
```

### Frontend

```bash
cd frontend
npx create-next-app@latest . --typescript --tailwind --app
npm install plotly.js-dist-min socket.io-client
npm run dev
```

### AI (Llama 3 on Colab)

1. Open https://colab.research.google.com/
2. Runtime -> Change runtime type -> GPU
3. Run:

```python
!pip install transformers torch
from transformers import AutoModelForCausalLM, AutoTokenizer
tokenizer = AutoTokenizer.from_pretrained("meta-llama/Meta-Llama-3-8B")
model = AutoModelForCausalLM.from_pretrained("meta-llama/Meta-Llama-3-8B")
```

## Demo

**Input**: `f(x) = x^2 * sin(x)`

**Output**:
1. Derivative: `2x*sin(x) + x^2*cos(x)`
2. AI Steps: "Apply product rule: d/dx[u*v] = u'v + uv'. u=x^2, v=sin(x)"
3. 3D Graph: Interactive plot with tangent animation
4. C++ Export: GiNaC code for embedded systems

Time: < 3 seconds

## Resources

- SymPy: https://docs.sympy.org
- Llama 3: https://huggingface.co/meta-llama/Meta-Llama-3-8B
- GiNaC: https://www.ginac.de
- Plotly.js: https://plotly.com/javascript
- Next.js: https://nextjs.org/docs

## Contact

Kier Christian F. Reyes  
University of Cabuyao, BSCS 4th Year  
reyeskierchristian64@uoc.edu.ph  
Cabuyao City, Calabarzon, PH

enjoy, diffy!!!