# connect-Web-DB

To-Do
Connecting a Web Page to a Database using "XAMPP"

1. Install XAMPP on your computer.
2. Start the Apache and MySQL services in XAMPP.
3. Create a new database in phpMyAdmin.
4. Create your own table in the database.
5.  Create a web page (.php) and establish a connection to the database using PHP.

### To begin with, I created a simple model using the direction icons from the Bootstrap library. I customized these icons using CSS to fit my own design and vision.

After that, I created a database called "robotcontrol" which contains a single table named "actions". This table has two columns - one for the "ID" and the other for "the action". This will help me track and log the control commands for the robot.

For me, it was important to create this simple and organized system for controlling the robot. I wanted to ensure that the user interface would be easy to use and visually appealing. At the same time, I wanted to be able to track and log all the commands I send to the robot through the database.

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



