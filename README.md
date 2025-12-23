<!-- Hero Banner -->
import { Code, Sparkles, Terminal, Cpu, Github, Layers, Zap, Star, Binary } from 'lucide-react';
import { useState } from 'react';

const bannerDesigns = [
  {
    id: 1,
    name: "Gradient Dreams",
    component: () => (
      <div className="relative w-full h-full bg-gradient-to-r from-indigo-600 via-purple-600 to-pink-600 overflow-hidden">
        {/* Animated background pattern */}
        <div className="absolute inset-0 opacity-20">
          <div className="absolute inset-0" style={{
            backgroundImage: `
              linear-gradient(30deg, transparent 12%, rgba(255,255,255,.1) 12%, rgba(255,255,255,.1) 13%, transparent 13%),
              linear-gradient(150deg, transparent 12%, rgba(255,255,255,.1) 12%, rgba(255,255,255,.1) 13%, transparent 13%)
            `,
            backgroundSize: '80px 140px'
          }}></div>
        </div>

        {/* Floating tech icons */}
        <div className="absolute top-8 right-12 opacity-20">
          <Code className="w-24 h-24 text-white" strokeWidth={1} />
        </div>
        <div className="absolute bottom-12 left-12 opacity-20">
          <Terminal className="w-20 h-20 text-white" strokeWidth={1} />
        </div>

        {/* Main content */}
        <div className="relative h-full flex flex-col items-center justify-center text-white px-8">
          <div className="absolute top-8 left-1/2 transform -translate-x-1/2">
            <Sparkles className="w-8 h-8 text-yellow-300 animate-pulse" />
          </div>

          <h1 className="text-7xl font-bold mb-4 bg-gradient-to-r from-white via-purple-100 to-pink-100 bg-clip-text text-transparent text-center">
            Aparna Mohanty
          </h1>

          <div className="flex items-center gap-3">
            <div className="h-px w-12 bg-gradient-to-r from-transparent to-white"></div>
            <p className="text-2xl text-purple-100">
              Full-Stack Developer & AI Learner
            </p>
            <div className="h-px w-12 bg-gradient-to-l from-transparent to-white"></div>
          </div>

          <div className="absolute bottom-8 left-8 text-purple-200/30 font-mono text-sm">
            {'<developer>'}
          </div>
          <div className="absolute bottom-8 right-8 text-purple-200/30 font-mono text-sm">
            {'</developer>'}
          </div>
        </div>
      </div>
    )
  },
  {
    id: 2,
    name: "Minimalist Dark",
    component: () => (
      <div className="relative w-full h-full bg-gradient-to-br from-gray-900 via-slate-900 to-black overflow-hidden">
        {/* Subtle grid */}
        <div className="absolute inset-0 opacity-10" style={{
          backgroundImage: `
            linear-gradient(rgba(255,255,255,0.05) 1px, transparent 1px),
            linear-gradient(90deg, rgba(255,255,255,0.05) 1px, transparent 1px)
          `,
          backgroundSize: '50px 50px'
        }}></div>

        {/* Accent line */}
        <div className="absolute top-0 left-0 right-0 h-1 bg-gradient-to-r from-transparent via-cyan-500 to-transparent"></div>
        <div className="absolute bottom-0 left-0 right-0 h-1 bg-gradient-to-r from-transparent via-cyan-500 to-transparent"></div>

        {/* Corner decorations */}
        <div className="absolute top-8 left-8">
          <div className="w-16 h-16 border-l-2 border-t-2 border-cyan-500/50"></div>
        </div>
        <div className="absolute bottom-8 right-8">
          <div className="w-16 h-16 border-r-2 border-b-2 border-cyan-500/50"></div>
        </div>

        {/* Main content */}
        <div className="relative h-full flex flex-col items-center justify-center text-white px-8">
          <h1 className="text-7xl font-bold mb-4 text-white tracking-tight">
            Aparna Mohanty
          </h1>
          <p className="text-2xl text-gray-400 tracking-wide">
            Full-Stack Developer & AI Learner
          </p>
          
          {/* Decorative code symbol */}
          <div className="absolute top-1/2 left-12 transform -translate-y-1/2">
            <Code className="w-12 h-12 text-cyan-500/30" strokeWidth={1.5} />
          </div>
          <div className="absolute top-1/2 right-12 transform -translate-y-1/2">
            <Terminal className="w-12 h-12 text-cyan-500/30" strokeWidth={1.5} />
          </div>
        </div>
      </div>
    )
  },
  {
    id: 3,
    name: "Neon Code",
    component: () => (
      <div className="relative w-full h-full bg-black overflow-hidden">
        {/* Matrix-like background */}
        <div className="absolute inset-0 opacity-20">
          <div className="font-mono text-xs text-green-500 leading-tight whitespace-pre overflow-hidden">
            {Array.from({ length: 20 }).map((_, i) => (
              <div key={i} className="opacity-40">
                {Array.from({ length: 100 }).map(() => Math.random() > 0.5 ? '1' : '0').join(' ')}
              </div>
            ))}
          </div>
        </div>

        {/* Neon glow circles */}
        <div className="absolute top-1/4 left-1/4 w-64 h-64 bg-cyan-500/20 rounded-full blur-3xl"></div>
        <div className="absolute bottom-1/4 right-1/4 w-64 h-64 bg-purple-500/20 rounded-full blur-3xl"></div>

        {/* Main content */}
        <div className="relative h-full flex flex-col items-center justify-center text-white px-8">
          <div className="flex items-center gap-4 mb-6">
            <Terminal className="w-10 h-10 text-cyan-400" strokeWidth={2} />
            <h1 className="text-7xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 via-blue-500 to-purple-600">
              Aparna Mohanty
            </h1>
            <Code className="w-10 h-10 text-purple-400" strokeWidth={2} />
          </div>
          
          <p className="text-2xl text-cyan-300 font-mono">
            {'>'} Full-Stack Developer & AI Learner
          </p>

          {/* Binary decorations */}
          <div className="absolute bottom-8 left-8 font-mono text-xs text-green-500/40">
            01001000 01000101 01001100 01001100 01001111
          </div>
          <div className="absolute top-8 right-8 font-mono text-xs text-purple-500/40">
            01010111 01001111 01010010 01001100 01000100
          </div>
        </div>
      </div>
    )
  },
  {
    id: 4,
    name: "Geometric Modern",
    component: () => (
      <div className="relative w-full h-full bg-gradient-to-br from-slate-800 via-slate-700 to-slate-900 overflow-hidden">
        {/* Geometric shapes */}
        <div className="absolute top-0 right-0 w-96 h-96 bg-gradient-to-br from-orange-500/30 to-pink-500/30 rounded-full blur-2xl transform translate-x-1/2 -translate-y-1/2"></div>
        <div className="absolute bottom-0 left-0 w-96 h-96 bg-gradient-to-tr from-blue-500/30 to-cyan-500/30 rounded-full blur-2xl transform -translate-x-1/2 translate-y-1/2"></div>

        {/* Geometric patterns */}
        <div className="absolute inset-0 opacity-10">
          {Array.from({ length: 6 }).map((_, i) => (
            <div
              key={i}
              className="absolute border border-white"
              style={{
                width: `${100 + i * 80}px`,
                height: `${100 + i * 80}px`,
                top: '50%',
                left: '50%',
                transform: `translate(-50%, -50%) rotate(${i * 15}deg)`,
              }}
            ></div>
          ))}
        </div>

        {/* Main content */}
        <div className="relative h-full flex flex-col items-center justify-center text-white px-8">
          <div className="backdrop-blur-sm bg-white/5 px-12 py-16 rounded-2xl border border-white/10">
            <h1 className="text-7xl font-bold mb-4 text-white text-center">
              Aparna Mohanty
            </h1>
            <div className="flex items-center gap-3 justify-center">
              <Layers className="w-6 h-6 text-orange-400" />
              <p className="text-2xl text-gray-300">
                Full-Stack Developer & AI Learner
              </p>
              <Cpu className="w-6 h-6 text-cyan-400" />
            </div>
          </div>
        </div>
      </div>
    )
  },
  {
    id: 5,
    name: "Cosmic Purple",
    component: () => (
      <div className="relative w-full h-full bg-gradient-to-br from-purple-900 via-indigo-900 to-blue-900 overflow-hidden">
        {/* Stars */}
        <div className="absolute inset-0">
          {Array.from({ length: 50 }).map((_, i) => (
            <div
              key={i}
              className="absolute w-1 h-1 bg-white rounded-full opacity-70"
              style={{
                top: `${Math.random() * 100}%`,
                left: `${Math.random() * 100}%`,
                animation: `pulse ${2 + Math.random() * 3}s infinite`
              }}
            ></div>
          ))}
        </div>

        {/* Glowing orbs */}
        <div className="absolute top-1/3 left-1/4 w-48 h-48 bg-purple-500/40 rounded-full blur-3xl"></div>
        <div className="absolute bottom-1/3 right-1/4 w-48 h-48 bg-pink-500/40 rounded-full blur-3xl"></div>
        <div className="absolute top-1/2 left-1/2 w-32 h-32 bg-blue-400/30 rounded-full blur-2xl"></div>

        {/* Main content */}
        <div className="relative h-full flex flex-col items-center justify-center text-white px-8">
          <div className="flex items-center gap-3 mb-6">
            <Star className="w-8 h-8 text-yellow-300 fill-yellow-300" />
            <Sparkles className="w-6 h-6 text-pink-300" />
          </div>
          
          <h1 className="text-7xl font-bold mb-4 text-white text-center drop-shadow-2xl">
            Aparna Mohanty
          </h1>
          
          <div className="h-px w-32 bg-gradient-to-r from-transparent via-white to-transparent mb-4"></div>
          
          <p className="text-2xl text-purple-200">
            Full-Stack Developer & AI Learner
          </p>

          {/* Sparkle decorations */}
          <div className="absolute top-12 left-16">
            <Sparkles className="w-6 h-6 text-yellow-300/60" />
          </div>
          <div className="absolute bottom-12 right-16">
            <Zap className="w-6 h-6 text-pink-300/60" />
          </div>
        </div>
      </div>
    )
  },
  {
    id: 6,
    name: "Developer Console",
    component: () => (
      <div className="relative w-full h-full bg-slate-950 overflow-hidden">
        {/* Terminal window header */}
        <div className="absolute top-0 left-0 right-0 h-10 bg-slate-800 border-b border-slate-700 flex items-center px-4 gap-2">
          <div className="w-3 h-3 rounded-full bg-red-500"></div>
          <div className="w-3 h-3 rounded-full bg-yellow-500"></div>
          <div className="w-3 h-3 rounded-full bg-green-500"></div>
          <span className="ml-4 text-xs text-slate-400 font-mono">developer.sh</span>
        </div>

        {/* Terminal content */}
        <div className="relative h-full flex flex-col items-start justify-center text-white px-16 pt-10 font-mono">
          <div className="text-green-400 mb-2">$ whoami</div>
          <h1 className="text-6xl font-bold text-white mb-6">
            Aparna Mohanty
          </h1>
          
          <div className="text-cyan-400 mb-2">$ cat role.txt</div>
          <p className="text-xl text-gray-300 mb-6">
            Full-Stack Developer & AI Learner
          </p>
          
          <div className="flex items-center gap-2">
            <span className="text-green-400">$</span>
            <div className="w-2 h-5 bg-white animate-pulse"></div>
          </div>

          {/* Code snippet decoration */}
          <div className="absolute top-1/3 right-12 text-xs text-slate-600 space-y-1">
            <div>{'function buildAmazingThings() {'}</div>
            <div className="pl-4">{'return innovation;'}</div>
            <div>{'}'}</div>
          </div>
        </div>
      </div>
    )
  }
];

