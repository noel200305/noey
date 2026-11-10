
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>ODIN PROJECT | Noel Thomas</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap');

:root {
    --bg: #080b14;
    --card: #111827;
    --text: #f8fafc;
    --muted: #9ca3af;
    --purple: #8b5cf6;
    --blue: #3b82f6;
    --border: rgba(255,255,255,0.09);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    font-family: 'Inter', sans-serif;
    background: var(--bg);
    color: var(--text);
    line-height: 1.7;
}

a {
    color: inherit;
    text-decoration: none;
}

.container {
    width: min(1100px, 90%);
    margin: auto;
}

/* NAVIGATION */

header {
    position: sticky;
    top: 0;
    z-index: 100;
    background: rgba(8,11,20,0.88);
    backdrop-filter: blur(18px);
    border-bottom: 1px solid var(--border);
}

nav {
    min-height: 75px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
}

.logo {
    font-size: 22px;
    font-weight: 800;
    letter-spacing: 1px;
}

.logo span {
    color: var(--purple);
}

.nav-links {
    display: flex;
    gap: 25px;
    list-style: none;
}

.nav-links a {
    color: var(--muted);
    font-size: 14px;
    transition: 0.3s;
}

.nav-links a:hover {
    color: white;
}

.menu-btn {
    display: none;
    background: none;
    border: 1px solid var(--border);
    color: white;
    padding: 8px 12px;
    border-radius: 8px;
    cursor: pointer;
}

/* HERO */

.hero {
    min-height: 85vh;
    display: flex;
    align-items: center;
    position: relative;
    overflow: hidden;
}

.hero::before {
    content: "";
    position: absolute;
    width: 450px;
    height: 450px;
    background: var(--purple);
    filter: blur(160px);
    opacity: 0.18;
    top: 5%;
    right: 5%;
}

.hero-content {
    position: relative;
    max-width: 800px;
}

.badge {
    display: inline-block;
    color: #c4b5fd;
    background: rgba(139,92,246,0.12);
    border: 1px solid rgba(139,92,246,0.3);
    padding: 7px 14px;
    border-radius: 30px;
    font-size: 13px;
    margin-bottom: 25px;
}

.hero h1 {
    font-size: clamp(42px, 8vw, 78px);
    line-height: 1.1;
    margin-bottom: 20px;
    letter-spacing: -3px;
}

.gradient-text {
    background: linear-gradient(90deg, #a78bfa, #60a5fa);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
}

.hero p {
    max-width: 650px;
    color: var(--muted);
    font-size: 17px;
    margin-bottom: 30px;
}

.buttons {
    display: flex;
    gap: 15px;
    flex-wrap: wrap;
}

.btn {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    padding: 12px 22px;
    border-radius: 10px;
    font-weight: 600;
    font-size: 14px;
    cursor: pointer;
    border: 1px solid var(--border);
    transition: 0.3s;
}

.btn-primary {
    background: linear-gradient(135deg, var(--purple), var(--blue));
    color: white;
    border: none;
}

.btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 35px rgba(139,92,246,0.25);
}

.btn-secondary {
    background: rgba(255,255,255,0.03);
}

.btn-secondary:hover {
    background: rgba(255,255,255,0.08);
}

/* SECTIONS */

section {
    padding: 100px 0;
    scroll-margin-top: 80px;
}

.section-heading {
    margin-bottom: 45px;
}

.section-heading .small-title {
    color: var(--purple);
    font-size: 13px;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: 700;
}

.section-heading h2 {
    font-size: clamp(30px, 5vw, 45px);
    margin-top: 8px;
    letter-spacing: -1px;
}

.section-heading p {
    color: var(--muted);
    margin-top: 10px;
}

/* ABOUT */

.about-grid {
    display: grid;
    grid-template-columns: 1.2fr 1fr;
    gap: 35px;
}

.about-text,
.info-card,
.skill-card,
.project-card,
.upload-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 18px;
    padding: 30px;
}

.about-text p {
    color: var(--muted);
    margin-bottom: 18px;
}

