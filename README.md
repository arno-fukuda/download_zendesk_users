# Python script to download Zendesk user data

## Configuration
- Edit config.json
- Change usernam, api_token and zndsk_subdomain

## Execution
- Executing the script file will output a csv in the same directory.
- The script extracts the users email address and id and appends it as a new row to the csv.

## Additional notes
- Edit the script to retrieve additional data. (available in `data` dictionary)
- Zendesk has rate limits on their api. Limits vary based on plans. Current script does 5 calls per second (edit `time.sleep(0.2)`)
- Zendesk default is 100 records per page. 
- When the script reaches the end of the list (by checking the value of "nextpage" in the response), it stops.