export default function App() {
  const [selectedDesign, setSelectedDesign] = useState(0);

  const downloadInstructions = () => {
    alert('To download your banner:\n\n1. Right-click on the banner design\n2. Select "Save image as..."\n3. Or take a screenshot of the banner area\n\nRecommended size: 1280×640 pixels for GitHub');
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900 p-8">
      <div className="max-w-7xl mx-auto space-y-8">
        {/* Header */}
        <div className="text-center space-y-2">
          <h2 className="text-4xl font-bold text-white">GitHub Banner Designs</h2>
          <p className="text-purple-200">Choose your favorite design</p>
        </div>

        {/* Main Selected Banner */}
        <div className="space-y-4">
          <div 
            className="w-full rounded-xl overflow-hidden shadow-2xl border-4 border-purple-500/50"
            style={{ aspectRatio: '2/1' }}
          >
            {bannerDesigns[selectedDesign].component()}
          </div>
          
          <div className="flex gap-4 justify-center">
            <button
              onClick={downloadInstructions}
              className="px-6 py-3 bg-gradient-to-r from-purple-600 to-pink-600 text-white rounded-lg hover:from-purple-700 hover:to-pink-700 transition-all shadow-lg"
            >
              Download Instructions
            </button>
            <span className="px-6 py-3 bg-white/10 text-white rounded-lg backdrop-blur-sm border border-white/20">
              {bannerDesigns[selectedDesign].name}
            </span>
          </div>
        </div>

        {/* Design Options Grid */}
        <div>
          <h3 className="text-2xl font-bold text-white mb-4 text-center">All Designs</h3>
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            {bannerDesigns.map((design, index) => (
              <div 
                key={design.id}
                onClick={() => setSelectedDesign(index)}
                className={`cursor-pointer rounded-lg overflow-hidden transition-all hover:scale-105 ${
                  selectedDesign === index 
                    ? 'ring-4 ring-purple-500 shadow-2xl' 
                    : 'ring-2 ring-white/20 hover:ring-purple-400'
                }`}
              >
                <div style={{ aspectRatio: '2/1' }}>
                  {design.component()}
                </div>
                <div className="bg-slate-800 p-3 text-center">
                  <p className="text-white font-medium">{design.name}</p>
                </div>
              </div>
            ))}
          </div>
        </div>

        {/* Instructions */}
        <div className="text-center space-y-2 text-purple-200 text-sm">
          <p>💡 Click any design to view it larger above</p>
          <p>📐 Optimized for GitHub profile banner (1280×640)</p>
        </div>
      </div>
    </div>
  );
}


