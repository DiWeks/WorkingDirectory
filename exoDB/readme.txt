Créer un fichier connectDB.php et créer la connexion à la base 

<?php
$servername = "localhost";	// Nom du serveur de la base
$dbname = "tp1";		// Nom de la base
$dbuser = "cha";       		// Nom d'utilisateur
$dbpassword = "1234";		//Mot de passe de la base

try {
  $bddConnect = new PDO("mysql:host=".$servername.";dbname=".$dbname, $dbuser, $dbpassword);
  $bddConnect->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
  echo "Connected successfully &#128515;";
} catch(PDOException $e) {
  echo "Connection failed: " . $e->getMessage();
}
 ?>
