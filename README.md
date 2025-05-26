<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Scholarship Application Form</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
            background-color: #f5f5f5;
            padding: 20px;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
        }
        
        h1 {
            text-align: center;
            color: #333;
            margin-bottom: 30px;
            font-size: 2em;
        }
        
        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
        }
        
        .form-group.full-width {
            grid-column: 1 / -1;
        }
        
        label {
            font-weight: bold;
            margin-bottom: 5px;
            color: #555;
        }
        
        input[type="text"],
        input[type="date"],
        input[type="number"],
        textarea {
            width: 100%;
            padding: 10px;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
            transition: border-color 0.3s;
        }
        
        input[type="text"]:focus,
        input[type="date"]:focus,
        input[type="number"]:focus,
        textarea:focus {
            outline: none;
            border-color: #4CAF50;
        }
        
        input[type="file"] {
            padding: 5px;
            border: 2px dashed #ddd;
            border-radius: 5px;
            background-color: #fafafa;
        }
        
        .submit-btn {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px 40px;
            border: none;
            border-radius: 25px;
            font-size: 18px;
            cursor: pointer;
            margin: 30px auto 0;
            display: block;
            transition: transform 0.3s;
        }
        
        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .file-section {
            background-color: #f8f9fa;
            padding: 20px;
            border-radius: 8px;
            margin-top: 20px;
        }
        
        .file-section h3 {
            margin-bottom: 15px;
            color: #333;
        }
        
        .optional {
            color: #666;
            font-style: italic;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Scholarship Application Form</h1>
        
        <form id="scholarshipForm">
            <div class="form-grid">
                <div class="form-group">
                    <label for="name">Full Name *</label>
                    <input type="text" id="name" name="name" required>
                </div>
                
                <div class="form-group">
                    <label for="dob">Date of Birth *</label>
                    <input type="date" id="dob" name="dob" required>
                </div>
                
                <div class="form-group">
                    <label for="age">Age *</label>
                    <input type="number" id="age" name="age" required>
                </div>
                
                <div class="form-group">
                    <label for="fatherName">Father's Name *</label>
                    <input type="text" id="fatherName" name="fatherName" required>
                </div>
                
                <div class="form-group">
                    <label for="motherName">Mother's Name *</label>
                    <input type="text" id="motherName" name="motherName" required>
                </div>
                
                <div class="form-group">
                    <label for="email">Email Address *</label>
                    <input type="email" id="email" name="email" required>
                </div>
                
                <div class="form-group">
                    <label for="phone">Phone Number *</label>
                    <input type="tel" id="phone" name="phone" pattern="[0-9]{10}" placeholder="10-digit number" required>
                </div>

                <div class="form-group">
                    <label for="church">Church Affiliation *</label>
                    <input type="text" id="church" name="church" required>
                </div>
                
                <div class="form-group full-width">
                    <label for="address">Address *</label>
                    <textarea id="address" name="address" rows="3" required></textarea>
                </div>
                
                <div class="form-group">
                    <label for="subjects12">Subjects Taken in Class 12 *</label>
                    <input type="text" id="subjects12" name="subjects12" required>
                </div>
                
                <div class="form-group">
                    <label for="marks12">Marks in Class 12 (%) *</label>
                    <input type="number" id="marks10" name="marks10" min="0" max="100" required>
                </div>
                
                <div class="form-group">
                    <label for="marks10">Marks in Class 10 (%) *</label>
                    <input type="number" id="marks12" name="marks12" min="0" max="100" required>
                </div>
                
                <div class="form-group">
                    <label for="course">Course Selected *</label>
                    <input type="text" id="course" name="course" required>
                </div>
                
                <div class="form-group">
                    <label for="years">Duration of Education (years) *</label>
                    <input type="number" id="years" name="years" min="1" max="10" required>
                </div>
                
                <div class="form-group">
                    <label for="tuitionFee">1st Year Tuition Fee (INR) *</label>
                    <input type="number" id="tuitionFee" name="tuitionFee" min="0" required>
                </div>
            </div>
            
            <div class="file-section">
                <h3>Required Documents</h3>
                <div class="form-grid">
                    <div class="form-group">
                        <label for="marksheet10">Upload 10th Marksheet *</label>
                        <input type="file" id="marksheet10" name="marksheet10" accept=".pdf,.jpg,.jpeg,.png" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="marksheet12">Upload 12th Marksheet *</label>
                        <input type="file" id="marksheet12" name="marksheet12" accept=".pdf,.jpg,.jpeg,.png" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="churchCert">Church Membership Certificate *</label>
                        <input type="file" id="churchCert" name="churchCert" accept=".pdf,.jpg,.jpeg,.png" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="aadhar">Aadhar Card *</label>
                        <input type="file" id="aadhar" name="aadhar" accept=".pdf,.jpg,.jpeg,.png" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="incomeCert">Income Certificate *</label>
                        <input type="file" id="incomeCert" name="incomeCert" accept=".pdf,.jpg,.jpeg,.png" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="deathCert">Parent(s) Death Certificate *</label>
                        <input type="file" id="deathCert" name="deathCert" accept=".pdf,.jpg,.jpeg,.png">
                    </div>
                </div>
            </div>
            
            <button type="submit" class="submit-btn">Submit Application</button>
        </form>
    </div>

    <script>
        document.getElementById('scholarshipForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form data
            const formData = new FormData(this);
            
            // Show success message
            alert('Application submitted successfully! We will review your application and get back to you soon.');
            
            // You can add code here to actually send the data to a server
            // For now, we'll just log it to console
            console.log('Form Data:', Object.fromEntries(formData));
            
            // Optionally reset the form
            // this.reset();
        });
        
        // Auto-calculate age from date of birth
        document.getElementById('dob').addEventListener('change', function() {
            const dob = new Date(this.value);
            const today = new Date();
            let age = today.getFullYear() - dob.getFullYear();
            const monthDiff = today.getMonth() - dob.getMonth();
            
            if (monthDiff < 0 || (monthDiff === 0 && today.getDate() < dob.getDate())) {
                age--;
            }
            
            document.getElementById('age').value = age;
        });
    </script>
</body>
</html>
