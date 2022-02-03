import pyautogui 
import time

from selenium import webdriver
import time

# Abre o navegador já na url do CRM
navegador = webdriver.Edge()

navegador.get("https://plugcrm.net/app#/deals/pipeline")

input_email = navegador.find_element_by_id("email")
input_password = navegador.find_element_by_id("password")

#Propriedade para inserir os dados no campo


input_email.send_keys("login")
input_password.send_keys("password")
btn_login = navegador.find_element_by_xpath("/html/body/div/div/div/div/div[2]/div/form/button")
btn_login.click()
time.sleep(10)

pyautogui.click(x=688, y=236)
time.sleep(10)

pyautogui.click(x=770, y=319)
time.sleep(4)
#responsvel
pyautogui.click(x=1006, y=237)
time.sleep(3)
#etapa do funil
pyautogui.click(x=994, y=271)
time.sleep(1)
#abre o status
pyautogui.click(x=49, y=277)
time.sleep(1)
#seleciona todos
pyautogui.click(x=890, y=316)
time.sleep(1)
#clica no botao de dentro
pyautogui.click(x=873, y=281)
time.sleep(1)
#clica em exportar
pyautogui.click(x=932, y=435)
time.sleep(1)
#exporta oportunidades
pyautogui.click(x=1031, y=173)
time.sleep(1)
# Abre config
pyautogui.click(x=898, y=468)
time.sleep(1)

# Maximizar tela
pyautogui.click(x=976, y=31)
time.sleep(1)

# Seleciona a caixa de pesquisa do google
pyautogui.click(x=318, y=49)
time.sleep(1)
#entra com a url
pyautogui.write("https://plugcrm.net/app#/settings/exports")
pyautogui.press("enter")

pyautogui.alert("AGUARDANDO BAIXAR A EXPORTAÇÃO ! ")
time.sleep(60)

pyautogui.press("F5")

# baixar o arquivo para excel
pyautogui.click(x=1256, y=706)
time.sleep(5) 

#abre gerenciador de downloads e abre o msm
pyautogui.hotkey('ctrl', 'j')
pyautogui.click(x=1041, y=140)
time.sleep(5) 
