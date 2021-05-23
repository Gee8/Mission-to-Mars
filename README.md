# Mission-to-Mars
In our Mission-to-Mars project, we created a program to scrape images, news and data from the web and organize them into our own html file. Within our `scraping.py` file, we created our functions that will scrape the webpages to gather data to put into our `index.html` file.

Our first function, `scrape_all()`, contained our `data` dictionary, which held the data unpacked from our other functions.

Our next function, `mars_news(browser)`, visited the website `https://redplanetscience.com/` to retreive the most current news title and its news preview.

Our `featured_image(browser)` function returned an image to display on our website.

The `mars_facts()` function read a table from `https://galaxyfacts-mars.com` that contained information about Mars and Earth into a datframe. Using Pandas .to_html() function, we used Bootstrap to format the table as striped.

In our `hemispheres()` function, we created an empty dictionary `hemisphere_image_urls`. We then used a for loop containing an empty dictionary `hemispheres` and found the href link for each hemisphere, clicked the link, then scraped the href and title for the hemisphere, placed it in our `hemispheres` dictionary, then appended it to our `hemisphere_image_urls` list. We then used `browser.back()` to return to the original page, and continue with our for loop to retreive the data for the next three hemispheres.

These functions were used to populate our `data` dictionary found in the `scrape_all()` function, which was used to place data into our `index.html` file. After running our `app.py`, we had a website that had all the information we scraped from the various websites. From here, we edited the `index.html` to include bootstrap elements to make the website more appealing. We made the website mobile responsive, and edited the html containing the images from our `hemispheres()` function so they would all appear on the same row when viewed from a large screen. We also edited the titles for each of the hemispheres so they are the color of mars. Finally, we edited the `Scrape New Data` button that retreives all of the scraped information to match the color of the hemisphere titles.