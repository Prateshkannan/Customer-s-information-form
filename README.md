# Customer-s-information-form
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Add Customer Information</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="customerInfoPage">
        <form id="customerInfoForm">
            <h2>Customer Information</h2>

            <label for="fullName">Full Name:</label>
            <input type="text" id="fullName" name="fullName" required>

            <label for="dob">Date of Birth:</label>
            <input type="date" id="dob" name="dob" required>

            <label for="address">Address:</label>
            <input type="text" id="address" name="address" required>

            <label for="contact">Contact Details:</label>
            <input type="tel" id="contact" name="contact" required>

            <label for="reference">Reference:</label>
            <input type="text" id="reference" name="reference">

            <label for="employment">Employment Information:</label>
            <input type="text" id="employment" name="employment">

            <label for="bankName">Bank Name:</label>
            <input type="text" id="bankName" name="bankName" required>

            <label for="branch">Branch:</label>
            <input type="text" id="branch" name="branch" required>

            <label for="accountNumber">Account Number:</label>
            <input type="text" id="accountNumber" name="accountNumber" required>

            <label for="ifscCode">IFSC Code:</label>
            <input type="text" id="ifscCode" name="ifscCode" required>

            <label for="idProof">ID Proof Upload:</label>
            <input type="file" id="idProof" name="idProof" accept="image/*" required>

            <label for="addressProof">Address Proof Upload:</label>
            <input type="file" id="addressProof" name="addressProof" accept="image/*" required>

            <label for="digitalSignature">Digital Signature:</label>
            <input type="file" id="digitalSignature" name="digitalSignature" accept="image/*" required>

            <button type="button" onclick="nextPage()">Next</button>
        </form>
    </div>

    <div id="additionalInfoPage" class="hidden">
        <form id="additionalInfoForm">
            <h2>Additional Information</h2>

            <!-- Add additional fields as needed -->

            <button type="submit">Submit</button>
        </form>
    </div>

    <script src="scripts.js"></script>
</body>
</html>

body {
    font-family: Arial, sans-serif;
    margin: 20px;
}

form {
    max-width: 600px;
    margin: auto;
}

label {
    display: block;
    margin-bottom: 8px;
}

input, select, button {
    width: 100%;
    padding: 10px;
    margin-bottom: 16px;
    box-sizing: border-box;
}

button {
    background-color: #4CAF50;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}

.hidden {
    display: none;
}

function nextPage() {
    // Switch to the next page
    document.getElementById('customerInfoPage').classList.add('hidden');
    document.getElementById('additionalInfoPage').classList.remove('hidden');
}
