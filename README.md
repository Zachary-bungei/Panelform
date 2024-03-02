<!DOCTYPE html>
<html>
<head>
  <title>Submit Email</title>
</head>
<body>
  <h1>Submit Email</h1>
  
  <form id="myForm">
    <label for="email">Email:</label>
    <textarea id="email" name="email"></textarea>
    <br>
    <button type="submit">Submit</button>
  </form>
  
  <script>
document.getElementById('myForm').addEventListener('submit', function(event) {
  event.preventDefault();  // Prevent form from submitting and page refreshing
  
  // Get the email value from the textarea
  var email = document.getElementById('email').value;
  
  // Send the email to the specified recipient
  var recipient = 'Zacharia.chemoiwyo@mpesafoundationacademy.ac.ke';
  sendEmail(email, recipient);
  
  // Clear the form
  document.getElementById('myForm').reset();
});

function sendEmail(email, recipient) {
  // You can implement your own logic here to send the email to the recipient
  // For demonstration purposes, we'll just log the email to the console
  console.log('Email sent to ' + recipient + ': ' + email);
}
</script>
</body>
</html>
