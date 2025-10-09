Make sure these are installed:

1. **Node.js (v18 or above)** → check with
    
    `node -v`
    
2. **npm** or **pnpm** (comes with Node) → check with
    
    `npm -v`
    
3. **VS Code** (with extensions like “ES7+ React Snippets” and “Prettier” — optional but helpful)
    

---

## 🚀 Step 1: Create a New Next.js App

Open your terminal (in VS Code or system terminal), then run:

`npx create-next-app@latest`

You’ll be asked a few questions 👇  
Answer like this (you can change later):

|Question|Answer|
|---|---|
|What is your project named?|`my-next-app`|
|Would you like to use TypeScript?|No (for now)|
|Would you like to use ESLint?|Yes|
|Would you like to use Tailwind CSS?|No (for now)|
|Would you like to use `src/` directory?|Yes|
|Would you like to use App Router?|Yes|
|Would you like to customize the default import alias?|No|

Then it will install all dependencies automatically.

---

## 📂 Step 2: Open It in VS Code

Go inside your project folder:

`cd my-next-app`

Then open VS Code:

`code .`

---

## ▶️ Step 3: Run the Development Server

Run this command:

`npm run dev`

Then open your browser and go to:

`http://localhost:3000`