.info-list {
    display: grid;
    gap: 15px;
}

.info-item {
    display: flex;
    justify-content: space-between;
    gap: 15px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--border);
}

.info-item span {
    color: var(--muted);
}

.info-item strong {
    text-align: right;
}

/* SKILLS */

.skills-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 18px;
}

.skill-card {
    text-align: center;
    padding: 25px 15px;
    transition: 0.3s;
}

.skill-card:hover,
.project-card:hover {
    transform: translateY(-5px);
    border-color: rgba(139,92,246,0.5);
}

.skill-icon {
    font-size: 30px;
    margin-bottom: 12px;
}

.skill-card p {
    color: var(--muted);
    font-size: 13px;
}

/* PROJECTS */

.projects-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.project-card {
    transition: 0.3s;
}

.project-number {
    color: var(--purple);
    font-size: 13px;
    margin-bottom: 15px;
}

.project-card h3 {
    margin-bottom: 10px;
}

.project-card p {
    color: var(--muted);
    font-size: 14px;
}

/* UPLOAD */

.upload-card {
    background: linear-gradient(
        145deg,
        rgba(139,92,246,0.08),
        var(--card)
    );
}

.upload-area {
    border: 2px dashed rgba(139,92,246,0.45);
    border-radius: 16px;
    padding: 45px 20px;
    text-align: center;
    cursor: pointer;
    transition: 0.3s;
}

.upload-area:hover {
    background: rgba(139,92,246,0.08);
    border-color: var(--purple);
}

.upload-icon {
    font-size: 45px;
    margin-bottom: 10px;
}

.upload-area h3 {
    margin-bottom: 8px;
}

.upload-area p {
    color: var(--muted);
    font-size: 14px;
}

.upload-area input {
    display: none;
}

.upload-actions {
    display: flex;
    gap: 12px;
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 20px;
}

.upload-info {
    color: var(--muted);
    font-size: 13px;
    margin-top: 18px;
    text-align: center;
}

.file-list {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 15px;
    margin-top: 30px;
}

.file-item {
    display: flex;
    align-items: center;
    gap: 14px;
    background: rgba(255,255,255,0.03);
    border: 1px solid var(--border);
    padding: 15px;
    border-radius: 12px;
    min-width: 0;
}

.file-icon {
    font-size: 25px;
}

.file-details {
    flex: 1;
    min-width: 0;
}

.file-details strong {
    display: block;
    overflow-wrap: anywhere;
    font-size: 13px;
}

.file-details small {
    color: var(--muted);
    font-size: 12px;
}

.file-buttons {
    display: flex;
    gap: 8px;
}

.file-buttons button {
    background: rgba(255,255,255,0.06);
    color: white;
    border: 1px solid var(--border);
    padding: 7px 10px;
    border-radius: 7px;
    cursor: pointer;
}

.file-buttons button:hover {
    background: rgba(139,92,246,0.2);
}

.empty-files {
    text-align: center;
    color: var(--muted);
    padding: 25px;
    border: 1px solid var(--border);
    border-radius: 12px;
    margin-top: 25px;
}

/* CONTACT */

.contact-card {
    text-align: center;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 45px 20px;
}

.contact-card p {
    color: var(--muted);
    margin: 15px 0 25px;
}

/* FOOTER */

footer {
    border-top: 1px solid var(--border);
    padding: 25px 0;
    color: var(--muted);
    text-align: center;
    font-size: 13px;
}

/* MOBILE */

@media (max-width: 800px) {
    .menu-btn {
        display: block;
    }

    .nav-links {
        display: none;
        position: absolute;
        top: 75px;
        left: 0;
        right: 0;
        background: #111827;
        flex-direction: column;
        padding: 25px 5%;
        border-bottom: 1px solid var(--border);
    }

    .nav-links.active {
        display: flex;
    }

    .about-grid,
    .projects-grid {
        grid-template-columns: 1fr;
    }

    .skills-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .file-list {
        grid-template-columns: 1fr;
    }

    section {
        padding: 70px 0;
    }

    .hero {
        min-height: 75vh;
    }
}

