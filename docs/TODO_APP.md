# Thinq Todo List Application

A beautiful, fully-functional to-do list application with local storage persistence built with React and Next.js.

## 📋 Features

### Core Functionality
- ✅ **Add Tasks** - Create new todos with automatic timestamps
- ✅ **Complete Tasks** - Mark tasks as done with checkboxes
- ✅ **Delete Tasks** - Remove individual tasks with the delete button
- ✅ **Clear Completed** - Bulk remove all finished tasks at once
- ✅ **Filter Tasks** - View All, Active, or Completed tasks separately
- ✅ **Local Storage** - All data automatically persists to browser storage
- ✅ **Task Timestamps** - See when each task was created

### User Interface
- 🎨 Beautiful gradient purple background (hex: #667eea to #764ba2)
- 🎯 Smooth animations and transitions
- 📱 Fully responsive design (mobile, tablet, desktop)
- 🌟 Interactive hover effects and feedback
- 💾 Auto-saves to browser's localStorage
- 📊 Real-time task counters (All, Active, Completed)
- 🎭 Empty state messages for better UX

## 🛠️ Tech Stack

- **Frontend Framework**: React 18 + Next.js 14
- **Styling**: Custom CSS3 with animations
- **Storage**: Browser localStorage API
- **Language**: JavaScript (JSX)

## 📁 Project Structure

```
frontend/
├── components/
│   ├── TodoApp.jsx          # Main React component (157 lines)
│   └── TodoApp.css          # Beautiful styling (330+ lines)
├── app/
│   └── todo/
│       └── page.js          # Todo page route
└── ...
```

## 🚀 Getting Started

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/Sudarsanankr/Thinq-.git
cd Thinq-
```

2. **Install dependencies**
```bash
npm install
cd frontend && npm install && cd ..
```

3. **Start the development server**
```bash
npm run dev
# or
cd frontend && npm run dev
```

4. **Open in browser**
```
http://localhost:3000/todo
```

### Usage

#### Adding a Task
1. Type your task in the input field
2. Click "Add Task" or press Enter
3. Task appears at the top of the list with timestamp

#### Completing a Task
1. Click the checkbox next to the task
2. Task text will strikethrough
3. Task moves to "Completed" filter

#### Deleting a Task
1. Click the ✕ button on the right side of the task
2. Task is instantly removed
3. Changes are auto-saved

#### Filtering Tasks
- **All** - Shows all tasks (count: total tasks)
- **Active** - Shows incomplete tasks only
- **Completed** - Shows finished tasks only

#### Clear Completed
- Click "Clear Completed Tasks" button to remove all finished tasks at once
- Only appears when you have completed tasks

## 💾 Local Storage

All todo data is automatically saved to your browser's localStorage:
- **Storage Key**: `thinq_todos`
- **Format**: JSON array of todo objects
- **Auto-save**: Changes save instantly
- **Persistence**: Survives page refreshes, browser restarts
- **No Backend Required**: Works completely offline

### Data Structure
```javascript
{
  id: 1234567890,           // Unique timestamp-based ID
  text: "Buy groceries",    // Task text
  completed: false,         // Completion status
  createdAt: "5/22/2026..." // Creation timestamp
}
```

## 🎨 Design Features

### Gradient Background
- Linear gradient from purple (#667eea) to deep purple (#764ba2)
- Full viewport height coverage

### Animations
- Slide-down header animation
- Staggered task list animations
- Smooth scale/transform effects on interactions
- Spring-like add button hover effects

### Responsive Breakpoints
- **Desktop** (>768px) - Full layout
- **Tablet** (480px-768px) - Adjusted spacing
- **Mobile** (<480px) - Optimized for small screens

### Interactive Elements
- Input field with focus glow
- Gradient button (pink #f093fb to red #f5576c)
- Smooth checkbox styling with custom accent color
- Delete button with hover expand effect
- Filter buttons with active state highlighting

## 🔐 Browser Compatibility

Works on all modern browsers:
- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 📝 Code Highlights

### Local Storage Integration
```javascript
// Load from localStorage on mount
useEffect(() => {
  const savedTodos = localStorage.getItem('thinq_todos');
  if (savedTodos) {
    setTodos(JSON.parse(savedTodos));
  }
}, []);

// Auto-save on state change
useEffect(() => {
  localStorage.setItem('thinq_todos', JSON.stringify(todos));
}, [todos]);
```

### Filter Logic
```javascript
const filteredTodos = todos.filter((todo) => {
  if (filter === 'active') return !todo.completed;
  if (filter === 'completed') return todo.completed;
  return true;
});
```

## 👤 Author

**Created by**: Sudarsanan K R  
📧 **Email**: [sudarsanankr49@gmail.com](mailto:sudarsanankr49@gmail.com)  
🔗 **GitHub**: [@Sudarsanankr](https://github.com/Sudarsanankr)  
🌐 **Project**: [Thinq Repository](https://github.com/Sudarsanankr/Thinq-)

## 📄 License

This project is part of the Thinq Music Streaming App and is licensed under the MIT License.

## 🤝 Contributing

Contributions are welcome! Feel free to:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🐛 Bug Reports & Feature Requests

Found a bug? Have a feature idea? Please [open an issue](https://github.com/Sudarsanankr/Thinq-/issues) on GitHub.

## 🎓 Learning Resources

This project demonstrates:
- React Hooks (useState, useEffect)
- Local Storage API
- CSS3 animations and transitions
- Responsive design patterns
- Component composition
- State management
- Event handling

## 🔄 Future Enhancements

Planned features for future versions:
- Cloud sync across devices
- Drag & drop to reorder tasks
- Task categories/tags
- Priority levels
- Due dates & reminders
- Dark mode toggle
- Export/Import functionality
- Task search functionality

---

**Version**: 1.0.0  
**Last Updated**: May 22, 2026  
**Branch**: feature/todo-app

Enjoy using Thinq Todo! 🚀
