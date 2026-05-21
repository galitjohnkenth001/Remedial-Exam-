:root {
  --bg-color: #0f172a;
  --card-bg: #1e293b;
  --nav-bg: #020617;
  --primary: #38bdf8;
  --accent: #22c55e;
  --text: #f1f5f9;
  --muted: #94a3b8;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
  background: var(--bg-color);
  color: var(--text);
  line-height: 1.6;
}

.side-nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 220px;
  height: 100vh;
  padding: 30px 20px;
  background: var(--nav-bg);
  border-right: 1px solid #334155;
  display: flex;
  flex-direction: column;
  gap: 14px;
  box-shadow: 4px 0 20px rgba(0, 0, 0, 0.35);
  z-index: 10;
}

.side-nav .brand {
  font-size: 20px;
  font-weight: 700;
  color: var(--primary);
  letter-spacing: 1px;
  margin-bottom: 10px;
}

.side-nav a {
  color: var(--text);
  text-decoration: none;
  padding: 10px 12px;
  border-radius: 8px;
  transition: background 0.2s ease, color 0.2s ease;
}

.side-nav a:hover,
.side-nav a:focus {
  background: rgba(56, 189, 248, 0.12);
  color: var(--primary);
}

.site-content {
  margin-left: 240px;
  padding: 20px 30px 40px;
}

header {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  text-align: left;
  padding: 40px 40px 30px;
  background: linear-gradient(135deg, #1e293b, var(--bg-color));
  border-radius: 16px;
  border: 1px solid #334155;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.25);
}

header h1 {
  margin: 0;
  font-size: 42px;
  letter-spacing: 2px;
  color: var(--primary);
}

header .title {
  margin: 12px 0 6px;
  font-size: 20px;
  color: #cbd5e1;
}

header p {
  max-width: 760px;
  margin: 0 0 24px;
  font-size: 18px;
  color: #e2e8f0;
}

.cta-button {
  display: inline-block;
  margin-top: 10px;
  padding: 14px 24px;
  background: var(--primary);
  color: var(--bg-color);
  border-radius: 999px;
  text-decoration: none;
  font-weight: 700;
}

.cta-button:hover {
  background: var(--accent);
}

section {
  max-width: 960px;
  margin: 30px auto;
  padding: 25px;
  background: var(--card-bg);
  border-radius: 16px;
  box-shadow: 0 0 18px rgba(0, 0, 0, 0.35);
  transition: transform 0.3s ease;
}

section:hover {
  transform: translateY(-4px);
}

h2 {
  color: var(--primary);
  border-left: 5px solid var(--primary);
  padding-left: 12px;
  margin-bottom: 18px;
}

.job-entry {
  margin-bottom: 24px;
}

.job-entry h3 {
  margin: 0 0 4px;
  font-size: 22px;
  color: #e2e8f0;
}

.job-meta {
  margin: 0 0 12px;
  color: var(--muted);
  font-size: 15px;
}

section ul {
  padding-left: 22px;
}

section ul li {
  margin: 10px 0;
}

form {
  display: grid;
  gap: 16px;
  max-width: 720px;
}

label {
  font-weight: 700;
  color: #cbd5e1;
}

input,
textarea {
  width: 100%;
  padding: 14px 16px;
  border-radius: 12px;
  border: 1px solid #334155;
  background: #0f172a;
  color: var(--text);
  font-size: 16px;
}

input:focus,
textarea:focus {
  outline: 2px solid var(--primary);
  outline-offset: 2px;
}

button[type="submit"] {
  width: fit-content;
  padding: 14px 26px;
  border: none;
  border-radius: 12px;
  background: var(--primary);
  color: var(--bg-color);
  font-weight: 700;
  cursor: pointer;
  transition: transform 0.2s ease, background 0.2s ease;
}

button[type="submit"]:hover {
  background: var(--accent);
  transform: translateY(-1px);
}

footer {
  text-align: center;
  padding: 24px 18px 14px;
  margin-top: 10px;
  background: var(--nav-bg);
  color: var(--muted);
  border-radius: 16px;
  border: 1px solid #334155;
}

.footer-nav {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 14px;
  margin-bottom: 16px;
}

.footer-nav a {
  color: var(--primary);
  font-weight: 600;
}

@media (max-width: 992px) {
  .site-content {
    margin-left: 0;
  }

  .side-nav {
    position: relative;
    width: 100%;
    height: auto;
    border-right: none;
    box-shadow: none;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 16px 10px;
  }

  .side-nav .brand {
    width: 100%;
    margin-bottom: 12px;
  }

  .side-nav a {
    margin: 0 6px;
  }
}

@media (max-width: 768px) {
  section {
    width: 92%;
    padding: 20px;
  }

  header {
    padding: 28px 20px 24px;
    align-items: center;
    text-align: center;
  }

  header h1 {
    font-size: 32px;
  }

  header p,
  header .title {
    font-size: 16px;
  }

  .cta-button {
    width: 100%;
    text-align: center;
  }
}
