## 1. Aim

To convert a desktop-only webpage into a responsive, mobile-first webpage using HTML, CSS, Flexbox, CSS Grid, and media queries.

## 2. Objective

- Make the webpage responsive on mobile, tablet, and desktop screens.
- Add the viewport meta tag.
- Follow a mobile-first CSS approach.
- Use at least two media-query breakpoints.
- Prevent horizontal overflow and overlapping elements.
- Test the webpage using Chrome DevTools Device Mode.

## 3. Project Structure

Create the following files inside your project folder:

```text
Assignment-9.1/
├── index.html
├── style.css
└── screenshots/
    ├── mobile.png
    ├── tablet.png
    └── desktop.png
```

## 4. HTML Code (index.html)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">

    <!-- Makes the webpage responsive on mobile devices -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <meta name="description" content="A responsive dashboard built using HTML and CSS">

    <title>Responsive Dashboard | Assignment 9.1</title>

    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Header -->
    <header class="header">
        <a href="#" class="logo">MyDashboard</a>

        <nav class="navigation">
            <a href="#home">Home</a>
            <a href="#overview">Overview</a>
            <a href="#projects">Projects</a>
            <a href="#contact">Contact</a>
        </nav>

        <button class="profile-button" type="button">
            My Profile
        </button>
    </header>

    <!-- Main Content -->
    <main class="container" id="home">

        <section class="welcome-section">
            <div>
                <p class="subtitle">DASHBOARD OVERVIEW</p>
                <h1>Welcome Back!</h1>
                <p class="welcome-text">
                    Manage your projects, track your progress, and stay
                    organized with your personal dashboard.
                </p>
            </div>

            <a href="#projects" class="primary-button">View Projects</a>
        </section>

        <!-- Statistics Cards -->
        <section class="stats-grid" id="overview">
            <article class="card stat-card">
                <div class="card-icon purple">P</div>
                <p class="card-label">Total Projects</p>
                <h2>12</h2>
                <p class="card-description">Projects in your workspace</p>
            </article>

            <article class="card stat-card">
                <div class="card-icon green">C</div>
                <p class="card-label">Completed</p>
                <h2>08</h2>
                <p class="card-description">Successfully completed</p>
            </article>

            <article class="card stat-card">
                <div class="card-icon orange">T</div>
                <p class="card-label">Tasks Pending</p>
                <h2>05</h2>
                <p class="card-description">Tasks remaining</p>
            </article>

            <article class="card stat-card">
                <div class="card-icon blue">P</div>
                <p class="card-label">Productivity</p>
                <h2>85%</h2>
                <p class="card-description">Your overall progress</p>
            </article>
        </section>

        <!-- Projects Section -->
        <section class="projects-section" id="projects">
            <div class="section-heading">
                <div>
                    <p class="subtitle">YOUR WORKSPACE</p>
                    <h2>Recent Projects</h2>
                </div>

                <a href="#projects" class="view-link">View All</a>
            </div>

            <div class="projects-grid">

                <article class="card project-card">
                    <div class="project-banner banner-purple">
                        <span>WEB DEVELOPMENT</span>
                    </div>

                    <div class="project-content">
                        <h3>Portfolio Website</h3>
                        <p>
                            A personal portfolio to showcase skills,
                            projects, and achievements.
                        </p>

                        <div class="progress-info">
                            <span>Progress</span>
                            <span>80%</span>
                        </div>

                        <div class="progress-bar">
                            <div class="progress-fill fill-purple progress-80"></div>
                        </div>

                        <div class="project-footer">
                            <span class="status completed">Completed Soon</span>
                            <span>12 Oct</span>
                        </div>
                    </div>
                </article>

                <article class="card project-card">
                    <div class="project-banner banner-green">
                        <span>UI / UX DESIGN</span>
                    </div>

                    <div class="project-content">
                        <h3>College Website</h3>
                        <p>
                            A responsive website for displaying college
                            information and student activities.
                        </p>

                        <div class="progress-info">
                            <span>Progress</span>
                            <span>55%</span>
                        </div>

                        <div class="progress-bar">
                            <div class="progress-fill fill-green progress-55"></div>
                        </div>

                        <div class="project-footer">
                            <span class="status in-progress">In Progress</span>
                            <span>18 Oct</span>
                        </div>
                    </div>
                </article>

                <article class="card project-card">
                    <div class="project-banner banner-orange">
                        <span>PROGRAMMING</span>
                    </div>

                    <div class="project-content">
                        <h3>Student Management</h3>
                        <p>
                            A simple system to organize student details
                            and academic information.
                        </p>

                        <div class="progress-info">
                            <span>Progress</span>
                            <span>30%</span>
                        </div>

                        <div class="progress-bar">
                            <div class="progress-fill fill-orange progress-30"></div>
                        </div>

                        <div class="project-footer">
                            <span class="status in-progress">In Progress</span>
                            <span>25 Oct</span>
                        </div>
                    </div>
                </article>

            </div>
        </section>

        <!-- Activity Section -->
        <section class="activity-section">
            <h2>Recent Activity</h2>

            <div class="card activity-card">
                <div class="activity-item">
                    <span class="activity-dot dot-purple"></span>
                    <div>
                        <h3>Portfolio Website updated</h3>
                        <p>Project progress was updated to 80%.</p>
                    </div>
                    <span class="activity-time">Today</span>
                </div>

                <div class="activity-item">
                    <span class="activity-dot dot-green"></span>
                    <div>
                        <h3>College Website started</h3>
                        <p>A new design task was added.</p>
                    </div>
                    <span class="activity-time">Yesterday</span>
                </div>

                <div class="activity-item">
                    <span class="activity-dot dot-orange"></span>
                    <div>
                        <h3>Student Management created</h3>
                        <p>A new programming project was created.</p>
                    </div>
                    <span class="activity-time">2 days ago</span>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="footer" id="contact">
        <p>&copy; 2026 MyDashboard. Created for Assignment 9.1.</p>
        <p>Designed with HTML and CSS.</p>
    </footer>

