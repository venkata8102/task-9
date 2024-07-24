```
from selenium import webdriver

# creating a new Chrome browser
driver = webdriver.Chrome()

# visiting the URL
driver.get("https://www.saucedemo.com/")

# locating the login fields and entering credentials
username_field = driver.find_element_by_css_selector("#user-name")
username_field.send_keys("standard_user")
password_field = driver.find_element_by_css_selector("#password")
password_field.send_keys("secret_sauce")

# submitting the login form
login_button = driver.find_element_by_css_selector(".btn_action")
login_button.click()

# getting title of the webpage
title = driver.title
print("Title of webpage:", title)

# getting current URL of the webpage
current_url = driver.current_url
print("Current URL of the webpage:", current_url)

# extracting the entire contents of the webpage and saving it in a text file
with open("webpage_task_11.txt", "w") as f:
    page_source = driver.page_source
    f.write(page_source)

# closing the browser
driver.quit()
```
