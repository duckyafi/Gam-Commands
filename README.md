<!DOCTYPE html>
 <html>

<head>
	<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
</head>

<body>


<ul>


<h1>GAM COMMANDS</h1>

----------------------------------

<p><b>Domain Level Commands</b></p>

<li>gam info domain (account information about your domain)</li>

<li> gam info org testorg (this shows info about an organization, ex. what users are in this certain organization)</li>

<p><b><br>User Functions</br></b></p>

<li>gam info user [username] (info about user, groups, login info, etc)</li>

<li>gam create alias coolguy user testuser (this command creates an alias named coolguy and appends to the user testuser)</li>

<li>gam create user [user.name] firstname "user" lastname "name" password "test405"  changepassword on (this creates a new user with a password set and a changepassword set once the user logs on)</li>

<li>gam delete user [username] (to delete user)</li>

<li>gam undelete user [username] (to undelete user)</li>

<li>gam update user [username] suspended on (to suspended user)</li>

<li>gam update user [username] suspended off (to unsuspended user)</li>

<li>gam update user [username] password newlysetpassword (this command updates user password)</li>

<li>gam user [username] show filelist (to show all files users owns)</li>

<li>gam update org /example ou add user example@google.com (Use this when you want to move a user to a new org)</li>

<p><b><br>Data Transfer</br></b></p>

<li>gam user [username] transfer drive [recieving username] (this moves the users files from drive to a new owner)</li>

<li>gam print datatransfers (This example prints all data transfers)</li>

<li>gam create datatransfer (old owner) [gdrive or calendar] (new owner) (this command is used to transfer users drive data and calendar resources)</li>

<li>Examples of using the data transfer command:</li>

<ul type="circle">

<li>gam create datatransfer (old owner) gdrive (new owner) privacy_level shared,private (this command just moves the G Drive data)</li>

<li>gam create datatransfer (old owner) calendar (new owner) release_resources true (this command just moves the calendar data)</li>

</ul type="circle">

<p><b><br>Google Print</br></b></p>

<li>gam print printers (this prints a list of all the Google Cloud Printers)</li>

<li>gam print printers todrive (this prints the list of all the Google Cloud Printers to a Google Sheet)</li>

<p><b><br>Calendar Functions</br></b></p>

<li>gam calendar [username] update owner [username] (this moves calendars resources to a new owner)</li>

<p><b><br>GOOGLE DRIVE FUNCTIONS</br></b></p>

<li>gam all users show fileinfo (insert file ID) owners (this command will search the owner of any file in your domain)</li>

----------------------------------

<h2>GROUP FUNCTIONS</h2>


<li>gam create group [group name] (This commands creates a group for you)</li>

<li>gam info group [groupname](this displays all the info of that group)</li>

<li>gam update group [groupname] add member [username] (add users to a group)</li>

<li>gam update group [groupname]update owner user [username] (this changes group ownership to another user)</li>

<li>gam print groups todrive (this command will push the output to your personal drive)</li>

----------------------------------

<h3>BULK OPERATIONS</h3>


<li>gam csv [path of csv file] gam delete user ~username (this deletes bulk amount of users using the names on the csv or textfile)</li>

<li>gam update org ["directory path"] add user [username] (this moves users to a different ou, make sure to use "/" to specificy which directory)</li>

<li>gam print users todrive (this command will push your user list to a google sheet)</li>

<li>gam print groups todrive (this command will push your google groups on your domain to a google sheet)</li>

<li>gam csv /location/of/csv gam update group example@company.com add members ~username (using the username field in my text editior or csv I can use this command to add a group of people to a particular google group)</li>

<li>gam user test@test.com show filelist | gam update user test@test.com password newpassword (using the pipe in between will run the command in order</li>

<li>gam batch file-name (using this command you can run multiple GAM commands at one time, each line should contain one GAM command per line) </li>

----------------------------------

<h4>EMAIL DELETION</h4>


<li>gam user [username] delete messages query rfc822msgid:[message ID]doit (this command deletes a single email sent to your org)</li>

<li>gam all users delete messages query rfc822msgid:[message ID] doit (this command will delete a sent email to the whole org)</li>

<li>gam all users delete messages query from:[Email address of the user sending spam] doit (Use this command when trying to delete emails from a specific user)</li>

----------------------------------

<h5>EMAIL ACTIONS</h5>

<li>gam user test@example.com add forwardingaddress persontoadd@example.com (this will command will add a forwarding address to the test@example.com address)</li>

----------------------------------

<h6>ADDITIONAL TOOLS</h6>

<p>Got Your Back (Got Your Back is a command line tool that backs up and restores your Gmail inbox).</p>

<p>* To install paste the command below:</p>


<li>bash <(curl -s -S -L https://git.io/gyb-install)</li>

<p> * Once Installed paste this command below to test install</p>

<li>gyb --email testemail@company.com --action estimate</li>

<p>* To note, to run the commands you must in the directory where you installed GYB.</p>

----------------------------------

<h7>HOW TO UPGRADE YOUR GAM SHELL</h7>

<P>* paste the command below into your terminal window</P>

<li>bash <(curl -s -S -L https://git.io/install-gam) -l</li>


----------------------------------

<h8>Note: When using GAM by default it doesn't set to your path correctly. You need update your bash_profile (if your using bash, which is default)</h8>

<li>To do that type: nano .bash_profile then appendend this "export PATH=/usr/local/bin:$PATH"</li>

<li>Make sure you are in the correct directory where your GAM folder is located at</li>

</ul>
	</body>

</html>
