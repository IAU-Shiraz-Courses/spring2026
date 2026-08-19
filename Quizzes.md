---
layout: page
title: Quizzes
permalink: /quizzes/
---

<style>
  .exercises-container {
    max-width: 900px;
    margin: 0 auto;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    padding: 0 15px;
  }

  .intro-text {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 30px 20px;
    border-radius: 15px;
    text-align: center;
    margin-bottom: 40px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
  }

  .intro-text h2 {
    margin-top: 0;
    font-size: 2em;
    font-weight: 600;
  }

  .intro-text p {
    font-size: 1.1em;
    margin-bottom: 0;
    opacity: 0.95;
  }

  .quiz-card {
    background: white;
    border-radius: 12px;
    padding: 25px 20px;
    margin-bottom: 25px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.08);
    transition: all 0.3s ease;
    border-left: 5px solid #667eea;
  }

  .quiz-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 25px rgba(0,0,0,0.15);
  }

  .quiz-card.last-quiz {
    border-left: 5px solid #f5576c;
  }

  .quiz-header {
    margin-bottom: 15px;
  }

  .quiz-badge {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 5px 15px;
    border-radius: 20px;
    font-size: 0.85em;
    font-weight: 600;
    display: inline-block;
    margin-bottom: 10px;
  }

  .quiz-badge.last-badge {
    background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
  }

  .quiz-title {
    font-size: 1.2em;
    font-weight: 600;
    color: #2d3748;
    margin: 10px 0;
    line-height: 1.4;
    word-wrap: break-word;
    overflow-wrap: break-word;
  }

  .due-date {
    background: #f7fafc;
    color: #4a5568;
    padding: 8px 15px;
    border-radius: 8px;
    font-size: 0.9em;
    display: inline-flex;
    align-items: center;
    font-weight: 500;
    margin-top: 10px;
  }

  .due-date::before {
    content: "📅";
    margin-right: 8px;
    font-size: 1.2em;
  }

  .download-links {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 12px;
    margin-top: 15px;
  }

  .download-btn {
    padding: 12px 15px;
    border-radius: 8px;
    text-decoration: none;
    font-weight: 600;
    text-align: center;
    transition: all 0.3s ease;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    font-size: 0.9em;
    white-space: nowrap;
  }

  .quiz-btn {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    box-shadow: 0 4px 10px rgba(102, 126, 234, 0.3);
  }

  .quiz-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 15px rgba(102, 126, 234, 0.4);
    color: white;
  }

  .solution-btn {
    background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
    color: white;
    box-shadow: 0 4px 10px rgba(245, 87, 108, 0.3);
  }

  .solution-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 15px rgba(245, 87, 108, 0.4);
    color: white;
  }

  .last-chapter-tag {
    display: inline-block;
    background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
    color: white;
    font-size: 0.78em;
    font-weight: 700;
    padding: 3px 12px;
    border-radius: 20px;
    margin-left: 10px;
    vertical-align: middle;
    letter-spacing: 0.5px;
    box-shadow: 0 2px 8px rgba(245, 87, 108, 0.3);
  }

  .note-box {
    background: #fffaf0;
    border-left: 4px solid #ed8936;
    padding: 25px;
    border-radius: 12px;
    margin-top: 40px;
    color: #744210;
    box-shadow: 0 4px 12px rgba(0,0,0,0.06);
  }

  .note-box h3 {
    margin-top: 0;
    font-size: 1.2em;
    color: #92400e;
  }

  .note-box p {
    margin-bottom: 0;
    font-size: 1em;
    line-height: 1.7;
  }

  /* Mobile Optimization */
  @media (max-width: 768px) {
    .exercises-container {
      padding: 0 10px;
    }

    .intro-text {
      padding: 20px 15px;
    }

    .intro-text h2 {
      font-size: 1.5em;
    }

    .intro-text p {
      font-size: 1em;
    }

    .quiz-card {
      padding: 20px 15px;
    }

    .quiz-title {
      font-size: 1.05em;
      line-height: 1.5;
    }

    .quiz-badge {
      font-size: 0.8em;
      padding: 4px 12px;
    }

    .download-links {
      grid-template-columns: 1fr;
      gap: 10px;
    }

    .download-btn {
      width: 100%;
      font-size: 0.85em;
      padding: 12px 10px;
    }

    .note-box {
      padding: 15px;
      font-size: 0.9em;
    }

    .last-chapter-tag {
      display: block;
      margin-left: 0;
      margin-top: 6px;
      width: fit-content;
    }
  }

  @media (max-width: 480px) {
    .quiz-title {
      font-size: 0.95em;
    }

    .quiz-badge {
      font-size: 0.75em;
    }

    .download-btn {
      font-size: 0.8em;
      padding: 10px 8px;
      gap: 5px;
    }
  }
</style>

<div class="exercises-container">

<div class="intro-text">
  <h2>📝 Quizzes</h2>
  <p>Here you can find all the quizzes for this course. Try to solve each quiz on your own before looking at the solution key — that's the best way to learn!</p>
</div>

