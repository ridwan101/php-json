<!DOCTYPE html>
<html>
<head>
	<title>Json Object</title>
</head>
<body>
	<h1>JSON</h1>
<?php
	$arr1=array("Firstname"=>'Ridwan',"Lastname"=>'Rahat',"gender"=>'male',"Username"=>'rahat',"password"=>'5555',"email"=>'ridwanrahat17gmail.com');

	$json_encoded_text=json_encode($arr1);


	$file1 =fopen("features1.txt","w");
	fwrite($file1, $json_encoded_text);

	$file2 = fopen("features1.txt", "r");
		$read = fread($file2, filesize("features1.txt"));
		fclose($file2);

		$json_decoded_text = json_decode($read, true);

		echo $json_decoded_text['Firstname'];
		echo "<br>";
		echo $json_decoded_text['Lastname'];
		echo "<br>";
		echo $json_decoded_text['gender'];
		echo "<br>";
		echo $json_decoded_text['Username'];
		echo "<br>";
		echo $json_decoded_text['password'];
		echo "<br>";
		echo $json_decoded_text['email'];
		echo "<br>";


$arr2=array("Username"=>'rahat',"password"=>'5555');
	$json_encoded_text=json_encode($arr2);

	$file1 =fopen("features1.txt","w");
	fwrite($file1, $json_encoded_text);

	$file2 = fopen("features1.txt", "r");
		$read = fread($file2, filesize("features1.txt"));
		fclose($file2);

		$json_decoded_text = json_decode($read, true);

		echo $json_decoded_text['Username'];
		echo "<br>";
		echo $json_decoded_text['password'];
		echo "<br>";

?>
</body>
</html>