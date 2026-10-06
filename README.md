# Selenium_automation_registration
## Date: 6/10/2026
```
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait, Select
from selenium.webdriver.support import expected_conditions as EC
import time

driver = webdriver.Chrome()

driver.get("https://vinothqaacademy.com/demo-site/")

wait = WebDriverWait(driver, 20)

# ---------------- FIRST NAME ----------------

fname = wait.until(
    EC.presence_of_element_located((By.ID, "vfb-5"))
)
fname.send_keys("Srii")


# ---------------- LAST NAME ----------------

lname = wait.until(
    EC.presence_of_element_located((By.ID, "vfb-7"))
)
lname.send_keys("Kaavyaa")


# ---------------- GENDER ----------------

female=driver.find_element(By.ID, "vfb-31-2")
if not female.is_selected():
    female.click()


# ---------------- ADDRESS ----------------

address = wait.until(
    EC.presence_of_element_located((By.ID, "vfb-13-address"))
)
address.send_keys("Saveetha College Chennai")


# ---------------- STREET / APT / BUILDING ----------------

street = wait.until(
    EC.presence_of_element_located((By.ID, "vfb-13-address-2"))
)
street.send_keys("No 3, Saveetha Nagar")


# ---------------- CITY ----------------

city = wait.until(
    EC.presence_of_element_located((By.ID, "vfb-13-city"))
)
city.send_keys("Chennai")


# ---------------- STATE ----------------

state = wait.until(
    EC.presence_of_element_located((By.ID, "vfb-13-state"))
)
state.send_keys("Tamil Nadu")


# ---------------- ZIP CODE ----------------

zip_code = wait.until(
    EC.presence_of_element_located((By.ID, "vfb-13-zip"))
)
zip_code.send_keys("600077")


# ---------------- COUNTRY ----------------

country_element = wait.until(
    EC.presence_of_element_located((By.ID, "vfb-13-country"))
)

country = Select(country_element)
country.select_by_visible_text("India")

# ---------------- EMAIL ----------------

email = wait.until(
    EC.presence_of_element_located((By.ID, "vfb-14"))
)
email.send_keys("sriikaavyaa@example.com")

# Keep browser open
time.sleep(50)
```
## output:
<img width="1852" height="950" alt="image" src="https://github.com/user-attachments/assets/034d507d-f5e3-4ec2-af32-007d6f3ad369" />
