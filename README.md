# ✅ TodoList
A clean and functional Todo List application built with React, TypeScript, and comprehensive testing. This project focuses on state management, user interactions, and code structure rather than flashy UI. I built this side project for learning purposes to strengthen my understanding of real-world frontend development patterns and maintainable architecture.

## 📦 Technologies
- Vite
- React.js
- TypeScript
- JavaScript
- CSS
- Testing Library
- Vitest
- Cypress

## 🦄 Features
Here's what you can do with TodoList:

**Add Tasks**: Quickly create new tasks with a minimal input flow. Type your task, hit enter, and it's instantly added to your list. The input field clears automatically, ready for the next task.

**Mark as Completed**: Toggle tasks between completed and active states with a single click. Completed tasks are visually distinct, making it easy to see what's done and what still needs attention.

**Delete Tasks**: Remove tasks cleanly without breaking the state. Each task has a delete button that safely removes it from your list, with no unintended side effects.

**Persistent State**: Tasks remain consistent during user interaction and updates. The application maintains a reliable state throughout all operations, preventing data loss or unexpected behavior.

**Clean UI & UX**: Focused on clarity and usability, without unnecessary distractions. Every element has a purpose, and the interface gets out of your way so you can focus on your tasks.

**Instant Feedback**: Visual and interactive feedback for every action. When you complete a task, add a new one, or delete something, you immediately see the result with smooth transitions.

## 🎯 Keyboard & Interaction Flow
- Fast task creation with input focus handling
- Immediate visual feedback on task completion
- Smooth state updates without page reloads
- Enter key submits new tasks
- Tab navigation between interactive elements

## 👩🏽‍🍳 The Process
I started this project with a clear goal: build a todo app that demonstrates proper React patterns, not just "make it work." I'd seen too many tutorial todo apps that took shortcuts or ignored best practices. I wanted to build it the right way.

First, I defined a clear data structure for tasks. What properties does a task need? An ID, text content, completion status. Simple, but I had to think about how these would be managed across components and updates.

From there, I focused on building reusable React components. Rather than cramming everything into one file, I split concerns: a component for the task list, another for individual tasks, one for the input form. Each had a single responsibility and predictable behavior.

State management was a key learning area. I implemented proper immutable updates, ensuring that modifying one task didn't accidentally affect others. This meant using techniques like spreading arrays and objects, rather than mutating them directly.

Once the core features were stable, I added testing. This was crucial – I wrote unit tests for components and end-to-end tests with Cypress to validate the entire user flow. Writing tests after implementing features taught me where my code was brittle and where it was solid.

Performance was another consideration. I learned to avoid unnecessary re-renders by properly structuring state and using React's optimization features. The app feels snappy because components only update when they actually need to.

Throughout development, I resisted the urge to add fancy features. No due dates, no categories, no

 cloud sync. Just tasks. This discipline kept me focused on doing the fundamentals exceptionally well rather than building a mediocre feature-rich app.

## 📚 What I Learned
During this project, I've picked up important skills and a deeper understanding of React development patterns and software engineering practices.

### 🧠 State Management
**React State Patterns**: I learned how to properly structure and update state in React. Understanding when to lift state up, when to keep it local, and how components communicate was fundamental to making the app work reliably.

**Immutability**: Every state update creates a new object or array rather than modifying the existing one. This pattern prevents bugs where components don't re-render because React can't detect the change. It was counterintuitive at first but became second nature.

**State Updates**: I learned that setState calls can be batched, that updates might be asynchronous, and how to handle cases where the new state depends on the old state using functional updates.

### 🧩 Component Design
**Single Responsibility Principle**: Each component does one thing well. The task input doesn't worry about how tasks are stored. The task list doesn't care about input validation. This separation made the code easier to reason about and test.

**Composition Over Props Drilling**: Rather than passing props through multiple layers, I structured components to communicate efficiently. This kept the component tree clean and maintainable.

**Reusability**: Building components that can be used in different contexts taught me about props APIs and flexible interfaces. A good component is easy to use correctly and hard to use incorrectly.

### 🧪 Testing Mindset
**Test User Behavior, Not Implementation**: I learned to write tests that verify what users experience, not how the code works internally. If I refactor a component's internals but it still behaves the same, tests should still pass.

**Test-Driven Thinking**: Even though I didn't strictly follow TDD, thinking about how to test a feature influenced how I built it. Code that's easy to test is usually well-designed code.

**End-to-End Testing**: Cypress taught me about testing complete user flows. Does clicking "Add Task" actually add a task? Can users complete and delete tasks in sequence? These integration tests caught issues unit tests missed.

### 🧱 Clean Code
**Naming Things**: Choosing clear, descriptive names for variables, functions, and components made the code self-documenting. `addTask` is better than `handleClick`. `isCompleted` is better than `status`.

**File Organization**: Structuring files logically made navigation easier. Components in one folder, hooks in another, utilities separate. As the project grew, this structure prevented chaos.

**Code Readability**: Writing code that's easy to read meant thinking about future me (or other developers). Comments explain why, not what. Functions are short and focused. Complexity is broken down into understandable pieces.

### 📈 Overall Growth
This project taught me that mastery comes from depth, not breadth. By building a "simple" todo app with care and attention, I learned more about React and software engineering than I would have by rushing through a complex application.

The act of testing forced me to think about edge cases: What happens if someone tries to add an empty task? What if they rapidly click complete/uncomplete? Handling these scenarios made the application robust.

Most importantly, I learned to value maintainability. Six months from now, will I understand this code? Can someone else contribute without drowning in confusion? These questions guided my decisions and resulted in a codebase I'm proud of.

## 💭 How can it be improved?
- Add task filtering (All / Active / Completed views)
- Add task editing functionality
- Persist tasks using localStorage or backend API
- Add drag & drop reordering
- Improve accessibility (ARIA labels, keyboard navigation)
- Add dark mode toggle
- Implement task categories or tags
- Add due dates and reminders
- Create bulk actions (delete all completed)
- Add task search functionality

## 🚦 Running the Project
To run the project in your local environment, follow these steps:

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/Shipwithsimo/todolist.git
   cd todolist
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Open the local URL shown in the terminal (usually `http://localhost:5173`) to view the app

5. Run tests:
   ```bash
   npm test              # Unit tests with Vitest
   npm run test:e2e      # End-to-end tests with Cypress
   ```

## 🎥 Preview
A clean, minimalist interface with an input field at the top for adding new tasks. Below, your task list displays each item with a checkbox to mark it complete and a delete button. Completed tasks show with strikethrough text. The interface is responsive and works smoothly on desktop and mobile devices.
