# todo-list

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TaskFlow | To-Do List</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap');

:root {
  --primary: #6c63ff;
  --bg: #f5f6ff;
  --text: #242541;
  --muted: #9294ad;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  min-height: 100vh;
  padding: 45px 16px;
  font-family: 'Inter', sans-serif;
  color: var(--text);
  background:
    radial-gradient(circle at top left, #e4e1ff, transparent 38%),
    radial-gradient(circle at bottom right, #d8f5ff, transparent 35%),
    var(--bg);
}

.app {
  max-width: 780px;
  margin: auto;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 28px;
}

.brand {
  display: flex;
  align-items: center;
  gap: 12px;
}

.logo {
  width: 48px;
  height: 48px;
  display: grid;
  place-items: center;
  color: white;
  font-size: 25px;
  border-radius: 16px;
  background: linear-gradient(135deg, #8277ff, #5749df);
  box-shadow: 0 8px 20px #6c63ff40;
}

h1 {
  font-size: 25px;
  letter-spacing: -1px;
}

.brand p {
  color: var(--muted);
  font-size: 12px;
  margin-top: 4px;
}

.date {
  font-size: 12px;
  color: #777995;
  text-align: right;
}

.welcome {
  padding: 30px;
  color: white;
  border-radius: 26px;
  background: linear-gradient(120deg, #7568f8, #5747d9);
  box-shadow: 0 15px 35px #6658e52b;
  position: relative;
  overflow: hidden;
}

.welcome::after {
  content: "✦";
  position: absolute;
  right: 32px;
  top: 12px;
  font-size: 110px;
  color: #ffffff18;
}

.welcome h2 {
  font-size: 27px;
  margin-bottom: 10px;
}

.welcome p {
  font-size: 14px;
  color: #e6e3ff;
  line-height: 1.7;
  max-width: 430px;
}

.stats {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 14px;
  margin: 22px 0;
}

.stat {
  background: #ffffffd9;
  border: 1px solid #ffffff;
  border-radius: 19px;
  padding: 19px;
  box-shadow: 0 5px 22px #34355a08;
}

.stat .symbol {
  font-size: 20px;
  margin-bottom: 14px;
}

.stat strong {
  display: block;
  font-size: 27px;
  margin-bottom: 5px;
}

.stat span {
  color: var(--muted);
  font-size: 12px;
}

.panel {
  padding: 25px;
  background: #ffffffed;
  border: 1px solid #ffffff;
  border-radius: 24px;
  box-shadow: 0 10px 35px #35365c0b;
}

.panel-title {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  gap: 12px;
}

.panel-title h3 {
  font-size: 19px;
}

.task-count {
  font-size: 12px;
  color: var(--primary);
  background: #eeecff;
  border-radius: 20px;
  padding: 8px 12px;
}

form {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

input, select {
  font-family: inherit;
  font-size: 13px;
  border: 1px solid #e8e8f2;
  background: #fafaff;
  border-radius: 12px;
  padding: 14px;
  outline: none;
  color: var(--text);
}

input:focus, select:focus {
  border-color: var(--primary);
  box-shadow: 0 0 0 3px #6c63ff14;
}

#taskInput {
  flex: 1 1 180px;
  min-width: 0;
}

#priority {
  flex: 0 1 125px;
}

.add-btn {
  background: linear-gradient(135deg, #7568f8, #5948db);
  color: white;
  font-weight: 600;
  border: none;
  border-radius: 12px;
  padding: 0 20px;
  cursor: pointer;
  transition: transform .2s, box-shadow .2s;
}

.add-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 7px 15px #6c63ff38;
}

.progress-wrap {
  margin: 24px 0;
}

.progress-info {
  display: flex;
  justify-content: space-between;
  color: var(--muted);
  font-size: 12px;
  margin-bottom: 10px;
}

.progress-track {
  height: 8px;
  border-radius: 20px;
  background: #efeff8;
  overflow: hidden;
}

#progressBar {
  height: 100%;
  width: 0%;
  border-radius: 20px;
  background: linear-gradient(90deg, #8c7dff, #5c4de4);
  transition: width .35s;
}

.filters {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
  margin: 8px 0 18px;
}

.filter {
  border: 1px solid #eeeeF7;
  color: #85869e;
  background: white;
  padding: 9px 15px;
  border-radius: 10px;
  cursor: pointer;
  font-size: 12px;
}

.filter.active {
  color: white;
  background: var(--text);
  border-color: var(--text);
}

#taskList {
  list-style: none;
}

.task {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 15px 12px;
  border: 1px solid #f0f0f8;
  border-radius: 15px;
  margin-bottom: 10px;
  animation: appear .25s ease;
  transition: background .2s, transform .2s;
}

.task:hover {
  background: #fbfaff;
  transform: translateX(3px);
}

@keyframes appear {
  from { opacity: 0; transform: translateY(7px); }
  to { opacity: 1; transform: translateY(0); }
}

.check {
  appearance: none;
  width: 21px;
  height: 21px;
  flex-shrink: 0;
  padding: 0;
  border: 2px solid #d8d8e8;
  border-radius: 7px;
  cursor: pointer;
  background: white;
}

.check:checked {
  background: var(--primary);
  border-color: var(--primary);
}

.check:checked::after {
  content: "✓";
  display: block;
  color: white;
  text-align: center;
  font-size: 13px;
  line-height: 17px;
}

.task-main {
  flex: 1;
  min-width: 0;
}

.task-name {
  font-size: 14px;
  font-weight: 600;
  overflow-wrap: anywhere;
}

.task.completed .task-name {
  text-decoration: line-through;
  color: #aaaabd;
}

.task-meta {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 7px;
}

.priority {
  font-size: 10px;
  font-weight: 700;
  padding: 5px 8px;
  border-radius: 7px;
}

.priority.High {
  color: #dc505d;
  background: #fff0f1;
}

.priority.Medium {
  color: #c18424;
  background: #fff7e6;
}

.priority.Low {
  color: #299c79;
  background: #e9faf3;
}

.task-date {
  font-size: 10px;
  color: var(--muted);
}

.delete-btn {
  background: transparent;
  color: #b4b4c8;
  padding: 8px;
  border-radius: 9px;
  cursor: pointer;
  font-size: 17px;
  border: none;
}

.delete-btn:hover {
  background: #fff0f1;
  color: #dc505d;
}

.empty {
  text-align: center;
  padding: 35px 10px;
  color: var(--muted);
  font-size: 13px;
  line-height: 2;
}

.empty .emoji {
  display: block;
  font-size: 37px;
  margin-bottom: 8px;
}

footer {
  text-align: center;
  margin-top: 23px;
  color: #a0a0b5;
  font-size: 11px;
}

@media (max-width: 520px) {
  body { padding: 25px 12px; }
  h1 { font-size: 21px; }
  .date { font-size: 10px; }
  .welcome { padding: 25px 21px; }
  .welcome h2 { font-size: 23px; }
  .stats { gap: 8px; }
  .stat { padding: 13px 10px; }
  .stat strong { font-size: 23px; }
  .stat span { font-size: 10px; }
  .panel { padding: 17px 13px; }
  #priority { flex: 1 1 90px; }
  .add-btn { padding: 13px 17px; }
}
</style>
</head>

<body>
<main class="app">
  <header>
    <div class="brand">
      <div class="logo">✓</div>
      <div>
        <h1>TaskFlow<span style="color:#7568f8">.</span></h1>
        <p>Your day, beautifully organized</p>
      </div>
    </div>
    <div class="date" id="today"></div>
  </header>

  <section class="welcome">
    <h2>Make today count ✨</h2>
    <p>A little progress every day adds up to big results.
       Let's make something happen!</p>
  </section>

  <section class="stats">
    <div class="stat">
      <div class="symbol">📋</div>
      <strong id="totalCount">0</strong>
      <span>Total tasks</span>
    </div>
    <div class="stat">
      <div class="symbol">⚡</div>
      <strong id="pendingCount">0</strong>
      <span>In progress</span>
    </div>
    <div class="stat">
      <div class="symbol">🎉</div>
      <strong id="doneCount">0</strong>
      <span>Completed</span>
    </div>
  </section>

  <section class="panel">
    <div class="panel-title">
      <h3>My tasks</h3>
      <span class="task-count" id="taskCount">0 tasks</span>
    </div>

    <form id="taskForm">
      <input id="taskInput" maxlength="200"
             placeholder="✦ What needs to get done?"
             aria-label="Task name" required>
      <select id="priority" aria-label="Task priority">
        <option value="Medium">🟡 Medium</option>
        <option value="High">🔴 High</option>
        <option value="Low">🟢 Low</option>
      </select>
      <button class="add-btn" type="submit">+ Add task</button>
    </form>

    <div class="progress-wrap">
      <div class="progress-info">
        <span>YOUR DAILY PROGRESS</span>
        <span id="progressText">0% completed</span>
      </div>
      <div class="progress-track">
        <div id="progressBar"></div>
      </div>
    </div>

    <div class="filters">
      <button class="filter active" data-filter="all">All tasks</button>
      <button class="filter" data-filter="pending">In progress</button>
      <button class="filter" data-filter="completed">Completed</button>
    </div>

    <ul id="taskList"></ul>
    <div id="emptyState" class="empty">
      <span class="emoji">🌱</span>
      <strong>Nothing here just yet</strong><br>
      Add a task above and start your journey!
    </div>
  </section>

  <footer>Made with 💜 · One task at a time</footer>
</main>

<script>
const $ = id => document.getElementById(id);

let tasks = [];
let filter = "all";

try {
  const saved = JSON.parse(localStorage.getItem("taskflow-tasks") || "[]");
  if (Array.isArray(saved)) {
    tasks = saved.filter(t =>
      t && typeof t.text === "string" &&
      typeof t.completed === "boolean"
    ).map(t => ({
      id: String(t.id || Math.random()),
      text: t.text.slice(0, 200),
      completed: t.completed,
      priority: ["High", "Medium", "Low"].includes(t.priority)
        ? t.priority : "Medium"
    }));
  }
} catch {
  tasks = [];
}

$("today").textContent = new Date().toLocaleDateString(
  undefined, { weekday: "short", month: "short", day: "numeric" }
);

function saveTasks() {
  try {
    localStorage.setItem("taskflow-tasks", JSON.stringify(tasks));
  } catch {
    // The app still works if browser storage is unavailable.
  }
}

function render() {
  const list = $("taskList");
  list.replaceChildren();

  const completed = tasks.filter(t => t.completed).length;
  const pending = tasks.length - completed;
  const progress = tasks.length
    ? Math.round(completed / tasks.length * 100) : 0;

  $("totalCount").textContent = tasks.length;
  $("pendingCount").textContent = pending;
  $("doneCount").textContent = completed;
  $("taskCount").textContent =
    `${tasks.length} ${tasks.length === 1 ? "task" : "tasks"}`;
  $("progressText").textContent = `${progress}% completed`;
  $("progressBar").style.width = `${progress}%`;

  const visible = tasks.filter(t =>
    filter === "all" ||
    (filter === "completed" && t.completed) ||
    (filter === "pending" && !t.completed)
  );

  $("emptyState").style.display = visible.length ? "none" : "block";

  if (!visible.length) {
    $("emptyState").innerHTML = filter === "completed"
      ? '<span class="emoji">🌟</span><strong>No completed tasks yet</strong><br>Finish a task to see it here!'
      : filter === "pending"
      ? '<span class="emoji">🎉</span><strong>All caught up!</strong><br>You have no pending tasks.'
      : '<span class="emoji">🌱</span><strong>Nothing here just yet</strong><br>Add a task above and start your journey!';
  }

  visible.forEach(task => {
    const li = document.createElement("li");
    li.className = "task" + (task.completed ? " completed" : "");

    const checkbox = document.createElement("input");
    checkbox.type = "checkbox";
    checkbox.className = "check";
    checkbox.checked = task.completed;
    checkbox.setAttribute("aria-label", "Mark task complete");
    checkbox.addEventListener("change", () => {
      task.completed = checkbox.checked;
      saveTasks();
      render();
    });

    const main = document.createElement("div");
    main.className = "task-main";

    const name = document.createElement("div");
    name.className = "task-name";
    name.textContent = task.text;

    const meta = document.createElement("div");
    meta.className = "task-meta";

    const badge = document.createElement("span");
    badge.className = "priority " + task.priority;
    badge.textContent = task.priority + " priority";

    const date = document.createElement("span");
    date.className = "task-date";
    date.textContent = task.completed ? "✓ Finished" : "◷ In your list";

    meta.append(badge, date);
    main.append(name, meta);

    const del = document.createElement("button");
    del.className = "delete-btn";
    del.textContent = "×";
    del.title = "Delete task";
    del.setAttribute("aria-label", "Delete " + task.text);
    del.addEventListener("click", () => {
      tasks = tasks.filter(t => t.id !== task.id);
      saveTasks();
      render();
    });

    li.append(checkbox, main, del);
    list.appendChild(li);
  });
}

$("taskForm").addEventListener("submit", event => {
  event.preventDefault();

  const text = $("taskInput").value.trim();
  if (!text) return;

  tasks.unshift({
    id: (crypto.randomUUID
      ? crypto.randomUUID()
      : Date.now() + "-" + Math.random()),
    text,
    completed: false,
    priority: $("priority").value
  });

  saveTasks();
  $("taskInput").value = "";
  $("priority").value = "Medium";
  render();
  $("taskInput").focus();
});

document.querySelectorAll(".filter").forEach(button => {
  button.addEventListener("click", () => {
    filter = button.dataset.filter;

    document.querySelectorAll(".filter").forEach(b => {
      b.classList.toggle("active", b === button);
    });

    render();
  });
});

render();
</script>
</body>
</html>
