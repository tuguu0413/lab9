<?php
$servername = "localhost";
$username = "Tuguu0413";
$password = "04130413";
$dbname = "lab10";

$connection = mysqli_connect($servername, $username, $password, $dbname);

if (!$connection) {
    die("Connection failed: " . mysqli_connect_error());
}
?>
    

    <?php
    if (isset($_GET['search_query'])) {
      
        $search_query = $_GET['search_query'];

        $sql = "SELECT * FROM Items WHERE ItemName LIKE '$search_query'";
        $result = mysqli_query($connection, $sql);

        if ($result && mysqli_num_rows($result) > 0) {
            echo "<h3>Search Results:</h3>";
            echo "<ul>";
            while ($row = mysqli_fetch_assoc($result)) {
                echo "<li>" . $row['ItemName'] . " - Category: " . $row['CategoryID'] . " - Description: " . $row['UsageDescription'] . "</li>";
            }
            echo "</ul>";
        } else {
            echo "No results found.";
        }
    }
    ?>

    <?php
    mysqli_close($connection);
    ?>
