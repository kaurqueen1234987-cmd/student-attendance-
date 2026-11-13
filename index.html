
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Student Attendance System</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background: #f0f4fa;
    color: #243047;
}

header {
    background: linear-gradient(120deg,#1746a2,#3979e8);
    color: white;
    padding: 25px;
    text-align: center;
}

header h1 {
    margin-bottom: 8px;
}

.container {
    max-width: 1100px;
    margin: 30px auto;
    padding: 15px;
}

.stats {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(180px,1fr));
    gap: 15px;
    margin-bottom: 25px;
}

.card {
    background: white;
    padding: 22px;
    border-radius: 12px;
    box-shadow: 0 3px 12px #00000010;
}

.card h3 {
    color: #65748b;
    font-size: 14px;
}

.card p {
    font-size: 30px;
    font-weight: bold;
    margin-top: 10px;
    color: #245ac1;
}

.form-box, .table-box {
    background: white;
    padding: 25px;
    border-radius: 12px;
    margin-bottom: 25px;
    box-shadow: 0 3px 12px #00000010;
}

h2 {
    margin-bottom: 20px;
    color: #194b9c;
}

.form-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(200px,1fr));
    gap: 15px;
}

label {
    display: block;
    margin-bottom: 7px;
    font-weight: bold;
}

input, select {
    width: 100%;
    padding: 12px;
    border: 1px solid #ccd5e3;
    border-radius: 7px;
    font-size: 15px;
}

button {
    padding: 11px 17px;
    border: none;
    border-radius: 7px;
    cursor: pointer;
    font-weight: bold;
    color: white;
    margin: 5px 3px;
}

.add-btn {
    background: #245fc5;
    margin-top: 20px;
}

.present-btn {
    background: #159957;
}

.absent-btn {
    background: #e24c4c;
}

.delete-btn {
    background: #596579;
}

.search {
    margin: 10px 0 20px;
    max-width: 350px;
}

table {
    width: 100%;
    border-collapse: collapse;
    min-width: 650px;
}

th, td {
    padding: 13px;
    border-bottom: 1px solid #e4e9f0;
    text-align: left;
}

th {
    background: #edf3ff;
    color: #194b9c;
}

.table-scroll {
    overflow-x: auto;
}

.status {
    font-weight: bold;
}

.present {
    color: #159957;
}

.absent {
    color: #e24c4c;
}

@media(max-width:600px) {
    .container {
        padding: 10px;
    }

    .form-box, .table-box {
        padding: 15px;
    }
}
</style>
</head>

<body>

<header>
    <h1>🎓 Student Attendance System</h1>
    <p>Manage Your Student Attendance Easily</p>
</header>

<div class="container">

    <!-- Dashboard -->
    <div class="stats">
        <div class="card">
            <h3>Total Students</h3>
            <p id="total">0</p>
        </div>

        <div class="card">
            <h3>Present Today</h3>
            <p id="presentCount">0</p>
        </div>

        <div class="card">
            <h3>Absent Today</h3>
            <p id="absentCount">0</p>
        </div>

        <div class="card">
            <h3>Attendance %</h3>
            <p id="percentage">0%</p>
        </div>
    </div>

    <!-- Registration Form -->
    <div class="form-box">
        <h2>➕ Register New Student</h2>

        <form id="studentForm">
            <div class="form-grid">

                <div>
                    <label>Full Name</label>
                    <input type="text" id="name"
                    placeholder="Enter student name" required>
                </div>

                <div>
                    <label>Roll Number</label>
                    <input type="text" id="roll"
                    placeholder="Enter roll number" required>
                </div>

                <div>
                    <label>Email</label>
                    <input type="email" id="email"
                    placeholder="Enter email" required>
                </div>

                <div>
                    <label>Course</label>
                    <select id="course" required>
                        <option value="">Select Course</option>
                        <option>B.Tech CSE</option>
                        <option>BCA</option>
                        <option>BBA</option>
                        <option>B.Com</option>
                        <option>MCA</option>
                    </select>
                </div>

            </div>

            <button type="submit" class="add-btn">
                Register Student
            </button>
        </form>
    </div>

    <!-- Attendance -->
    <div class="table-box">
        <h2>📋 Mark Student Attendance</h2>

        <label>Select Attendance Date</label>
        <input type="date" id="attendanceDate">

        <input type="text" id="search"
        class="search" placeholder="🔍 Search student...">

        <div class="table-scroll">
            <table>
                <thead>
                    <tr>
                        <th>Roll No.</th>
                        <th>Name</th>
                        <th>Course</th>
                        <th>Status</th>
                        <th>Action</th>
                    </tr>
                </thead>

                <tbody id="studentList"></tbody>
            </table>
        </div>
    </div>