@media (max-width: 450px) {
    .hero h1 {
        letter-spacing: -1.5px;
    }

    .info-item {
        flex-direction: column;
        gap: 3px;
    }

    .info-item strong {
        text-align: left;
    }
}
</style>
</head>

<body>

<!-- NAVIGATION -->

<header>
    <nav class="container">

        <a href="#home" class="logo">
            ODIN<span>.</span>
        </a>

        <button class="menu-btn" id="menuBtn"
                aria-label="Open navigation menu">
            ☰
        </button>

        <ul class="nav-links" id="navLinks">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About Me</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#upload">Upload All</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>

    </nav>
</header>

<!-- HOME -->

<section class="hero" id="home">

    <div class="container hero-content">

        <span class="badge">
            Computer Systems Student
        </span>

        <h1>
            Hello, I'm<br>
            <span class="gradient-text">Noel Thomas</span>
        </h1>

        <p>
            Welcome to ODIN PROJECT, my personal digital portfolio.
            Explore my academic journey, technical interests,
            projects, and learning experiences.
        </p>

        <div class="buttons">
            <a href="#about" class="btn btn-primary">
                About Me →
            </a>

            <a href="#upload" class="btn btn-secondary">
                Upload Files
            </a>
        </div>

    </div>

</section>

<!-- ABOUT ME -->

<section id="about">

    <div class="container">

        <div class="section-heading">
            <span class="small-title">Introduction</span>
            <h2>About Me</h2>
            <p>Get to know me and my educational journey.</p>
        </div>

        <div class="about-grid">

            <div class="about-text">

                <h3>Hello! I'm Noel Thomas,</h3>

                <br>

                <p>
                    I am currently studying Computer Systems
                    in my 6th semester at RNU.
                </p>

                <p>
                    I am passionate about technology, computer
                    systems, and learning new concepts in the
                    digital world. Through my studies, I continue
                    to explore subjects such as artificial
                    intelligence, modern computing, and
                    emerging technologies.
                </p>

                <p>
                    ODIN PROJECT is my personal digital portfolio,
                    created to showcase my projects, educational
                    materials, and academic progress.
                </p>

            </div>

            <div class="info-card">

                <h3>Personal Information</h3>

                <br>

                <div class="info-list">

                    <div class="info-item">
                        <span>Name</span>
                        <strong>Noel Thomas</strong>
                    </div>

                    <div class="info-item">
                        <span>University</span>
                        <strong>RNU</strong>
                    </div>

                    <div class="info-item">
                        <span>Program</span>
                        <strong>Computer Systems</strong>
                    </div>

                    <div class="info-item">
                        <span>Semester</span>
                        <strong>6th</strong>
                    </div>

                    <div class="info-item">
                        <span>Interests</span>
                        <strong>AI, Computing, Technology</strong>
                    </div>

                </div>

            </div>

        </div>

    </div>

</section>

<!-- SKILLS -->

<section id="skills">

    <div class="container">

        <div class="section-heading">
            <span class="small-title">What I Learn</span>
            <h2>My Skills</h2>
            <p>Technologies and subjects I explore during my studies.</p>
        </div>

        <div class="skills-grid">

            <div class="skill-card">
                <div class="skill-icon">💻</div>
                <h3>Programming</h3>
                <p>C, C++, Java</p>
            </div>

            <div class="skill-card">
                <div class="skill-icon">🌐</div>
                <h3>Web Development</h3>
                <p>HTML, CSS, JavaScript</p>
            </div>

            <div class="skill-card">
                <div class="skill-icon">🗄️</div>
                <h3>Database</h3>
                <p>SQL, MySQL</p>
            </div>

            <div class="skill-card">
                <div class="skill-icon">☁️</div>
                <h3>Cloud</h3>
                <p>AWS, Cloud Computing</p>
            </div>

        </div>

    </div>

</section>

<!-- PROJECTS -->

