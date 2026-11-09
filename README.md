# dr-habibul.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dr. Academic Name - Faculty Profile</title>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Academicons -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/jpswalsh/academicons@1/css/academicons.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Merriweather:ital,wght@0,300;0,400;0,700;1,300&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --primary: #1e3a8a;
            --primary-hover: #1d4ed8;
            --secondary: #0f172a;
            --accent: #2563eb;
            --bg-body: #f8fafc;
            --bg-card: #ffffff;
            --text-main: #334155;
            --text-dark: #0f172a;
            --text-muted: #64748b;
            --border-color: #e2e8f0;
            --sidebar-width: 290px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-body);
            color: var(--text-main);
            line-height: 1.6;
            display: flex;
            min-height: 100vh;
        }

        /* Sidebar Styling */
        aside {
            width: var(--sidebar-width);
            background-color: var(--bg-card);
            border-right: 1px solid var(--border-color);
            position: fixed;
            height: 100vh;
            overflow-y: auto;
            padding: 2.5rem 1.5rem;
            display: flex;
            flex-direction: column;
            z-index: 100;
        }

        .profile-card {
            text-align: center;
            margin-bottom: 2rem;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--border-color);
            margin-bottom: 1rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }

        .profile-name {
            font-family: 'Merriweather', serif;
            font-size: 1.35rem;
            color: var(--text-dark);
            font-weight: 700;
            margin-bottom: 0.25rem;
        }

        .profile-title {
            font-size: 0.9rem;
            color: var(--primary);
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .profile-dept {
            font-size: 0.85rem;
            color: var(--text-muted);
            margin-bottom: 1.25rem;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 0.75rem;
            flex-wrap: wrap;
            margin-bottom: 1.5rem;
        }

        .social-links a {
            color: var(--text-muted);
            font-size: 1.25rem;
            transition: color 0.2s ease;
            text-decoration: none;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            background-color: var(--bg-body);
            display: inline-flex;
            align-items: center;
            justify-content: center;
        }

        .social-links a:hover {
            color: var(--primary);
            background-color: #e0e7ff;
        }

        nav ul {
            list-style: none;
        }

        nav li {
            margin-bottom: 0.35rem;
        }

        nav a {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            padding: 0.65rem 1rem;
            color: var(--text-main);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            border-radius: 6px;
            transition: all 0.2s ease;
        }

        nav a:hover, nav a.active {
            background-color: #eff6ff;
            color: var(--primary);
        }

        nav a i {
            width: 20px;
            text-align: center;
        }

        /* Main Content Layout */
        main {
            margin-left: var(--sidebar-width);
            flex: 1;
            padding: 3rem 4rem;
            max-width: 1100px;
        }

        section {
            margin-bottom: 3.5rem;
            scroll-margin-top: 2rem;
        }

        .section-title {
            font-family: 'Merriweather', serif;
            font-size: 1.6rem;
            color: var(--text-dark);
            border-bottom: 2px solid var(--border-color);
            padding-bottom: 0.5rem;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .section-title i {
            color: var(--primary);
            font-size: 1.3rem;
        }

        /* Cards & Components */
        .card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            padding: 1.5rem;
            margin-bottom: 1.25rem;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .card:hover {
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.07);
        }

        /* Biography Section */
        .bio-text {
            font-size: 1.05rem;
            line-height: 1.8;
            color: var(--text-main);
            margin-bottom: 1.5rem;
        }

        .research-interests-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }

        .interest-card {
            background-color: #f1f5f9;
            border-left: 4px solid var(--primary);
            padding: 1rem;
            border-radius: 4px;
            font-weight: 500;
            color: var(--text-dark);
        }

        /* Timeline / Education */
        .timeline-item {
            position: relative;
            padding-left: 2rem;
            border-left: 2px solid var(--border-color);
            margin-bottom: 1.5rem;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -7px;
            top: 4px;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background-color: var(--primary);
        }

        .timeline-degree {
            font-weight: 700;
            font-size: 1.1rem;
            color: var(--text-dark);
        }

        .timeline-inst {
            color: var(--primary);
            font-size: 0.95rem;
            font-weight: 500;
        }

        .timeline-year {
            font-size: 0.85rem;
            color: var(--text-muted);
            margin-bottom: 0.4rem;
        }

        /* Publications Section */
        .filter-buttons {
            display: flex;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
            flex-wrap: wrap;
        }

        .filter-btn {
            background-color: var(--bg-card);
            border: 1px solid var(--border-color);
            padding: 0.4rem 0.9rem;
            border-radius: 20px;
            font-size: 0.85rem;
            cursor: pointer;
            font-weight: 500;
            color: var(--text-muted);
            transition: all 0.2s ease;
        }

        .filter-btn.active, .filter-btn:hover {
            background-color: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .pub-title {
            font-weight: 600;
            font-size: 1.05rem;
            color: var(--text-dark);
            margin-bottom: 0.25rem;
        }

        .pub-authors {
            font-size: 0.95rem;
            color: var(--text-main);
            margin-bottom: 0.25rem;
        }

        .pub-venue {
            font-size: 0.9rem;
            font-style: italic;
            color: var(--text-muted);
            margin-bottom: 0.75rem;
        }

        .pub-actions {
            display: flex;
            gap: 0.75rem;
            align-items: center;
        }

        .pub-btn {
            font-size: 0.8rem;
            padding: 0.25rem 0.6rem;
            border-radius: 4px;
            text-decoration: none;
            border: 1px solid var(--border-color);
            color: var(--text-main);
            background: var(--bg-body);
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 0.3rem;
            transition: background 0.2s ease;
        }

        .pub-btn:hover {
            background: #e2e8f0;
        }

        .bibtex-code {
            display: none;
            background-color: #0f172a;
            color: #f8fafc;
            padding: 1rem;
            border-radius: 6px;
            font-family: monospace;
            font-size: 0.8rem;
            margin-top: 0.75rem;
            white-space: pre-wrap;
            overflow-x: auto;
        }

        /* Teaching & Advisees */
        .badge {
            display: inline-block;
            padding: 0.2rem 0.5rem;
            font-size: 0.75rem;
            font-weight: 600;
            border-radius: 4px;
            background-color: #dbeafe;
            color: #1e40af;
            margin-left: 0.5rem;
        }

        .badge-phd { background-color: #fef3c7; color: #92400e; }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .contact-info-list {
            list-style: none;
        }

        .contact-info-list li {
            display: flex;
            align-items: flex-start;
            gap: 0.75rem;
            margin-bottom: 1rem;
        }

        .contact-info-list i {
            color: var(--primary);
            font-size: 1.1rem;
            margin-top: 0.2rem;
        }

        /* Mobile Responsive Drawer Toggle */
        .mobile-header {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            height: 60px;
            background: var(--bg-card);
            border-bottom: 1px solid var(--border-color);
            padding: 0 1.5rem;
            align-items: center;
            justify-content: space-between;
            z-index: 200;
        }

        .menu-toggle {
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--text-dark);
            cursor: pointer;
        }

        @media (max-width: 900px) {
            .mobile-header { display: flex; }
            aside {
                transform: translateX(-100%);
                transition: transform 0.3s ease;
                top: 60px;
                height: calc(100vh - 60px);
            }
            aside.open { transform: translateX(0); }
            main {
                margin-left: 0;
                padding: 5rem 1.5rem 2rem 1.5rem;
            }
        }
    </style>
