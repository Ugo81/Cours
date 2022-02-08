
Remplacer ces variables :
  -$servername 
  -$dbname 
  -$dbuser 
  -$dbpassword 

Dans fichier connectDb.php ajouter : 
$servername = "";
$dbname = "";
$dbuser = "";
$dbpassword = "";

try {
  $bddConnect = new PDO("mysql:host=".$servername.";dbname=".$dbname, $dbuser, $dbpassword);
  
  $bddConnect->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
  
  echo "Connected successfully &#128515;";
  
} catch(PDOException $e) {

  echo "Connection failed: " . $e->getMessage();
}

