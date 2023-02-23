# royal.mod.apk
Here you can find unlocked and mod of games/ app
<!DOCTYPE html>
<html>
<head>
	<title>APK File Upload</title>
</head>
<body>
	<h1>Upload your APK Files</h1>
	<form action="upload.php" method="POST" enctype="multipart/form-data">
		<label for="file">Select APK Files:</label>
		<input type="file" name="file[]" id="file" multiple><br><br>
		<input type="submit" name="submit" value="Upload Files">
	</form>

	<h2>Download APK Files</h2>
	<?php
		// Get the list of uploaded APK files
		$files = glob('uploads/*.apk');

		// Display the list of files as download links
		foreach($files as $file) {
			$filename = basename($file);
			echo '<a href="downloads/'.$filename.'" download>'.$filename.'</a><br>';
		}
	?>
</body>
</html>
