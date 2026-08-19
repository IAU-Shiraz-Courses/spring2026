---
layout: page
title: Materials
permalink: /materials/
---

<style>
  .materials-container {
    max-width: 900px;
    margin: 0 auto;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    padding: 0 15px;
  }

  /* ── Handout Card ── */
  .handout-card {
    background: white;
    border-radius: 15px;
    padding: 30px;
    margin-bottom: 35px;
    box-shadow: 0 5px 20px rgba(0,0,0,0.08);
    border-left: 5px solid #3b82f6;
    display: flex;
    gap: 25px;
    align-items: flex-start;
  }

  .handout-cover {
    width: 130px;
    min-width: 130px;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.15);
    object-fit: cover;
  }

  .handout-info h2 {
    margin-top: 0;
    color: #1e293b;
    font-size: 1.4em;
  }

  .handout-info p {
    color: #475569;
    font-size: 0.95em;
    margin-bottom: 15px;
  }

  .authors-label {
    font-weight: 700;
    color: #1e293b;
    font-size: 0.95em;
    margin-bottom: 10px;
    display: block;
  }

  .authors-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 20px;
  }

  .author-badge {
    background: #eff6ff;
    color: #1d4ed8;
    border: 1px solid #bfdbfe;
    padding: 5px 12px;
    border-radius: 20px;
    font-size: 0.82em;
    font-weight: 600;
    white-space: nowrap;
  }

  .download-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: linear-gradient(135deg, #3b82f6 0%, #1d4ed8 100%);
    color: white;
    padding: 12px 24px;
    border-radius: 30px;
    text-decoration: none;
    font-weight: 600;
    font-size: 0.95em;
    transition: all 0.3s ease;
    box-shadow: 0 4px 15px rgba(59, 130, 246, 0.3);
  }

  .download-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(59, 130, 246, 0.4);
    color: white;
  }

  /* ── Section Title ── */
  .section-title {
    font-size: 1.4em;
    font-weight: 700;
    color: #1e293b;
    margin: 40px 0 20px 0;
    padding-bottom: 10px;
    border-bottom: 3px solid #e2e8f0;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  /* ── Similar Courses ── */
  .courses-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 15px;
    margin-bottom: 10px;
  }

  .course-card {
    background: white;
    border-radius: 12px;
    padding: 18px 20px;
    box-shadow: 0 3px 12px rgba(0,0,0,0.07);
    transition: all 0.3s ease;
    border-top: 4px solid #3b82f6;
    text-decoration: none;
    display: block;
    color: inherit;
  }

  .course-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 25px rgba(0,0,0,0.12);
    color: inherit;
  }

  .course-card .course-name {
    font-weight: 700;
    color: #1e293b;
    font-size: 0.95em;
    margin-bottom: 5px;
  }

  .course-card .course-uni {
    color: #64748b;
    font-size: 0.82em;
  }

  /* ── Books ── */
  .books-list {
    display: flex;
    flex-direction: column;
    gap: 12px;
    margin-bottom: 10px;
  }

  .book-item {
    background: white;
    border-radius: 10px;
    padding: 18px 20px;
    box-shadow: 0 3px 12px rgba(0,0,0,0.07);
    border-left: 4px solid #8b5cf6;
    color: #1e293b;
    font-size: 0.95em;
    line-height: 1.5;
  }

  .book-item strong {
    color: #4c1d95;
  }

  /* ── Online Judges ── */
  .judges-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 12px;
    margin-top: 15px;
  }

  .judge-btn {
    background: linear-gradient(135deg, #f97316 0%, #ea580c 100%);
    color: white;
    padding: 14px 10px;
    border-radius: 10px;
    text-decoration: none;
    font-weight: 600;
    text-align: center;
    font-size: 0.9em;
    transition: all 0.3s ease;
    box-shadow: 0 4px 12px rgba(249, 115, 22, 0.3);
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 6px;
  }

  .judge-btn:nth-child(2) {
    background: linear-gradient(135deg, #22c55e 0%, #16a34a 100%);
    box-shadow: 0 4px 12px rgba(34, 197, 94, 0.3);
  }

  .judge-btn:nth-child(3) {
    background: linear-gradient(135deg, #3b82f6 0%, #1d4ed8 100%);
    box-shadow: 0 4px 12px rgba(59, 130, 246, 0.3);
  }

  .judge-btn:hover {
    transform: translateY(-3px);
    color: white;
  }

  /* ── Additional Resources ── */
  .resources-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
    gap: 12px;
  }

  .resource-card {
    background: white;
    border-radius: 10px;
    padding: 16px 18px;
    box-shadow: 0 3px 12px rgba(0,0,0,0.07);
    border-top: 4px solid #10b981;
    transition: all 0.3s ease;
    text-decoration: none;
    display: block;
    color: inherit;
  }

  .resource-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 20px rgba(0,0,0,0.1);
    color: inherit;
  }

  .resource-card .res-name {
    font-weight: 700;
    color: #065f46;
    font-size: 0.95em;
    margin-bottom: 4px;
  }

  .resource-card .res-desc {
    color: #64748b;
    font-size: 0.82em;
  }

  /* ── Mobile ── */
  @media (max-width: 768px) {
    .handout-card {
      flex-direction: column;
      align-items: center;
      text-align: center;
      padding: 20px 15px;
    }

    .handout-cover {
      width: 110px;
      min-width: 110px;
    }

    .authors-grid {
      justify-content: center;
    }

    .handout-info h2 {
      font-size: 1.2em;
    }

    .courses-grid {
      grid-template-columns: 1fr;
    }

    .resources-grid {
      grid-template-columns: 1fr;
    }

    .judges-grid {
      grid-template-columns: 1fr;
    }

    .section-title {
      font-size: 1.2em;
    }
  }
</style>

<div class="materials-container">

  <!-- ── Handout ── -->
  <div class="handout-card">
    <img src="/_images/screenshots/book.jpeg" alt="Textbook Cover" class="handout-cover" />
    <div class="handout-info">
      <h2>📖 Course Hand-out</h2>
      <p>Data Structures & Algorithms (DSA) – Spring 2026 – Dr. Eskandari</p>

   <span class="authors-label">✍️ Authors</span>
      <div class="authors-grid">
        <span class="author-badge">Hamid Namjoo</span>
        <span class="author-badge">Amir Hossein Hemmati</span>
        <span class="author-badge">Amir Mohammad Asadjoo</span>
        <span class="author-badge">Padina Razmjooei</span>
        <span class="author-badge">Mohammadreza Fasli</span>
        <span class="author-badge">Maryam Ghorbani Zad</span>
        <span class="author-badge">Alireza Heydari</span>
        <span class="author-badge">Ava Keshavarz</span>
        <span class="author-badge">Abolfazl Tadrisi</span>
        <span class="author-badge">Armin Janfaza</span>
        <span class="author-badge">Amirhossein Nazari</span>
        <span class="author-badge">Aynaz Zendedel</span>
      </div>

   <a href="https://my.files.ir/drive/s/zljs1uotDqVC65rJubm89qF1b63k3o" class="download-btn" target="_blank">
        📥 Download Full Textbook (PDF)
      </a>
    </div>
  </div>

  <!-- ── Similar Courses ── -->
  <div class="section-title">🎓 Similar Courses</div>
  <div class="courses-grid">

   <a href="https://www.manning.com/books/grokking-algorithms" class="course-card" target="_blank">
      <div class="course-name">Grokking Data Structures & Algorithms</div>
      <div class="course-uni">📘 Visual & simple guide with Python</div>
    </a>

   <a href="https://web.stanford.edu/class/cs106b" class="course-card" target="_blank">
      <div class="course-name">CS106B: Programming Abstractions</div>
      <div class="course-uni">🏛️ Stanford University</div>
    </a>

   <a href="https://sp21.datastructur.es" class="course-card" target="_blank">
      <div class="course-name">CS61B: Data Structures</div>
      <div class="course-uni">🏛️ UC Berkeley</div>
    </a>

   <a href="https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-spring-2020/pages/lecture-notes/" class="course-card" target="_blank">
      <div class="course-name">6.006 Introduction to Algorithms</div>
      <div class="course-uni">🏛️ MIT OpenCourseWare</div>
    </a>

   <a href="https://courses.engr.illinois.edu/cs225" class="course-card" target="_blank">
      <div class="course-name">CS 225: Data Structures</div>
      <div class="course-uni">🏛️ University of Illinois Urbana‑Champaign</div>
    </a>

   <a href="https://student.cs.uwaterloo.ca/~cs240" class="course-card" target="_blank">
      <div class="course-name">CS 240: Data Structures & Data Management</div>
      <div class="course-uni">🏛️ University of Waterloo</div>
    </a>

   <a href="https://www.cs.purdue.edu/homes/ayg/CS251" class="course-card" target="_blank">
      <div class="course-name">CS 251: Data Structures and Algorithms</div>
      <div class="course-uni">🏛️ Purdue University</div>
    </a>

   <a href="https://www.cs.ox.ac.uk/teaching/courses/2022-2023/algorithms/" class="course-card" target="_blank">
      <div class="course-name">Data Structures</div>
      <div class="course-uni">🏛️ University of Oxford</div>
    </a>

   <a href="https://www.cs.princeton.edu/~wayne/kleinberg-tardos/" class="course-card" target="_blank">
      <div class="course-name">Algorithm Design Slides (Kleinberg & Tardos)</div>
      <div class="course-uni">🏛️ Princeton University</div>
    </a>

  </div>

  <!-- ── Recommended Books ── -->
  <div class="section-title">📚 Recommended Books & References</div>
  <div class="table-scroll">
  <table class="data-table books-table">
    <thead>
      <tr>
        <th data-label="Book">Book</th>
        <th data-label="Author">Author(s)</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td data-label="Book">📗 <strong>Data Structures &amp; Algorithm Analysis</strong></td>
        <td data-label="Author">Mark Allen Weiss</td>
      </tr>
      <tr>
        <td data-label="Book">📘 <strong>Algorithms</strong></td>
        <td data-label="Author">Robert Sedgewick &amp; Kevin Wayne</td>
      </tr>
    </tbody>
  </table>
  </div>

  <div class="judges-grid">
    <a href="https://leetcode.com/" class="judge-btn" target="_blank">💻 LeetCode</a>
    <a href="https://www.hackerrank.com/" class="judge-btn" target="_blank">🎯 HackerRank</a>
    <a href="https://codeforces.com/" class="judge-btn" target="_blank">🏆 Codeforces</a>
  </div>

  <!-- ── Additional Resources ── -->
  <div class="section-title">🔗 Additional Course Materials</div>
  <div class="resources-grid">

   <a href="https://docs.python.org/3/tutorial/" class="resource-card" target="_blank">
      <div class="res-name">🐍 Python for Beginners</div>
      <div class="res-desc">Official Python tutorial</div>
    </a>

   <a href="https://visualgo.net" class="resource-card" target="_blank">
      <div class="res-name">🎨 Visualgo</div>
      <div class="res-desc">Data structure visualizations</div>
    </a>

   <a href="https://geeksforgeeks.org" class="resource-card" target="_blank">
      <div class="res-name">🧠 GeeksforGeeks</div>
      <div class="res-desc">DSA problems and solutions</div>
    </a>

  </div>

</div>
