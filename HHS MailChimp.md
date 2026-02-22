# Overall Process
Get an up-to-date members list from TidyHQ
Add it to Mailchimp as a recipient set
Compose your email
Send

# 

## Update Mailchimp's lists
Mailchimp maintains a single data set of "Hobart Hackerspace Inc Members", and applies tags to allow us to select the recipients of a particular mailout. Usually we use dates as tags.

This allows us to upload an entire current membership list and let it update any who have changed some detail, insert those who are new and tag all those in a single upload with the same tag. We can a set of current recipients and use that now, without losing the details of those no longer current.

This guide assumes that you've generated a CSV file by passing a TidyHQ export through Brian's `thq2db.py` script, but doesn't demand that. It simply requires a CSV file which contains at least Firstname, Lastname and Email address in different columns.

### Process:
1. Log into [Mailchimp](https://login.mailchimp.com/). The credentials are in [the password vault](https://vault.bitwarden.com/#/login)
2. Select `Audience` >> `All contacts` from the side menu, then click on `Add Contacts` >> `Import Contacts`
3. Select `Upload a File` and click `Continue`
4. Drag & drop your fresh `mailchimp_file.csv` (or other CSV file) onto the file selector and upload it.
5. The Audience is "Hobart Hackerspace Inc Members". This doesn't change. Choose `Update any existing contacts`.
6. Tag the imported contacts with a tag relating to the date, eg "2025-Mar". (Type the tag name in and click on `Create ...`) This allows us to identify them from among all the other sets.
7. Check that the three columns to be imported match their content. This will be true if you've generated the file from the python script, but should be checked if you've generated the file some other way.
8. Approve the *Subscribed* email status and finalise the import. 
9. Verify that the Tag has been accepted. It should show:
> Imported from: File upload
> Email marketing status: Subscribed
> Update existing contacts: Yes
> Tagged: 2025-Mar
10. Click on `Complete import`
11. It will report the number of contacts added or updated. It may also report errors. The response will look like:
> You attempted to import 49 contacts through File Upload on Mar 3, 2025 • 11:02 AM
> Several errors were encountered; we suggest that you resolve them before attempting to import again.
> 6 new contacts were added
> 41 existing contacts were updated
> 2 errors were encountered
12. You can see what the individual errors were by downloading the error file (it's another CSV) and looking in it. It includes the three columns of the upload file and adds one with the error message for that record. If you don't need the recipients mentioned in the error file, you can proceed without issues. Otherwise you may need to resolve the errors first.

# Composing your email to members
Mailchimp doesn't have a facility to simply forward a given email to a bunch of recipients. Unfortunately, the old-fashioned "email exploder" is a thing of the past, as email misuse has exploded and spam prevention and detection systems have grown to match. So we end up using something like Mailchimp, which is primarily a marketing tool, as a means of simple communication.

A single outgoing email to members is considered part of a *Campaign* (as in "advertising campaign"). We create a *campaign*, set its audience, subject, send time and content, and then kick it off.

### Process:
1. From the Mailchimp dashboard, go to `Campaigns` >> `All campains` and click on `Create`.
2. Choose `Regular email` and click on `Design Email`.
3. In the `To` panel, click on `All subscribed contacts` to open the choice of subscriber tags. (For some reason we've changed from *Audience* to *Subscribers* :-). Choose your tag from the drop-down list.
4. You can usually leave the `From` panel alone, unless you want something different from "Committee" as the sender.
5. The `Subject` panel allows you to put in both an email Subject and a "Preview Text" (summary). The summary allows you to put in a tickler that folks will see in their inbox list.
6. Choose a `Send time` if "right now" isn't what you want.
7. Then you have to "Design" your email. As we're not usually actually doing marketing, this can be simple (and will likely get more readers that way.) Start this by clicking on `Design email`.
		1. Staying with "Simple", choose either "1 Column" or "Simple text". 
			- "1 Column" provides a centred constrained-width column (like a Facebook post, but without anything in the borders). The default "1 Column" template has our logo centred at the top.
			- "Simple" gives you a basic left-justified block of text, looking more like a classic simple email, with no logo.
		2. You'll be presented with a design screen with a set of "blocks" on the left and an editing panel on the right. 
			- Select a block on the left, click the pencil icon and then edit its content on the right, or
			- Drag a block from the options on the right to a place in the blocks on the left.
		3. When you're happy with the looks of a block that you're working on, click `Save & Close` (bottom right).
		4. When you're done with all blocks, click `Continue` (top right)
8. When you've got something that looks right, click `Preview` to view the formatted email as it might look on both large & small screens.
9. Then send yourself a test email, so you can see how it really looks as a received email. Click `Send a test email` and put in your address and any others that you may want to approve or review it.
10. Then  you can click **`Send`**. It'll pop up a confirm window and that's it.




