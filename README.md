# bot1
import telebot
import sqlite3
from telebot import apihelper

apihelper.proxy ={'https':'socks5://241821320:0vb9A8oz@orbtl.s5.opennetwork.cc:999'}
#apihelper.proxy = {'https': 'socks5://userproxy:password@ams3.proxy.veesecurity.com:443'}
#apihelper.proxy = {'http':'http://51.15.51.14:1081'}

bot = telebot.TeleBot ('953280714:AAGSEGrYCRHD1QBUfzbOIW3B7gO1jvF3tC0');
@bot.message_handler(content_types=['text'])
def get_text_messages(message):
    if message.text == "Hi":
        bot.send_message(message.from_user.id, "Hello")
    else message.text == "/help":
        bot.send_message(message.from_user.id, "?")
   
bot.polling(none_stop=True, interval=0)
