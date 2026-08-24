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

  .book-description {
    color: #64748b;
    font-size: 0.88em;
    line-height: 1.6;
    margin-bottom: 20px;
    padding: 12px 16px;
    background: #f8fafc;
    border-radius: 8px;
    border-left: 3px solid #cbd5e1;
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

  .download-btn-sm {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    background: linear-gradient(135deg, #8b5cf6 0%, #6d28d9 100%);
    color: white;
    padding: 8px 18px;
    border-radius: 25px;
    text-decoration: none;
    font-weight: 600;
    font-size: 0.85em;
    transition: all 0.3s ease;
    box-shadow: 0 3px 10px rgba(139, 92, 246, 0.3);
    white-space: nowrap;
  }

  .download-btn-sm:hover {
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(139, 92, 246, 0.4);
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

  .book-flex {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 10px;
  }

  .book-author {
    color: #64748b;
    font-size: 0.85em;
  }

  /* ── GitHub Repos ── */
  .repos-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    gap: 12px;
    margin-bottom: 10px;
  }

  .repo-card {
    background: white;
    border-radius: 10px;
    padding: 16px 18px;
    box-shadow: 0 3px 12px rgba(0,0,0,0.07);
    border-top: 4px solid #6366f1;
    transition: all 0.3s ease;
    text-decoration: none;
    display: block;
    color: inherit;
  }

  .repo-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 20px rgba(0,0,0,0.1);
    color: inherit;
  }

  .repo-card .repo-name {
    font-weight: 700;
    color: #312e81;
    font-size: 0.92em;
    margin-bottom: 4px;
    display: flex;
    align-items: center;
    gap: 6px;
  }

  .repo-card .repo-desc {
    color: #64748b;
    font-size: 0.80em;
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

    .handout-info h2 {
      font-size: 1.2em;
    }

    .courses-grid,
    .repos-grid,
    .resources-grid {
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
      <p>Data Mining – Spring 2026 – Dr. Eskandari</p>

      <div class="book-description">
        A comprehensive textbook covering the principles and techniques of data mining,
        including data preprocessing, classification, clustering, association rule mining,
        and practical applications for knowledge discovery in large datasets.
      </div>

      <a href="https://drive.google.com/file/d/1kWLBZbtj8a8pim4e3oT0FlPTgVMEEA0J/view?usp=sharing" class="download-btn" target="_blank">
        📥 Download Full Textbook (PDF)
      </a>
    </div>
  </div>

  <!-- ── Similar Courses ── -->
  <div class="section-title">🎓 Similar Courses</div>
  <div class="courses-grid">

    <a href="http://www.mmds.org/" class="course-card" target="_blank">
      <div class="course-name">Mining of Massive Datasets</div>
      <div class="course-uni">📘 Leskovec, Rajaraman & Ullman</div>
    </a>

    <a href="https://dataminingbook.info/book_html/" class="course-card" target="_blank">
      <div class="course-name">Data Mining and Machine Learning</div>
      <div class="course-uni">📘 Zaki & Meira – dataminingbook.info</div>
    </a>

    <a href="https://web.stanford.edu/class/cs246/" class="course-card" target="_blank">
      <div class="course-name">CS246: Mining Massive Data Sets</div>
      <div class="course-uni">🏛️ Stanford University</div>
    </a>

    <a href="https://ocw.mit.edu/courses/15-062-data-mining-spring-2003/download/" class="course-card" target="_blank">
      <div class="course-name">15.062 Data Mining</div>
      <div class="course-uni">🏛️ MIT OpenCourseWare</div>
    </a>

    <a href="https://ds100.org/sp24/" class="course-card" target="_blank">
      <div class="course-name">DATA 100: Principles and Techniques of Data Science</div>
      <div class="course-uni">🏛️ UC Berkeley</div>
    </a>

    <a href="https://github.com/DS-100/sp24/blob/main/resources.md" class="course-card" target="_blank">
      <div class="course-name">DATA 100 – Course Resources</div>
      <div class="course-uni">🔗 UC Berkeley (GitHub)</div>
    </a>

    <a href="https://online.stanford.edu/courses/soe-ycs0007-mining-massive-data-sets" class="course-card" target="_blank">
      <div class="course-name">Mining Massive Data Sets (Online)</div>
      <div class="course-uni">🏛️ Stanford Online</div>
    </a>

    <a href="https://nptel.ac.in/courses/106105174" class="course-card" target="_blank">
      <div class="course-name">Data Mining</div>
      <div class="course-uni">🏛️ NPTEL</div>
    </a>

    <a href="https://courses.cs.washington.edu/courses/csep590a/25sp/" class="course-card" target="_blank">
      <div class="course-name">CSEP590A: Data Mining</div>
      <div class="course-uni">🏛️ University of Washington</div>
    </a>

    <a href="https://las.inf.ethz.ch/teaching/dm-f16" class="course-card" target="_blank">
      <div class="course-name">Data Mining (DM)</div>
      <div class="course-uni">🏛️ ETH Zurich</div>
    </a>

    <a href="https://www.cs.cmu.edu/~christos/courses/826.F25/syllabus.html" class="course-card" target="_blank">
      <div class="course-name">CS 826: Data Mining</div>
      <div class="course-uni">🏛️ Carnegie Mellon University</div>
    </a>

    <a href="https://tommasorigon.github.io/datamining/" class="course-card" target="_blank">
      <div class="course-name">Data Mining – Course Notes</div>
      <div class="course-uni">📘 Tommaso Rigon</div>
    </a>

  </div>

  <!-- ── Recommended Books ── -->
  <div class="section-title">📚 Recommended Books & References</div>
  <div class="books-list">
    <div class="book-item">
      <div class="book-flex">
        <div>
          📗 <strong>Data Mining: Concepts and Techniques</strong><br>
          <span class="book-author">by Jiawei Han</span>
        </div>
        <a href="https://drive.google.com/file/d/1oWmgqytQg5Bj_05crGnUqXSXrqRxqu2P/view?usp=sharing" class="download-btn-sm" target="_blank">
          📥 Download (PDF)
        </a>
      </div>
    </div>
  </div>

  <!-- ── GitHub Repositories ── -->
  <div class="section-title">💻 GitHub Repositories & Implementations</div>
  <div class="repos-grid">

    <a href="https://github.com/bartdag/pymining" class="repo-card" target="_blank">
      <div class="repo-name">📦 pymining</div>
      <div class="repo-desc">Collection of data mining algorithms in Python</div>
    </a>

    <a href="https://github.com/fatihsen20/Frequent-Mining-Algorithms" class="repo-card" target="_blank">
      <div class="repo-name">📦 FIMProject</div>
      <div class="repo-desc">Frequent Itemset & Sequence Mining algorithms in Python</div>
    </a>

    <a href="https://github.com/topics/data-mining-algorithms?l=python&o=desc&s=updated" class="repo-card" target="_blank">
      <div class="repo-name">📦 data-mining-algorithms</div>
      <div class="repo-desc">GitHub topic – Python data mining algorithms</div>
    </a>

    <a href="https://github.com/jacksonpradolima/gsp-py" class="repo-card" target="_blank">
      <div class="repo-name">📦 gsp-py</div>
      <div class="repo-desc">Generalized Sequential Pattern (GSP) algorithm in Python</div>
    </a>

    <a href="https://github.com/yueliu1999/Awesome-Deep-Graph-Clustering" class="repo-card" target="_blank">
      <div class="repo-name">📦 Awesome-Deep-Graph-Clustering</div>
      <div class="repo-desc">Deep graph clustering resources and papers</div>
    </a>

    <a href="https://github.com/rupensa/tauCC" class="repo-card" target="_blank">
      <div class="repo-name">📦 tauCC</div>
      <div class="repo-desc">Clustering coefficient implementation</div>
    </a>

    <a href="https://github.com/Amey-Thakur/DATA-WAREHOUSING-AND-MINING-AND-DATA-WAREHOUSING-AND-MINING-LAB" class="repo-card" target="_blank">
      <div class="repo-name">📦 DATA-WAREHOUSING-AND-MINING-LAB</div>
      <div class="repo-desc">Lab exercises for data warehousing & mining</div>
    </a>

    <a href="https://github.com/therohitjagan/E-Learning-Recommendation-System" class="repo-card" target="_blank">
      <div class="repo-name">📦 E-Learning-Recommendation-System</div>
      <div class="repo-desc">Recommendation system for e-learning platforms</div>
    </a>

    <a href="https://github.com/Rheyhan/X-Post-Scraper" class="repo-card" target="_blank">
      <div class="repo-name">📦 X-Post-Scraper</div>
      <div class="repo-desc">X (Twitter) post scraper for data collection</div>
    </a>

    <a href="https://github.com/nerkolt/Clustering_Visualizer_Game" class="repo-card" target="_blank">
      <div class="repo-name">📦 Clustering_Visualizer_Game</div>
      <div class="repo-desc">Interactive clustering visualization game</div>
    </a>

    <a href="https://github.com/Cheshulko/Apriori-py" class="repo-card" target="_blank">
      <div class="repo-name">📦 Apriori-py</div>
      <div class="repo-desc">Apriori algorithm implementation in Python</div>
    </a>

    <a href="https://github.com/rainman226/holte-1r" class="repo-card" target="_blank">
      <div class="repo-name">📦 holte-1r</div>
      <div class="repo-desc">Holte's 1R classifier implementation</div>
    </a>

    <a href="https://github.com/eyupipler/NeuraML" class="repo-card" target="_blank">
      <div class="repo-name">📦 NeuraML</div>
      <div class="repo-desc">Neural network / machine learning library</div>
    </a>

    <a href="https://github.com/JoseCarlosGarcia/diversity-impact" class="repo-card" target="_blank">
      <div class="repo-name">📦 diversity-impact</div>
      <div class="repo-desc">Diversity impact analysis in data mining</div>
    </a>

    <a href="https://github.com/elequaranta/MS-GSP-Algorithm" class="repo-card" target="_blank">
      <div class="repo-name">📦 MS-GSP-Algorithm</div>
      <div class="repo-desc">Multiple Support GSP algorithm implementation</div>
    </a>

    <a href="https://github.com/AAAA-source/MBTI-Predict" class="repo-card" target="_blank">
      <div class="repo-name">📦 MBTI-Predict</div>
      <div class="repo-desc">MBTI personality type prediction using data mining</div>
    </a>

    <a href="https://github.com/Jensen-holm/Numpy-Neuron" class="repo-card" target="_blank">
      <div class="repo-name">📦 Numpy-Neuron</div>
      <div class="repo-desc">Neural network built from scratch with NumPy</div>
    </a>

    <a href="https://github.com/wanxinhang/Awesome-Semi-supervised-Multi-view-classification" class="repo-card" target="_blank">
      <div class="repo-name">📦 Awesome-Semi-supervised-Multi-view-classification</div>
      <div class="repo-desc">Semi-supervised multi-view classification resources</div>
    </a>

    <a href="https://github.com/Four-af/Data-Mining-Lab" class="repo-card" target="_blank">
      <div class="repo-name">📦 Data-Mining-Lab</div>
      <div class="repo-desc">Data mining lab implementations</div>
    </a>

    <a href="https://github.com/jaejungscene/Data-Mining" class="repo-card" target="_blank">
      <div class="repo-name">📦 Data-Mining</div>
      <div class="repo-desc">Data mining algorithms and examples</div>
    </a>

    <a href="https://github.com/ksek87/data-mining-algos-from-scratch" class="repo-card" target="_blank">
      <div class="repo-name">📦 data-mining-algos-from-scratch</div>
      <div class="repo-desc">Data mining algorithms implemented from scratch</div>
    </a>

    <a href="https://github.com/PSNAppz/Machine-Learning-and-Data-Mining-Algorithms" class="repo-card" target="_blank">
      <div class="repo-name">📦 ML-and-DM-Algorithms</div>
      <div class="repo-desc">Machine learning & data mining algorithm collection</div>
    </a>

    <a href="https://github.com/mhahsler/Introduction_to_Data_Mining_R_Examples" class="repo-card" target="_blank">
      <div class="repo-name">📦 R Companion for Introduction to Data Mining</div>
      <div class="repo-desc">R examples accompanying the Introduction to Data Mining textbook</div>
    </a>

    <a href="https://github.com/markhliu/ml_animated" class="repo-card" target="_blank">
      <div class="repo-name">📦 ml_animated</div>
      <div class="repo-desc">Animated machine learning algorithm visualizations</div>
    </a>

  </div>

  <!-- ── Additional Resources ── -->
  <div class="section-title">🔗 Additional Course Materials</div>
  <div class="resources-grid">

    <a href="https://pzs.dstu.dp.ua/DataMining/bibl/LECTURE%20NOTES%20IN%20%20DATA%20MINING.pdf" class="resource-card" target="_blank">
      <div class="res-name">📝 Lecture Notes in Data Mining</div>
      <div class="res-desc">University of Tennessee – PDF</div>
    </a>

    <a href="https://annamacharyauniversity.edu.in/wp-content/uploads/2025/10/1_DATA-WAREHOUSING-AND-DATA-MINING_5th-Sem.pdf" class="resource-card" target="_blank">
      <div class="res-name">📝 Data Warehousing & Data Mining</div>
      <div class="res-desc">Annamacharya University – 5th Sem Notes</div>
    </a>

    <a href="https://mrcet.com/pdf/Lab%20Manuals/IT/IT_3-2_(R20)_DATA%20WAREHOUSING%20AND%20DATA%20MINING_DIGITAL%20NOTES_(2023-24).pdf" class="resource-card" target="_blank">
      <div class="res-name">📝 DW & DM Digital Notes</div>
      <div class="res-desc">Malla Reddy College of Engineering & Technology</div>
    </a>

    <a href="https://www.vssut.ac.in/lecture_notes/lecture1428550844.pdf" class="resource-card" target="_blank">
      <div class="res-name">📝 Lecture Notes on DM & DW</div>
      <div class="res-desc">VSSUT – Course Code: BCS-403</div>
    </a>

    <a href="https://www.geeksforgeeks.org/data-science/data-mining/" class="resource-card" target="_blank">
      <div class="res-name">🧠 Data Mining Tutorial</div>
      <div class="res-desc">GeeksforGeeks – comprehensive tutorial</div>
    </a>

    <a href="https://studyglance.in/lecturenotes/display.php?tno=7&subject=Data%20Mining&title=Data%20Mining%20Unit-1%20Lecture%20Notes" class="resource-card" target="_blank">
      <div class="res-name">📖 Study Glance – DM Notes</div>
      <div class="res-desc">Data Mining Unit-1 Lecture Notes</div>
    </a>

    <a href="https://www.tutorialspoint.com/data_mining/index.htm" class="resource-card" target="_blank">
      <div class="res-name">📚 TutorialsPoint – Data Mining</div>
      <div class="res-desc">Step-by-step data mining tutorial</div>
    </a>

    <a href="https://algomaster.io/animations/ai-ml" class="resource-card" target="_blank">
      <div class="res-name">🎨 AlgoMaster Animations</div>
      <div class="res-desc">AI/ML algorithm animations & visualizations</div>
    </a>

  </div>

</div>