</div>

<script>

// Get saved students
let students = JSON.parse(
    localStorage.getItem("students")
) || [];

// Today's date
const dateInput = document.getElementById("attendanceDate");
dateInput.value = new Date().toISOString().split("T")[0];

// Save data
function saveData() {
    localStorage.setItem("students", JSON.stringify(students));
}

// Register student
document.getElementById("studentForm")
.addEventListener("submit", function(e) {

    e.preventDefault();

    const roll = document.getElementById("roll").value.trim();

    if(students.some(s => s.roll.toLowerCase() === roll.toLowerCase())) {
        alert("This roll number already exists!");
        return;
    }

    const student = {
        name: document.getElementById("name").value.trim(),
        roll: roll,
        email: document.getElementById("email").value.trim(),
        course: document.getElementById("course").value,
        attendance: {}
    };

    students.push(student);

    saveData();
    this.reset();
    renderStudents();

    alert("Student registered successfully!");
});

// Mark attendance
function markAttendance(index, status) {

    const date = dateInput.value;

    if(!date) {
        alert("Please select a date!");
        return;
    }

    students[index].attendance[date] = status;

    saveData();
    renderStudents();
}

// Delete student
function deleteStudent(index) {

    if(confirm("Are you sure you want to delete this student?")) {
        students.splice(index, 1);
        saveData();
        renderStudents();
    }
}

// Display students
function renderStudents() {

    const list = document.getElementById("studentList");
    const search = document.getElementById("search").value.toLowerCase();
    const date = dateInput.value;

    list.innerHTML = "";

    let present = 0;
    let absent = 0;

    students.forEach((student, index) => {

        const status = student.attendance[date] || "Not Marked";

        if(status === "Present") present++;
        if(status === "Absent") absent++;

        if(
            student.name.toLowerCase().includes(search) ||
            student.roll.toLowerCase().includes(search)
        ) {

            const row = document.createElement("tr");

            const cells = [
                student.roll,
                student.name,
                student.course,
                status
            ];

            cells.forEach((value, i) => {
                const td = document.createElement("td");
                td.textContent = value;

                if(i === 3) {
                    td.className = "status " +
                        (status === "Present" ? "present" :
                        status === "Absent" ? "absent" : "");
                }

                row.appendChild(td);
            });

            const action = document.createElement("td");

            const pBtn = document.createElement("button");
            pBtn.textContent = "Present";
            pBtn.className = "present-btn";
            pBtn.onclick = () => markAttendance(index, "Present");

            const aBtn = document.createElement("button");
            aBtn.textContent = "Absent";
            aBtn.className = "absent-btn";
            aBtn.onclick = () => markAttendance(index, "Absent");

            const dBtn = document.createElement("button");
            dBtn.textContent = "Delete";
            dBtn.className = "delete-btn";
            dBtn.onclick = () => deleteStudent(index);

            action.append(pBtn, aBtn, dBtn);
            row.appendChild(action);

            list.appendChild(row);
        }
    });

    const total = students.length;
    const marked = present + absent;
    const percentage = marked > 0
        ? ((present / marked) * 100).toFixed(1)
        : 0;

    document.getElementById("total").textContent = total;
    document.getElementById("presentCount").textContent = present;
    document.getElementById("absentCount").textContent = absent;
    document.getElementById("percentage").textContent = percentage + "%";
}

// Search students
document.getElementById("search")
.addEventListener("input", renderStudents);

// Date change
dateInput.addEventListener("change", renderStudents);

// Initial display
renderStudents();

</script>

</body>
</html>
