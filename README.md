# seleniumv1.0
from selenium import  webdriver
import  os

class RunChromeTestsWindows() :

    def test(self) :
        driverLocation = "C:\\Users\\LocalUser\\Documents\\libs\\chromedriver.exe"
        os.environ["webdriver.chrome.driver"] = driverLocation
        driver = webdriver.Chrome(driverLocation)
        driver.get("https://www.google.com")

        chrome_options = Options()
        chrome_options.binary_location="../Google Chrome"
        chrome_options.add_argument("disable-infobars");

chromeTest = RunChromeTestsWindows()
chromeTest.test()
