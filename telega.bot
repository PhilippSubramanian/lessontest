import telebot
from config import token 
import random
    # Замени 'TOKEN' на токен твоего бота
    # Этот токен ты получаешь от BotFather, чтобы бот мог работать
bot = telebot.TeleBot(token)

facts = ['Почти 50% всего пластика было произведено в последние 15 лет', 'Трещина разбитого стекла движется с рекордной скоростью 4828 км/ч.', 'Одна батарейка загрязняет вредными компонентами 400 л воды']

@bot.message_handler(commands=['start'])
def send_welcome(message):
    bot.reply_to(message, "Привет! Я твой Telegram бот. Напиши что-нибудь!")
    
@bot.message_handler(commands=['hello'])
def send_hello(message):
    bot.reply_to(message, "Привет! Как дела?")
    
@bot.message_handler(commands=['bye'])
def send_bye(message):
    bot.reply_to(message, "Пока! Удачи!")
    
@bot.message_handler(commands=['info'])
def send_info(message):
    bot.reply_to(message, "Привет! Я умею:eco_info,")

@bot.message_handler(commands=['eco_info'])
def send_info(message):
    bot.reply_to(message, "здравствуйте! Я бот который поможет вам понять как нужно правильно содержать планету в чистоте!")
    bot.reply_to(message, "впишите команду: glass, battery, plastic, что бы узнать подробности, или facts для рандомных фактов")

@bot.message_handler(commands=['facts'])
def send_fact(message):
    bot.reply_to(message, random.choice(facts))

@bot.message_handler(func=lambda message: True)
def echo_all(message):
    bot.reply_to(message, message.text)

    
bot.polling()
