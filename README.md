# fb-auto
import time
from selenium import webdriver
from selenium.webdriver.common.action_chains import ActionChains
browser = webdriver.Firefox()
browser.get('https://www.facebook.com')
emailElem = browser.find_element_by_id('email')
emailElem.send_keys('mymail')
passwordElem = browser.find_element_by_id('pass')
passwordElem.send_keys('mypass')
passwordElem.submit()
time.sleep(20)
Logout1 = browser.find_element_by_id('logoutMenu')
Hover = ActionChains(browser).move_to_element(Logout1)
Hover.click()
