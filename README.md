# Portfolio
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Sriram Thiruvengadam - AI Engineer Portfolio</title>
<style>
  /* Trendy soft pastel with blue accent color scheme */
  :root {
    --background: #edf7f6;
    --primary: #51e2f5;
    --accent: #ffa8b6;
    --text-dark: #333;
    --text-light: #555;
    --card-bg: #fff;
  }
  body {
    background: var(--background);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: var(--text-dark);
    margin: 0;
    line-height: 1.6;
  }
  header {
    background: var(--primary);
    color: white;
    padding: 2rem 1rem;
    text-align: center;
    position: sticky;
    top: 0;
    box-shadow: 0 2px 8px rgba(0,0,0,0.15);
  }
  header h1 {
    margin: 0;
    font-weight: 700;
    font-size: 2.5rem;
  }
  header h2 {
    margin: 0.25rem 0 0;
    font-weight: 400;
    font-style: italic;
    font-size: 1.25rem;
    color: var(--accent);
  }
  main {
    max-width: 900px;
    margin: 2rem auto;
    padding: 0 1rem;
  }
  section {
    background: var(--card-bg);
    border-radius: 10px;
    padding: 1.5rem 2rem;
    margin-bottom: 2rem;
    box-shadow: 0 4px 10px rgba(0,0,0,0.05);
    opacity: 0;
    transform: translateY(20px);
    animation-fill-mode: forwards;
    animation-duration: 1s;
  }
  section.visible {
    opacity: 1;
    transform: translateY(0);
  }
  h3 {
    color: var(--primary);
    margin-bottom: 1rem;
  }
  ul {
    padding-left: 1.5rem;
  }
  li {
    margin-bottom: 0.5rem;
  }
  .typing {
    font-weight: 600;
    color: var(--accent);
    white-space: nowrap;
    border-right: 2px solid var(--accent);
    overflow: hidden;
  }
  .project-card {
    background: var(--background);
    border-left: 4px solid var(--primary);
    padding: 0.75rem 1rem;
    margin-bottom: 1rem;
    border-radius: 6px;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .project-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(81, 226, 245, 0.3);
  }
  footer {
    text-align: center;
    margin: 3rem 0 1rem;
    color: var(--text-light);
    font-size: 0.9rem;
  }
  a {
    color: var(--primary);
    text-decoration: none;
  }
  a:hover {
    text-decoration: underline;
  }
</style>
</head>
<body>
<header>
  <h1>Sriram Thiruvengadam</h1>
  <h2><span id="typing" class="typing"></span></h2>
</header>

<main>
  <section id="about">
    <h3>About Me</h3>
    <p>
      I am an aspiring AI Engineer with a solid foundation in machine learning, data science, and programming languages such as Python and Java. Passionate about building intelligent systems and solving real-world problems, I aim to contribute to advancements in AI through innovative solutions.
    </p>
  </section>

  <section id="skills">
    <h3>Skills</h3>
    <ul>
      <li>Programming: Java, Python basics</li>
      <li>Machine Learning Concepts: Basic ML and Generative AI</li>
      <li>Web Development: Clean interfaces and intuitive UI/UX design</li>
      <li>Tools & Concepts: Data science fundamentals, real-time sensor-based anomaly detection</li>
      <li>Soft Skills: Communication, project management, creativity, problem-solving</li>
    </ul>
  </section>

  <section id="projects">
    <h3>Projects</h3>
    <div class="project-card">
      <strong>Real-time Sensor-Based Anomaly Detection System</strong>
      <p>Developed as part of the Naan Mudhalvan project, creating a real-time system to detect sensor anomalies.</p>
    </div>
    <div class="project-card">
      <strong>Web Development Internship Projects</strong>
      <p>Collaborated with trainers at Altitudes, Coimbatore to design clean and intuitive web interfaces.</p>
    </div>
  </section>

  <section id="experience">
    <h3>Experience</h3>
    <ul>
      <li><strong>Web Developer Intern</strong>, Altitudes, Coimbatore (Feb 2024 – Mar 2024) - Created clean interfaces and intuitive interactions.</li>
      <li><strong>Detection System Developer</strong>, Naan Mudhalvan Project (Apr 2024 – May 2024) - Built a real-time anomaly detection system.</li>
    </ul>
  </section>

  <section id="education">
    <h3>Education</h3>
    <ul>
      <li>B.Tech in Artificial Intelligence and Data Science (2022 – Present) - Dhanalakshmi Srinivasan College of Engineering, Coimbatore. CGPA: 7.95</li>
      <li>Higher Secondary (XII) – 77.83% in Computer Science</li>
      <li>Secondary (X) – 71%</li>
    </ul>
  </section>

  <section id="certifications">
    <h3>Certifications</h3>
    <ul>
      <li>IBM Skills Build</li>
      <li>Oracle University</li>
    </ul>
  </section>

  <section id="contact">
    <h3>Contact</h3>
    <p>Email: <a href="mailto:sriramthiru64@gmail.com">sriramthiru64@gmail.com</a></p>
    <p>Phone: +91 8148827377</p>
    <p>LinkedIn: <a href="https://linkedin.com/in/sriram-t-6sk4" target="_blank">linkedin.com/in/sriram-t-6sk4</a></p>
  </section>
</main>

<footer>&copy; 2025 Sriram Thiruvengadam</footer>

<script>
  // Typing effect for header subtitle
  const typingText = "Aspiring AI Engineer";
  const typingElem = document.getElementById('typing');
  let index = 0;
  function type() {
    if (index < typingText.length) {
      typingElem.textContent += typingText.charAt(index);
      index++;
      setTimeout(type, 120);
    }
  }
  type();

  // Fade-in sections on scroll
  const sections = document.querySelectorAll('section');

  function revealOnScroll() {
    const triggerBottom = window.innerHeight * 0.85;
    sections.forEach(section => {
      const sectionTop = section.getBoundingClientRect().top;
      if (sectionTop < triggerBottom) {
        section.classList.add('visible');
      }
    });
  }
  window.addEventListener('scroll', revealOnScroll);
  revealOnScroll();
</script>
</body>
</html>
```

Citations:
[1] Sriram-T_Resume.pdf https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/90598523/16a0f413-a9ed-4036-b302-0c14e24b0683/Sriram-T_Resume.pdf
