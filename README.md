# Advanced HTML5 Elements and Forms

## Objectives
Implement HTML5 images, lists, tables, forms and input types.
Use form validation attributes.
Apply multimedia elements such as audio and video.

## Instructions

- Create an index.html file.
- Add an ordered list with roman numerals
- Add an external image from pexels.com
- Add a table of 5 contacts with; name, address, mobile and emails
- Add a registration form

>[!NOTE]
>  The registration form should have:
>- Name, email, password, and date fields.
>- A dropdown, radio buttons, and checkboxes.
>- Proper labels and placeholders.
>- Required fields and validation attributes.
>- Ensure proper indentation and commenting.
 
# Tasks
- Create a well-structured HTML5 document.
- Ensure semantic correctness.

  <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My HTML Document</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            background-color: #f4f4f4;
            color: #333;
        }
        h1, h2, h3 {
            color: #0056b3;
        }
        section {
            background-color: #fff;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        img {
            max-width: 100%;
            height: auto;
            display: block;
            margin-top: 15px;
            border-radius: 5px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
        }
        table, th, td {
            border: 1px solid #ddd;
        }
        th, td {
            padding: 10px;
            text-align: left;
        }
        th {
            background-color: #0056b3;
            color: white;
        }
        form {
            display: grid;
            gap: 15px;
            margin-top: 15px;
        }
        label {
            font-weight: bold;
            margin-bottom: 5px;
            display: block;
        }
        input[type="text"],
        input[type="email"],
        input[type="password"],
        input[type="date"],
        select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box; /* Ensures padding doesn't affect total width */
        }
        input[type="radio"],
        input[type="checkbox"] {
            margin-right: 5px;
        }
        .form-group {
            margin-bottom: 10px;
        }
        .form-group.radio-group,
        .form-group.checkbox-group {
            border: 1px solid #eee;
            padding: 10px;
            border-radius: 4px;
            background-color: #f9f9f9;
        }
        button {
            background-color: #28a745;
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }
        button:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>

    <header>
        <h1>Welcome to My HTML Document</h1>
        <p>This document demonstrates various HTML5 elements.</p>
    </header>

    <main>
        <section>
            <h2>My Favorite Hobbies</h2>
            <ol type="I">
                <li>Reading</li>
                <li>Hiking</li>
                <li>Coding</li>
                <li>Photography</li>
                <li>Cooking</li>
            </ol>
        </section>

        <section>
            <h2>A Beautiful Landscape</h2>
            <img src="https://images.pexels.com/photos/33045/lion-tiger-cat-animal.jpg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" alt="A majestic lion looking into the distance" title="Lion from Pexels">
            <p>Image courtesy of Pexels.com</p>
        </section>

        <section>
            <h2>Contact List</h2>
            <table>
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Address</th>
                        <th>Mobile</th>
                        <th>Email</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>John Doe</td>
                        <td>123 Main St, Anytown</td>
                        <td>+254 712 345678</td>
                        <td>john.doe@example.com</td>
                    </tr>
                    <tr>
                        <td>Jane Smith</td>
                        <td>456 Oak Ave, Somewhere</td>
                        <td>+254 723 456789</td>
                        <td>jane.smith@example.com</td>
                    </tr>
                    <tr>
                        <td>Peter Jones</td>
                        <td>789 Pine Rd, Nowhere</td>
                        <td>+254 734 567890</td>
                        <td>peter.jones@example.com</td>
                    </tr>
                    <tr>
                        <td>Mary Brown</td>
                        <td>101 Cedar Blvd, Here</td>
                        <td>+254 745 678901</td>
                        <td>mary.brown@example.com</td>
                    </tr>
                    <tr>
                        <td>Robert White</td>
                        <td>202 Birch Ln, There</td>
                        <td>+254 756 789012</td>
                        <td>robert.white@example.com</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <section>
            <h2>User Registration</h2>
            <form action="#" method="post">
                <div class="form-group">
                    <label for="fullName">Full Name:</label>
                    <input type="text" id="fullName" name="fullName" placeholder="Enter your full name" required minlength="3">
                    </div>

                <div class="form-group">
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" placeholder="Enter your email address" required>
                    </div>

                <div class="form-group">
                    <label for="password">Password:</label>
                    <input type="password" id="password" name="password" placeholder="Create a password" required minlength="8" pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,}">
                    <small>Password must be at least 8 characters long and contain at least one uppercase letter, one lowercase letter, and one number.</small>
                </div>

                <div class="form-group">
                    <label for="birthDate">Date of Birth:</label>
                    <input type="date" id="birthDate" name="birthDate" required max="2025-07-03">
                    </div>

                <div class="form-group">
                    <label for="country">Country:</label>
                    <select id="country" name="country" required>
                        <option value="">--Please choose an option--</option>
                        <option value="kenya">Kenya</option>
                        <option value="uganda">Uganda</option>
                        <option value="tanzania">Tanzania</option>
                        <option value="rwanda">Rwanda</option>
                        <option value="other">Other</option>
                    </select>
                </div>

                <div class="form-group radio-group">
                    <label>Gender:</label><br>
                    <input type="radio" id="male" name="gender" value="male" required>
                    <label for="male">Male</label><br>
                    <input type="radio" id="female" name="gender" value="female">
                    <label for="female">Female</label><br>
                    <input type="radio" id="otherGender" name="gender" value="other">
                    <label for="otherGender">Other</label>
                    </div>

                <div class="form-group checkbox-group">
                    <label>Interests (Select all that apply):</label><br>
                    <input type="checkbox" id="coding" name="interests" value="coding">
                    <label for="coding">Coding</label><br>
                    <input type="checkbox" id="design" name="interests" value="design">
                    <label for="design">Design</label><br>
                    <input type="checkbox" id="marketing" name="interests" value="marketing">
                    <label for="marketing">Marketing</label><br>
                    <input type="checkbox" id="management" name="interests" value="management">
                    <label for="management">Project Management</label>
                    </div>

                <button type="submit">Register</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 My HTML Document. All rights reserved.</p>
    </footer>

</body>
</html>

Happy Coding! 💻✨
