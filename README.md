#Автоматические массовые сообщения Telegram

Это скрипт на python, который автоматически отправляет сообщения Telegram из настольного приложения Telegram. Его можно настроить для отправки рекламных сообщений. Он считывает данные с листа Excel и отправляет настроенное сообщение людям.

## Демо-версия
* Видеоклип о выполнении скрипта на YouTube. https://youtu.be/wnZGUy7zFNc

## Важное примечание
* Если этот репозиторий помог вам понять хотя бы что-то новое, пожалуйста, дайте звезду этому репозиторию, который мотивирует меня продолжать работать над подобными проектами.

## Предварительные условия

Чтобы запустить скрипт на python, в вашей системе должны быть установлены следующие программы / пакеты, а контактный номер должен быть сохранен в вашем телефоне (вы можете использовать процедуру массового сохранения контактного номера по электронной почте). Существует способ без сохранения контактного номера, но с ограничением на отправку вложения.
* Python 3.8: Download it from https://www.python.org/downloads
* Pandas : Run in command prompt **pip install pandas**
* Xlrd : Run in command prompt **pip install xlrd**
* Pyautogui: Run in command prompt pip install pyautogui
* Telegram Desktop App : Download from https://desktop.telegram.org/

## Подход
* Сначала нужно клонировать этот респираторный
* Пользователь сканирует QR-код для входа в Telegram, чтобы войти в настольное приложение Telegram.
* Запустите скрипт на python script.py использование py script.py в терминале
* Скрипт считывает настроенное сообщение с листа Excel.
* Скрипт считывает строки одну за другой и выполняет поиск этого имени пользователя в окне поиска настольного приложения Telegram, если имя пользователя найдено в Telegram, то он отправит настроенное сообщение, в противном случае он считывает следующую строку. 
* Цикл выполняется до тех пор, пока все строки не будут завершены.

Примечание: Если вы хотите отправить изображение или документы вместо текста, вы можете написать код для добавления функции отправки вложений.

## Юридический
* Этот код никоим образом не связан, не авторизован, не поддерживается, не спонсируется и не одобрен Telegram или любым из ее филиалов или дочерних компаний. Это независимое и неофициальное программное обеспечение. Используйте на свой страх и риск. Коммерческое использование этого кода/репозитория строго запрещено.

## Код
```
# Программа для массовой отправки пользовательских сообщений через настольное приложение Telegram
# Автор @fraddyrad

import pyautogui
import pandas
import time

excel_data = pandas.read_excel('Recipients data.xlsx', sheet_name='Recipients')

count = 0

time.sleep(3)

for column in excel_data['Username'].tolist():

      pyautogui.press('esc')
      pyautogui.hotkey('ctrl', 'f')
      time.sleep(1)
      pyautogui.write(str(excel_data['Username'][count]));
      pyautogui.press('enter')
      time.sleep(2)
      pyautogui.press('down')
      pyautogui.press('enter')
      pyautogui.write(str(excel_data['Message'][0]));
      pyautogui.press('enter')
      pyautogui.press('esc')
      count = count + 1

print('The script executed successfully.')
```
Примечание: Скрипт может не сработать в случае, если доступность Telegram изменилась.

Найдите это на youtube. https://youtu.be/wnZGUy7zFNc

Создаем виртуальное окружение и активируем его:
virtualenv venv
venv\Scripts\activate


1.pip install pandas
#
2.pip install xlrd
#
3.pip install pyautogui
#
4.pip install Telethon
#
5.pip install telegrambaseclient
#
6.pip install sync
#
7.pip install import
#
8.pip install pyinstaller
#
9.pip install telebot
#
сборка в ехе в 1 файл pyinstaller --onefile Путь до файла TG-SENDER.py
#
в моём случае это C:\Users\soft_nulled_2023\0\1\TG-SENDER.py
#
pyinstaller --onefile C:\Users\soft_nulled_2023\0\1\TG-SENDER.py
#
