# Tracking changes with Github actions

* Step 1: Inspect mode > Network > Fetch/XHR > to find the file with the data. Then, copying the data file you are interested in as cURL and go to curlconverter.com
* Step 2: Paste the cURL that you copied from the original website in the first box and select Python>http.client. Copy the code. 
* Step 3: Create a repository (with a readme and public) and create a new file called start.py. Paste the python code. 
* Step 4: Before commiting the changes, go to the header section and remove all the lines except the ones starting with "content-type" and "x-requested-with" to avoid errors (the common error is something like code converter error). Max has figured out that these are the only two lines he needs by trying and error. He suggested leaving everything if we want at the beginning and see if the code runs, and then starts removing lines from this section to see what works. Then commit changes.
* Step 5: Create a new file. It has to be called exactly: ".github/workflow/run.yml" and copy the code from this [site]( https://gist.github.com/maxharlow/b327f7d8a5d7f70555b6597d0b7bf51b) or [here](https://github.com/Carmen-Aguilar/tracking_changesDH23/blob/main/.github/workflows/run.yml) if that does not work.
* A bit of explanation about the code on the yml file: the schedule - cron is how frequent you want to run the code. Go to https://crontab.guru/ to see how that "cron" parameter works. Permissions: write-all is to allow github to add files. the Jobs section is what is happening when the code run. The first run line indicates where the data is being sent/stored. 
* Step 6: Go to the action tab on your repository to check it is running. For some reasons (Max doesn't know why), it runs the file twice and the first one fails. The second one should be green. 
* On the code tab, we have the data.json where the data is being stored. 
* Step 7: Adding "flat" at the beginning of the github repository, it opens the data in a table with a commit dropdown menu where we can track the changes. Eg: flatgithub.com/Carmen-Aguilar/tracking_changesDH23 and eg: https://flatgithub.com/yayadrian/pizza-express-locations
