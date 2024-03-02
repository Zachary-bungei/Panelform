<!DOCTYPE html>
<html>
<head>
  <title>Submit Email</title>
</head>
<body>
  <h1>Submit Email</h1>
  
  <form id="myForm">
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    <br>
    <label for="message">Message:</label>
    <textarea id="message" name="message" required></textarea>
    <br>
    <button type="submit" onclick="sendEmail">Submit</button>
  </form>
  
  <script src="script.js">
document.getElementById('myForm').addEventListener('submit', function(event) {
  event.preventDefault();  // Prevent form from submitting and page refreshing
  
  // Get the email and message values from the form inputs
  let email = document.getElementById('email').value;
  let message = document.getElementById('message').value;
  
  // Send the email and message to the specified recipient
 let recipient = 'Zacharia.chemoiwyo@mpesafoundationacademy.ac.ke';
  sendEmail(email, recipient, message);
  
  // Clear the form
  document.getElementById('myForm').reset();
});

function sendEmail(email, recipient, message) {
  // You can implement your own logic here to send the email to the recipient
  // For demonstration purposes, we'll just log the email and message to the console
  alert('Email sent to ' + recipient + ' from ' + email + ': ' + message);
}
</script>
</body>
</html>
