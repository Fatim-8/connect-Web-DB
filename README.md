# connect-Web-DB

To-Do
Connecting a Web Page to a Database using "XAMPP"

Firstly. Install XAMPP on your computer.

Secondly, Start the Apache and MySQL services in XAMPP.

Third, Create a new database in phpMyAdmin.

Fourthly, Create your own table in the database.

Fifth,  Create a web page (.php) and establish a connection to the database using PHP.

## Now we will see how to connect the page to the database in an actual way:

### To connect the page to the database u can using this command
```
$connect = new mysqli($servername, $username, $password, $dbname);
```
### Now, I verified that the form was submitted via POST request and that a specific field (action) was included in the form data by using this:
```
if ($_SERVER["REQUEST_METHOD"] == "POST" && isset($_POST['action'])) {
    $action = $_POST['action'];
```
### Now that you have verified the success of the connection through:
```
if ($stmt->execute()) {
        header("Location: ControlPanel.php?status=success");
        exit();
    } else {
        echo "Error: " . $stmt->error;
    }

  ```
### Closing the database connection after completing the database operations in the code:
```
$stmt->close();
$connect->close();
```
Here is a video of my web page:

https://github.com/user-attachments/assets/82386385-e5cf-41bd-b335-f0d8098b87f1