<section id="projects">

    <div class="container">

        <div class="section-heading">
            <span class="small-title">My Work</span>
            <h2>My Projects</h2>
            <p>Some areas of technology I work with and explore.</p>
        </div>

        <div class="projects-grid">

            <div class="project-card">
                <div class="project-number">PROJECT 01</div>
                <h3>Smart Home Automation</h3>
                <p>
                    A project exploring smart home systems,
                    automation, connected devices, and
                    modern technology.
                </p>
            </div>

            <div class="project-card">
                <div class="project-number">PROJECT 02</div>
                <h3>Android Application</h3>
                <p>
                    An Android application developed using
                    Kotlin and Jetpack Compose.
                </p>
            </div>

            <div class="project-card">
                <div class="project-number">PROJECT 03</div>
                <h3>Database Design</h3>
                <p>
                    A database project involving relational
                    models, SQL queries, and data management.
                </p>
            </div>

        </div>

    </div>

</section>

<!-- UPLOAD ALL -->

<section id="upload">

    <div class="container">

        <div class="section-heading">
            <span class="small-title">Personal Documents</span>
            <h2>Upload All</h2>
            <p>
                Upload and manage your files in one place.
            </p>
        </div>

        <div class="upload-card">

            <label class="upload-area" for="fileInput">

                <div class="upload-icon">📁</div>

                <h3>Upload Your Files</h3>

                <p>
                    Click here or drag files into this area.
                </p>

                <p>
                    Select multiple files at once.
                </p>

            </label>

            <input
                type="file"
                id="fileInput"
                multiple
            >

            <div class="upload-actions">

                <button class="btn btn-primary"
                        id="uploadBtn">
                    + Select Files
                </button>

                <button class="btn btn-secondary"
                        id="clearBtn">
                    Clear All
                </button>

            </div>

            <p class="upload-info" id="uploadInfo">
                No files uploaded yet.
            </p>

            <div id="fileList" class="file-list"></div>

        </div>

    </div>

</section>

<!-- CONTACT -->

<section id="contact">

    <div class="container">

        <div class="section-heading">
            <span class="small-title">Get In Touch</span>
            <h2>Contact Me</h2>
        </div>

        <div class="contact-card">

            <h3>Let's Connect</h3>

            <p>
                Thank you for visiting my personal portfolio.
                Feel free to connect with me.
            </p>

            <a href="#home" class="btn btn-primary">
                Back to Home ↑
            </a>

        </div>

    </div>

</section>

<!-- FOOTER -->

<footer>

    <div class="container">

        <p>
            © <span id="year"></span>
            Noel Thomas | ODIN PROJECT
        </p>

        <p>
            Designed with passion for technology.
        </p>

    </div>

</footer>

<script>

// MOBILE NAVIGATION

const menuBtn = document.getElementById("menuBtn");
const navLinks = document.getElementById("navLinks");

menuBtn.addEventListener("click", () => {
    navLinks.classList.toggle("active");
});

document.querySelectorAll(".nav-links a").forEach(link => {
    link.addEventListener("click", () => {
        navLinks.classList.remove("active");
    });
});

// FOOTER YEAR

document.getElementById("year").textContent =
    new Date().getFullYear();

// FILE UPLOAD

const fileInput = document.getElementById("fileInput");
const uploadBtn = document.getElementById("uploadBtn");
const clearBtn = document.getElementById("clearBtn");
const fileList = document.getElementById("fileList");
const uploadInfo = document.getElementById("uploadInfo");

let uploadedFiles = [];
let nextFileId = 0;

// OPEN FILE SELECTOR

uploadBtn.addEventListener("click", () => {
    fileInput.click();
});

// FILE SELECTION

fileInput.addEventListener("change", (event) => {

    const selectedFiles = Array.from(event.target.files);

    addFiles(selectedFiles);

    // Allow selecting the same file again
    fileInput.value = "";

});

// ADD FILES

function addFiles(files) {

    files.forEach(file => {

        const fileObject = {
            id: nextFileId++,
            file: file,
            url: URL.createObjectURL(file)
        };

        uploadedFiles.push(fileObject);

    });

    renderFiles();

}

