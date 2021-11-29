from typing import Any
import pytest
# webdriver drives - refers to the language bindings and the implementations of the individual browser controlling code
from selenium import webdriver
# import Options - The Options Class is a concept in Selenium WebDriver for manipulating various properties of browsers
from selenium.webdriver.chrome.options import Options
# ActionChains - are a way to automate low level interactions such as mouse movements
from selenium.webdriver.common.action_chains import ActionChains
# timeout function
from time import sleep
# import Options - The Chromeoptions Class is a concept in Selenium WebDriver for manipulating various properties of the Chrome driver
from selenium.webdriver import ChromeOptions
# The Keys class provides keys in the keyboard like RETURN, F1, ALT etc.
from selenium.webdriver.common.keys import Keys
# Variables in By() class are simple strings and you can use "id" instead of By.ID
from selenium.webdriver.common.by import By
# An explicit wait is a code you define to wait for a certain condition to occur before proceeding further in the code
from selenium.webdriver.support.ui import WebDriverWait
# EC = expected conditions
from selenium.webdriver.support import expected_conditions as EC
# specific file from project
# from files import files

class TestRetoolSearch:
    @classmethod
    def setup_class(cls):
        # Options manipulating various properties of browsers 
        cls.options = Options()
        # Adds an experimental option which is passed to chrome.
        cls.options.add_experimental_option('excludeSwitches', ['enable-logging'])
        cls.options.add_experimental_option("excludeSwitches", ['enable-automation'])
        # Add a command-line argument to use when starting Chrome.
        cls.options.add_argument("user-data-dir=/tmp/Deafult")
        # Creates capabilities with all the options that have been set and returns a dictionary with everything.
        cls.capabilities = cls.options.to_capabilities()
        # Remote WebDriver is an object that can control the browser in the grid by configuring the node and the hub.
        # Remote WebDriver is a class that implements the WebDriver interface. 
        cls.driver = webdriver.Remote(command_executor="http://localhost:4446",desired_capabilities = cls.capabilities)
        # replace with the url for the test website
        cls.driver.get("https://admin.dev.arborknot.io/apps/Book%20Manager")
        # manipulating property of maximize_window() of the Chrome driver.
        cls.driver.maximize_window()
       
        
            
    @classmethod
    def teardown_class(cls):
        cls.driver.quit()

 
    def test_main(self):
        try: 
            # function that runs on website (line 39) 
            button = WebDriverWait(self.driver, 50).until(
                # locate specific element 
                EC.presence_of_element_located((By.CSS_SELECTOR, "#root > div > div > div > div.core-layout__viewport > div > div > div.h-100 > div > div.presentation-canvas-padding > div.retool-canvas-container > div > div > div > div > div > div > div._retool-ModalWidget > div > div > div > button"))          
            )
            button.click()
            sleep(1)

            book = WebDriverWait(self.driver, 3).until(
                # locate another specific element 
                EC.presence_of_element_located((By.CSS_SELECTOR, "#root > div > div > div > div.core-layout__viewport > div > div > div.h-100 > div > div.presentation-canvas-padding > div.retool-canvas-container > div > div > div:nth-child(4) > div > div > div > div.ant-modal-content > div > div > div > div:nth-child(5) > div > div._124-M._retool-txtFormBookCreateName > div > div > div > div > span > input"))
            )
            book.send_keys("Book 29.11 a")
            sleep(1)

            company = WebDriverWait(self.driver, 5).until(
                # locate another specific element               
                EC.presence_of_element_located((By.CSS_SELECTOR, "#root > div > div > div > div.core-layout__viewport > div > div > div.h-100 > div > div.presentation-canvas-padding > div.retool-canvas-container > div > div > div:nth-child(5) > div > div > div > div.ant-modal-content > div > div > div > div:nth-child(7) > div > div._124-M._retool-txtFormBookCreateCompanyName > div > div > div > div > span > input"))
            )
            company.send_keys("Some Company Name")
            sleep(1)

            entitydropdown = WebDriverWait(self.driver, 10).until(
                # locate another specific element 
                EC.presence_of_element_located((By.CSS_SELECTOR, "#root > div > div > div > div.core-layout__viewport > div > div > div.h-100 > div > div.presentation-canvas-padding > div.retool-canvas-container > div > div > div:nth-child(4) > div > div > div > div.ant-modal-content > div > div > div > div._retool-SelectWidget2 > div > div._124-M._retool-select1 > div > div > span > div > div > div._Usfys"))
            )
            entitydropdown.click()
            sleep(1)

            entityname = WebDriverWait(self.driver, 10).until(
                # locate another specific element 
                EC.presence_of_element_located((By.XPATH, "//*[contains(text(),'RCG')]"))
            )
            entityname.click()
            sleep(1)

            buttonsave = WebDriverWait(self.driver, 5).until(
                # locate specific element 
                EC.presence_of_element_located((By.CSS_SELECTOR, "#root > div > div > div > div.core-layout__viewport > div > div > div.h-100 > div > div.presentation-canvas-padding > div.retool-canvas-container > div > div > div:nth-child(4) > div > div > div > div.ant-modal-content > div > div > div > div:nth-child(14) > div > div._124-M._retool-btnFormBookCreateSave > div > div > button"))          
            )
            buttonsave.click()
            sleep(1)

             #refresh page
            self.driver.refresh()

            dropdown = WebDriverWait(self.driver, 40).until(
                # locate specific element 
                EC.presence_of_element_located((By.CSS_SELECTOR, "div#root div.ant-select-selection__placeholder"))
            )
            dropdown.click()
            sleep(1)

            choosebook = WebDriverWait(self.driver, 10).until(
                # locate another specific element 
                EC.presence_of_element_located((By.XPATH, "//*[contains(text(),'Book 29.11 a)]"))
            )
            choosebook.click()
            sleep(1)

            deals = WebDriverWait(self.driver, 10).until(
                # locate another specific element 
                EC.presence_of_element_located((By.CSS_SELECTOR, "#root > div > div > div > div.core-layout__viewport > div > div > div.h-100 > div > div.presentation-canvas-padding > div.retool-canvas-container > div > div > div.retool-container.root.no-border.no-drop-shadow._retool- > div > div > div > div._retool-TabbedContainerWidget > div > div > div > div > div.ant-tabs-bar.ant-tabs-top-bar > div > div > div > div > div:nth-child(1) > div.ant-tabs-tab-active.ant-tabs-tab"))
            )
            deals.click()
            sleep(1)
            

            # click button Add deals
            # selector #root > div > div > div > div.core-layout__viewport > div > div > div.h-100 > div > div.presentation-canvas-padding > div.retool-canvas-container > div > div > div.retool-container.root.no-border.no-drop-shadow._retool- > div > div > div > div._retool-TabbedContainerWidget > div > div > div > div > div.ant-tabs-content.ant-tabs-content-no-animated.ant-tabs-top-content > div.ant-tabs-tabpane.ant-tabs-tabpane-active._retool-tcntPages > div.retool-grid > div > div._retool-FormWidget > div > div > div.retool-container.retool-form-container._retool-formCntDeals > form > div > div > div > div._retool-ModalWidget > div > div > div > button

            dealsadd = WebDriverWait(self.driver, 50).until(
                # locate specific element 
                EC.presence_of_element_located((By.CSS_SELECTOR, "#root > div > div > div > div.core-layout__viewport > div > div > div.h-100 > div > div.presentation-canvas-padding > div.retool-canvas-container > div > div > div.retool-container.root.no-border.no-drop-shadow._retool- > div > div > div > div._retool-TabbedContainerWidget > div > div > div > div > div.ant-tabs-content.ant-tabs-content-no-animated.ant-tabs-top-content > div.ant-tabs-tabpane.ant-tabs-tabpane-active._retool-tcntPages > div.retool-grid > div > div._retool-FormWidget > div > div > div.retool-container.retool-form-container._retool-formCntDeals > form > div > div > div > div._retool-ModalWidget > div > div > div > button"))          
            )
            dealsadd.click()
            sleep(1)


            # choose Deal name
            dealname = WebDriverWait(self.driver, 10).until(
                # locate another specific element 
                EC.presence_of_element_located((By.CSS_SELECTOR, "#root > div > div > div > div.core-layout__viewport > div > div > div.h-100 > div > div.presentation-canvas-padding > div.retool-canvas-container > div > div > div:nth-child(5) > div > div > div > div.ant-modal-content > div > div > div > div:nth-child(5) > div > div._124-M._retool-txtFormCreateDealName > div > div > div > div > span > input"))
            )
            dealname.send_keys("Deal to Book 29.11")
            sleep(1)





        except:
            # anable to avoid a pause at the end of the run
            self.driver.quit()
        
if __name__ == "__main__": 
     pytest.main()