<!-- Intro -->
<h1 align="center">Hi, I'm Aparna Mohanty 👋</h1>

<p align="center">
  <b>Full-Stack Developer & AI Learner</b> building modern web apps, AI-powered experiences, and polished UIs.
  <br/>
  Currently focused on <b>React</b>, <b>Node.js</b>, <b>Firebase</b>, and <b>AI assistants</b>.
</p>

<p align="center">
  <a href="https://your-portfolio-link.com">Portfolio</a> •
  <a href="mailto:yourmail@example.com">Email</a> •
  <a href="https://www.linkedin.com/in/your-linkedin/">LinkedIn</a>
</p>

---

## 🚀 What I Build

<table>
  <tr>
    <td align="center">
      <h3>AI Experiences</h3>
      <p>Chatbots, assistants, and smart UIs that feel alive.</p>
      <a href="https://github.com/your-user/your-ai-project"><b>View AI Projects →</b></a>
    </td>
    <td align="center">
      <h3>Full-Stack Products</h3>
      <p>End‑to‑end apps with auth, data, and clean APIs.</p>
      <a href="https://github.com/your-user/your-fullstack-project"><b>View Full-Stack Apps →</b></a>
    </td>
    <td align="center">
      <h3>Modern Dashboards</h3>
      <p>Responsive dashboards with animations & dark UI.</p>
      <a href="https://github.com/your-user/your-dashboard-project"><b>View Dashboards →</b></a>
    </td>
  </tr>