</body>
</html>
```

## 5. CSS Code (style.css)

```css
/* =====================================
   1. Global Styles
===================================== */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #f5f7fb;
    color: #1e293b;
    line-height: 1.6;
    min-width: 0;
}

a {
    text-decoration: none;
    color: inherit;
}

button,
a {
    -webkit-tap-highlight-color: transparent;
}

button {
    font: inherit;
}

img {
    max-width: 100%;
    height: auto;
    display: block;
}

.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 24px 16px;
}

/* =====================================
   2. Header — Mobile First
===================================== */

.header {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 16px;
    padding: 18px 16px;
    background-color: #ffffff;
    border-bottom: 1px solid #e5e7eb;
}

.logo {
    font-size: 22px;
    font-weight: 800;
    color: #6546d7;
    overflow-wrap: anywhere;
}

.navigation {
    display: flex;
    flex-wrap: wrap;
    gap: 10px 16px;
    width: 100%;
}

.navigation a {
    font-size: 14px;
    color: #64748b;
}

.navigation a:hover {
    color: #6546d7;
}

.profile-button {
    padding: 9px 15px;
    border: none;
    border-radius: 8px;
    background-color: #6546d7;
    color: #ffffff;
    cursor: pointer;
}

/* =====================================
   3. Welcome Section
===================================== */

.welcome-section {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;
    margin-bottom: 28px;
}

.subtitle {
    color: #6546d7;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 1.5px;
    margin-bottom: 8px;
}

.welcome-section h1 {
    font-size: clamp(27px, 6vw, 36px);
    line-height: 1.2;
    margin-bottom: 12px;
}

.welcome-text {
    max-width: 560px;
    color: #64748b;
    font-size: 15px;
    overflow-wrap: anywhere;
}

.primary-button {
    display: inline-block;
    padding: 11px 18px;
    background-color: #6546d7;
    color: #ffffff;
    border-radius: 8px;
    font-size: 14px;
    font-weight: 600;
}

.primary-button:hover {
    background-color: #5033bc;
}

/* =====================================
   4. Statistics Grid
===================================== */

.stats-grid {
    display: grid;
    grid-template-columns: minmax(0, 1fr);
    gap: 16px;
    margin-bottom: 38px;
}

.card {
    background-color: #ffffff;
    border: 1px solid #e8ebf2;
    border-radius: 14px;
    box-shadow: 0 4px 15px rgba(30, 41, 59, 0.04);
    min-width: 0;
}

.stat-card {
    padding: 20px;
}

.card-icon {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 40px;
    height: 40px;
    border-radius: 10px;
    font-weight: 800;
    margin-bottom: 15px;
}

.purple {
    background-color: #eee8ff;
    color: #6546d7;
}

.green {
    background-color: #dcfce7;
    color: #15803d;
}

.orange {
    background-color: #ffedd5;
    color: #c2410c;
}

.blue {
    background-color: #dbeafe;
    color: #1d4ed8;
}

.card-label {
    color: #64748b;
    font-size: 13px;
}

.stat-card h2 {
    font-size: 29px;
    margin: 4px 0;
}

.card-description {
    color: #94a3b8;
    font-size: 12px;
    overflow-wrap: anywhere;
}

