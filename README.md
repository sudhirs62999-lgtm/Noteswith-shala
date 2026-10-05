# Noteswith-shala<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Notes Shala | Study Notes</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background: #f5f7fb;
            color: #172033;
        }

        /* NAVBAR */
        nav {
            height: 70px;
            background: white;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 7%;
            box-shadow: 0 2px 12px rgba(0,0,0,0.08);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .logo {
            font-size: 27px;
            font-weight: bold;
            color: #4f46e5;
        }

        .logo span {
            color: #f97316;
        }

        nav a {
            text-decoration: none;
            color: #333;
            margin-left: 25px;
            font-weight: 500;
        }

        nav a:hover {
            color: #4f46e5;
        }

        /* HERO */
        .hero {
            min-height: 430px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 60px 8%;
            background: linear-gradient(135deg, #eef2ff, #fff7ed);
        }

        .hero-text {
            max-width: 600px;
        }

        .hero h1 {
            font-size: 52px;
            line-height: 1.1;
            margin-bottom: 20px;
        }

        .hero h1 span {
            color: #4f46e5;
        }

        .hero p {
            font-size: 18px;
            color: #667085;
            line-height: 1.6;
            margin-bottom: 30px;
        }

        .hero-btn {
            display: inline-block;
            background: #4f46e5;
            color: white;
            padding: 14px 25px;
            border-radius: 10px;
            text-decoration: none;
            font-weight: bold;
        }

        .hero-btn:hover {
            background: #3730a3;
        }

        .hero-image {
            font-size: 150px;
        }

        /* SEARCH */
        .search-area {
            padding: 35px 8%;
            background: white;
            text-align: center;
        }

        .search-box {
            width: 70%;
            max-width: 650px;
            padding: 16px 20px;
            border: 1px solid #ddd;
            border-radius: 30px;
            font-size: 16px;
            outline: none;
        }

        .search-box:focus {
            border-color: #4f46e5;
        }

        /* SUBJECTS */
        .section {
            padding: 60px 8%;
        }

        .section-title {
            text-align: center;
            font-size: 32px;
            margin-bottom: 40px;
        }

        .subjects {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .subject-card {
            background: white;
            padding: 35px;
            border-radius: 18px;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0,0,0,0.07);
            transition: 0.3s;
            cursor: pointer;
        }

        .subject-card:hover {
            transform: translateY(-7px);
            box-shadow: 0 12px 30px rgba(0,0,0,0.12);
        }

        .subject-icon {
            font-size: 55px;
            margin-bottom: 15px;
        }

        .subject-card h3 {
            font-size: 23px;
            margin-bottom: 10px;
        }

        .subject-card p {
            color: #667085;
        }

        /* NOTES */
        .notes-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .note-card {
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.06);
        }

        .note-card .tag {
            display: inline-block;
            background: #eef2ff;
            color: #4f46e5;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 12px;
            margin-bottom: 12px;
        }

        .note-card h3 {
            margin-bottom: 10px;
        }

        .note-card p {
            color: #667085;
            margin-bottom: 18px;
        }

        .view-btn {
            border: none;
            background: #4f46e5;
            color: white;
            padding: 10px 16px;
            border-radius: 7px;
            cursor: pointer;
        }

        /* UPLOAD */
        .upload-section {
            background: #111827;
            color: white;
            padding: 65px 8%;
        }

        .upload-box {
            max-width: 700px;
            margin: auto;
            background: #1f2937;
            padding: 35px;
            border-radius: 18px;
        }

        .upload-box h2 {
            text-align: center;
            margin-bottom: 25px;
        }

        .input {
            width: 100%;
            padding: 13px;
            margin-bottom: 15px;
            border: none;
            border-radius: 8px;
            outline: none;
        }

        select.input {
            background: white;
        }

        .upload-btn {
            width: 100%;
            padding: 14px;
            border: none;
            border-radius: 8px;
            background: #f97316;
            color: white;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
        }

        .upload-btn:hover {
            background: #ea580c;
        }

        /* FOOTER */
        footer {
            background: #0b1120;
            color: #9ca3af;
            text-align: center;
            padding: 25px;
        }

        footer strong {
            color: white;
        }

        /* MOBILE */
        @media(max-width: 800px) {

            nav {
                padding: 0 5%;
            }

            nav div:last-child {
                display: none;
            }

            .hero {
                text-align: center;
                padding: 50px 6%;
            }

            .hero h1 {
                font-size: 40px;
            }

            .hero-image {
                display: none;
            }

            .subjects,
            .notes-container {
                grid-template-columns: 1fr;
            }

            .search-box {
                width: 95%;
            }
        }
    </style>
</head>

<body>

    <!-- NAVBAR -->
    <nav>
        <div class="logo">Notes <span>Shala</span></div>

        <div>
            <a href="#home">Home</a>
            <a href="#subjects">Subjects</a>
            <a href="#notes">Notes</a>
            <a href="#upload">Upload</a>
        </div>
    </nav>


    <!-- HERO -->
    <section class="hero" id="home">

        <div class="hero-text">

            <h1>
                Study Smart with
                <span>Notes Shala</span>
            </h1>

            <p>
                Your one-stop destination for Physics, Chemistry
                and Mathematics notes. Learn better, revise faster
                and score higher.
            </p>

            <a href="#subjects" class="hero-btn">
                Explore Notes →
            </a>

        </div>

        <div class="hero-image">
            📚
        </div>

    </section>


    <!-- SEARCH -->
    <section class="search-area">

        <input
            type="text"
            id="search"
            class="search-box"
            placeholder="🔍 Search notes, chapters or topics..."
            onkeyup="searchNotes()"
        >

    </section>


    <!-- SUBJECTS -->
    <section class="section" id="subjects">

        <h2 class="section-title">
            Choose Your Subject
        </h2>

        <div class="subjects">

            <div class="subject-card"
                 onclick="filterSubject('Physics')">

                <div class="subject-icon">⚡</div>

                <h3>Physics</h3>

                <p>
                    Concepts, formulas,
                    derivations and numericals.
                </p>

            </div>


            <div class="subject-card"
                 onclick="filterSubject('Chemistry')">

                <div class="subject-icon">🧪</div>

                <h3>Chemistry</h3>

                <p>
                    Organic, inorganic and
                    physical chemistry notes.
                </p>

            </div>


            <div class="subject-card"
                 onclick="filterSubject('Mathematics')">

                <div class="subject-icon">📐</div>

                <h3>Mathematics</h3>

                <p>
                    Formulas, concepts and
                    step-by-step solutions.
                </p>

            </div>

        </div>

    </section>


    <!-- NOTES -->
    <section class="section" id="notes">

        <h2 class="section-title">
            Latest Notes
        </h2>

        <div class="notes-container" id="notesContainer">


            <div class="note-card">

                <span class="tag">Physics</span>

                <h3>Electrostatics</h3>

                <p>
                    Important concepts, formulas
                    and numerical problems.
                </p>

                <button class="view-btn"
                        onclick="openNote('Electrostatics')">
                    View Notes
                </button>

            </div>


            <div class="note-card">

                <span class="tag">Chemistry</span>

                <h3>Chemical Bonding</h3>

                <p>
                    Complete revision notes
                    for chemical bonding.
                </p>

                <button class="view-btn"
                        onclick="openNote('Chemical Bonding')">
                    View Notes
                </button>

            </div>


            <div class="note-card">

                <span class="tag">Mathematics</span>

                <h3>Matrices</h3>

                <p>
                    Important formulas and
                    solved examples.
                </p>

                <button class="view-btn"
                        onclick="openNote('Matrices')">
                    View Notes
                </button>

            </div>


        </div>

    </section>


    <!-- UPLOAD -->
    <section class="upload-section" id="upload">

        <div class="upload-box">

            <h2>📤 Upload Your Notes</h2>

            <input
                type="text"
                id="noteTitle"
                class="input"
                placeholder="Enter note title"
            >

            <select id="noteSubject" class="input">

                <option value="">
                    Select Subject
                </option>

                <option value="Physics">
                    Physics
                </option>

                <option value="Chemistry">
                    Chemistry
                </option>

                <option value="Mathematics">
                    Mathematics
                </option>

            </select>

            <input
                type="file"
                id="noteFile"
                class="input"
                accept=".pdf,.doc,.docx,.ppt,.pptx"
            >

            <button
                class="upload-btn"
                onclick="uploadNote()">
                Upload Note
            </button>

        </div>

    </section>


    <!-- FOOTER -->
    <footer>

        <p>
            © 2026 <strong>Notes Shala</strong>.
            Made for students 📚
        </p>

    </footer>


    <!-- JAVASCRIPT -->
    <script>

        function searchNotes() {

            let search =
                document.getElementById("search")
                .value
                .toLowerCase();

            let cards =
                document.querySelectorAll(".note-card");

            cards.forEach(function(card) {

                let text =
                    card.innerText.toLowerCase();

                if (text.includes(search)) {
                    card.style.display = "block";
                } else {
                    card.style.display = "none";
                }

            });

        }


        function filterSubject(subject) {

            let cards =
                document.querySelectorAll(".note-card");

            cards.forEach(function(card) {

                let text =
                    card.innerText.toLowerCase();

                if (text.includes(subject.toLowerCase())) {
                    card.style.display = "block";
                } else {
                    card.style.display = "none";
                }

            });

            document.getElementById("notes")
                .scrollIntoView({
                    behavior: "smooth"
                });

        }


        function openNote(noteName) {

            alert(
                "📚 " + noteName +
                "\\n\\nNotes will open here once you connect a PDF/file."
            );

        }


        function uploadNote() {

            let title =
                document.getElementById("noteTitle").value;

            let subject =
                document.getElementById("noteSubject").value;

            let file =
                document.getElementById("noteFile").files[0];


            if (title === "" ||
                subject === "" ||
                !file) {

                alert(
                    "Please enter title, select subject and choose a file."
                );

                return;
            }


            let container =
                document.getElementById("notesContainer");


            let card =
                document.createElement("div");

            card.className = "note-card";


            card.innerHTML = `

                <span class="tag">
                    ${subject}
                </span>

                <h3>
                    ${title}
                </h3>

                <p>
                    Uploaded file:
                    ${file.name}
                </p>

                <button class="view-btn">
                    ${file.name}
                </button>

            `;


            container.appendChild(card);


            alert(
                "✅ Note uploaded successfully!"
            );


            document.getElementById("noteTitle").value = "";

            document.getElementById("noteSubject").value = "";

            document.getElementById("noteFile").value = "";

        }

    </script>

</body>
</html>
