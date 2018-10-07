#!/usr/bin/env python
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.common.exceptions import NoSuchElementException
import time
import datetime

driver = webdriver.Firefox(executable_path=r"geckodriver.exe")

############################################################## LOGIN ##############################################################################
driver.get("https://cointiply.com/login")

time.sleep(10)

username = driver.find_element_by_xpath("//input[@type='text']")
password = driver.find_element_by_xpath("//input[@type='password']")
username.send_keys("#########")
password.send_keys("#########")
time.sleep(3)
login_attempt = driver.find_element_by_xpath("//form/button[1]")
login_attempt.submit()

time.sleep(10)
############################################################ MARKET PLACE #########################################################################
driver.get("https://cointiply.com/mg")

#marketplace_attempt = driver.find_element_by_xpath("//div[@class='menu-item'][contains(.,'Marketplace')]")
#time.sleep(4)
#marketplace_attempt.click()

#time.sleep(4)

# marketplace_attempt.refresh() refresh the Marketplace page
########################################################## CLOSE CHAT  ############################################################################
time.sleep(4)
closechat_attempt = driver.find_element_by_xpath("/html/body/div[3]/div[2]/div[2]/div[1]/div/div[1]/div[1]/div/div[9]")
closechat_attempt.click()

########################################################## CLAIM FREE GEMS ########################################################################

def cointiply_func():
    freeGems_attempt = driver.find_elements_by_xpath("/html/body/div[3]/div[2]/div[2]/div[1]/div/div[1]/div[1]/div/div[2]/div/button[1]")
    if len(freeGems_attempt) > 0 :
        freeGems_attempt[0].click()
        time.sleep(10)
        print("clicked!")
        try :
            gem1 =driver.find_element_by_xpath("/html/body/div[3]/div[2]/div[2]/div[1]/div/div[1]/div[5]/div[1]/div[1]/div/div[2]/a")
            gem1.click()
        except NoSuchElementException as exceptions:
            try :
                gem2 = driver.find_element_by_xpath("/html/body/div[3]/div[2]/div[2]/div[1]/div/div[1]/div[5]/div[1]/div[2]/div/div[2]/a")
                gem2.click()
            except NoSuchElementException as exceptions:
                try :  
                    gem3 = driver.find_element_by_xpath("/html/body/div[3]/div[2]/div[2]/div[1]/div/div[1]/div[5]/div[1]/div[3]/div/div[2]/a")
                    gem3.click()
                except NoSuchElementException as exceptions: 
                    try :
                        gem4 = driver.find_element_by_xpath("/html/body/div[3]/div[2]/div[2]/div[1]/div/div[1]/div[5]/div[1]/div[4]/div/div[2]/a")
                        gem4.click()
                    except NoSuchElementException as exceptions:
                        try :
                            gem5 = driver.find_element_by_xpath("/html/body/div[3]/div[2]/div[2]/div[1]/div/div[1]/div[5]/div[1]/div[5]/div/div[2]/a")
                            gem5.click()
                        except NoSuchElementException as exceptions:
                            try :
                                gem6 = driver.find_element_by_xpath("/html/body/div[3]/div[2]/div[2]/div[1]/div/div[1]/div[5]/div[1]/div[6]/div/div[2]/a")
                                gem6.click()
                            except NoSuchElementException as exceptions:
                                try :
                                    gem7 = driver.find_element_by_xpath("/html/body/div[3]/div[2]/div[2]/div[1]/div/div[1]/div[5]/div[1]/div[7]/div/div[2]/a")
                                    gem7.click()
                                except NoSuchElementException as exceptions:
                                    try :
                                        gem8 = driver.find_element_by_xpath("/html/body/div[3]/div[2]/div[2]/div[1]/div/div[1]/div[5]/div[1]/div[8]/div/div[2]/a")
                                        gem8.click()
                                    except NoSuchElementException as exceptions:
                                        try :
                                            gem9 = driver.find_element_by_xpath("/html/body/div[3]/div[2]/div[2]/div[1]/div/div[1]/div[5]/div[1]/div[9]/div/div[2]/a")
                                            gem9.click()
                                        except NoSuchElementException as exceptions:
                                            print("!!!!!!!")
        else :
            print("Not found!")    
    else :
        print("Claim Free Gems is not found!")
    return

while True :
    try :
        driver.find_element_by_xpath("/html/body/div[3]/div[2]/div[2]/div[1]/div/div[1]/div[1]/div/div[2]/div/button[1]/i[contains(text(), 'grade')]").is_displayed()
        cointiply_func()
    except NoSuchElementException as exceptions :
        print("Claimed")
        time.sleep(3700)

    
