<!DOCTYPE html>
 <html>

<head>
	<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
</head>

<body>

	
<ul>


<h1>GAM COMMANDS</h1>

<li>This is a quick refernce guide for anyone who is a GAM user.</li>


----------------------------------

<h2><br>USER FUNCTIONS</br></h2>
	

<li>gam info domain (account information about your domain)</li>

<li>gam info user [username] (info about user, groups, login info, etc)</li>

<li>gam create alias coolguy user testuser (this command creates an alias named coolguy and appends to the user testuser)</li>
	
<li>gam create user [user.name] firstname "user" lastname "name" password "test405"  changepassword on (this creates a new user with a password set and a changepassword set once the user logs on)</li>
	
<li>gam delete user [username] (to delete user)</li>

<li>gam undelete user [username] (to undelete user)</li>

<li>gam update user [username] suspended on (to suspended user)</li>

<li>gam update user [username] suspended off (to unsuspended user)</li>

<li>gam update user [username] password newlysetpassword (this command updates user password)</li>
	
<li>gam user [username] show filelist (to show all files users owns)</li>
	
<li>gam user [username] transfer drive [recieving username] (this moves the users files from drive to a new owner)</li>

<li>gam print datatransfers (This example prints all data transfers)</li>

<li>gam create datatransfer (old owner) [gdrive or calendar] (new owner) (this command is used to transfer users drive data and calendar resources)</li>

<li>gam print printers (this prints a list of all the Google Cloud Printers)</li>

<li>gam print printers todrive (this prints the list of all the Google Cloud Printers to a Google Sheet)</li>

<li>Examples of using the data transfer command:</li>

<ul type="circle">

<li>gam create datatransfer (old owner) gdrive (new owner) privacy_level shared,private (this command just moves the G Drive data)</li>

<li>gam create datatransfer (old owner) calendar (new owner) release_resources true (this command just moves the calendar data)</li>

</ul type="circle">

----------------------------------

<h3><br>GROUP FUNCTIONS</br></h3>
	

<li>gam create group [group name] (This commands creates a group for you)</li>

<li>gam info group [groupname](this displays all the info of that group)</li>
	
<li>gam update group [groupname] add member [username] (add users to a group)</li>
	
<li>gam update group [groupname]update owner user [username] (this changes group ownership to another user)</li>

<li>gam print groups todrive (this command will push the output to your personal drive)</li>

----------------------------------

<h4><br>CALENDAR FUNCTIONS</br></h4>	


<li>gam calendar [username] update owner [username] (this moves calendars resources to a new owner)</li>

----------------------------------	

<h5><br>Bulk Operations</br></h5>


<li>gam csv [path of csv file] gam delete user ~username (this deletes bulk amount of users using the names on the csv or textfile)</li>
	
<li>gam update org ["directory path"] add user [username] (this moves users to a different ou, make sure to use "/" to specificy which directory)</li>

<li>gam print users todrive (this command will push your user list to a google sheet)</li>

<li>gam print groups todrive (this command will push your google groups on your domain to a google sheet)</li>

<li>gam csv /location/of/csv gam update group example@company.com add members ~username (using the username field in my text editior or csv I can use this command to add a group of people to a particular google group)</li>

<li>gam user test@test.com show filelist | gam update user test@test.com password newpassword (using the pipe in between will run the command in order</li>

<li>gam batch file-name (using this command you can run multiple GAM commands at one time, each line should contain one GAM command per line) </li>

----------------------------------

<h6><br>Email Deletion</br></h6>


<li>gam user [username] delete messages query rfc822msgid:[message ID]doit (this command deletes a single email sent to your org)</li>
	
<li>gam all users delete messages query rfc822msgid:[message ID] doit (this command will delete a sent email to the whole org)</li>

<li>gam all users delete messages query from:[Email address of the user sending spam] doit (Use this command when trying to delete emails from a specific user)</li>

----------------------------------

<h7><br>Google Drive Functions</br></h7>


<li>gam all users show fileinfo (insert file ID) owners (this command will search the owner of any file in your domain)</li>


----------------------------------

<h8><br>Email Actions</br></h8>

<li>gam user test@example.com add forwardingaddress persontoadd@example.com (this will command will add a forwarding address to the test@example.com address)</li>

----------------------------------

<h9><br>Additional Tools</br></h9>

<p>Got Your Back (Got Your Back is a command line tool that backs up and restores your Gmail inbox).</p>

<p>* To install paste the command below:</p>


<li>bash <(curl -s -S -L https://git.io/gyb-install)</li>

<p> * Once Installed paste this command below to test install</p>

<li>gyb --email testemail@company.com --action estimate</li>

<p>* To note, to run the commands you must in the directory where you installed GYB.</p>

----------------------------------

<h10><br>How to upgrade just the GAM shell, paste the command below into your terminal.</h10></br>

<li>bash <(curl -s -S -L https://git.io/install-gam) -l</li>


----------------------------------

<h11><br>Note: When using GAM by default it doesn't set to your path correctly. You need update your bash_profile (if your using bash, which is default)</h11></br>

<li>To do that type: nano .bash_profile then appendend this "export PATH=/usr/local/bin:$PATH"</li>

<li>Make sure you are in the correct directory where your GAM folder is located at</li>
	
</ul>
	</body>

</html>
