## Getting the Members list from TidyHQ
We have to extract the data from TidyHQ, download it and massage it into a suitable file.

### Process:
1. Go to TidyHQ & log in to admin dashboard
2. Select `Memberships` >> `Reports`
3. Choose a Membership Level appropriate for what you need:
	- `Active` for a mailout to current members
	- `All` for a door database update (it includes recently-expired members)
4. Click on Options and select all of: 
	- Membership Level	
	- Contact	
	- Start Date	
	- End Date	
	- Status	
	- Registered	
	- First Name	
	- Last Name	
	- Nickname	
	- Contact Email	
	- Phone	
	- RFID Tag
	- Door access only
	- Member badge issued
5. Click `Search` then sort by End Date descending
6. `Export CSV` and choose a file name
7. Process it with Brian's `thq2db.py` Python script
	1. This produces both a SQLite3 database and a CSV text file
	2. Mailchimp needs the CSV file
	3. The SQLite3 database works with the door system