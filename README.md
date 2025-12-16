# Internet Shutdown Tracker
Live map from Internet Society Data

### What I've done

This data is scraped daily from Internetsociety.org's pulse tracker. which I have updating hourly at the moment.

I've pumped it into datarwapper using githubactions to automate the daily scraping and updating. 

The final .csv being used for the visualizations is internet_shutdowns_processed.csv

### Scrapping 

I used beautiful soup and the magic scraping prompt to get a scraper to grab each part if the data card. From there, I had chat help me write some code which turns the Duration in an int for using in the map.

### What I tried and failed to do

The data from Pulse is really messy because their data cards place diferent types of data into similar HTML spots, making the scrapping very unclean.

Some of them for example have the specific region that is being shutdown, and I wanted to map that out, however I had trouble on the datawrapper side as the Pulse entries that didn't have regions associated with them (like Russia or China) wouldn't populate. I tried using the library pycountry and some python code to populate every reagion of each country so that it would work, but the characters with non-english shapes and accents wouldn't compute with the datawrapper map, so I abandonded that part. 

### What I learned and where I grew

I learned a little about scrapping, but the material on my site was pretty basic. I learned the most about data cleaning as I couldn't for the life of me figure out why my duration data wasn't working for the Chlorepleth map, and it took me many days to realize it was a string and not an int. 

I learned alot about HTML and CSS as well since I used chat to write some code to help make my map bigger and it ended up making the map cover the whole screen which I slowly had to undo. 

