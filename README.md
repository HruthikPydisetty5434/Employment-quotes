# Employment-quotes
•	Firstly, Import selenium, Beautiful soup and Pandas packages.
•	Automate a blank browser using browser = webdriver.FireFox()
•	url = ‘https://devtomanager.com/interviews/’
•	Initiate the required URL that we need to scrape using browser.get(“url”)
•	Now let’s  get the html code of the webpage using browser.page_source.
•	Parse the html code using soup = BeautifulSoup(browser.page_source, 'html.parser')
•	To know the div and class we need to use inspect mode right clicking on the mouse
•	All Employee Name, Job role and company are in division: ’h5’ and class: ‘card-title’. We need to use Indexing in order to get desired text
•	Scrape and iterate employee name using: [i.text.strip().split(', ')[0] for i in soup.find_all('h5', class_ = 'card-title')]
•	We need to use two split() functions in order to scrape and iterate Job role: [i.text.strip().split(', ')[1].split('at')[0] for i in soup.find_all('h5', class_ = 'card-title')]
