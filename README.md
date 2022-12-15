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

<li>gam user [username] signout (this signs out the user mentioned in the username section)</li>

<li>gam update user [username] suspended on (to suspended user)</li>

<li>gam update user [username] suspended off (to unsuspended user)</li>

<li>gam update user [username] password newlysetpassword (this command updates user password)</li>

<li>gam user [username] show filelist (to show all files users owns)</li>

<li>gam user email@testdomain.com update backupcodes (use this command to create backup codes for users)</li>

<li>gam update org /example ou add user example@google.com (Use this when you want to move a user to a new org)</li>

<li>gam whatis test.user@example.com (Use this command to determine if address is a Email address, user, alias or group)</li>

<li>gam delete alias test.user (This deletes a users alias attached to their account)</li>

<li>gam update user example@test.com relation manager manager@test.com (Use this command to add relation to user profile)</li>

<li>gam update user test.user organization title "IT Support" primary (Use this command if you want to update a users job title)</li>

<li>gam update user jschmoe organization title Teacher department Math primary (This updates the job title and the department in one command)</li>

<li>gam user test.user show signature (this displays any current signature)</li>

<li>gam update user test.user otheremail work test.usersotheremail.com (Use this to add other email to a users G-Suite profile)</li>

<li>gam update user test.user otheremail home test.usersotheremail.com (Use this to add other email to a users G-Suite profile)</li>

<li>gam user test.user@test.com show vacation (This command will show users active vacation email settings)</li>

<li>gam user test.user@test.com vacation off (This command turns off users vacation status)</li>

<li>gam user test.user@test.com vacation on subject "Out Of Office" message "Thank you for your email. I am currently out of the office and look forward to responding when I’m back online." startdate 2021-01-01 enddate 2021-01-10 (this command will setup a users vacation response)</li>


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

<li>gam calendar [calendaremail] showacl (This shows who can access the calendar and who has permission)</li>

<li>gam calendar [calendaremail] add [permission (owner|editor)] [useremail] (This changes permissions on a users calendars)</li>

<p><b><br>Google Drive Functions</br></b></p>

<li>gam all users show fileinfo (insert file ID) owners (this command will search the owner of any file in your domain)</li>

<li>gam all users show filelist query "fullText contains 'Project Doc'" todrive (Use this command to search the entire domain for a specific document)</li>

<p><b><br>Email Forwarding</br></b></p>

<li> gam user test.user add forwardingaddress test.forward (this adds a forwarding address to test.user)</li>

<li>gam user test.user forward on test.forward@example.com keep (Use this command when turning on forwarding for a user, this command only works if the user already has a forwarding address added on their account)</li>

<li>gam user testuser@example.com delete forwardingaddress testforwarding@example.com (use this to delete a forwarding address)</li>

<li>gam user test.user show forwardingaddresses (this shows what forwarding address this user has attached to their account)</li>

<p><b><br>Email Deletion</br></b></p>

<li>gam user [username] delete messages query rfc822msgid:[message ID]doit (this command deletes a single email sent to your org)</li>

<li>gam all users delete messages query rfc822msgid:[message ID] doit (this command will delete a sent email to the whole org)</li>

<li>gam all users delete messages query from:[Email address of the user sending spam] doit (Use this command when trying to delete emails from a specific user)</li>

<li>gam user test.user@example.com delete message query from:spam.email.address@example.com doit max_to_delete 3 (input any value that you might need)</li>

----------------------------------

<h2>GROUP FUNCTIONS</h2>


<li>gam create group [group name] (This commands creates a group for you)</li>

<li>gam info group [groupname](this displays all the info of that group)</li>

<li>gam update group [groupname] add member [username] (add users to a group)</li>

<li>gam update group [groupname]update owner user [username] (this changes group ownership to another user)</li>

<li>gam user <email address> delete groups (this removes user from all google groups)</li>

<li>gam print groups todrive (this command will print all the groups in your domain to your personal drive)</li>

<li>gam print group-members group_ns example_group todrive (This prints out group members for a specific group)</li>

<li>gam print groups name members owners managers delimiter "|" todrive (This prints out all the groups in your domain and prints out each manager, members, and owners to drive)</li>

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
<h4>GAMADV-XTD3 Commands</h4>

<p><b><br>Google Groups</br></b></p>

<li>gam print groups member <user email address> (This will only show direct memebership. It will not show where a User is a memeber of a sub-group)</li> 

<p><b><br>Google Drive</br></b></p>

<li>gam user (admin email) show filelist fullpath select "google drive ID" tordive (This will show the full file path within a google drive)</li>


----------------------------------

<h4>ADDITIONAL TOOLS</h4>

<p>Got Your Back (Got Your Back is a command line tool that backs up and restores your Gmail inbox).</p>

<p>* To install paste the command below:</p>


<li>bash <(curl -s -S -L https://git.io/gyb-install)</li>

<p> Note: Once Installed paste this command below to test install</p>

<li>gyb --email testemail@company.com --action estimate</li>

<li>gyb --email yourusersemail@yourcompany.com --service-account</li>

<p>(use this once you enabled the service account option after creating the symlink)</p>

<p>Note: To run the commands you must in the directory where you installed GYB.</p>

<li>bash <(curl -s -S -L https://git.io/gyb-install) -l (use this command to update GYB)</li>


<p><b><br>How To Upgrade Your Gam Shell</br></b></p>

<P>Note: Paste the command below into your terminal window</P>

<li>bash <(curl -s -S -L https://git.io/install-gam) -l</li>

<p><b><br>How To Set Your Gam Path</br></b></p>


<p>Note: When using GAM by default it doesn't set to your path correctly. You need update your bash_profile (if your using bash, which is default)</p>

<li>To do that type: nano .bash_profile then appendend this "export PATH=/usr/local/bin:$PATH"</li>

<li>Make sure you are in the correct directory where your GAM folder is located at</li>

</ul>
	</body>

</html>