/* =====================================
   5. Projects Section
===================================== */

.projects-section {
    margin-bottom: 38px;
}

.section-heading {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
    margin-bottom: 20px;
}

.section-heading h2,
.activity-section > h2 {
    font-size: 22px;
    line-height: 1.3;
}

.view-link {
    color: #6546d7;
    font-size: 13px;
    font-weight: 700;
    flex-shrink: 0;
}

.projects-grid {
    display: grid;
    grid-template-columns: minmax(0, 1fr);
    gap: 18px;
}

.project-card {
    overflow: hidden;
}

.project-banner {
    min-height: 120px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
}

.project-banner span {
    padding: 7px 10px;
    border-radius: 6px;
    background-color: rgba(255, 255, 255, 0.85);
    color: #334155;
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 1px;
    text-align: center;
}

.banner-purple {
    background: linear-gradient(135deg, #ddd6fe, #a78bfa);
}

.banner-green {
    background: linear-gradient(135deg, #bbf7d0, #6ee7b7);
}

.banner-orange {
    background: linear-gradient(135deg, #fed7aa, #fdba74);
}

.project-content {
    padding: 20px;
}

.project-content h3 {
    font-size: 17px;
    margin-bottom: 8px;
}

.project-content > p {
    color: #64748b;
    font-size: 13px;
    min-height: 42px;
    overflow-wrap: anywhere;
}

.progress-info {
    display: flex;
    justify-content: space-between;
    gap: 10px;
    margin-top: 20px;
    margin-bottom: 8px;
    color: #64748b;
    font-size: 12px;
}

.progress-bar {
    height: 7px;
    background-color: #e9edf5;
    border-radius: 20px;
    overflow: hidden;
}

.progress-fill {
    height: 100%;
    border-radius: 20px;
}

.progress-80 {
    width: 80%;
}

.progress-55 {
    width: 55%;
}

.progress-30 {
    width: 30%;
}

.fill-purple {
    background-color: #6546d7;
}

.fill-green {
    background-color: #22c55e;
}

.fill-orange {
    background-color: #f97316;
}

.project-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 18px;
    color: #94a3b8;
    font-size: 12px;
}

.status {
    padding: 5px 8px;
    border-radius: 6px;
    font-size: 11px;
    font-weight: 700;
}

.completed {
    background-color: #dcfce7;
    color: #15803d;
}

.in-progress {
    background-color: #fef3c7;
    color: #92400e;
}

/* =====================================
   6. Recent Activity
===================================== */

.activity-section {
    margin-bottom: 24px;
}

.activity-section > h2 {
    margin-bottom: 18px;
}

.activity-card {
    padding: 4px 18px;
}

.activity-item {
    display: grid;
    grid-template-columns: 10px minmax(0, 1fr);
    align-items: start;
    gap: 12px;
    padding: 18px 0;
    border-bottom: 1px solid #edf0f5;
}

.activity-item:last-child {
    border-bottom: none;
}

.activity-dot {
    width: 9px;
    height: 9px;
    border-radius: 50%;
    margin-top: 7px;
}

.dot-purple {
    background-color: #6546d7;
}

.dot-green {
    background-color: #22c55e;
}

.dot-orange {
    background-color: #f97316;
}

.activity-item h3 {
    font-size: 14px;
    overflow-wrap: anywhere;
}

.activity-item p {
    color: #64748b;
    font-size: 12px;
    overflow-wrap: anywhere;
}

.activity-time {
    grid-column: 2;
    color: #94a3b8;
    font-size: 11px;
}

/* =====================================
   7. Footer
===================================== */

.footer {
    display: flex;
    flex-direction: column;
    gap: 5px;
    text-align: center;
    padding: 22px 16px;
    background-color: #ffffff;
    border-top: 1px solid #e5e7eb;
    color: #64748b;
    font-size: 12px;
}

/* =====================================
   8. Breakpoint 1 — Tablet
   Screens 600px and wider
===================================== */

@media (min-width: 600px) {

    .header {
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        padding: 18px 24px;
    }

    .navigation {
        width: auto;
        flex: 1;
        justify-content: center;
        gap: 16px;
    }

    .container {
        padding: 32px 24px;
    }

    .welcome-section {
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    .stats-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .projects-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .activity-item {
        grid-template-columns: 10px minmax(0, 1fr) auto;
        align-items: center;
    }

    .activity-time {
        grid-column: auto;
    }

    .footer {
        flex-direction: row;
        justify-content: space-between;
        padding: 22px 24px;
    }
}

/* =====================================
   9. Breakpoint 2 — Desktop
   Screens 1024px and wider
===================================== */

@media (min-width: 1024px) {

    .header {
        padding: 20px max(32px, calc((100% - 1152px) / 2));
    }

    .container {
        padding: 40px 24px;
    }

    .welcome-section {
        margin-bottom: 36px;
    }

    .stats-grid {
        grid-template-columns: repeat(4, minmax(0, 1fr));
        gap: 20px;
    }

    .projects-grid {
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 22px;
    }

    .project-banner {
        min-height: 150px;
    }

    .footer {
        padding-left: max(32px, calc((100% - 1152px) / 2));
        padding-right: max(32px, calc((100% - 1152px) / 2));
    }
}

/* =====================================
   10. Extra Small Screen Protection
===================================== */

@media (max-width: 360px) {

    .container {
        padding-left: 12px;
        padding-right: 12px;
    }

    .header {
        padding-left: 12px;
        padding-right: 12px;
    }

    .navigation {
        gap: 8px 12px;
    }

    .stat-card,
    .project-content {
        padding: 15px;
    }

    .section-heading h2,
    .activity-section > h2 {
        font-size: 19px;
    }
}
```

## 6. Mobile-First Design Explanation

The webpage is designed for mobile devices first. The default CSS styles are applied to smaller screens, and media queries progressively improve the layout for larger devices.

### Breakpoints Used

| Screen Type | Breakpoint | Layout |
|---|---|---|
| Mobile | Below 600px | One-column cards and vertically arranged header |
| Tablet | 600px and above | Two-column statistics and project cards |
| Desktop | 1024px and above | Four-column statistics and three-column project cards |

An additional breakpoint at 360px helps the layout fit smaller mobile screens.

## 7. Steps to Run the Project

1. Open Visual Studio Code.
2. Create a folder named `Assignment-9.1`.
3. Create `index.html` and `style.css`.
4. Copy the HTML code into `index.html`.
5. Copy the CSS code into `style.css`.
6. Save both files.
7. Open `index.html` using the Live Server extension.
8. Verify that the webpage opens correctly in your browser.

## 8. Testing Using Chrome DevTools

1. Open the webpage in Google Chrome.
2. Right-click anywhere on the page and select **Inspect**.
3. Click the **Toggle Device Toolbar** icon, or press `Ctrl + Shift + M`.
4. Select a mobile device or enter a custom viewport size.
5. Test the following viewport sizes:

| Device Type | Example Viewport |
|---|---|
| Mobile | 375 × 812 |
| Tablet | 768 × 1024 |
| Desktop | 1440 × 900 |

6. Check that cards fit the available width.
7. Check that navigation links wrap without overlapping.
8. Confirm that no unwanted horizontal scrollbar appears.
9. Check that text remains readable and buttons remain accessible.
10. Repeat the tests at different viewport sizes.

## 9. Screenshot Submission

Capture three screenshots of the running webpage using Chrome DevTools.

- **Mobile:** Set the viewport to 375 × 812 and save the screenshot as `mobile.png`.
- **Tablet:** Set the viewport to 768 × 1024 and save the screenshot as `tablet.png`.
- **Desktop:** Set the viewport to 1440 × 900 and save the screenshot as `desktop.png`.

Save all three images inside the `screenshots` folder.

To capture each screenshot, use Chrome DevTools' device toolbar and the browser's screenshot option, or use your computer's screenshot tool. Make sure the full webpage layout is visible and readable in each screenshot. The screenshots should be captured from the actual running webpage.

## 10. Problems Fixed

1. Added the viewport meta tag to support mobile scaling.
2. Replaced fixed multi-column layouts with responsive CSS Grid.
3. Used Flexbox to arrange and wrap navigation links.
4. Added breakpoints for tablet and desktop layouts.
5. Used `minmax(0, 1fr)` to help prevent grid items from overflowing.
6. Used `box-sizing: border-box` for predictable element sizing.
7. Used flexible widths, wrapping, and responsive font sizes.
8. Added extra-small-screen adjustments to prevent content from becoming cramped.
9. Checked for overlapping elements and unwanted horizontal scrolling.

## 11. Result

The desktop-style dashboard was converted into a responsive, mobile-first webpage using HTML and CSS. The layout adjusts to mobile, tablet, and desktop screen sizes with responsive cards, navigation, project sections, and footer content.

The webpage can be tested using Chrome DevTools Device Mode, and screenshots of the three viewport sizes can be submitted with the HTML and CSS files.

## 12. Conclusion

This assignment demonstrates how to create responsive websites using a mobile-first approach. By using CSS Grid, Flexbox, media queries, and the viewport meta tag, a webpage can provide a consistent and user-friendly experience across different screen sizes.
