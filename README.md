<!DOCTYPE html>
 <html>

<head>
	<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
</head>

<body>

<a href="">
	
<ul>

   <img src="http://www.mediafire.com/view/yj376hbxdfzu9sn/Google%20Logo%20Black%20And%20White.png"> 


<h1>My Most Used GAM Commands</h1>

<p>* Feel Free To Reach Out If You Would Like Me To Add Additional Commands.</p>


<h2><br>User Functions</br></h2>
	

<li>gam info domain (account information about your domain)</li>

<li>gam info user [username] (info about user, groups, login info, etc)</li>
	
<li>gam create user [user.name] firstname "user" lastname "name" password "test405"  changepassword on (this creates a new user with a password set and a changepassword set once the user logs on)</li>
	
<li>gam delete user [username] (to delete user)</li>
	
<li>gam user [username] show filelist (to show all files users owns)</li>
	
<li>gam user [username] transfer drive [recieving username] (this moves the users files from drive to a new owner)</li>
	

<h3><br>Group Functions</br></h3>
	

<li>gam create group [group name] (This commands creates a group for you)</li>

<li>gam info group [groupname](this displays all the info of that group)</li>
	
<li>gam update group [groupname] add member [username] (add users to a group)</li>
	
<li>gam update group [groupname]update owner user [username] (this changes group ownership to another user)</li>


<h4><br>Calendar Functions</br></h4>	


<li>gam calendar [username] update owner [username] (this moves calendars resources to a new owner)</li>
	

<h5><br>Bulk Operations</br></h5>


<li>gam csv [path of csv file] gam delete user ~username (this deletes bulk amount of users using the names on the csv or textfile)</li>
	
<li>gam update org ["directory path"] add user [username] (this moves users to a different ou, make sure to use "/" to specificy which directory)</li>

<li>gam print users todrive (this command will push your user list to a google sheet)</li>

<li>gam print groups todrive (this command will push your google groups on your domain to a google sheet)</li>

<h6><br>Email Deletion</br></h6>


<li>gam user [username] delete messages query rfc822msgid:[message ID]doit (this command deletes a single email sent to your org)</li>
	
<li>gam all users delete messages query rfc822msgid:[message ID] doit (this command will delete a sent email to the whole org)</li>


<h7><br>Google Drive Functions</br></h7>

<li>gam print groups todrive (this command will push the output to your personal drive)</li>
	
</ul>
	</body>

</html>