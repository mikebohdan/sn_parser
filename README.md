# Social Network Parser
Simple parser that takes info from file "links.csv" and analyze all companies from it.
### CSV file format
+--------------------+--------------------+---------------------+---------------------+<br />
|    Company Name    |     Twitter ID     |     Facebook ID     |   Wikipedia page    |<br />
+--------------------+--------------------+---------------------+---------------------+<br />
|       IBM          |        ibm         |         -           |         IBM         |<br />
+--------------------+--------------------+---------------------+---------------------+<br />
|       Cisco        |         -          |        Cisco        |     Cisco_Sysetms   |<br />
+--------------------+--------------------+---------------------+---------------------+<br />
|                    |                    |                     |                     |<br />

If there no links for company (like IBM have no Facebook account or Cisco has no Twitter account) you must add an '-' symbol

### Result of execution
After execution you'll recive bunch of files '<company name>.txt' and 'result.txt' file.
In company-specific file you'll can find data from all networks that company use.
In 'result.txt' file you'll can find top 10 phrases for each company. Lenght of those phrases
are between 1 and 3 (minimum 1 word and maximum is 3). And top 10 words for all companies in field  'all words' .

### Instrucitons
For running this code you must specify next environment variables:
```
TWITTER_CUSTOMER_KEY - customer key for your twitter app
TWITTER_CUSTOMER_SECRET - customer secret for your twitter app
FB_KEY - customer key for your facebook app
FB_SECRET - customer secret for your facebook app
```
If you use bash or zsh you can do this with following command:
```
export TWITTER_CUSTOMER_KEY="your_supersecret_key"
```
