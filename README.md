<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration Form</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 20px; }
        .form-container { width: 400px; border: 1px solid #ccc; padding: 20px; }
        .form-group { margin-bottom: 15px; }
        .form-group label { display: block; margin-bottom: 5px; }
        .form-group input, .form-group select, .form-group textarea { width: 100%; padding: 8px; }
        .form-group input[type="radio"], .form-group input[type="checkbox"] { width: auto; margin-right: 10px; }
        .form-group .hobbies { display: flex; gap: 10px; flex-wrap: wrap; }
        button { padding: 10px 20px; margin-right: 10px; }
        .error { color: red; font-size: 12px; display: none; }
    </style>
</head>
<body>
    <div class="form-container">
        <h2>Registration Form</h2>
        <form id="registrationForm" onsubmit="return validateForm(event)">
            <div class="form-group">
                <label for="firstName">Enter First Name</label>
                <input type="text" id="firstName" name="firstName" value="John" required>
                <span class="error" id="firstNameError">First name is required</span>
            </div>
            <div class="form-group">
                <label for="lastName">Enter Last Name</label>
                <input type="text" id="lastName" name="lastName" value="Doe" required>
                <span class="error" id="lastNameError">Last name is required</span>
            </div>
            <div class="form-group">
                <label for="password">Enter Password</label>
                <input type="password" id="password" name="password" value="Pass123" required>
                <span class="error" id="passwordError">Password is required (min 6 chars)</span>
            </div>
            <div class="form-group">
                <label for="rePassword">Re-enter Password</label>
                <input type="password" id="rePassword" name="rePassword" value="Pass123" required>
                <span class="error" id="rePasswordError">Passwords do not match</span>
            </div>
            <div class="form-group">
                <label for="email">Enter E-mail</label>
                <input type="email" id="email" name="email" value="john.doe@example.com" required>
                <span class="error" id="emailError">Valid email is required</span>
            </div>
            <div class="form-group">
                <label for="mobile">Enter Mobile</label>
                <input type="tel" id="mobile" name="mobile" value="1234567890" pattern="[0-9]{10}" required>
                <span class="error" id="mobileError">10-digit mobile number required</span>
            </div>
            <div class="form-group">
                <label>Enter Address</label>
                <textarea id="address" name="address" rows="4" required>123 Main St, City</textarea>
                <span class="error" id="addressError">Address is required</span>
            </div>
            <div class="form-group">
                <label>Select your gender</label>
                <input type="radio" id="male" name="gender" value="male" checked required> Male
                <input type="radio" id="female" name="gender" value="female"> Female
                <span class="error" id="genderError">Gender is required</span>
            </div>
            <div class="form-group">
                <label>Select your hobbies</label>
                <div class="hobbies">
                    <input type="checkbox" id="hobby1" name="hobbies" value="Reading" checked> Reading
                    <input type="checkbox" id="hobby2" name="hobbies" value="Gaming"> Gaming
                    <input type="checkbox" id="hobby3" name="hobbies" value="Sports"> Sports
                </div>
            </div>
            <div class="form-group">
                <label for="dob">Select your DOB</label>
                <input type="date" id="dob" name="dob" value="1990-01-01" required>
                <span class="error" id="dobError">DOB is required</span>
            </div>
            <div class="form-group">
                <label for="country">Select Country</label>
                <select id="country" name="country" required>
                    <option value="">Select your country</option>
                    <option value="india" selected>India</option>
                    <option value="usa">USA</option>
                    <option value="uk">UK</option>
                </select>
                <span class="error" id="countryError">Country is required</span>
            </div>
            <div class="form-group">
                <label for="pic">Upload your pic</label>
                <input type="file" id="pic" name="pic" accept="image/*">
            </div>
            <button type="submit">Save My Data</button>
            <button type="reset">Reset Data</button>
        </form>
    </div>

    <script src="script.js"></script>
</body>
</html>