<div class="table-scroll">
<table class="data-table">
  <thead>
    <tr>
      <th data-label="Quiz">Quiz</th>
      <th data-label="Date">Release Date</th>
      <th data-label="Question Sheet">Question Sheet</th>
      <th data-label="Answer Key">Answer Key</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td data-label="Quiz">Quiz 1</td>
      <td data-label="Date">April 13, 2026</td>
      <td data-label="Question Sheet" class="material-links"><a href="/static_files/Quizzes/Quiz 01 - Questions.pdf">📄 Quiz Sheet</a></td>
      <td data-label="Answer Key" class="material-links"><a href="/static_files/Quizzes/Quiz 01 - Answers.pdf">📋 Solution Key</a></td>
    </tr>
    <tr>
      <td data-label="Quiz">Quiz 2</td>
      <td data-label="Date">April 27, 2026</td>
      <td data-label="Question Sheet" class="material-links"><a href="/static_files/Quizzes/Quiz 02 - Questions.pdf">📄 Quiz Sheet</a></td>
      <td data-label="Answer Key" class="material-links"><a href="/static_files/Quizzes/Quiz 02 - Answers.pdf">📋 Solution Key</a></td>
    </tr>
    <tr>
      <td data-label="Quiz">Quiz 3</td>
      <td data-label="Date">May 11, 2026</td>
      <td data-label="Question Sheet" class="material-links"><a href="/static_files/Quizzes/Quiz 03 - Questions.pdf">📄 Quiz Sheet</a></td>
      <td data-label="Answer Key" class="material-links"><a href="/static_files/Quizzes/Quiz 03 - Answers.pdf">📋 Solution Key</a></td>
    </tr>
    <tr>
      <td data-label="Quiz">Quiz 4</td>
      <td data-label="Date">May 25, 2026</td>
      <td data-label="Question Sheet" class="material-links"><a href="/static_files/Quizzes/Quiz 04 - Questions.pdf">📄 Quiz Sheet</a></td>
      <td data-label="Answer Key" class="material-links"><a href="/static_files/Quizzes/Quiz 04 - Answers.pdf">📋 Solution Key</a></td>
    </tr>
    <tr>
      <td data-label="Quiz">Quiz 5 <span class="flag-tag">last chapter</span></td>
      <td data-label="Date">June 1, 2026</td>
      <td data-label="Question Sheet" class="material-links"><a href="/static_files/Quizzes/Quiz 05 - Questions.pdf">📄 Quiz Sheet</a></td>
      <td data-label="Answer Key" class="material-links"><a href="/static_files/Quizzes/Quiz 05 - Answers.pdf">📋 Solution Key</a></td>
    </tr>
  </tbody>
</table>
</div>

<!-- Quiz 1 -->
<div class="quiz-card">
  <div class="quiz-header">
    <span class="quiz-badge">Quiz 1</span>
    <span class="due-date">April 13, 2026</span>
  </div>
  <div class="download-links">
    <a href="/static_files/Quizzes/Quiz 01 - Questions.pdf" class="download-btn quiz-btn">
      📄 Quiz Sheet
    </a>
    <a href="/static_files/Quizzes/Quiz 01 - Answers.pdf" class="download-btn solution-btn">
      📋 Solution Key
    </a>
  </div>
</div>

<!-- Quiz 2 -->
<div class="quiz-card">
  <div class="quiz-header">
    <span class="quiz-badge">Quiz 2</span>
    <span class="due-date">April 27, 2026</span>
  </div>
  <div class="download-links">
    <a href="/static_files/Quizzes/Quiz 02 - Questions.pdf" class="download-btn quiz-btn">
      📄 Quiz Sheet
    </a>
    <a href="/static_files/Quizzes/Quiz 02 - Answers.pdf" class="download-btn solution-btn">
      📋 Solution Key
    </a>
  </div>
</div>

<!-- Quiz 3 -->
<div class="quiz-card">
  <div class="quiz-header">
    <span class="quiz-badge">Quiz 3</span>
    <span class="due-date">May 11, 2026</span>
  </div>
  <div class="download-links">
    <a href="/static_files/Quizzes/Quiz 03 - Questions.pdf" class="download-btn quiz-btn">
      📄 Quiz Sheet
    </a>
    <a href="/static_files/Quizzes/Quiz 03 - Answers.pdf" class="download-btn solution-btn">
      📋 Solution Key
    </a>
  </div>
</div>

<!-- Quiz 4 -->
<div class="quiz-card">
  <div class="quiz-header">
    <span class="quiz-badge">Quiz 4</span>
    <span class="due-date">May 25, 2026</span>
  </div>
  <div class="download-links">
    <a href="/static_files/Quizzes/Quiz 04 - Questions.pdf" class="download-btn quiz-btn">
      📄 Quiz Sheet
    </a>
    <a href="/static_files/Quizzes/Quiz 04 - Answers.pdf" class="download-btn solution-btn">
      📋 Solution Key
    </a>
  </div>
</div>

<!-- Quiz 5 - Last Chapter -->
<div class="quiz-card last-quiz">
  <div class="quiz-header">
    <span class="quiz-badge last-badge">Quiz 5_⭐ The Last Chapter</span>
    <span class="due-date">June 1, 2026</span>
  </div>
  <div class="download-links">
    <a href="/static_files/Quizzes/Quiz 05 - Questions.pdf" class="download-btn quiz-btn">
      📄 Quiz Sheet
    </a>
    <a href="/static_files/Quizzes/Quiz 05 - Answers.pdf" class="download-btn solution-btn">
      📋 Solution Key
    </a>
  </div>
</div>

<div class="note-box">
  <h3>📌 Note</h3>
  <p>
    These are the official quizzes of the course. Each quiz contains a set of questions along with a solution key.
    We strongly recommend that you first carefully read and attempt the quiz questions on your own, and only then refer to the solution key to check your answers.
    This approach will help you better understand the material and identify areas that need more practice.
  </p>
</div>

</div>