// FILE SIZE

function formatFileSize(bytes) {

    if (bytes < 1024) {
        return bytes + " B";
    }

    if (bytes < 1024 * 1024) {
        return (bytes / 1024).toFixed(1) + " KB";
    }

    return (bytes / (1024 * 1024)).toFixed(1) + " MB";

}

// FILE ICON

function getFileIcon(fileName) {

    const extension = fileName
        .split(".")
        .pop()
        .toLowerCase();

    const icons = {
        pdf: "📕",
        doc: "📘",
        docx: "📘",
        ppt: "📊",
        pptx: "📊",
        xls: "📗",
        xlsx: "📗",
        jpg: "🖼️",
        jpeg: "🖼️",
        png: "🖼️",
        gif: "🖼️",
        zip: "📦",
        rar: "📦",
        txt: "📄",
        html: "🌐",
        css: "🎨",
        js: "💻",
        java: "☕",
        cpp: "💻"
    };

    return icons[extension] || "📄";

}

// DISPLAY FILES

function renderFiles() {

    fileList.innerHTML = "";

    const totalSize = uploadedFiles.reduce(
        (total, item) => total + item.file.size,
        0
    );

    uploadInfo.textContent =
        uploadedFiles.length +
        " file(s) selected • " +
        formatFileSize(totalSize);

    if (uploadedFiles.length === 0) {

        fileList.innerHTML = `
            <div class="empty-files">
                Your uploaded files will appear here.
            </div>
        `;

        return;

    }

    uploadedFiles.forEach(item => {

        const file = item.file;

        const fileElement = document.createElement("div");

        fileElement.className = "file-item";

        const icon = document.createElement("div");
        icon.className = "file-icon";
        icon.textContent = getFileIcon(file.name);

        const details = document.createElement("div");
        details.className = "file-details";

        const name = document.createElement("strong");
        name.textContent = file.name;

        const size = document.createElement("small");
        size.textContent = formatFileSize(file.size);

        details.appendChild(name);
        details.appendChild(size);

        const buttons = document.createElement("div");
        buttons.className = "file-buttons";

        const download = document.createElement("button");
        download.textContent = "↓";
        download.title = "Download file";

        download.addEventListener("click", () => {

            const link = document.createElement("a");

            link.href = item.url;
            link.download = file.name;

            document.body.appendChild(link);
            link.click();
            link.remove();

        });

        const remove = document.createElement("button");
        remove.textContent = "×";
        remove.title = "Remove file";

        remove.addEventListener("click", () => {

            removeFile(item.id);

        });

        buttons.appendChild(download);
        buttons.appendChild(remove);

        fileElement.appendChild(icon);
        fileElement.appendChild(details);
        fileElement.appendChild(buttons);

        fileList.appendChild(fileElement);

    });

}

// REMOVE FILE

function removeFile(id) {

    const fileToRemove = uploadedFiles.find(
        item => item.id === id
    );

    if (fileToRemove) {
        URL.revokeObjectURL(fileToRemove.url);
    }

    uploadedFiles = uploadedFiles.filter(
        item => item.id !== id
    );

    renderFiles();

}

// CLEAR ALL FILES

clearBtn.addEventListener("click", () => {

    uploadedFiles.forEach(item => {
        URL.revokeObjectURL(item.url);
    });

    uploadedFiles = [];

    renderFiles();

});

// DRAG AND DROP

const uploadArea = document.querySelector(".upload-area");

uploadArea.addEventListener("dragover", (event) => {

    event.preventDefault();

    uploadArea.style.background =
        "rgba(139,92,246,0.15)";

});

uploadArea.addEventListener("dragleave", () => {

    uploadArea.style.background = "";

});

uploadArea.addEventListener("drop", (event) => {

    event.preventDefault();

    uploadArea.style.background = "";

    const files = Array.from(event.dataTransfer.files);

    addFiles(files);

});

// INITIALIZE

renderFiles();

</script>

</body>
</html>

