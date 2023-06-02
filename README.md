# Tracking changes with Github actions

* Step 1: Inspect mode > Network > Fetch/XHR > to find the file with the data. 
* Step 2: Copy as cURL and go to curlconverter.com
* Step 3: Paste the cURL that you copied from the original website in the first box and select Python>http.client
* Step 4: Create a repository (with a readme and public)
* Step 5: Create a new file called start.py and paste the code into the box
* Step 6: In the header sections, remove all the lines except the ones starting content-type and x-requested-with to avoid errors (something like code converter error). Max has figured this out by try and error. He suggested leaving everytihng in and then start removing lines in this section to see what works. Then > commit changes
* Step 7: create a new file. It has to be called exactly: ".github/workflow/run.yml" and copy the code in this site: https://gist.github.com/maxharlow/b327f7d8a5d7f70555b6597d0b7bf51b 
* On that code, the schedule - cron is how frequent you want to run the code. Go to crontab guru to see how that "cron" parameter works. Permissions: write-all is to allow github to add files. the Jobs section is what is happening when the code run. The first run indicates where the data is being sent/stored. 
* 