</head>
<body>

    <!-- Mobile Drawer Header -->
    <header class="mobile-header">
        <span style="font-weight: 700; color: var(--primary);">Dr. Academic Name</span>
        <button class="menu-toggle" id="menuToggle"><i class="fa-solid fa-bars"></i></button>
    </header>

    <!-- Sidebar Navigation -->
    <aside id="sidebar">
        <div class="profile-card">
            <!-- Replace profile.jpg with your own image file -->
            <img src="https://via.placeholder.com/150" alt="Profile Picture" class="profile-img">
            <h1 class="profile-name">Dr. Academic Name</h1>
            <p class="profile-title">Assistant Professor</p>
            <p class="profile-dept">Department of Mathematics<br>University / Institute Name</p>
            
            <div class="social-links">
                <a href="mailto:email@institution.edu" title="Email"><i class="fa-solid fa-envelope"></i></a>
                <a href="#" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>
                <a href="#" title="ORCID"><i class="ai ai-orcid"></i></a>
                <a href="#" title="ResearchGate"><i class="ai ai-researchgate"></i></a>
                <a href="#" title="GitHub"><i class="fa-brands fa-github"></i></a>
            </div>
        </div>

        <nav>
            <ul>
                <li><a href="#about" class="active"><i class="fa-solid fa-user"></i> About Me</a></li>
                <li><a href="#education"><i class="fa-solid fa-graduation-cap"></i> Education</a></li>
                <li><a href="#research"><i class="fa-solid fa-flask"></i> Research</a></li>
                <li><a href="#publications"><i class="fa-solid fa-book-open"></i> Publications</a></li>
                <li><a href="#teaching"><i class="fa-solid fa-chalkboard-user"></i> Teaching</a></li>
                <li><a href="#students"><i class="fa-solid fa-users"></i> Advisees</a></li>
                <li><a href="#contact"><i class="fa-solid fa-address-book"></i> Contact</a></li>
            </ul>
        </nav>
    </aside>

    <!-- Main Content Area -->
    <main>
        
        <!-- About Section -->
        <section id="about">
            <h2 class="section-title"><i class="fa-solid fa-user"></i> Biography</h2>
            <p class="bio-text">
                Welcome to my academic homepage. I am an Assistant Professor in the Department of Mathematics at [Your University/Institute Name]. My research lies at the intersection of pure and applied mathematics, focusing primarily on theoretical and practical aspects of algebraic coding theory, quantum information theory, and matrix computations.
            </p>
            <p class="bio-text">
                I teach undergraduate and postgraduate courses in Linear Algebra, Abstract Algebra, and Coding Theory, while mentoring research scholars working on quantum error-correcting codes and finite field applications.
            </p>

            <h3 style="font-size: 1.1rem; color: var(--text-dark); margin-top: 1.5rem;">Primary Research Focus</h3>
            <div class="research-interests-grid">
                <div class="interest-card">Algebraic Coding Theory</div>
                <div class="interest-card">Quantum Error-Correction</div>
                <div class="interest-card">Galois & Hermitian Hulls</div>
                <div class="interest-card">Matrix & Graph Theory</div>
            </div>
        </section>

        <!-- Education Section -->
        <section id="education">
            <h2 class="section-title"><i class="fa-solid fa-graduation-cap"></i> Education</h2>
            
            <div class="timeline-item">
                <div class="timeline-degree">Ph.D. in Mathematics</div>
                <div class="timeline-inst">Indian Institute of Technology / University Name</div>
                <div class="timeline-year">2018 – 2022</div>
                <p style="font-size: 0.9rem; color: var(--text-muted);">Thesis: <em>Contributions to Algebraic Codes and Quantum Error-Correcting Structures</em></p>
            </div>

            <div class="timeline-item">
                <div class="timeline-degree">M.Sc. in Mathematics</div>
                <div class="timeline-inst">University / Institute Name</div>
                <div class="timeline-year">2016 – 2018</div>
            </div>

            <div class="timeline-item">
                <div class="timeline-degree">B.Sc. in Mathematics & Computer Science</div>
                <div class="timeline-inst">University / Institute Name</div>
                <div class="timeline-year">2013 – 2016</div>
            </div>
        </section>

        <!-- Research Section -->
        <section id="research">
            <h2 class="section-title"><i class="fa-solid fa-flask"></i> Research Directions</h2>
            
            <div class="card">
                <h3 style="color: var(--primary); margin-bottom: 0.5rem;">Quantum Error-Correcting Codes (QECCs)</h3>
                <p>Developing entangling and non-entangling quantum codes using linear and non-linear codes over finite fields, focusing on parameter optimization and Galois hull dimension bounds.</p>
            </div>

            <div class="card">
                <h3 style="color: var(--primary); margin-bottom: 0.5rem;">Constacyclic & Skew Constacyclic Code Hulls</h3>
                <p>Investigating the algebraic structural properties, dualities, and hull dimensions of constacyclic codes and Plotkin sum constructions over finite rings and fields.</p>
            </div>
        </section>

        <!-- Publications Section -->
        <section id="publications">
            <h2 class="section-title"><i class="fa-solid fa-book-open"></i> Publications</h2>

            <div class="filter-buttons">
                <button class="filter-btn active" onclick="filterPubs('all')">All</button>
                <button class="filter-btn" onclick="filterPubs('journal')">Journals</button>
                <button class="filter-btn" onclick="filterPubs('conference')">Conferences</button>
                <button class="filter-btn" onclick="filterPubs('preprint')">Preprints</button>
            </div>

            <!-- Publication 1 -->
            <div class="card pub-item" data-category="journal">
                <div class="pub-title">On the Relative Galois Hulls of Constacyclic Codes over Finite Fields</div>
                <div class="pub-authors"><strong>Dr. Academic Name</strong>, Co-Author One, Co-Author Two</div>
                <div class="pub-venue">Finite Fields and Their Applications, Vol. 88, 2025.</div>
                <div class="pub-actions">
                    <a href="#" class="pub-btn"><i class="fa-solid fa-file-pdf"></i> PDF</a>
                    <a href="#" class="pub-btn"><i class="fa-solid fa-link"></i> DOI</a>
                    <button class="pub-btn" onclick="toggleBib('bib1')"><i class="fa-solid fa-quote-right"></i> BibTeX</button>
                </div>
                <div id="bib1" class="bibtex-code">@article{name2025relative,
  title={On the Relative Galois Hulls of Constacyclic Codes over Finite Fields},
  author={Name, Academic and One, Co-Author and Two, Co-Author},
  journal={Finite Fields and Their Applications},
  volume={88},
  pages={102--115},
  year={2025},
  publisher={Elsevier}
}</div>
            </div>

            <!-- Publication 2 -->
            <div class="card pub-item" data-category="journal">
                <div class="pub-title">Entanglement-Assisted Quantum Codes derived from Skew Constacyclic Hulls</div>
                <div class="pub-authors">Co-Author One, <strong>Dr. Academic Name</strong></div>
                <div class="pub-venue">IEEE Transactions on Information Theory, Vol. 70, No. 4, 2024.</div>
                <div class="pub-actions">
                    <a href="#" class="pub-btn"><i class="fa-solid fa-file-pdf"></i> PDF</a>
                    <a href="#" class="pub-btn"><i class="fa-solid fa-link"></i> DOI</a>
                    <button class="pub-btn" onclick="toggleBib('bib2')"><i class="fa-solid fa-quote-right"></i> BibTeX</button>
                </div>
                <div id="bib2" class="bibtex-code">@article{name2024entanglement,
  title={Entanglement-Assisted Quantum Codes derived from Skew Constacyclic Hulls},
  author={One, Co-Author and Name, Academic},
  journal={IEEE Transactions on Information Theory},
  volume={70},
  number={4},
  pages={2450--2462},
  year={2024}
}</div>
            </div>

            <!-- Publication 3 -->
            <div class="card pub-item" data-category="preprint">
                <div class="pub-title">New Constructions of Linear Complementary Dual Codes via Plotkin Sums</div>
                <div class="pub-authors"><strong>Dr. Academic Name</strong>, Student Researcher</div>
                <div class="pub-venue">arXiv preprint arXiv:2601.12345, 2026.</div>
                <div class="pub-actions">
                    <a href="#" class="pub-btn"><i class="fa-solid fa-file-pdf"></i> arXiv</a>
                    <button class="pub-btn" onclick="toggleBib('bib3')"><i class="fa-solid fa-quote-right"></i> BibTeX</button>
                </div>
                <div id="bib3" class="bibtex-code">@article{name2026new,
  title={New Constructions of Linear Complementary Dual Codes via Plotkin Sums},
  author={Name, Academic and Researcher, Student},
  journal={arXiv preprint arXiv:2601.12345},
  year={2026}
}</div>
            </div>
        </section>

        <!-- Teaching Section -->
        <section id="teaching">
            <h2 class="section-title"><i class="fa-solid fa-chalkboard-user"></i> Teaching</h2>
            
            <div class="card">
                <h3 style="color: var(--text-dark);">Current Courses (Spring Semester 2026)</h3>
                <ul style="margin-top: 0.75rem; padding-left: 1.25rem;">
                    <li style="margin-bottom: 0.5rem;">
                        <strong>MAL 201: Linear Algebra & Matrix Theory</strong> <span class="badge">B.Tech</span>
                        <br><span style="font-size: 0.85rem; color: var(--text-muted);">Vector spaces, rank-nullity theorem, eigenvalues, matrix decompositions.</span>
                    </li>
                    <li>
                        <strong>MAL 705: Algebraic Coding Theory</strong> <span class="badge badge-phd">M.Tech / Ph.D.</span>
                        <br><span style="font-size: 0.85rem; color: var(--text-muted);">Linear codes, generator matrices, cyclic codes, bounds on code parameters.</span>
                    </li>
                </ul>
            </div>

            <div class="card">
                <h3 style="color: var(--text-dark);">Past Courses</h3>
                <ul style="margin-top: 0.75rem; padding-left: 1.25rem;">
                    <li style="margin-bottom: 0.5rem;"><strong>MAL 102: Discrete Mathematics & Graph Theory</strong> (Autumn 2025)</li>
                    <li><strong>MAL 304: Abstract Algebra & Rings</strong> (Spring 2025)</li>
                </ul>
            </div>
        </section>

        <!-- Students / Advisees Section -->
        <section id="students">
            <h2 class="section-title"><i class="fa-solid fa-users"></i> Advisees & Students</h2>

            <div class="card">
                <h3 style="color: var(--primary); margin-bottom: 0.75rem;">Doctoral Researchers (Ph.D.)</h3>
                <ul style="list-style: none;">
                    <li style="margin-bottom: 0.75rem; border-bottom: 1px solid var(--border-color); padding-bottom: 0.5rem;">
                        <strong>Student Name One</strong> <span class="badge badge-phd">Ongoing</span>
                        <br><span style="font-size: 0.85rem; color: var(--text-muted);">Research Area: Construction of Galois Hulls and EAQECCs over Finite Fields.</span>
                    </li>
                    <li>
                        <strong>Student Name Two</strong> <span class="badge badge-phd">Ongoing</span>
                        <br><span style="font-size: 0.85rem; color: var(--text-muted);">Research Area: Skew Constacyclic Code Hulls & Plotkin Sum Code Bounds.</span>
                    </li>
                </ul>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact">
            <h2 class="section-title"><i class="fa-solid fa-address-book"></i> Contact & Office Hours</h2>

            <div class="contact-grid">
                <div class="card">
                    <h3 style="margin-bottom: 1rem; color: var(--text-dark);">Contact Details</h3>
                    <ul class="contact-info-list">
                        <li>
                            <i class="fa-solid fa-location-dot"></i>
                            <div>
                                <strong>Office Address:</strong><br>
                                Room 304, Academic Block<br>
                                Department of Mathematics<br>
                                Institute Name, City - Pin Code
                            </div>
                        </li>
                        <li>
                            <i class="fa-solid fa-envelope"></i>
                            <div>
                                <strong>Email:</strong><br>
                                <a href="mailto:academic@institution.edu" style="color: var(--primary);">academic@institution.edu</a>
                            </div>
                        </li>
                    </ul>
                </div>

                <div class="card">
                    <h3 style="margin-bottom: 1rem; color: var(--text-dark);">Office Hours</h3>
                    <p style="font-size: 0.9rem; margin-bottom: 0.75rem;">Students are welcome to drop by during scheduled office hours or by appointment via email.</p>
                    <table style="width: 100%; font-size: 0.9rem; border-collapse: collapse;">
                        <tr style="border-bottom: 1px solid var(--border-color);">
                            <td style="padding: 0.4rem 0;"><strong>Mon / Wed:</strong></td>
                            <td style="padding: 0.4rem 0;">3:00 PM – 4:30 PM</td>
                        </tr>
                        <tr>
                            <td style="padding: 0.4rem 0;"><strong>Friday:</strong></td>
                            <td style="padding: 0.4rem 0;">10:30 AM – 12:00 PM</td>
                        </tr>
                    </table>
                </div>
            </div>
        </section>

    </main>

    <!-- JavaScript Interactivity -->
    <script>
        // Mobile Navigation Toggle
        const menuToggle = document.getElementById('menuToggle');
        const sidebar = document.getElementById('sidebar');

        menuToggle.addEventListener('click', () => {
            sidebar.classList.toggle('open');
        });

        // Publication Filtering
        function filterPubs(category) {
            const items = document.querySelectorAll('.pub-item');
            const buttons = document.querySelectorAll('.filter-btn');

            buttons.forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');

            items.forEach(item => {
                if (category === 'all' || item.getAttribute('data-category') === category) {
                    item.style.display = 'block';
                } else {
                    item.style.display = 'none';
                }
            });
        }

        // Toggle BibTeX snippet view
        function toggleBib(id) {
            const element = document.getElementById(id);
            if (element.style.display === 'block') {
                element.style.display = 'none';
            } else {
                element.style.display = 'block';
            }
        }
    </script>
</body>
</html>
