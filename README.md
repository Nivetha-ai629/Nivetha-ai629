<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Student Form Output</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f4f8;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            min-height: 100vh;
        }

        .container {
            background-color: white;
            padding: 30px;
            margin-top: 40px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            width: 350px;
        }

        h2 {
            text-align: center;
            color: #333;
        }

        label {
            font-weight: bold;
        }

        input[type="text"],
        input[type="email"],
        input[type="number"] {
            width: 100%;
            padding: 10px;
            margin: 6px 0 15px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        input[type="submit"] {
            width: 100%;
            background-color: #4CAF50;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }

        input[type="submit"]:hover {
            background-color: #45a049;
        }

        .output {
            margin-top: 30px;
            padding: 15px;
            background-color: #e7f5ff;
            border: 1px solid #b3d4fc;
            border-radius: 8px;
            width: 350px;
        }

        .output p {
            margin: 5px 0;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Student Registration</h2>
    <form id="studentForm">
        <label for="dept">Department:</label>
        <input type="text" id="dept" name="dept" value="M.Tech CSE Integrated" required>

        <label for="id">Student ID:</label>
        <input type="text" id="id" name="id" value="sec21cj064" required>

        <label for="name">Name:</label>
        <input type="text" id="name" name="name" value="Nivetha D" required>

        <label for="cgpa">CGPA:</label>
        <input type="number" id="cgpa" name="cgpa" step="0.1" value="6" required>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email" value="sec21cj064@sairamtap.edu.in" required>

        <input type="submit" value="Submit">
    </form>
</div>

<!-- Output Display -->
<div class="output" id="outputBox" style="display:none;">
    <h3>Submitted Details:</h3>
    <p id="outDept"></p>
    <p id="outID"></p>
    <p id="outName"></p>
    <p id="outCGPA"></p>
    <p id="outEmail"></p>
</div>

<script>
    document.getElementById('studentForm').addEventListener('submit', function(event) {
        event.preventDefault();

        // Get input values
        const dept = document.getElementById('dept').value;
        const id = document.getElementById('id').value;
        const name = document.getElementById('name').value;
        const cgpa = document.getElementById('cgpa').value;
        const email = document.getElementById('email').value;

        // Display in output section
        document.getElementById('outDept').textContent = "Department: " + dept;
        document.getElementById('outID').textContent = "Student ID: " + id;
        document.getElementById('outName').textContent = "Name: " + name;
        document.getElementById('outCGPA').textContent = "CGPA: " + cgpa;
        document.getElementById('outEmail').textContent = "Email: " + email;

        document.getElementById('outputBox').style.display = "block";
    });
</script>

</body>
</html>