</table>

---

## 🧠 Tech Stack

**Frontend**

![React](https://img.shields.io/badge/React-0A1A2F?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-0A1A2F?style=for-the-badge&logo=typescript&logoColor=3178C6)
![JavaScript](https://img.shields.io/badge/JavaScript-0A1A2F?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-0A1A2F?style=for-the-badge&logo=tailwind-css&logoColor=38BDF8)

**Backend & DB**

![Node.js](https://img.shields.io/badge/Node.js-0A1A2F?style=for-the-badge&logo=node.js&logoColor=339933)
![Express](https://img.shields.io/badge/Express-0A1A2F?style=for-the-badge&logo=express&logoColor=FFFFFF)
![Firebase](https://img.shields.io/badge/Firebase-0A1A2F?style=for-the-badge&logo=firebase&logoColor=FFCA28)
![MongoDB](https://img.shields.io/badge/MongoDB-0A1A2F?style=for-the-badge&logo=mongodb&logoColor=47A248)

**Tools & Platforms**

![Git](https://img.shields.io/badge/Git-0A1A2F?style=for-the-badge&logo=git&logoColor=F05032)
![GitHub](https://img.shields.io/badge/GitHub-0A1A2F?style=for-the-badge&logo=github&logoColor=FFFFFF)
![Vercel](https://img.shields.io/badge/Vercel-0A1A2F?style=for-the-badge&logo=vercel&logoColor=FFFFFF)
![Figma](https://img.shields.io/badge/Figma-0A1A2F?style=for-the-badge&logo=figma&logoColor=F24E1E)

---

## 🌌 Featured Projects

| Project | Stack | What it shows |
|--------|-------|----------------|
| [HeritageConnect](https://github.com/your-user/heritageconnect) | React · Node · Firebase · Tailwind | AI museum assistant with ticket booking, offers, and modern card UI. |
| [AI Chatbot](https://github.com/your-user/ai-chatbot) | React · API · Tailwind | Conversational UI with quick actions, typing animations, and context handling. |
| [TasksTracker-TS](https://github.com/your-user/TasksTracker-TS) | React · TypeScript | Clean productivity dashboard with filters, state management, and dark mode. |
| [Portfolio](https://github.com/your-user/portfolio) | React · Tailwind | Futuristic developer portfolio with animated hero and sections for skills & projects. |

---

## 📊 Activity & Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&theme=radical" alt="GitHub stats" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com?user=YOUR_GITHUB_USERNAME&theme=radical" alt="GitHub streak" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&theme=radical" alt="Top languages" />
</p>

---

## 🤝 Let’s Build

- 💬 Ask me about: React, Node.js, Firebase, Tailwind, and integrating AI into real products.  
- 🚀 Open to: internships, junior roles, and collaborative projects.  
- 📩 Reach out: **yourmail@example.com**

