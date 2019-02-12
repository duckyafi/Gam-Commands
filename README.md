<!DOCTYPE html>
 <html>

<head>
	<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
	
#My Most Used GAM Commands

<title></title>

</head>

<body>
	
<ul>

<h1>User Functions</h1>
	
<li>gam info domain (account information about your domain)</li>

<li>gam info user [username] (info about user, groups, login info, etc)</li>
	
<li>gam create user [user.name] firstname "user" lastname "name" password "test405"  changepassword on (this creates a new user with a password set and a changepassword set once the user logs on)</li>
	
<li>gam delete user [username] (to delete user)</li>
	
<li>gam user [username] show filelist (to show all files users owns)</li>
	
<li>gam user [username] transfer drive [recieving username] (this moves the users files from drive to a new owner)</li>
	
<h2>Group Functions</h2>
	
<li>gam create group [group name] (This commands creates a group for you)</li>

<li>gam info group [groupname](this displays all the info of that group)</li>
	
<li>gam update group [groupname] add member [username] (add users to a group)</li>
	
<li>gam update group [groupname]update owner user [username] (this changes group ownership to another user)</li>

<h3>Calendar</h3>	

<li>gam calendar [username] update owner [username] (this moves calendars resources to a new owner)</li>
	
<h4>Bulk Operations</h4>

<li>gam csv [path of csv file] gam delete user ~username (this deletes bulk amount of users using the names on the csv or textfile)</li>
	
<li>gam update org ["directory path"] add user [username] (this moves users to a different ou, make sure to use "/" to specificy which directory)</li>

<h5>Email Deletion</h5>

<li>gam user [username] delete messages query rfc822msgid:[message ID]doit (this command deletes a single email sent to your org)</li>
	
<li>gam all users delete messages query rfc822msgid:[message ID] doit (this command will delete a sent email to the whole org)</li>
	
</ul>
	</body>

</html>