# scraping all-rookie team data from basketball reference

*** Question 1 ***
Write me python code to do the following:
- scrape all-rookie team data from 2001-02 to 2021-22 from https://www.basketball-reference.com/awards/all_rookie.html
- build a pandas dataframe with the following columns: name and team (1 if the player is on the first team, 2 if on the second team)
- write that pandas dataframe to a csv called "all_rookie.csv"

*** Question 2 ***
Okay that didn't work. I'll describe the way the site is set up so we can parse the data correctly.

All the data I need is wrapped in the tbody tag. Inside that tag, each row of data is wrapped in a tr tag. Each value for each row is wrapped inside a td tag.
The rows of data look like this:

2021-2022 | NBA | 1st | Scottie Barnes | Cade Cunningham | Evan Mobley | Franz Vagner | Jalen Green
2021-2022 | NBA | 2nd | Herbert Jones | Josh Giddey | Bones Hyland | Ayo Dosunmu | Chris Duarte

I'd like to convert the rows into a dataframe like this:

2022 | Scottie Barnes | 1st
2022 | Cade Cunningham | 1st
2022 | Evan Mobley | 1st
2022 | Franz Vagner | 1st
2022 | Jalen Green | 1st
2022 | Herbert Jones | 2nd
2022 | Josh Giddey | 2nd
2022 | Bones Hyland | 2nd
2022 | Ayo Dosunmu | 2nd
2022 | Chris Duarte | 2nd

Where the columns are named "year", "name", and "team".

*** Question 3 ***
How can I use python to grab all tr tags that have no class attribute within a soup object?

*** Question 4 ***
How would I extract a tags where the href begins with "/players"?

*** Question 5 ***
What python code could I use to grab all tags that match this html: `<td class="left" data-stat="all_team">`?

*** Question 6 ***
How would I extract the text that those tags contain?